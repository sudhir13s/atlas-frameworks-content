---
id: framework-category/training
type: framework-category
slug: training
schema_version: 3.0
title: Training Frameworks
label: Training
layer: train
order: 2
short_description: The core libraries you define, train, and differentiate neural networks in.
why_it_matters: The training framework sets how models are written, differentiated and run on hardware.
defacto:
  framework_id: framework/pytorch
  reason: Python package for GPU-accelerated tensor computation and deep neural networks built on tape-based autograd.
rising:
- framework_id: framework/jax
  reason: Composable transformations (grad, jit) of Python and NumPy functions, compiled by XLA for TPUs, GPUs and other accelerators.
- framework_id: framework/lightning
  reason: 'Organizes PyTorch code and automates the training engineering: mixed precision, multi-GPU and distributed training.'
alternatives:
- framework_id: framework/tensorflow
  reason: End-to-end open-source machine-learning platform, first developed at Google Brain, with tools to build and deploy ML applications.
- framework_id: framework/keras
  reason: Multi-backend deep-learning API that runs on JAX, TensorFlow or PyTorch.
- framework_id: framework/flax
  reason: Neural network library for JAX; Flax NNX is its current API.
key_concepts:
- autograd
- dynamic vs static graphs
- mixed precision
- the training loop
- checkpointing
canonical_reading:
- title: PyTorch — learn the basics
  url: https://docs.pytorch.org/tutorials/beginner/basics/intro.html
- title: JAX — quickstart
  url: https://docs.jax.dev/en/latest/quickstart.html
- title: PyTorch Lightning — introduction
  url: https://lightning.ai/docs/pytorch/stable/home/introduction
tags:
- training
- deep-learning
- autograd
updated: '2026-11-21'
sources:
- url: https://github.com/pytorch/pytorch
  title: PyTorch repository
  trust: 0.9
- url: https://github.com/jax-ml/jax
  title: JAX repository
  trust: 0.9
- url: https://github.com/Lightning-AI/pytorch-lightning
  title: PyTorch Lightning repository
  trust: 0.9
- url: https://github.com/tensorflow/tensorflow
  title: TensorFlow repository
  trust: 0.9
- url: https://github.com/keras-team/keras
  title: Keras repository
  trust: 0.9
- url: https://github.com/google/flax
  title: Flax repository
  trust: 0.9
---


