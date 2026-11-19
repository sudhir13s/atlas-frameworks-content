---
id: use-case/train-llm
type: use-case
slug: train-llm
schema_version: 1.1
title: Train an LLM from Scratch
label: Train from scratch
order: 5
goal: Pre-train a transformer language model from initialization, scaling from a laptop nanoGPT to a multi-GPU run.
languages:
- python
levels:
- advanced
stack:
- framework_id: framework/pytorch
  role: Core framework
  why: 'The research default: dynamic graphs, full control over the training loop, and every new paper ships PyTorch first.'
  install: pip install torch
  quickstart_url: https://pytorch.org/tutorials/beginner/basics/intro.html
  docs_url: https://pytorch.org/docs/stable/index.html
- framework_id: framework/lightning
  role: Training loop scaffolding
  why: Removes boilerplate (device placement, mixed precision, checkpointing) while keeping the model code pure PyTorch.
  install: pip install lightning
  quickstart_url: https://lightning.ai/docs/pytorch/stable/starter/introduction.html
  docs_url: https://lightning.ai/docs/pytorch/stable/
- framework_id: framework/deepspeed
  role: Distributed training
  why: ZeRO partitions optimizer state, gradients, and parameters across GPUs so large models fit and scale.
  install: pip install deepspeed
  quickstart_url: https://www.deepspeed.ai/getting-started/
  docs_url: https://www.deepspeed.ai/
- framework_id: framework/wandb
  role: Experiment tracking
  why: Long pre-training runs need loss curves, throughput, and grad-norm dashboards to catch divergence early.
  install: pip install wandb
  quickstart_url: https://docs.wandb.ai/quickstart/
  docs_url: https://docs.wandb.ai/
day1_plan:
- step: 1
  task: Run nanoGPT on a small corpus
  estimate: 60 min
  details: Train a tiny char/BPE model end to end so the whole loop (data → tokens → model → loss) is concrete.
- step: 2
  task: Swap in a real tokenizer + dataset
  estimate: 60 min
  details: Use a BPE tokenizer and a streamed dataset; verify token throughput and that loss decreases.
- step: 3
  task: Add mixed precision + checkpointing
  estimate: 45 min
  details: Enable bf16 and gradient checkpointing via Lightning; confirm memory drops and resumption works.
- step: 4
  task: Scale to multiple GPUs
  estimate: 90 min
  details: Introduce DeepSpeed ZeRO or FSDP; watch scaling efficiency and keep the effective batch size sane.
starter_templates:
- name: nanoGPT
  repo: https://github.com/karpathy/nanoGPT
  why: The canonical minimal, readable GPT training loop — the best place to start.
- name: litGPT
  repo: https://github.com/Lightning-AI/litgpt
  why: Production-grade pretraining/finetuning recipes for open LLMs on Lightning.
learn_next:
- title: 'Let''s build GPT: from scratch (Karpathy)'
  url: https://www.youtube.com/watch?v=kCc8FmEb1nY
  kind: video
- title: Scaling Laws for Neural Language Models
  url: https://arxiv.org/abs/2001.08361
  kind: paper
- title: DeepSpeed — ZeRO
  url: https://www.deepspeed.ai/tutorials/zero/
  kind: docs
pitfalls:
- 'Learning rate too high: loss spikes to NaN. Use warmup + cosine decay and watch the grad norm.'
- 'Under-provisioned data: a model starved of tokens will not learn. Respect the compute-optimal token budget.'
- 'Skipping the tiny run: debug the full loop on a small model before spending GPU-days on a big one.'
when_to_level_up: When a single node is the limit, add tensor/pipeline parallelism (Megatron-LM) on top of ZeRO/FSDP; when the goal is a usable assistant, move from pre-training to fine-tuning and alignment.
community:
- name: EleutherAI Discord
  url: https://www.eleuther.ai/community
- name: Hugging Face Forums
  url: https://discuss.huggingface.co/
- name: PyTorch Forums
  url: https://discuss.pytorch.org/
dont_use:
- what: Training a foundation model from scratch to save money
  why: Pre-training is compute-dominated and expensive; fine-tuning an open base model is almost always the right call.
- what: A high-level framework you cannot see into
  why: At this level you need to inspect the loss, gradients, and data path — keep the model code transparent.
related_use_cases:
- use-case/fine-tune
- use-case/serve-in-production
tags:
- training
- pretraining
- transformers
- distributed
updated: '2026-11-19'
sources:
- url: https://github.com/karpathy/nanoGPT
  title: nanoGPT
  trust: 0.9
- url: https://arxiv.org/abs/2001.08361
  title: Scaling Laws for Neural Language Models
  trust: 0.95
- url: https://www.deepspeed.ai/tutorials/zero/
  title: DeepSpeed ZeRO tutorial
  trust: 0.9
---

## Overview

Training from scratch means starting from random weights and learning everything from data. Most
people should not do this for a foundation model — but building a small one end to end is the single
best way to understand how LLMs actually work, and it scales cleanly from a laptop to a cluster.

## Why this stack

PyTorch is the research default and keeps the loop transparent. Lightning strips the boilerplate
(devices, precision, checkpoints) without hiding the model. DeepSpeed's ZeRO is what makes large runs
fit across GPUs. Weights & Biases catches divergence early on runs that last hours or days. Start with
nanoGPT to make the whole pipeline concrete before scaling.

## Notes

The classic failure modes are a too-high learning rate (loss goes NaN) and too few training tokens
(the model never converges). Always debug on a tiny model first. For most real goals, fine-tuning an
open base model beats pre-training on both cost and quality.
