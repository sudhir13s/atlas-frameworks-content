---
id: framework/hugging-face-transformers
type: framework
slug: hugging-face-transformers
schema_version: 3.0
title: Hugging Face Transformers
status: curated
kind: library
category: framework-category/llm-frameworks
subcategory: model-library
tagline: The model-definition framework for machine learning models in text, vision, audio, and multimodal models, for both inference and training.
description: Model-definition framework from Hugging Face for machine learning models in text, computer vision, audio, video and multimodal tasks, for both inference and training. It centralizes model definitions so that they work across training frameworks, inference engines and adjacent modeling libraries. It runs on PyTorch and loads Transformers model checkpoints from the Hugging Face Hub.
best_for: Inference with pretrained models, Fine-tuning pretrained models, Research iteration on model architectures
not_ideal_for: Building networks from modular building blocks, Generic training loops for models outside Transformers (the docs point to Accelerate)
key_features:
- Pretrained model checkpoints on the Hugging Face Hub
- Pipeline API for text, audio, vision and multimodal inference
- Trainer with mixed precision, torch.compile, FlashAttention and distributed training
- generate for LLM and VLM text generation with streaming
- Every model built from a configuration, a model and a preprocessor class
- Quantization methods including bitsandbytes and GGUF
- PEFT integration for training LoRA adapters
use_cases:
- LLM inference and fine-tuning
- Text classification and named entity recognition
- Image classification and object detection
- Speech recognition and text to speech
- Multimodal tasks such as visual question answering
pros:
- One API across all its pretrained models
- Model files can be used independently of the library
- Examples reproduce the results published by each architecture's original authors
- Runs on many PyTorch hardware backends
cons:
- Model files deliberately avoid shared abstractions so it is not a modular building-block toolbox
- The training API is optimized for PyTorch models provided by Transformers
language: Python
languages_supported:
- Python
maintained_by: Hugging Face
license_spdx: Apache-2.0
github_url: https://github.com/huggingface/transformers
docs_url: https://huggingface.co/docs/transformers/
website_url: https://huggingface.co/
maturity: production
backing:
  type: corporate
  orgs:
  - organization/hugging-face
alternatives:
- framework/vllm
- framework/llama-cpp
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 169318
  downloads_monthly: 120882484
  latest_version: 5.23.0
  latest_release_date: '2026-11-13'
  observed_at: '2026-11-20'
  source: https://github.com/huggingface/transformers
aliases:
- huggingface/transformers
tags:
- llm
- transformers
- nlp
- multimodal
- model-hub
- fine-tuning
updated: '2026-11-21'
sources:
- url: https://github.com/huggingface/transformers
  title: GitHub repository
- url: https://huggingface.co/docs/transformers/
  title: Documentation
- url: https://huggingface.co/docs/transformers/installation
  title: Installation
- url: https://huggingface.co/docs/transformers/accelerator_selection
  title: Hardware
- url: https://huggingface.co/docs/transformers/perf_train_special
  title: Apple Silicon
- url: https://pypi.org/project/transformers/
  title: transformers — PyPI
---


