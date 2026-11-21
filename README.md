# atlas-frameworks-content

Portable, reusable reference knowledge about the **AI framework ecosystem** — authored as Markdown
with structured YAML frontmatter, validated by JSON Schema, and readable by both humans and AI
agents. This repo is **content only**: no code, no build step, no framework lock-in. Any project can
vendor it (as a git submodule or a plain checkout) and render it however it likes.

It is the `frameworks` domain of a multi-repo reference library
(`atlas-models-content`, `atlas-evaluation-content`, `atlas-frameworks-content`,
`atlas-hardware-content`, `atlas-news-content`, `atlas-practices-content`, `atlas-research-content`), all following the same
[content-repo standard](CONTENT-STANDARD.md).

## What's inside

| Type | Folder | What it captures |
|------|--------|------------------|
| `framework` | `frameworks/` | One framework, library or tool: what it is, who it suits, licence, backing, links to alternatives, and a block of numbers that change over time |
| `use-case` | `use-cases/` | A goal ("Build a RAG app") and the building blocks the system needs, ordered by where they sit in it, each with a default choice, alternatives, how to choose and links to the records in the Atlas |
| `framework-category` | `categories/` | A per-category landscape: the defacto choice, who is rising, alternatives, key concepts, and canonical reading |

Framework references (`defacto.framework_id`, `rising[]`, `alternatives[]`) are IDs of `framework`
records (`framework/pytorch`, `framework/langchain`) and are checked to resolve. So is every
`blocks[].options[].record` of a use case, which may also name a model or benchmark record.

## Quick start

```bash
# Vendor it
git clone https://github.com/sudhir13s/atlas-frameworks-content.git
# or as a submodule of your project
git submodule add https://github.com/sudhir13s/atlas-frameworks-content.git content/frameworks-src
```

Every content file is a Markdown file with YAML frontmatter (the structured fields the UI reads) and
a Markdown body (prose for a human reader). Enumerate the library by globbing `**/*.md` and reading
each file's frontmatter, or start from [`meta.json`](meta.json) and
[`schema/registry.json`](schema/registry.json).

## Structure

```
meta.json                 # repo descriptor (machine entrypoint 1)
schema/registry.json      # type → folder/schema/sections map (machine entrypoint 2)
schema/*.schema.json      # JSON Schema per content type
templates/*.template.md   # copy these to author new content
frameworks/ use-cases/ categories/   # one folder per content type; files are <slug>.md
assets/                   # SVG diagrams
```

## Contributing

See [CONVENTIONS.md](CONVENTIONS.md) for the authoring rules, and [AGENTS.md](AGENTS.md) for the
machine-navigation guide. In short: copy a template, fill the frontmatter and required sections, use
`framework/<slug>` IDs for framework references and IDs for every other link, and open a PR. Content must be
open-source-sourced and cited (official framework docs first) — never copied from paywalled material.

## License

Content is licensed **CC-BY-4.0** (see [LICENSE](LICENSE)) — reuse freely with attribution.
