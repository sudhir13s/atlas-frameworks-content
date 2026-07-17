# Changelog

All notable changes to `ai-frameworks-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

### Added
- Repository scaffold to the content-repo standard: `meta.json`, `schema/registry.json`, the three
  JSON Schemas (`_shared`, `use-case`, `framework-category`), templates, and docs (`README`,
  `AGENTS`, `CONVENTIONS`).
- Initial content library (schema version 1.0), all cited against official framework documentation
  and cross-link-validated:
  - **8 getting-started use cases** — build a RAG app, build an agent, fine-tune an LLM, serve a
    model in production, train an LLM from scratch, deploy on-device, build an ML data pipeline,
    build a multimodal app — each with a concrete stack, day-1 plan, starter templates, pitfalls,
    what to learn next, community, and what not to use.
  - **10 framework categories** — LLM frameworks, training, inference, RAG, agents, data/ETL,
    experiment tracking (MLOps), vector DBs, fine-tuning/PEFT, and deployment/serving — each with the
    defacto choice, rising alternatives, key concepts, and canonical reading.

## Schema versions

- **1.0** — initial schema for the two frameworks content types (`use-case`, `framework-category`).
