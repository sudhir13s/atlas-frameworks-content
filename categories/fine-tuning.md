---
id: framework-category/fine-tuning
type: framework-category
slug: fine-tuning
schema_version: 1.1
title: Fine-tuning & PEFT
label: Fine-tuning & PEFT
order: 9
short_description: Libraries for adapting open base models — supervised fine-tuning, parameter-efficient adapters (LoRA/QLoRA), and preference tuning.
why_it_matters: Fine-tuning changes a model's behaviour and style cheaply; PEFT brings even 70B adaptation within a single GPU.
defacto:
  framework_id: framework/hugging-face-transformers
  reason: The Trainer plus the PEFT and TRL libraries make LoRA/QLoRA SFT and DPO a few lines of config on any open model.
rising:
- framework_id: framework/deepspeed
  reason: ZeRO offloading fits large fine-tunes into tight memory and scales multi-GPU.
alternatives:
- framework_id: framework/pytorch
  reason: Drop to a raw training loop when you need full control over the fine-tuning process.
- framework_id: framework/jax
  reason: Functional composition and XLA speed for teams already training in JAX.
key_concepts:
- LoRA / QLoRA
- supervised fine-tuning
- preference tuning (DPO)
- catastrophic forgetting
- quantized training
canonical_reading:
- title: 'LoRA: Low-Rank Adaptation of Large Language Models'
  url: https://arxiv.org/abs/2106.09685
- title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
  url: https://arxiv.org/abs/2305.14314
- title: Hugging Face PEFT — documentation
  url: https://huggingface.co/docs/peft/index
did_you_know:
- LoRA reduces trainable parameters by ~10,000x versus full fine-tuning.
- QLoRA made 65B-parameter fine-tuning possible on a single 48GB GPU.
- DPO removed the need for a separate reward model that RLHF required.
tags:
- fine-tuning
- peft
- lora
- qlora
- alignment
updated: '2026-11-19'
sources:
- url: https://huggingface.co/docs/peft/index
  title: Hugging Face PEFT documentation
  trust: 0.9
- url: https://arxiv.org/abs/2106.09685
  title: 'LoRA: Low-Rank Adaptation of Large Language Models'
  trust: 0.95
- url: https://arxiv.org/abs/2305.14314
  title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
  trust: 0.95
---

## Overview

Fine-tuning adapts an open base model to a task, format, or tone. Parameter-efficient methods (LoRA,
QLoRA) train a tiny adapter instead of the whole model, and preference tuning (DPO/ORPO) aligns a model
to human choices — together they cover most real adaptation needs without full retraining.

## Landscape

The Hugging Face stack — Transformers + PEFT + TRL — is the default path: PEFT attaches the adapter and
TRL wraps SFT and DPO. When one GPU is not enough, PyTorch FSDP and DeepSpeed ZeRO scale the fine-tune
across devices. Dropping to raw PyTorch or JAX is the choice when you need full control of the loop.

## Notes

Data quality dominates — a few hundred clean examples beat thousands of noisy ones. Mind the learning
rate (LoRA tolerates ~2e-4; full fine-tuning wants ~2e-5) to avoid catastrophic forgetting, and reach
for SFT before preference tuning. If the goal is fresh knowledge rather than behaviour, use RAG instead.
