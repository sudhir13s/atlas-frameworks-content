---
id: use-case/build-multimodal-app
type: use-case
slug: build-multimodal-app
schema_version: 1.0
title: "Build a Multimodal App"
label: "Multimodal app"
order: 8
goal: "Combine images (or audio) with text — caption, search across modalities, or answer questions about a picture."
languages: [python]
levels: [intermediate, advanced]
stack:
  - frameworkId: hugging-face-transformers
    role: "Multimodal models"
    why: "One API for CLIP, BLIP, LLaVA, and Whisper — load a vision-language or speech model in a few lines."
    install: "pip install transformers"
    quickstartUrl: "https://huggingface.co/docs/transformers/tasks/image_text_to_text"
    docsUrl: "https://huggingface.co/docs/transformers/index"
  - frameworkId: sentence-transformers
    role: "Cross-modal embeddings"
    why: "CLIP-style models embed text and images into one space, enabling image search by text query."
    install: "pip install sentence-transformers"
    quickstartUrl: "https://www.sbert.net/examples/applications/image-search/README.html"
    docsUrl: "https://www.sbert.net/"
  - frameworkId: torchvision
    role: "Image I/O + transforms"
    why: "Standard, tested image decoding, preprocessing, and augmentation that pairs with PyTorch models."
    install: "pip install torchvision"
    quickstartUrl: "https://pytorch.org/vision/stable/transforms.html"
    docsUrl: "https://pytorch.org/vision/stable/index.html"
  - frameworkId: qdrant
    role: "Multimodal vector search"
    why: "Stores the joint embeddings and serves fast nearest-neighbour search across text and images."
    install: "pip install qdrant-client"
    quickstartUrl: "https://qdrant.tech/documentation/quickstart/"
    docsUrl: "https://qdrant.tech/documentation/"
day1Plan:
  - step: 1
    task: "Load a vision-language model"
    estimate: "30 min"
    details: "Load BLIP or LLaVA via Transformers and caption a single image to confirm the pipeline works."
  - step: 2
    task: "Embed images and text with CLIP"
    estimate: "45 min"
    details: "Use sentence-transformers CLIP to embed a folder of images and a set of text queries into one space."
  - step: 3
    task: "Index and search"
    estimate: "45 min"
    details: "Upsert image embeddings into Qdrant and run a text query to retrieve matching images."
  - step: 4
    task: "Wrap it in a small app"
    estimate: "60 min"
    details: "Expose an endpoint that takes an image or text and returns captions or cross-modal search results."
starterTemplates:
  - name: "Sentence-Transformers image search"
    repo: "https://github.com/UKPLab/sentence-transformers/tree/master/examples/applications/image-search"
    why: "Runnable CLIP image-search example to copy the embed-index-query flow."
  - name: "Transformers multimodal examples"
    repo: "https://github.com/huggingface/transformers/tree/main/examples"
    why: "Official task examples spanning vision, speech, and vision-language."
learnNext:
  - title: "Learning Transferable Visual Models From Natural Language Supervision (CLIP)"
    url: "https://arxiv.org/abs/2103.00020"
    kind: paper
  - title: "Visual Instruction Tuning (LLaVA)"
    url: "https://arxiv.org/abs/2304.08485"
    kind: paper
  - title: "Transformers — image-text-to-text"
    url: "https://huggingface.co/docs/transformers/tasks/image_text_to_text"
    kind: docs
pitfalls:
  - "Mismatched preprocessing: each vision model expects its own image size/normalization. Use the model's own processor."
  - "Embedding modalities with different models: text and image must share one CLIP space to compare."
  - "Underestimating VRAM: vision-language models are heavy. Check memory before batching."
whenToLevelUp: "When zero-shot quality plateaus, fine-tune the vision-language model on your domain; add a reranker over cross-modal retrieval, and move to a frontier multimodal model for hard reasoning."
community:
  - name: "Hugging Face Forums"
    url: "https://discuss.huggingface.co/"
  - name: "Qdrant Discord"
    url: "https://qdrant.to/discord"
  - name: "PyTorch Forums"
    url: "https://discuss.pytorch.org/"
dontUse:
  - what: "Separate text and image embedding models for cross-modal search"
    why: "They live in different spaces; you cannot compare their vectors. Use one CLIP-style model."
  - what: "A raw filesystem scan for image search"
    why: "It does not scale and cannot do semantic matching. Index embeddings in a vector DB."
relatedUseCases: [use-case/build-a-rag-app, use-case/deploy-on-device]
tags: [multimodal, vision-language, clip, image-search]
updated: 2026-07-17
sources:
  - { url: "https://huggingface.co/docs/transformers/tasks/image_text_to_text", title: "Transformers — image-text-to-text", trust: 0.9 }
  - { url: "https://arxiv.org/abs/2103.00020", title: "Learning Transferable Visual Models From Natural Language Supervision (CLIP)", trust: 0.95 }
  - { url: "https://www.sbert.net/examples/applications/image-search/README.html", title: "Sentence-Transformers — Image Search", trust: 0.85 }
---

## Overview
A multimodal app reasons across more than one kind of input — most commonly images plus text. The two
workhorse patterns are captioning / visual question answering (a vision-language model) and cross-modal
search (embed images and text into one space, then query one with the other).

## Why this stack
Hugging Face Transformers gives one API over CLIP, BLIP, LLaVA, and Whisper. Sentence-Transformers
wraps CLIP for the embed-and-search pattern. torchvision handles correct, tested image I/O and
transforms, and Qdrant stores the joint embeddings for fast nearest-neighbour search. Everything here
is open source and runs locally.

## Notes
The subtle bug in multimodal work is space mismatch — text and images must be embedded by the *same*
CLIP-style model to be comparable, and each vision model needs its own processor for preprocessing.
These models are VRAM-heavy, so check memory before batching. Fine-tune only once zero-shot quality
clearly plateaus.
