# AGENTS.md — machine navigation guide

This repository is designed to be read and extended by AI agents with **no external context**.
Follow these steps.

## 1. Orient

1. Read [`meta.json`](meta.json) — the repo descriptor. It gives `domain`, `schema_version`, the
   list of content `types`, and pointers to the human/agent/convention docs and the registry.
2. Read [`schema/registry.json`](schema/registry.json) — the type map. For each `type` it gives:
   - `folder` — where files of that type live
   - `schema` — the JSON Schema that validates that type's frontmatter
   - `id_prefix` — the stable-ID namespace (`<type>/`)
   - `sections` — the required Markdown body sections, in order

After these two reads you know every type, where it lives, how to validate it, and how it must be
structured.

## 2. Discover content

Two equivalent ways to enumerate the library:

- **Glob**: read every `**/*.md`, parse its YAML frontmatter, key on `id` / `type`.
- **By type**: for a known `type`, list its `folder` from the registry and read each `<slug>.md`.

Every file self-identifies via frontmatter (`id`, `type`, `slug`, `title`, `tags`, …), so no
separate index is needed and none can fall out of sync.

## 3. Read a file

- **Frontmatter** carries the structured data the UI consumes (all fields the schema defines). Parse
  it as YAML.
- **Body** carries prose under `##` headings matching the type's required `sections`. It is for human
  readers; the web pages render from frontmatter, not the body.
- **Links** (`related`, `related_use_cases`, a framework's `category`, `alternatives` and
  `ecosystem_connections`) are **IDs** of the form `<type>/<slug>`.
- **Framework references** (`defacto.framework_id`, `rising[]`, `alternatives[]`) are IDs of
  `framework` records (`framework/<slug>`), files in this repo. A use case's
  `blocks[].options[].record` and `blocks[].browse.record` are IDs of any record in the corpus.
- Frontmatter keys are `snake_case`. A framework's `registry_signals` block is owned by the jobs.

## 4. Validate

- Load the type's schema from `schema/<type>.schema.json` (shared `$defs` in `schema/_shared.schema.json`).
- Validate the file's frontmatter against it (any JSON-Schema draft-2020-12 validator, e.g. `ajv`).
- Check that every intra-repo referenced ID resolves to an existing file (no dangling references).

## 5. Add or edit content

1. Pick the `type`; copy `templates/<type>.template.md`.
2. Set `id` = `<type>/<slug>`, `slug` = filename, `schema_version` from `meta.json`, and `updated`
   to today's date.
3. Fill the type-specific frontmatter fields (schema `required` first) and every required body
   section in order.
4. Use `framework/<slug>` IDs for framework references and `<type>/<slug>` IDs for every other link.
5. Validate (step 4 above). Do not introduce code files — this repo is content-only.
6. Follow open-source-first sourcing: cite official framework docs in `sources[]`; never copy
   paywalled text.

## 6. Invariants (do not violate)

- `id` is immutable; renaming a slug is a breaking change (note it in `CHANGELOG.md`).
- No `.js` / `.ts` / `.mjs` / `package.json` / build scripts anywhere.
- Every link is an ID that resolves to a record in this repo.
- Frontmatter must pass the type schema before a change is complete.
