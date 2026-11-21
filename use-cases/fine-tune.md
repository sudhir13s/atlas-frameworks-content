---
id: use-case/fine-tune
type: use-case
slug: fine-tune
schema_version: 2.0
title: Fine-tune an LLM
label: Fine-tune an LLM
order: 3
goal: Adapt an open pretrained language model to your task, format or style, check it against the base model for gains, regressions and safety, and serve the result.
stages:
- id: prepare
  name: Prepare
  note: Runs before training and fixes the dataset, the base model and the method.
- id: train
  name: Train
  note: Runs on GPUs while the weights or adapters are updated.
- id: evaluate
  name: Evaluate
  note: Runs after every training run, before anything is released.
- id: release
  name: Release
  note: Runs once a checkpoint passes evaluation and keeps running in production.
blocks:
- id: dataset
  stage: prepare
  name: Dataset and format
  purpose: Holds the training examples and a held-out evaluation split in the column layout the trainer expects.
  options:
  - record: framework/datasets
    choice: default
    when: Loads local JSON or Parquet files and Hub datasets into Apache Arrow-backed tables, the dataset type the TRL documentation builds on.
  - record: framework/label-studio
    choice: alternative
    when: When people must write or label the examples first; it is an Apache-2.0 labelling tool for text, images, audio, video and time series.
  how_to_choose:
  - Supervised fine-tuning (SFT) takes language-modelling or prompt-completion rows; Direct Preference Optimization (DPO) takes preference rows with a chosen and a rejected answer.
  - Use the conversational format (messages with a role and content) for chat models so their chat template is applied.
  - Split off the evaluation examples before training and never train on them.
  browse:
    label: All data tools
    record: framework-category/data
- id: base-model
  stage: prepare
  name: Base model
  purpose: The pretrained checkpoint whose weights, or whose adapters, the run changes.
  options:
  - record: model/qwen3-8b-base
    choice: default
    when: Apache-2.0 licence and published as a pretraining-stage checkpoint with no post-training, so the chat format and behaviour come from your data.
  - record: model/qwen3-8b
    choice: alternative
    when: When you want to keep an existing chat behaviour; the same family after post-training, with switchable thinking and non-thinking modes, under Apache-2.0.
  - record: model/mistral-7b-v0-1
    choice: alternative
    when: Apache-2.0 base model whose card states it has no moderation mechanisms, so safety behaviour must come from your data and checks.
  - record: model/meta-llama-3-8b
    choice: alternative
    when: When the Meta Llama 3 Community License fits your use; downloads are gated behind accepting it on Hugging Face.
  - record: model/smollm3-3b
    choice: alternative
    when: When a smaller Apache-2.0 model is enough; its card publishes the training configs and pretraining data mixture, with a separate base checkpoint.
  how_to_choose:
  - Read the licence first; Qwen3, Mistral 7B and SmolLM3 are Apache-2.0, while Llama 3 uses a custom community licence.
  - Start from a base checkpoint to define your own chat format, and from a post-trained checkpoint to adjust a chat behaviour you already like.
  - Pick the smallest model that reaches your quality bar on the held-out set, since memory and serving cost grow with parameter count.
  browse:
    label: All text-generation models
    record: task/text-generation
- id: method
  stage: prepare
  name: Adaptation method
  purpose: Decides which weights change, either all of them or small adapters on a frozen base.
  options:
  - name: Low-rank adaptation (LoRA)
    url: https://arxiv.org/abs/2106.09685
    choice: default
    when: Freezes the pretrained weights and trains low-rank matrices in each layer; Biderman et al. measured that it forgets less of the base model's abilities than full fine-tuning.
  - name: Quantized LoRA (QLoRA)
    url: https://arxiv.org/abs/2305.14314
    choice: alternative
    when: When the base model does not fit in GPU memory at 16-bit precision; it backpropagates through a frozen 4-bit base into LoRA adapters.
  - name: Full fine-tuning
    url: https://huggingface.co/docs/transformers/training
    choice: alternative
    when: When the target domain needs more change than adapters give and the GPUs can hold every weight, gradient and optimizer state.
  how_to_choose:
  - Biderman et al. found LoRA learns less than full fine-tuning on code and maths but keeps more of the base model's other abilities.
  - Prefer full fine-tuning only when target-domain quality outweighs retained general ability.
  - Keep the unmerged adapter, because merging into a quantized base re-quantizes the weights and is not exactly reversible.
- id: training-framework
  stage: train
  name: Training framework
  purpose: Runs the training loop with batching, loss, optimizer, checkpoints and the chosen method.
  options:
  - record: framework/llamafactory
    choice: default
    when: One Apache-2.0 tool covers full, freeze, LoRA and QLoRA tuning and SFT, reward modelling, PPO, DPO, KTO and ORPO from a CLI or web UI.
  - name: TRL
    url: https://huggingface.co/docs/trl/index
    choice: alternative
    when: When you write the training script yourself; the Hugging Face library provides SFT, DPO, GRPO and reward-model trainers on top of Transformers.
  - record: framework/unsloth
    choice: alternative
    when: When you train on one machine and want GGUF export built in; the core package is Apache-2.0 (its Studio UI is AGPL-3.0) and supports LoRA, QLoRA, full fine-tuning and GRPO.
  - record: framework/peft
    choice: alternative
    when: When you already have a Transformers training loop and only need to wrap the model with LoRA or another adapter method.
  how_to_choose:
  - Choose LlamaFactory when your model and method are on its supported list and configuration is enough.
  - Choose TRL when you need a custom loss, reward or data collator.
  - Pick the trainer and the data format together, since each TRL trainer expects one dataset type.
  browse:
    label: All fine-tuning frameworks
    record: framework-category/fine-tuning
- id: compute
  stage: train
  name: Distributed training and memory
  purpose: Spreads weights, gradients and optimizer states across GPUs when one GPU cannot hold the run.
  options:
  - record: framework/deepspeed
    choice: default
    when: ZeRO shards optimizer states, gradients and parameters across GPUs and can offload to CPU or NVMe, and the Transformers Trainer takes a DeepSpeed config directly.
  - record: framework/pytorch
    choice: alternative
    when: When you want to stay inside PyTorch; its Fully Sharded Data Parallel (FSDP2) shards parameters, gradients and optimizer states and is enabled in the Trainer through fsdp_config.
  how_to_choose:
  - If the run fits on one GPU, skip this block.
  - Start with ZeRO stage 2 and move to stage 3 only when the model does not fit across the GPUs with stage 2.
  - Save a consolidated checkpoint at the end, because sharded DeepSpeed and FSDP checkpoints do not load directly with from_pretrained.
  browse:
    label: All distributed-training frameworks
    record: framework-category/distributed-training
- id: tracking
  stage: train
  name: Experiment tracking
  purpose: Records hyperparameters, loss curves and checkpoints for each run so runs can be compared.
  options:
  - record: framework/mlflow
    choice: default
    when: Apache-2.0 and self-hostable; tracks parameters, metrics and evaluation results and keeps a model registry.
  - record: framework/wandb
    choice: alternative
    when: When you prefer a managed service; the SDK is MIT-licensed and the server runs as multi-tenant cloud, dedicated cloud or self-managed.
  how_to_choose:
  - LlamaFactory lists both MLflow and Weights & Biases as experiment monitors, so this choice does not constrain the training framework.
  - Choose a self-hosted server when training data, prompts or metrics may not leave your infrastructure.
  browse:
    label: All MLOps tools
    record: framework-category/mlops
- id: evaluation-harness
  stage: evaluate
  name: Evaluation harness
  purpose: Scores the fine-tuned model and the base model on the same tasks so gains and regressions show side by side.
  options:
  - name: lm-evaluation-harness
    url: https://github.com/EleutherAI/lm-evaluation-harness
    choice: default
    when: MIT-licensed few-shot evaluation framework that evaluates PEFT adapters such as LoRA directly and is the backend of the Hugging Face Open LLM Leaderboard.
  - record: framework/deepeval
    choice: alternative
    when: When you want public benchmarks and LLM-output metrics in one tool; it ships MMLU, HellaSwag, GSM8K, HumanEval, TruthfulQA, BIG-Bench Hard and DROP for any wrapped model.
  - record: framework/promptfoo
    choice: alternative
    when: When the real test is your own prompts; an open-source CLI that scores outputs against declared test cases and compares models in a matrix view.
  how_to_choose:
  - Run identical tasks, prompts and decoding settings on the base and the fine-tuned model.
  - Treat a drop on general tasks as a regression even when the target task improves.
  - Add a held-out set from your own data, since public benchmarks do not measure your task.
  browse:
    label: All evaluation frameworks
    record: framework-category/evaluation
- id: regression-benchmarks
  stage: evaluate
  name: Regression benchmarks
  purpose: Public tasks that show whether the base model's general abilities survived the fine-tune.
  options:
  - record: benchmark/mmlu
    choice: default
    when: Multiple-choice questions across subjects from elementary mathematics to law that need world knowledge and problem solving, a broad check on retained knowledge.
  - record: benchmark/ifeval
    choice: alternative
    when: When the fine-tune changes response format or style; it scores instruction following with automatically verifiable constraints.
  - record: benchmark/gsm8k
    choice: alternative
    when: When the base model's multi-step arithmetic reasoning must be kept; grade-school maths word problems.
  - record: benchmark/humaneval
    choice: alternative
    when: When coding ability must be kept; it measures functional correctness of programs written from docstrings.
  how_to_choose:
  - Pick benchmarks for abilities the base model had and you need to keep, not only for the target task.
  - Keep the benchmark set fixed across runs so scores stay comparable.
- id: safety
  stage: evaluate
  name: Safety checks
  purpose: Checks that refusal and harmful-content behaviour did not degrade during fine-tuning.
  options:
  - record: benchmark/harmbench
    choice: default
    when: A standardized evaluation framework for automated red teaming that measures how target models and defences hold up against attack methods.
  - record: benchmark/strongreject
    choice: alternative
    when: Pairs forbidden prompts with an automated evaluator that scores how useful a response is to the harmful request; its authors found earlier evaluators overstate jailbreak success.
  - record: framework/promptfoo
    choice: alternative
    when: When you need to probe your own application; its open-source red-teaming plugins test for harmful content and role or access violations.
  - record: model/llama-guard-4-12b
    choice: alternative
    when: A classifier that labels prompts and responses safe or unsafe against the MLCommons hazard taxonomy, usable to score outputs in bulk or filter them in production.
  how_to_choose:
  - Run the safety suite even after training on benign data; Qi et al. found benign fine-tuning can degrade safety alignment, though less than adversarial data.
  - A base checkpoint brings no refusal behaviour of its own, so add a guard model at serving time if your data does not teach refusals.
- id: packaging
  stage: release
  name: Merge and quantise
  purpose: Turns the trained adapter into the artifact the serving runtime loads.
  options:
  - record: framework/peft
    choice: default
    when: merge_and_unload folds the LoRA weights into the base for a standalone model with no adapter latency, and unmerged adapters can be loaded side by side.
  - record: framework/llama-cpp
    choice: alternative
    when: When the target is a CPU or a laptop; convert the checkpoint to GGUF, then llama-quantize lowers weight precision.
  how_to_choose:
  - Keep adapters unmerged when one base model serves several fine-tunes.
  - Merge into the full-precision base before quantising to GGUF.
  - Measure quantisation loss before release; llama.cpp reports it as perplexity or Kullback-Leibler divergence.
- id: serving
  stage: release
  name: Serving
  purpose: Serves the fine-tuned model behind an API.
  options:
  - record: framework/vllm
    choice: default
    when: Apache-2.0 server with an OpenAI-compatible API that serves LoRA adapters on top of one base model, selected per request by model name.
  - record: framework/llama-cpp
    choice: alternative
    when: When serving GGUF files on CPUs or laptops; MIT-licensed C/C++ inference with an OpenAI-compatible server.
  - record: framework/ollama
    choice: alternative
    when: When the model runs on a developer machine; it imports Safetensors or GGUF weights through a Modelfile but does not quantize GGUF on import.
  how_to_choose:
  - Choose vLLM for GPU serving of one base model with several adapters.
  - Choose llama.cpp or Ollama when no data-centre GPU is available.
  browse:
    label: All LLM serving frameworks
    record: framework-category/llm-serving
- id: monitoring
  stage: release
  name: Tracing and monitoring
  purpose: Traces production requests and scores outputs so quality drift after release is visible.
  options:
  - record: framework/langfuse
    choice: default
    when: MIT-licensed outside its ee folders, self-hostable and built on OpenTelemetry, with tracing, evaluations, prompt management and datasets.
  - record: framework/langsmith
    choice: alternative
    when: When you want a managed service with cloud, hybrid or self-hosted deployment; tracing works with many frameworks and providers, not only LangChain.
  - record: framework/mlflow
    choice: alternative
    when: When MLflow already tracks your training runs; it also captures traces of LLM applications and agents.
  how_to_choose:
  - Turn sampled production traces into evaluation examples so the next fine-tune is tested on real traffic.
  - Self-host when prompts and outputs may not leave your infrastructure.
learn_next:
- title: 'LoRA: Low-Rank Adaptation of Large Language Models'
  url: https://arxiv.org/abs/2106.09685
  kind: paper
- title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
  url: https://arxiv.org/abs/2305.14314
  kind: paper
- title: LoRA Learns Less and Forgets Less
  url: https://arxiv.org/abs/2405.09673
  kind: paper
- title: Fine-tuning Aligned Language Models Compromises Safety, Even When Users Do Not Intend To!
  url: https://arxiv.org/abs/2310.03693
  kind: paper
- title: TRL dataset formats and types
  url: https://huggingface.co/docs/trl/dataset_formats
  kind: docs
related_use_cases:
- use-case/train-llm
- use-case/serve-in-production
- use-case/ml-data-pipeline
tags:
- fine-tuning
- lora
- qlora
- peft
- evaluation
- safety
updated: '2026-11-21'
sources:
- url: https://huggingface.co/docs/trl/dataset_formats
  title: TRL documentation, dataset formats and types
  trust: 0.9
- url: https://huggingface.co/docs/trl/index
  title: TRL documentation
  trust: 0.9
- url: https://huggingface.co/docs/datasets/index
  title: Hugging Face Datasets documentation
  trust: 0.9
- url: https://github.com/HumanSignal/label-studio
  title: HumanSignal/label-studio, GitHub repository
  trust: 0.85
- url: https://huggingface.co/Qwen/Qwen3-8B-Base
  title: Qwen/Qwen3-8B-Base, model card
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen3-8B
  title: Qwen/Qwen3-8B, model card
  trust: 0.9
- url: https://huggingface.co/mistralai/Mistral-7B-v0.1
  title: mistralai/Mistral-7B-v0.1, model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Meta-Llama-3-8B
  title: meta-llama/Meta-Llama-3-8B, model card
  trust: 0.9
- url: https://huggingface.co/HuggingFaceTB/SmolLM3-3B
  title: HuggingFaceTB/SmolLM3-3B, model card
  trust: 0.9
- url: https://arxiv.org/abs/2106.09685
  title: 'LoRA: Low-Rank Adaptation of Large Language Models'
  trust: 0.95
- url: https://arxiv.org/abs/2305.14314
  title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
  trust: 0.95
- url: https://arxiv.org/abs/2405.09673
  title: LoRA Learns Less and Forgets Less
  trust: 0.95
- url: https://huggingface.co/docs/transformers/training
  title: Transformers documentation, fine-tuning
  trust: 0.9
- url: https://huggingface.co/docs/peft/index
  title: PEFT documentation
  trust: 0.9
- url: https://huggingface.co/docs/peft/developer_guides/lora
  title: PEFT documentation, LoRA developer guide
  trust: 0.9
- url: https://github.com/hiyouga/LlamaFactory
  title: hiyouga/LlamaFactory, GitHub repository
  trust: 0.85
- url: https://github.com/unslothai/unsloth
  title: unslothai/unsloth, GitHub repository
  trust: 0.85
- url: https://huggingface.co/docs/transformers/deepspeed
  title: Transformers documentation, DeepSpeed ZeRO
  trust: 0.9
- url: https://huggingface.co/docs/transformers/fsdp
  title: Transformers documentation, FSDP2
  trust: 0.9
- url: https://github.com/mlflow/mlflow
  title: mlflow/mlflow, GitHub repository
  trust: 0.85
- url: https://github.com/wandb/wandb
  title: wandb/wandb, GitHub repository
  trust: 0.85
- url: https://github.com/EleutherAI/lm-evaluation-harness
  title: EleutherAI/lm-evaluation-harness, GitHub repository
  trust: 0.85
- url: https://deepeval.com/docs/benchmarks-introduction
  title: DeepEval documentation, benchmarks
  trust: 0.9
- url: https://www.promptfoo.dev/docs/intro/
  title: Promptfoo documentation, introduction
  trust: 0.9
- url: https://www.promptfoo.dev/docs/red-team/
  title: Promptfoo documentation, red teaming
  trust: 0.9
- url: https://arxiv.org/abs/2009.03300
  title: Measuring Massive Multitask Language Understanding
  trust: 0.95
- url: https://arxiv.org/abs/2311.07911
  title: Instruction-Following Evaluation for Large Language Models
  trust: 0.95
- url: https://arxiv.org/abs/2110.14168
  title: Training Verifiers to Solve Math Word Problems
  trust: 0.95
- url: https://arxiv.org/abs/2107.03374
  title: Evaluating Large Language Models Trained on Code
  trust: 0.95
- url: https://arxiv.org/abs/2402.04249
  title: 'HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal'
  trust: 0.95
- url: https://arxiv.org/abs/2402.10260
  title: A StrongREJECT for Empty Jailbreaks
  trust: 0.95
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B, model card
  trust: 0.9
- url: https://arxiv.org/abs/2310.03693
  title: Fine-tuning Aligned Language Models Compromises Safety, Even When Users Do Not Intend To!
  trust: 0.95
- url: https://github.com/ggml-org/llama.cpp/blob/master/tools/quantize/README.md
  title: llama.cpp, llama-quantize README
  trust: 0.85
- url: https://github.com/ggml-org/llama.cpp
  title: ggml-org/llama.cpp, GitHub repository
  trust: 0.85
- url: https://docs.vllm.ai/en/latest/features/lora/
  title: vLLM documentation, LoRA adapters
  trust: 0.9
- url: https://docs.ollama.com/import
  title: Ollama documentation, importing a model
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: langfuse/langfuse, GitHub repository
  trust: 0.85
- url: https://docs.langchain.com/langsmith/home
  title: LangSmith documentation
  trust: 0.9
---

## Overview

Fine-tuning continues training a pretrained model on a smaller dataset for one task or domain. The system starts with a dataset in the trainer's format, a base model and a choice between full fine-tuning and adapters.

Training runs in a fine-tuning framework, sharded across GPUs only when needed and logged to a tracker. Every candidate is then scored against the base model for regressions and safety before it is merged or quantised, served and traced in production.
