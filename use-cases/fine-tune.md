---
id: use-case/fine-tune
type: use-case
slug: fine-tune
schema_version: 1.0
title: "Fine-tune an LLM"
label: "Fine-tune an LLM"
order: 3
goal: "Adapt an open base model to your task or style with parameter-efficient fine-tuning on a single GPU."
languages: [python]
levels: [intermediate, advanced]
stack:
  - frameworkId: hugging-face-transformers
    role: "Training + PEFT"
    why: "The Trainer API plus the PEFT/LoRA libraries make adapter fine-tuning a few lines of config."
    install: "pip install transformers peft trl datasets accelerate"
    quickstartUrl: "https://huggingface.co/docs/transformers/training"
    docsUrl: "https://huggingface.co/docs/peft/index"
  - frameworkId: pytorch
    role: "Compute backend"
    why: "The tensor/autograd engine underneath Transformers; where mixed precision and device placement happen."
    install: "pip install torch"
    quickstartUrl: "https://pytorch.org/get-started/locally/"
    docsUrl: "https://pytorch.org/docs/stable/index.html"
  - frameworkId: wandb
    role: "Experiment tracking"
    why: "Logs loss, LR, and GPU memory per run so you can compare configs instead of guessing."
    install: "pip install wandb"
    quickstartUrl: "https://docs.wandb.ai/quickstart/"
    docsUrl: "https://docs.wandb.ai/"
  - frameworkId: deepspeed
    role: "Memory optimization"
    why: "ZeRO offloading lets you fine-tune models that would otherwise not fit, when a single GPU is tight."
    install: "pip install deepspeed"
    quickstartUrl: "https://www.deepspeed.ai/getting-started/"
    docsUrl: "https://www.deepspeed.ai/"
day1Plan:
  - step: 1
    task: "Prepare a clean dataset"
    estimate: "60 min"
    details: "Format as instruction/response (or chat) pairs; a few hundred high-quality examples beat thousands of noisy ones."
  - step: 2
    task: "Load the base model in 4-bit"
    estimate: "30 min"
    details: "Quantize with bitsandbytes and attach a LoRA adapter via PEFT to keep memory on a consumer GPU."
  - step: 3
    task: "Run a short training run"
    estimate: "60 min"
    details: "1-3 epochs, LR ~2e-4 for LoRA, track loss in W&B. Stop when eval loss stops improving."
  - step: 4
    task: "Merge, evaluate, and save"
    estimate: "45 min"
    details: "Evaluate on held-out prompts, merge the adapter if you want a standalone model, and push to the Hub."
starterTemplates:
  - name: "TRL SFT example"
    repo: "https://github.com/huggingface/trl/tree/main/examples"
    why: "Official supervised-fine-tuning scripts with LoRA/QLoRA flags you can run today."
  - name: "PEFT examples"
    repo: "https://github.com/huggingface/peft/tree/main/examples"
    why: "Reference notebooks for LoRA, QLoRA, and adapter merging."
learnNext:
  - title: "LoRA: Low-Rank Adaptation of Large Language Models"
    url: "https://arxiv.org/abs/2106.09685"
    kind: paper
  - title: "QLoRA: Efficient Finetuning of Quantized LLMs"
    url: "https://arxiv.org/abs/2305.14314"
    kind: paper
  - title: "Hugging Face PEFT — conceptual guides"
    url: "https://huggingface.co/docs/peft/conceptual_guides/lora"
    kind: docs
pitfalls:
  - "Reusing the pre-training learning rate: for full fine-tuning drop to ~2e-5 or you cause catastrophic forgetting."
  - "No held-out eval set: you will overfit and not notice. Split off eval data before you start."
  - "Fine-tuning to add facts: that is a retrieval problem (RAG), not a fine-tuning one."
whenToLevelUp: "When one GPU is not enough, move to multi-GPU with FSDP or DeepSpeed ZeRO-3; when you need alignment beyond SFT, add preference tuning (DPO/ORPO)."
community:
  - name: "Hugging Face Forums"
    url: "https://discuss.huggingface.co/"
  - name: "r/LocalLLaMA"
    url: "https://www.reddit.com/r/LocalLLaMA/"
  - name: "EleutherAI Discord"
    url: "https://www.eleuther.ai/community"
dontUse:
  - what: "Full fine-tuning on a single consumer GPU"
    why: "It rarely fits and rarely beats LoRA/QLoRA for adaptation. Start parameter-efficient."
  - what: "RLHF as a first step"
    why: "Supervised fine-tuning gets you most of the way; add preference tuning only once SFT plateaus."
relatedUseCases: [use-case/train-llm, use-case/serve-in-production]
tags: [fine-tuning, lora, qlora, peft, training]
updated: 2026-07-17
sources:
  - { url: "https://huggingface.co/docs/peft/index", title: "Hugging Face PEFT documentation", trust: 0.9 }
  - { url: "https://arxiv.org/abs/2106.09685", title: "LoRA: Low-Rank Adaptation of Large Language Models", trust: 0.95 }
  - { url: "https://arxiv.org/abs/2305.14314", title: "QLoRA: Efficient Finetuning of Quantized LLMs", trust: 0.95 }
---

## Overview
Fine-tuning adapts an open base model to your task, format, or tone. Parameter-efficient methods (LoRA
and QLoRA) train a tiny set of adapter weights instead of the whole model, which brings even a 7B-70B
fine-tune within reach of a single GPU.

## Why this stack
Hugging Face Transformers + PEFT + TRL is the path of least resistance: the Trainer handles the loop,
PEFT attaches the LoRA adapter, and TRL wraps supervised fine-tuning. PyTorch is the engine
underneath. Weights & Biases turns "did that config help?" from a guess into a chart. DeepSpeed is the
escape hatch when memory is tight. All open source, all swappable.

## Notes
Data quality dominates everything else — a few hundred clean examples outperform thousands of noisy
ones. Watch the learning rate (LoRA tolerates ~2e-4; full fine-tuning wants ~2e-5) and always keep a
held-out eval set. If your goal is *fresh knowledge* rather than *behaviour*, use RAG instead.
