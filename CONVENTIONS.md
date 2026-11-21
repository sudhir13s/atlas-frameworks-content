# CONVENTIONS.md — authoring rules

The rules every file follows. Humans and agents follow the identical process. The authoritative
cross-repo spec is the
[content-repo standard](https://github.com/sudhir13s/TheAIAtlas/blob/main/docs/content-repo-standard.md);
this file is the `frameworks`-domain instance.

## Slugs and file names

- Slugs are **lowercase, hyphen-separated, ASCII** — no spaces, no underscores. Example:
  `build-a-rag-app`, `fine-tuning`, `vector-dbs`. A `framework` slug is the project's catalog id
  (`pytorch`, `hugging-face-transformers`).
- The file name is `<slug>.md` and **must equal** the `slug` frontmatter field.
- A file lives in the folder mapped to its `type` in `schema/registry.json`
  (`use-case` → `use-cases/`, `framework-category` → `categories/`, `framework` → `frameworks/`).
- **Frontmatter keys are `snake_case`** at every depth (`short_description`, `framework_id`).

## IDs and references

- `id` = `<type>/<slug>` (e.g. `use-case/build-a-rag-app`). Globally unique, **immutable**.
- **Every link is an ID** (`<type>/<slug>`) that must resolve to an existing record. Dangling
  references fail validation. This covers `related`, `related_use_cases`, a framework's `category`,
  `alternatives` and `ecosystem_connections`, and every framework reference in a category or use
  case (`stack[].framework_id`, `defacto.framework_id`, `rising[].framework_id`,
  `alternatives[].framework_id`), which is `framework/<slug>`. The site reader strips the
  `use-case/` and `framework/` prefixes so the pages receive bare slugs.

## Frontmatter

Base fields on **every** file: `id`, `type`, `slug`, `schema_version`, `title`, `tags`, `updated`,
`sources`. Optional base fields: `related`, `aliases` (other written names, so later sources can
match the record), `locked` (field paths no job may change; a human edits them). Each type adds its
own fields — see `schema/<type>.schema.json`. Put **structured/reference data in frontmatter**
(arrays, stacks, plans, reading lists) so it stays machine-parseable; the body carries only prose.

- `tags`: lowercase, hyphen-separated.
- `updated`: ISO date (`YYYY-MM-DD`).
- `sources[]`: `{ url, title, trust }` — `trust` in `[0,1]`. Open-source-first; cite, do not copy.
- `schema_version`: the `major.minor` the file was authored against (currently `1.2`; a file authored against `1.1` stays valid).

## Body sections

- Prose lives under `##` headings. The **required sections** and their order per type are declared in
  `schema/registry.json → types.<type>.sections`; `optional_sections` may be absent and, when present,
  follow the required ones in the declared order.
- The body is for human readers. The web pages (`/frameworks/getting-started`,
  `/frameworks/categories`) render from frontmatter, so keep every UI-visible fact in frontmatter.

## Per-type specifics

- **use-case** — a task-oriented starting path. Carries `goal`, `languages`, `levels`, and the
  structured `stack[]`, `day1_plan[]`, `starter_templates[]`, `learn_next[]`, `pitfalls[]`,
  `when_to_level_up`, `community[]`, `dont_use[]`, and `related_use_cases[]` (IDs). `label` is the
  short card/tab name; `order` controls display order. Body sections: Overview → Why this stack → Notes.
- **framework-category** — a per-category landscape. Carries `short_description`, `why_it_matters`,
  an optional single `defacto` framework (absent until someone has judged it), `rising[]`,
  `alternatives[]`, `key_concepts[]`, `canonical_reading[]`, and `did_you_know[]`. `label` is the
  section heading; `order` controls display order and a category without `order` or `defacto` is
  not listed by the site. All body sections (Overview → Landscape → Notes) are optional.
- **framework** — one framework, library or tool. `kind` is `framework` (code you build inside),
  `library` (code you call) or `tool` (a program or service you run); it is absent on a record
  copied from GitHub facts alone, because no fact says which it is. `category` is a
  `framework-category/<slug>` ID. Authored fields: `tagline`, `description`, `best_for`,
  `not_ideal_for`, `key_features`, `use_cases`, `pros`, `cons`, `language`, `languages_supported`,
  `subcategory`, the three URLs, `first_release`, `maintained_by`, `gpu_support`, `learning_curve`,
  `community_size`, `maturity`, `signal_strength`, `backing`. The licence is `license_spdx` (one
  SPDX identifier) or, when compound or proprietary, `license_note` (the original text).
  `alternatives` and `ecosystem_connections` are lists of `framework/<slug>` IDs. The agent-owned
  block `registry_signals` holds the numbers that change (`github_stars`, `downloads_monthly`,
  `latest_version`, `latest_release_date`) with `observed_at` and `source`; an unknown value is
  absent, never `0`. Optional body section: Overview (the `description`).

## Sourcing

Open-source-first, zero plagiarism. Prefer official framework documentation, open papers, and public
repositories. Reference paywalled material only as a cited pointer, never as copied text. Record
everything in `sources[]`.
