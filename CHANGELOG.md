# Changelog

All notable changes to `ai-frameworks-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

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

- **1.0** — initial schema for the two frameworks content types (`use-case`, `framework-category`).
- **1.2** — `kind` of a `framework` record is optional; `framework-category/other`.
- **1.1** — `framework` type, `snake_case` keys, ID references for frameworks, shared `aliases`
  and `locked`, optional `defacto` and optional category body sections.
