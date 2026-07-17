---
id: framework-category/training
type: framework-category
slug: training
schema_version: 1.0
title: "Training Frameworks"
label: "Training"
order: 2
shortDescription: "The core libraries you define, train, and differentiate neural networks in."
whyItMatters: "Your training framework decides how you express models, how fast you iterate, and what the ecosystem hands you."
defacto:
  frameworkId: pytorch
  reason: "The research and production default — dynamic graphs, a huge ecosystem, and first-class code in nearly every new paper."
rising:
  - frameworkId: jax
    reason: "Functional, composable transforms (grad/jit/vmap) and XLA speed; the default at several frontier labs."
  - frameworkId: lightning
    reason: "Strips training-loop boilerplate while keeping the model code pure PyTorch."
alternatives:
  - frameworkId: tensorflow
    reason: "Still strong in production/serving and mobile; the incumbent before PyTorch."
  - frameworkId: keras
    reason: "High-level API, now multi-backend (TF/JAX/PyTorch), ideal for fast prototyping."
  - frameworkId: flax
    reason: "The neural-net layer library most JAX users reach for."
keyConcepts:
  - "autograd"
  - "dynamic vs static graphs"
  - "mixed precision"
  - "the training loop"
  - "checkpointing"
canonicalReading:
  - title: "PyTorch — learn the basics"
    url: "https://pytorch.org/tutorials/beginner/basics/intro.html"
  - title: "JAX — quickstart"
    url: "https://jax.readthedocs.io/en/latest/quickstart.html"
  - title: "PyTorch Lightning — introduction"
    url: "https://lightning.ai/docs/pytorch/stable/starter/introduction.html"
didYouKnow:
  - "PyTorch was originally a Python port of Torch (Lua), released by Meta AI in 2016."
  - "JAX has no built-in neural-net layer library — Flax and Haiku fill that gap."
  - "Almost every new arXiv paper in 2024-2025 ships PyTorch code first."
tags: [training, deep-learning, autograd]
updated: 2026-07-17
sources:
  - { url: "https://pytorch.org/docs/stable/index.html", title: "PyTorch documentation", trust: 0.95 }
  - { url: "https://jax.readthedocs.io/", title: "JAX documentation", trust: 0.9 }
  - { url: "https://lightning.ai/docs/pytorch/stable/", title: "PyTorch Lightning documentation", trust: 0.9 }
---

## Overview
Training frameworks are the substrate you build and optimize models on: they provide tensors,
automatic differentiation, hardware acceleration, and the training loop. The choice shapes iteration
speed and which pretrained models and tools you can reuse.

## Landscape
PyTorch is the default almost everywhere, thanks to dynamic graphs and an ecosystem that ships PyTorch
code first. JAX is rising fast where functional composition and XLA performance matter (and dominates
at some frontier labs). Lightning removes loop boilerplate on top of PyTorch. TensorFlow, Keras, and
Flax hold specific niches — production/mobile, prototyping, and JAX layers respectively.

## Notes
For a new project in 2026, PyTorch is the safe default and JAX the considered bet for large-scale or
research-heavy work. Whichever you pick, learn mixed precision and checkpointing early — they decide
whether your runs fit and survive.
