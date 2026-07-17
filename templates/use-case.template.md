---
id: use-case/<slug>
type: use-case
slug: <slug>
schema_version: 1.0
title: "<Human Readable Title>"
label: "<Short label for tabs/cards>"
order: <int>                       # display order on the getting-started page
goal: "<One sentence: the outcome the reader wants.>"
languages: [python]                # python | typescript | rust | swift | kotlin | go
levels: [beginner, intermediate]   # beginner | intermediate | advanced
stack:
  - frameworkId: <catalog-slug>    # must be a slug in the frameworks catalog (e.g. langchain, vllm)
    role: "<what this tool does in the stack>"
    why: "<why this pick, one line>"
    install: "<install command>"
    quickstartUrl: "<official quickstart url>"
    docsUrl: "<official docs url>"
day1Plan:
  - step: 1
    task: "<what to do>"
    estimate: "<time>"
    details: "<one line of detail>"
starterTemplates:
  - name: "<template name>"
    repo: "<github url>"
    why: "<why this template>"
learnNext:
  - title: "<resource title>"
    url: "<url>"
    kind: doc                      # video | course | paper | doc | docs | blog
pitfalls:
  - "<a common mistake and how to avoid it>"
whenToLevelUp: "<the signal that you have outgrown this starter stack>"
community:
  - name: "<community name>"
    url: "<url>"
dontUse:
  - what: "<framework or approach to avoid here>"
    why: "<why it is the wrong tool for this use case>"
relatedUseCases: [use-case/<other-slug>]
tags: [<tag>]
updated: <YYYY-MM-DD>
sources:
  - { url: "<url>", title: "<title>", trust: 0.9 }
---

## Overview
<2-3 sentences: what you are building and the shape of the solution.>

## Why this stack
<Why these tools fit together for this goal; the trade-offs behind each pick.>

## Notes
<Gotchas, scaling notes, and when to revisit the choices.>
