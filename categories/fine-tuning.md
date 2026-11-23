---
id: framework-category/fine-tuning
type: framework-category
slug: fine-tuning
schema_version: 3.0
title: Fine-tuning & PEFT
label: Fine-tuning & PEFT
layer: train
order: 9
short_description: Libraries for adapting open base models — supervised fine-tuning, parameter-efficient adapters (LoRA/QLoRA), and preference tuning.
why_it_matters: Fine-tuning adapts an open model to a task or style; the QLoRA paper fine-tuned a 65B-parameter model on a single 48 GB GPU.
defacto:
  framework_id: framework/hugging-face-transformers
  reason: Its Trainer is a complete training API for Transformers models, and the PEFT (parameter-efficient adapters) and TRL (SFTTrainer, DPOTrainer) libraries are integrated with Transformers.
rising:
- framework_id: framework/deepspeed
  reason: Training library built around ZeRO, ZeRO-Infinity and 3D parallelism for training large models across GPUs.
alternatives:
- framework_id: framework/pytorch
  reason: Tensor library with GPU acceleration and tape-based autograd, for writing the training loop yourself.
- framework_id: framework/jax
  reason: Composable function transformations (grad, jit) compiled by XLA for GPUs and TPUs.
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
tags:
- fine-tuning
- peft
- lora
- qlora
- alignment
updated: '2026-11-21'
sources:
- url: https://huggingface.co/docs/transformers/main_classes/trainer
  title: Transformers — Trainer
  trust: 0.9
- url: https://huggingface.co/docs/peft/index
  title: Hugging Face PEFT — documentation
  trust: 0.9
- url: https://huggingface.co/docs/trl/index
  title: TRL — documentation
  trust: 0.9
- url: https://github.com/deepspeedai/DeepSpeed
  title: DeepSpeed repository
  trust: 0.9
- url: https://github.com/pytorch/pytorch
  title: PyTorch repository
  trust: 0.9
- url: https://github.com/jax-ml/jax
  title: JAX repository
  trust: 0.9
- url: https://arxiv.org/abs/2305.14314
  title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
  trust: 0.9
---


