---
id: use-case/build-multimodal-app
type: use-case
slug: build-multimodal-app
schema_version: 2.0
title: Build a Multimodal App
label: Build a multimodal app
order: 8
goal: Accept images, documents, audio and video alongside text, answer questions about them, search across them, and reply in text or speech.
stages:
- id: input
  name: Input
  note: Runs on every request, and offline when files are indexed for search.
- id: model
  name: Understanding and response
  note: Runs on every request after the input is prepared.
- id: quality
  name: Quality and operations
  note: Runs before each release and continuously in production.
blocks:
- id: user-interface
  stage: input
  name: User interface
  purpose: Collects text, uploaded files and microphone recordings from the user and shows the reply.
  options:
  - record: framework/gradio
    choice: default
    when: Apache-2.0 Python library whose multimodal textbox takes text plus image, audio and video uploads or a microphone recording, with public share links and hosting on Hugging Face Spaces.
  - record: framework/streamlit
    choice: alternative
    when: Pick it for a data app or dashboard around the model; its chat input accepts files and audio recordings, under Apache-2.0.
  how_to_choose:
  - 'A demo or internal tool in Python: one of these; a product front end: your own web app calling the same API.'
  - Restrict accepted file types at the interface so later steps only see formats they handle.
  browse:
    label: All app and UI tools
    record: framework-category/other
- id: speech-to-text
  stage: input
  name: Speech recognition
  purpose: Transcribes spoken input into text with timestamps for models or pipelines that take text.
  options:
  - record: framework/faster-whisper
    choice: default
    when: MIT-licensed reimplementation of Whisper on the CTranslate2 engine that runs on CPU or NVIDIA GPU, supports quantization on both, filters silence with voice activity detection and returns word timestamps.
  - record: framework/whisper-cpp
    choice: alternative
    when: Pick it for devices and browsers; it is a dependency-free C/C++ implementation for Apple Silicon, iOS, Android, WebAssembly and CPU-only machines.
  - record: model/whisper-large-v3-turbo
    choice: alternative
    when: Pick this checkpoint when speed matters more than the last bit of accuracy; it is a pruned large-v3 that is faster at a minor quality cost, under MIT.
  how_to_choose:
  - 'Server-side transcription: faster-whisper; on-device or in-browser: whisper.cpp.'
  - Skip this block when the chosen model takes audio directly.
  browse:
    label: All speech recognition models
    record: task/speech-recognition
- id: document-ocr
  stage: input
  name: Document and image text extraction
  purpose: Extracts text, tables and layout from scanned pages, photos and PDFs so they can be searched or passed to a text model.
  options:
  - record: framework/paddleocr
    choice: default
    when: Apache-2.0 toolkit that recognises text in many languages and converts PDFs and images to Markdown or JSON with table and text coordinates.
  - record: model/paddleocr-vl
    choice: alternative
    when: Pick it for a lightweight vision-language model built for document parsing, from the same project and licence.
  - record: framework/surya
    choice: alternative
    when: Pick it for layout, reading order, HTML tables and inline LaTeX; its code is Apache-2.0 but its weights carry a modified OpenRAIL-M licence with commercial limits.
  - record: framework/tesseract
    choice: alternative
    when: Pick it for an Apache-2.0 library and command-line engine that reads many languages out of the box and outputs plain text, hOCR, PDF, TSV and ALTO.
  how_to_choose:
  - 'Need exact text, coordinates or tables for search and citation: run OCR; need only a question answered about the image: send it to the vision-language model.'
  - Check model-weight licences before commercial use.
  browse:
    label: All OCR models
    record: task/ocr
- id: multimodal-embeddings
  stage: input
  name: Multimodal embeddings
  purpose: Maps images and text into one vector space so users can search images with text or find similar images.
  options:
  - record: model/siglip-so400m-patch14-384
    choice: default
    when: Apache-2.0 image-text model trained with a sigmoid loss, intended for zero-shot image classification and image-text retrieval.
  - record: framework/sentence-transformers
    choice: alternative
    when: Pick it as the library that computes embeddings from text, images, audio or video and fine-tunes them on your own pairs.
  how_to_choose:
  - Store image vectors in the same vector database as text so one query covers both.
  - Fine-tune only after measuring retrieval on your own image-text pairs.
  browse:
    label: All image and multimodal embedding models
    record: task/image-and-multimodal-embeddings
- id: vision-language-model
  stage: model
  name: Multimodal model
  purpose: Reads the text together with images, audio or video frames and produces the answer.
  options:
  - record: model/gemma-4-e4b-it
    choice: default
    when: Apache-2.0 model that takes text, images and audio (video as frames), supports structured tool use, and is designed for local execution on laptops and phones.
  - record: model/qwen2-5-omni-7b
    choice: alternative
    when: Pick it when the reply must be spoken; it takes text, images, audio and video and streams text and natural speech, under Apache-2.0.
  how_to_choose:
  - 'Need speech out of the same model: an omni model; need text out: a vision-language model.'
  - Compare candidates on the multimodal benchmarks below, then on your own files.
  browse:
    label: All vision-language models
    record: task/vision-language-models
- id: model-serving
  stage: model
  name: Model serving
  purpose: Runs the multimodal model behind an API that accepts images, video and audio in the request.
  options:
  - record: framework/vllm
    choice: default
    when: Apache-2.0 engine whose OpenAI-compatible Chat Completions API accepts image, video and audio inputs.
  - record: framework/sglang
    choice: alternative
    when: Pick it for serving vision-language models with an OpenAI-compatible API on a wide range of accelerators.
  - record: framework/llama-cpp
    choice: alternative
    when: Pick it for multimodal inference with minimal setup on a wide range of hardware, with an OpenAI-compatible server.
  how_to_choose:
  - Check that the engine lists your exact model before choosing it.
  - Send media in the same OpenAI-style request format so engines stay swappable.
  browse:
    label: All serving tools
    record: framework-category/llm-serving
- id: text-to-speech
  stage: model
  name: Speech output
  purpose: Turns the text reply into speech when the app talks back.
  options:
  - record: model/kokoro-82m
    choice: default
    when: Small open-weight text-to-speech model with Apache-licensed weights that its makers state can be deployed in production or personal projects.
  - record: model/qwen2-5-omni-7b
    choice: alternative
    when: Pick it to generate speech in the same model that understands the input, without a separate speech step.
  - record: model/xtts-v2
    choice: alternative
    when: Pick it to clone a voice from a short reference clip across languages; read the Coqui Public Model License before use.
  how_to_choose:
  - Read each speech model's licence; several restrict commercial use.
  - Clone a voice only with the speaker's recorded consent.
  browse:
    label: All text-to-speech models
    record: task/text-to-speech
- id: safety
  stage: quality
  name: Guardrails
  purpose: Classifies text and images in the request and the reply for unsafe content before they are processed or shown.
  options:
  - record: model/llama-guard-4-12b
    choice: default
    when: A multimodal safety classifier for prompts and responses that handles text with multiple images, returning the violated hazard categories; released under the Llama 4 Community License.
  - record: model/nsfw-image-detection
    choice: alternative
    when: Pick it for an Apache-2.0 image-classification model published for NSFW image detection, to screen uploads before they reach the main model.
  - record: model/llama-prompt-guard-2-86m
    choice: alternative
    when: Pick it to scan text pulled from files and transcripts for prompt injection and jailbreaks.
  how_to_choose:
  - Screen images as well as text; instructions and unsafe content can arrive inside uploaded files.
  - Filter both the input and the reply.
  browse:
    label: All safety and guard models
    record: task/safety-and-guard-models
- id: evaluation
  stage: quality
  name: Evaluation
  purpose: Scores whether answers about images and other media are correct and supported by the input.
  options:
  - record: framework/ragas
    choice: default
    when: Provides multimodal faithfulness and multimodal relevance metrics alongside its text metrics.
  - record: framework/promptfoo
    choice: alternative
    when: Pick it for declarative test cases run locally and in CI, with red teaming of the same app.
  how_to_choose:
  - Build a labelled set from your own files, not only public images.
  - Measure each input path (image, document, audio) separately.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
- id: benchmarks
  stage: quality
  name: Benchmarks for model choice
  purpose: Compares candidate models on public multimodal tasks before you test them on your own data.
  options:
  - record: benchmark/mmmu-pro
    choice: default
    when: A harder version of the college-level multimodal benchmark MMMU that removes questions text-only models can answer and adds a vision-only setting.
  - record: benchmark/lvbench
    choice: alternative
    when: Use it for video apps; it tests long-term memory and comprehension over long videos.
  - record: benchmark/voicebench
    choice: alternative
    when: Use it for voice assistants; it tests spoken and typed instructions across question answering, instruction following, reasoning and safety.
  how_to_choose:
  - Read the benchmark that matches your input type; image scores do not transfer to video or speech.
- id: tracing
  stage: quality
  name: Tracing and observability
  purpose: Records each request's inputs, model calls, outputs, latency and cost so failures can be traced to the step that caused them.
  options:
  - record: framework/langfuse
    choice: default
    when: Open-source platform built on OpenTelemetry that traces model calls and related steps, evaluates them, and can be self-hosted.
  - record: framework/mlflow
    choice: alternative
    when: Pick it when you already run MLflow; its tracing is OpenTelemetry-compatible and the data stays on your infrastructure.
  how_to_choose:
  - Log references to stored media rather than raw files, to keep traces small.
  - Prefer a tool that accepts OpenTelemetry so you can switch backends later.
learn_next:
- title: vLLM multimodal inputs
  url: https://docs.vllm.ai/en/latest/features/multimodal_inputs.html
  kind: docs
- title: 'MMMU-Pro: A More Robust Multi-discipline Multimodal Understanding Benchmark'
  url: https://arxiv.org/abs/2409.02813
  kind: paper
- title: Gradio MultimodalTextbox
  url: https://www.gradio.app/docs/gradio/multimodaltextbox
  kind: docs
related_use_cases:
- use-case/build-a-rag-app
- use-case/build-an-agent
- use-case/serve-in-production
tags:
- multimodal
- vision-language
- speech
- ocr
- embeddings
updated: '2026-11-21'
sources:
- url: https://github.com/gradio-app/gradio
  title: Gradio repository
  trust: 0.9
- url: https://www.gradio.app/docs/gradio/multimodaltextbox
  title: Gradio MultimodalTextbox documentation
  trust: 0.9
- url: https://github.com/streamlit/streamlit
  title: Streamlit repository
  trust: 0.9
- url: https://docs.streamlit.io/develop/api-reference/chat/st.chat_input
  title: Streamlit st.chat_input documentation
  trust: 0.9
- url: https://github.com/SYSTRAN/faster-whisper
  title: faster-whisper repository
  trust: 0.9
- url: https://github.com/ggml-org/whisper.cpp
  title: whisper.cpp repository
  trust: 0.9
- url: https://huggingface.co/openai/whisper-large-v3-turbo
  title: openai/whisper-large-v3-turbo model card
  trust: 0.9
- url: https://github.com/PaddlePaddle/PaddleOCR
  title: PaddleOCR repository
  trust: 0.9
- url: https://github.com/datalab-to/surya
  title: Surya repository
  trust: 0.9
- url: https://github.com/tesseract-ocr/tesseract
  title: Tesseract repository
  trust: 0.9
- url: https://huggingface.co/google/siglip-so400m-patch14-384
  title: google/siglip-so400m-patch14-384 model card
  trust: 0.9
- url: https://sbert.net/
  title: Sentence Transformers documentation
  trust: 0.9
- url: https://huggingface.co/google/gemma-4-E4B-it
  title: google/gemma-4-E4B-it model card
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen2.5-Omni-7B
  title: Qwen/Qwen2.5-Omni-7B model card
  trust: 0.9
- url: https://docs.vllm.ai/en/latest/features/multimodal_inputs.html
  title: vLLM multimodal inputs
  trust: 0.9
- url: https://github.com/vllm-project/vllm
  title: vLLM repository
  trust: 0.9
- url: https://github.com/sgl-project/sglang
  title: SGLang repository
  trust: 0.9
- url: https://docs.sglang.io/
  title: SGLang documentation
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp repository
  trust: 0.9
- url: https://huggingface.co/hexgrad/Kokoro-82M
  title: hexgrad/Kokoro-82M model card
  trust: 0.9
- url: https://huggingface.co/coqui/XTTS-v2
  title: coqui/XTTS-v2 model card
  trust: 0.9
- url: https://huggingface.co/microsoft/VibeVoice-1.5B
  title: microsoft/VibeVoice-1.5B model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B model card
  trust: 0.9
- url: https://huggingface.co/Falconsai/nsfw_image_detection
  title: Falconsai/nsfw_image_detection model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-86M
  title: meta-llama/Llama-Prompt-Guard-2-86M model card
  trust: 0.9
- url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  title: OWASP LLM01:2025 Prompt Injection
  trust: 0.9
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
  title: Ragas available metrics
  trust: 0.9
- url: https://github.com/promptfoo/promptfoo
  title: promptfoo repository
  trust: 0.9
- url: https://arxiv.org/abs/2409.02813
  title: 'MMMU-Pro: A More Robust Multi-discipline Multimodal Understanding Benchmark (arXiv)'
  trust: 0.95
- url: https://mmmu-benchmark.github.io/
  title: MMMU benchmark site
  trust: 0.9
- url: https://arxiv.org/abs/2406.08035
  title: 'LVBench: An Extreme Long Video Understanding Benchmark (arXiv)'
  trust: 0.95
- url: https://github.com/MatthewCYM/VoiceBench
  title: VoiceBench repository
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://mlflow.org/docs/latest/genai/tracing/
  title: MLflow Tracing documentation
  trust: 0.9
---

## Overview

A multimodal app takes images, documents, audio and video with the text. **Input** blocks collect files, transcribe speech, extract document text and embed images for search; some models take the raw media directly.

The **model** blocks run a multimodal model behind an API that accepts media and can speak the reply. **Quality** blocks screen text and images, score answers, compare models on benchmarks matching the input type, and trace every request.
