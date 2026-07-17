# CONVENTIONS.md — authoring rules

The rules every file follows. Humans and agents follow the identical process. The authoritative
cross-repo spec is the
[content-repo standard](https://github.com/sudhir13s/TheAIAtlas/blob/main/docs/standards/content-repo-standard.md);
this file is the `frameworks`-domain instance.

## Slugs and file names

- Slugs are **lowercase, hyphen-separated, ASCII** — no spaces, no underscores. Example:
  `build-a-rag-app`, `fine-tuning`, `vector-dbs`.
- The file name is `<slug>.md` and **must equal** the `slug` frontmatter field.
- A file lives in the folder mapped to its `type` in `schema/registry.json`
  (`use-case` → `use-cases/`, `framework-category` → `categories/`).

## IDs and references

- `id` = `<type>/<slug>` (e.g. `use-case/build-a-rag-app`). Globally unique, **immutable**.
- **Intra-repo links use IDs**: `related`, `relatedUseCases` point at `<type>/<slug>` and must
  resolve to an existing file. Dangling references fail validation. The compiler strips the
  `use-case/` prefix from `relatedUseCases` so the web receives bare slugs.
- **Framework references use catalog slugs**: `stack[].frameworkId`, `defacto.frameworkId`,
  `rising[].frameworkId`, `alternatives[].frameworkId` are the `id` of a framework in the consuming
  project's frameworks catalog (e.g. `pytorch`, `langchain`, `vllm`, `chromadb`). They are external
  references — the UI resolves them to names, star counts, and links at render time. Prefer slugs
  that exist in the catalog; an unknown slug still renders (as a fallback chip) but should be avoided.

## Frontmatter

Base fields on **every** file: `id`, `type`, `slug`, `schema_version`, `title`, `tags`, `updated`,
`sources`. Optional base field: `related`. Each type adds its own fields — see
`schema/<type>.schema.json`. Put **structured/reference data in frontmatter** (arrays, stacks,
plans, reading lists) so it stays machine-parseable; the body carries only prose.

- `tags`: lowercase, hyphen-separated.
- `updated`: ISO date (`YYYY-MM-DD`).
- `sources[]`: `{ url, title, trust }` — `trust` in `[0,1]`. Open-source-first; cite, do not copy.
- `schema_version`: the `major.minor` the file was authored against (currently `1.0`).

## Body sections

- Prose lives under `##` headings. The **required sections** and their order per type are declared in
  `schema/registry.json → types.<type>.sections`.
- The body is for human readers. The web pages (`/frameworks/getting-started`,
  `/frameworks/categories`) render from frontmatter, so keep every UI-visible fact in frontmatter.

## Per-type specifics

- **use-case** — a task-oriented starting path. Carries `goal`, `languages`, `levels`, and the
  structured `stack[]`, `day1Plan[]`, `starterTemplates[]`, `learnNext[]`, `pitfalls[]`,
  `whenToLevelUp`, `community[]`, `dontUse[]`, and `relatedUseCases[]` (IDs). `label` is the short
  card/tab name; `order` controls display order. Body sections: Overview → Why this stack → Notes.
- **framework-category** — a per-category landscape. Carries `shortDescription`, `whyItMatters`,
  a single `defacto` framework, `rising[]`, `alternatives[]`, `keyConcepts[]`, `canonicalReading[]`,
  and `didYouKnow[]`. `label` is the section heading; `order` controls display order. Body sections:
  Overview → Landscape → Notes.

## Sourcing

Open-source-first, zero plagiarism. Prefer official framework documentation, open papers, and public
repositories. Reference paywalled material only as a cited pointer, never as copied text. Record
everything in `sources[]`.
