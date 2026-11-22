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
  case (`defacto.framework_id`, `rising[].framework_id`, `alternatives[].framework_id`), which is
  `framework/<slug>`, and every `blocks[].options[].record` and `blocks[].browse.record` of a use
  case (a framework, model, benchmark, category or task record, in any repo). The site reader strips the
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
- `schema_version`: the `major.minor` the file was authored against (currently `2.4`; `framework` records authored against `1.1` or `1.2` stay valid, a `use-case` must be `2.0` or newer, a `framework-category` must be `2.1`).

## Body sections

- Prose lives under `##` headings. The **required sections** and their order per type are declared in
  `schema/registry.json → types.<type>.sections`; `optional_sections` may be absent and, when present,
  follow the required ones in the declared order.
- The body is for human readers. The web pages (`/frameworks/getting-started`,
  `/frameworks/categories`) render from frontmatter, so keep every UI-visible fact in frontmatter.

## Per-type specifics

- **use-case** — "I want to build X: what do I need?". Carries `goal`, `stages[]` (2 to 4 ordered
  lanes of the system: `id`, `name`, `note`), `blocks[]` (ordered by where they sit in the system:
  `id`, `stage`, `name`, `purpose`, `options[]`, `how_to_choose[]`, optional `browse`), `learn_next[]`
  and `related_use_cases[]` (IDs). An option is an Atlas record (`record`) or, until the Atlas has
  one, `name` + `url`; `choice` is `default` (exactly one per block, listed first) or `alternative`.
  No install commands or day plans. `label` is the short goal name; `order` controls display order.
  Body section: Overview.
- **framework-category** — a per-category landscape. Carries `short_description`, `why_it_matters`,
  an optional single `defacto` framework (absent until someone has judged it), `rising[]`,
  `alternatives[]`, `key_concepts[]`, `canonical_reading[]`, and `did_you_know[]`. `label` is the
  category name; `layer` (required: `build`, `train`, `data`, `run`, `operate`, `domain` or `other`)
  files it under a layer of the AI stack and `order` sorts it within the layer. Every category is
  listed by the site; one without `defacto` simply shows no default pick. All body sections
  (Overview → Landscape → Notes) are optional.
- **framework** — one framework, library or tool. `kind` is `framework` (code you build inside),
  `library` (code you call) or `tool` (a program or service you run); it is absent on a record
  copied from GitHub facts alone, because no fact says which it is. `category` is a
  `framework-category/<slug>` ID. Authored fields: `tagline`, `description`, `best_for`,
  `not_ideal_for`, `key_features`, `use_cases`, `pros`, `cons`, `language`, `languages_supported`,
  `subcategory`, the three URLs, `maintained_by`, `maturity`, `backing`. The licence is `license_spdx` (one
  SPDX identifier) or, when compound or proprietary, `license_note` (the original text). GPU
  support is not a field here: it lives, with its source pages, in the `framework-support` record
  of the hardware content repo whose `framework` names this record.
  `alternatives` and `ecosystem_connections` are lists of `framework/<slug>` IDs. The agent-owned
  block `registry_signals` holds the numbers that change (`github_stars`, `downloads_monthly`,
  `latest_version`, `latest_release_date`) with `observed_at` and `source`; an unknown value is
  absent, never `0`. Optional body section: Overview (the `description`).

## Sourcing

Open-source-first, zero plagiarism. Prefer official framework documentation, open papers, and public
repositories. Reference paywalled material only as a cited pointer, never as copied text. Record
everything in `sources[]`.
