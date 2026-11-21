---
id: use-case/train-llm
type: use-case
slug: train-llm
schema_version: 2.0
title: Train an LLM from Scratch
label: Train from scratch
order: 5
goal: Pre-train a transformer language model from random initialization on a curated text corpus across many accelerators and release a base checkpoint that standard tools can load.
stages:
- id: data
  name: Data
  note: Runs before training and produces the filtered, tokenized corpus.
- id: pretrain
  name: Pre-train
  note: Runs on the GPU or TPU cluster for the whole training run.
- id: evaluate
  name: Evaluate
  note: Runs on saved checkpoints during and after training.
- id: release
  name: Release
  note: Runs once a checkpoint is chosen for post-training or serving.
blocks:
- id: corpus
  stage: data
  name: Pre-training corpus
  purpose: The raw text the model learns language and knowledge from.
  options:
  - name: FineWeb
    url: https://huggingface.co/datasets/HuggingFaceFW/fineweb
    choice: default
    when: English web text from Common Crawl under ODC-By whose authors document and ablate every curation choice and release the curation code.
  - name: FineWeb-Edu
    url: https://huggingface.co/datasets/HuggingFaceFW/fineweb-edu
    choice: alternative
    when: When you want the educational subset; the same authors filtered it from FineWeb and release it under ODC-By.
  - name: Dolma
    url: https://huggingface.co/datasets/allenai/dolma
    choice: alternative
    when: When you need more than web text; an ODC-By corpus mixing web pages, academic papers, code, books and encyclopedic material, used to train OLMo.
  how_to_choose:
  - Check the corpus licence and the terms of its original sources; the Dolma card requires both.
  - Size the corpus from the model you plan, since Hoffmann et al. found compute-optimal training scales tokens and parameters equally.
- id: processing
  stage: data
  name: Filtering and deduplication
  purpose: Removes duplicate and low-quality documents before tokenization.
  options:
  - name: DataTrove
    url: https://github.com/huggingface/datatrove
    choice: default
    when: Apache-2.0 library built to process, filter and deduplicate text at very large scale, with local, Slurm and Ray executors.
  - record: framework/dask
    choice: alternative
    when: When your filters are pandas or plain Python code that must scale from one machine to a cluster.
  - name: Apache Spark
    url: https://spark.apache.org/
    choice: alternative
    when: When the corpus already lives in a Spark cluster; a multi-language engine for batch jobs and distributed SQL.
  how_to_choose:
  - Reuse the deduplication and filtering choices the FineWeb authors ablated before designing new filters.
  - Run the same pipeline on a small sample first and read the output by hand.
  browse:
    label: All data tools
    record: framework-category/data
- id: tokenizer
  stage: data
  name: Tokenizer
  purpose: Learns the subword vocabulary and turns text into token IDs.
  options:
  - name: SentencePiece
    url: https://github.com/google/sentencepiece
    choice: default
    when: Apache-2.0 tokenizer that trains byte-pair encoding (BPE) or unigram vocabularies directly from raw sentences with no language-specific preprocessing.
  - name: Hugging Face Tokenizers
    url: https://github.com/huggingface/tokenizers
    choice: alternative
    when: Apache-2.0 Rust library implementing BPE, Unigram, WordPiece and WordLevel models, with Python bindings.
  how_to_choose:
  - Train the tokenizer on a sample of the filtered corpus in the languages the model must handle.
  - Fix the vocabulary before training starts, since changing it later means retraining the embeddings.
- id: training-engine
  stage: pretrain
  name: Training framework and parallelism
  purpose: Runs forward and backward passes across many accelerators with data, tensor, pipeline and context parallelism.
  options:
  - record: framework/megatron-lm
    choice: default
    when: Megatron Core provides GPU-optimized tensor, pipeline, data, expert and context parallelism, and Megatron Bridge converts checkpoints to and from Hugging Face format.
  - name: torchtitan
    url: https://github.com/pytorch/torchtitan
    choice: alternative
    when: When you want a PyTorch-native code base; BSD-3-Clause, composes FSDP, tensor, pipeline, context and expert parallelism, and reads and writes Hugging Face safetensors.
  - record: framework/deepspeed
    choice: alternative
    when: When the cluster is not NVIDIA-only; Apache-2.0 library with ZeRO and 3D parallelism that supports NVIDIA, AMD, Intel Gaudi and other accelerators.
  - name: MaxText
    url: https://github.com/AI-Hypercomputer/maxtext
    choice: alternative
    when: When training on Google Cloud TPUs; an Apache-2.0 JAX library for pre-training and post-training.
  - name: nanochat
    url: https://github.com/karpathy/nanochat
    choice: alternative
    when: When learning or training a small model on one GPU node; an MIT harness covering tokenization, pretraining, finetuning, evaluation and inference in one code base.
  how_to_choose:
  - Pick by hardware first; NVIDIA GPUs fit Megatron-LM or torchtitan, TPUs fit MaxText, mixed accelerator vendors fit DeepSpeed.
  - Validate data, tokenizer and training loop at small scale with nanochat before booking a cluster; its predecessor nanoGPT is deprecated.
  browse:
    label: All distributed-training frameworks
    record: framework-category/distributed-training
- id: tracking
  stage: pretrain
  name: Experiment tracking
  purpose: Logs loss, throughput and memory per step so diverging or stalled runs are caught early.
  options:
  - record: framework/wandb
    choice: default
    when: torchtitan sends loss, memory, throughput and model FLOPs utilization (MFU) to it, and it runs as a managed cloud or a self-managed server.
  - record: framework/mlflow
    choice: alternative
    when: When the tracking server must be open source and self-hosted; Apache-2.0 with a model registry.
  how_to_choose:
  - Log throughput and memory next to loss, since both reveal a parallelism problem before loss does.
  - Keep checkpoints and logs tied to the same run ID so a loss spike can be traced to its checkpoint.
  browse:
    label: All MLOps tools
    record: framework-category/mlops
- id: evaluation-harness
  stage: evaluate
  name: Evaluation harness
  purpose: Scores checkpoints on fixed tasks so progress and the final choice of checkpoint rest on numbers.
  options:
  - name: lm-evaluation-harness
    url: https://github.com/EleutherAI/lm-evaluation-harness
    choice: default
    when: MIT-licensed few-shot evaluation framework that reads Hugging Face and Megatron-DeepSpeed models and is the backend of the Hugging Face Open LLM Leaderboard.
  - record: framework/deepeval
    choice: alternative
    when: When you also need LLM-output metrics; it ships MMLU, HellaSwag, GSM8K, HumanEval, TruthfulQA, BIG-Bench Hard and DROP for any wrapped model.
  how_to_choose:
  - Evaluate intermediate checkpoints, not only the last, to see whether scores are still rising.
  - Keep the task list, few-shot count and prompts fixed across checkpoints.
  browse:
    label: All evaluation frameworks
    record: framework-category/evaluation
- id: benchmarks
  stage: evaluate
  name: Base-model benchmarks
  purpose: Public tasks that a model without instruction tuning can answer by completion or multiple choice.
  options:
  - record: benchmark/hellaswag
    choice: default
    when: Commonsense next-event completion whose wrong endings were selected by adversarial filtering, answered by scoring each ending.
  - record: benchmark/arc-challenge
    choice: alternative
    when: Grade-school science questions that both a retrieval baseline and a word co-occurrence baseline answered incorrectly.
  - record: benchmark/mmlu
    choice: alternative
    when: Multiple-choice questions across subjects from elementary mathematics to law that need world knowledge and problem solving.
  how_to_choose:
  - A pre-trained base model has no chat format, so use completion or multiple-choice benchmarks rather than instruction-following ones.
  - Compare against a published model of similar size evaluated with the same harness settings.
- id: release
  stage: release
  name: Checkpoint format
  purpose: Converts the training checkpoint into a format that post-training, evaluation and serving tools load.
  options:
  - record: framework/hugging-face-transformers
    choice: default
    when: Megatron Bridge and torchtitan both convert to and from Hugging Face format, which TRL, PEFT and lm-evaluation-harness load.
  how_to_choose:
  - Convert and reload the checkpoint, then compare its outputs with the training framework's outputs on the same prompts.
  - Post-train the base model with supervised fine-tuning or preference tuning before exposing it to users.
learn_next:
- title: 'The Ultra-Scale Playbook: Training LLMs on GPU Clusters'
  url: https://nanotron-ultrascale-playbook.static.hf.space/index.html
  kind: blog
- title: Training Compute-Optimal Large Language Models
  url: https://arxiv.org/abs/2203.15556
  kind: paper
- title: 'The FineWeb Datasets: Decanting the Web for the Finest Text Data at Scale'
  url: https://arxiv.org/abs/2406.17557
  kind: paper
- title: nanochat
  url: https://github.com/karpathy/nanochat
  kind: docs
related_use_cases:
- use-case/ml-data-pipeline
- use-case/fine-tune
- use-case/serve-in-production
tags:
- pre-training
- llm
- distributed-training
- tokenizer
- evaluation
updated: '2026-11-21'
sources:
- url: https://huggingface.co/datasets/HuggingFaceFW/fineweb
  title: HuggingFaceFW/fineweb, dataset card
  trust: 0.9
- url: https://huggingface.co/datasets/HuggingFaceFW/fineweb-edu
  title: HuggingFaceFW/fineweb-edu, dataset card
  trust: 0.9
- url: https://arxiv.org/abs/2406.17557
  title: 'The FineWeb Datasets: Decanting the Web for the Finest Text Data at Scale'
  trust: 0.95
- url: https://huggingface.co/datasets/allenai/dolma
  title: allenai/dolma, dataset card
  trust: 0.9
- url: https://arxiv.org/abs/2203.15556
  title: Training Compute-Optimal Large Language Models
  trust: 0.95
- url: https://github.com/huggingface/datatrove
  title: huggingface/datatrove, GitHub repository
  trust: 0.85
- url: https://docs.dask.org/en/stable/
  title: Dask documentation
  trust: 0.9
- url: https://spark.apache.org/
  title: Apache Spark
  trust: 0.9
- url: https://github.com/google/sentencepiece
  title: google/sentencepiece, GitHub repository
  trust: 0.85
- url: https://github.com/huggingface/tokenizers
  title: huggingface/tokenizers, GitHub repository
  trust: 0.85
- url: https://github.com/NVIDIA/Megatron-LM
  title: NVIDIA/Megatron-LM, GitHub repository
  trust: 0.85
- url: https://github.com/pytorch/torchtitan
  title: pytorch/torchtitan, GitHub repository
  trust: 0.85
- url: https://github.com/deepspeedai/DeepSpeed
  title: deepspeedai/DeepSpeed, GitHub repository
  trust: 0.85
- url: https://github.com/AI-Hypercomputer/maxtext
  title: AI-Hypercomputer/maxtext, GitHub repository
  trust: 0.85
- url: https://github.com/karpathy/nanochat
  title: karpathy/nanochat, GitHub repository
  trust: 0.85
- url: https://github.com/karpathy/nanoGPT
  title: karpathy/nanoGPT, GitHub repository
  trust: 0.85
- url: https://github.com/wandb/wandb
  title: wandb/wandb, GitHub repository
  trust: 0.85
- url: https://github.com/mlflow/mlflow
  title: mlflow/mlflow, GitHub repository
  trust: 0.85
- url: https://github.com/EleutherAI/lm-evaluation-harness
  title: EleutherAI/lm-evaluation-harness, GitHub repository
  trust: 0.85
- url: https://deepeval.com/docs/benchmarks-introduction
  title: DeepEval documentation, benchmarks
  trust: 0.9
- url: https://arxiv.org/abs/1905.07830
  title: 'HellaSwag: Can a Machine Really Finish Your Sentence?'
  trust: 0.95
- url: https://arxiv.org/abs/1803.05457
  title: Think you have Solved Question Answering? Try ARC, the AI2 Reasoning Challenge
  trust: 0.95
- url: https://arxiv.org/abs/2009.03300
  title: Measuring Massive Multitask Language Understanding
  trust: 0.95
- url: https://huggingface.co/docs/trl/index
  title: TRL documentation
  trust: 0.9
- url: https://huggingface.co/docs/peft/index
  title: PEFT documentation
  trust: 0.9
- url: https://nanotron-ultrascale-playbook.static.hf.space/index.html
  title: 'The Ultra-Scale Playbook: Training LLMs on GPU Clusters'
  trust: 0.85
---

## Overview

Pre-training builds a language model from random weights. The data lane picks a web-scale corpus, filters and deduplicates it, and trains a tokenizer that turns it into token IDs.

A distributed training framework then spreads the model over many accelerators while a tracker logs every step. Checkpoints are scored on base-model benchmarks, and the chosen one is converted to Hugging Face format for post-training and serving.
