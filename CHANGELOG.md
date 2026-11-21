# Changelog

All notable changes to `ai-frameworks-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

### Content (category accuracy pass)

- **Changed** the default pick reason and every rising and alternative reason in the ten
  categories that name frameworks: each now states only what the framework's own repository or
  documentation says it is or does. Popularity, speed multiples and adoption claims are gone.
- **Changed** `description` and "when you need it" text in those categories to plain statements;
  the fine-tuning and inference lines cite the QLoRA and PagedAttention papers for their figures.
- **Removed** `framework/autogen` from the agents category's rising picks: its repository is
  archived and points new users to Microsoft Agent Framework. The semantic-kernel reason now names
  that successor.
- **Removed** every `did_you_know` list and every `Overview`, `Landscape` and `Notes` body section
  from the category records. The site shows none of them and they cited no source. All are
  optional in the schema and the registry.
- **Changed** further-reading links that had moved to their current pages (LangGraph, CrewAI,
  LangChain, LlamaIndex, vLLM, PyTorch, JAX, Lightning, Weights & Biases), and set `sources` to the
  pages each record now relies on.

### Schema 2.2 (fine-tuning methods as options)

- **Changed** `use-case` option `record` also accepts `fine-tuning-method/<slug>` (a record of the
  models content repo), so a block can point at a method such as LoRA. This loosens a rule, so no
  record was converted; records authored against 2.1 stay valid.
- **Changed** the "Adaptation method" block of `use-case/fine-tune`: its LoRA, QLoRA and full
  fine-tuning options now name `fine-tuning-method/lora`, `fine-tuning-method/qlora` and
  `fine-tuning-method/full-fine-tuning` instead of an outside link; the LoRA text now says
  "selected linear layers", as the method record does.

### Content (observability category)

- **Added** the `observability` category ("Observability & Tracing", layer `operate`).
- **Changed** `langfuse`, `arize-phoenix` and `langsmith` move from `evaluation` to `observability`:
  their own documentation describes them first as observability and tracing platforms. The
  `evaluation` description no longer mentions tracing.

### Schema 2.1 (category layers)

- **Added (breaking)** `framework-category.layer`, required: `build`, `train`, `data`, `run`,
  `operate`, `domain` or `other`. The categories page groups categories by it. All 18 category
  records carry it and `schema_version: 2.1`.
- **Changed** every category is listed by the site; a category without `defacto` shows no default
  pick instead of being left out. `order` now sorts within a layer.

### Schema 2.0 (use cases as building blocks)

- **Changed (breaking)** `use-case` is now "I want to build X: what do I need?". A record carries
  `goal`, `stages[]` (2 to 4 ordered lanes: `id`, `name`, `note`) and `blocks[]` (`id`, `stage`,
  `name`, `purpose`, `options[]`, `how_to_choose[]`, optional `browse`). An option is an Atlas record
  (`record`: `framework/`, `model/` or `benchmark/`) or, until the Atlas has one, `name` + `url`; its
  `choice` is `default` (exactly one per block) or `alternative`. `browse.record` points at the
  `framework-category/`, `task-group/` or `task/` record that holds the full list. Body section:
  Overview only.
- **Removed** from `use-case`: `languages`, `levels`, `stack`, `day1_plan`, `starter_templates`,
  `pitfalls`, `when_to_level_up`, `community`, `dont_use`; the body sections "Why this stack" and
  "Notes". Records authored against 1.x fail the new schema and must be rewritten.
- **Changed** the loader checks a block's `stage` exists in `stages`, each block has exactly one
  default option, and block ids are unique; every `record` and `browse.record` is a reference the
  loader resolves like any other, so a dangling one names the file.
- `framework` and `framework-category` records are unchanged.

### Schema 1.2 (framework discovery)

- **Changed** `framework`: `kind` is optional. A record copied from GitHub facts alone cannot say
  whether the project is a framework, a library or a tool, so it carries no `kind`. This loosens a
  rule, so no record was converted; records authored against 1.1 stay valid.
- **Added** the `framework-category/other` record, for repositories whose GitHub topics match no
  other category yet.

### Schema 1.1 (migration of the framework snapshot)

- **Added** the `framework` type (`frameworks/`, `framework/<slug>`): `kind` (framework, library,
  tool), `category` (ID), the authored fields of the snapshot, `license_spdx` or `license_note`,
  `alternatives` and `ecosystem_connections` (ID lists), and the agent-owned `registry_signals`
  block (`github_stars`, `downloads_monthly`, `latest_version`, `latest_release_date`,
  `observed_at`, `source`). Optional body section: Overview.
- **Added** the shared optional `aliases` and `locked` fields to every type.
- **Changed** every frontmatter key of `framework-category` and `use-case` to `snake_case`
  (`shortDescription` → `short_description`, `frameworkId` → `framework_id`, `day1Plan` →
  `day1_plan`, and so on, at every depth); the 10 category and 8 use-case records were converted.
- **Changed** framework references (`stack[].framework_id`, `defacto`, `rising[]`,
  `alternatives[]`) from catalog slugs to `framework/<slug>` IDs that resolve inside this repo.
- **Changed** `framework-category`: `defacto` is optional, and every body section is now optional
  (registry `optional_sections`), so a category with no editorial judgement yet needs only
  `label` and `short_description`.
- **Added** 92 `framework` records (one per entry of the framework snapshot) and 7
  `framework-category` records for snapshot categories no existing record covered (automl,
  computer-vision, distributed-training, edge-mobile, evaluation, nlp, reinforcement-learning).

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

- **2.2** — `use-case` options may name a `fine-tuning-method/` record.
- **2.0** — `use-case` rebuilt as stages and building blocks with options (breaking).
- **1.0** — initial schema for the two frameworks content types (`use-case`, `framework-category`).
- **1.2** — `kind` of a `framework` record is optional; `framework-category/other`.
- **1.1** — `framework` type, `snake_case` keys, ID references for frameworks, shared `aliases`
  and `locked`, optional `defacto` and optional category body sections.
