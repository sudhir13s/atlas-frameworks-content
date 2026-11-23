---
id: framework-category/<slug>
type: framework-category
slug: <slug>
schema_version: 3.0              # the schema's current version; the schema refuses any other
title: "<Human Readable Title>"
label: "<Category name for the section heading>"
layer: <build|train|data|run|operate|domain|other>   # the layer of the AI stack; the categories page groups by it
order: <int>                       # display order within the layer
short_description: "<one line: what this slice of the ecosystem covers>"
why_it_matters: "<one line: why a builder cares>"
defacto:                           # omit until someone has judged the default choice
  framework_id: framework/<slug>   # the current default choice; must be a framework record
  reason: "<why it is the default>"
rising:
  - framework_id: framework/<slug>
    reason: "<why it is gaining ground>"
alternatives:
  - framework_id: framework/<slug>
    reason: "<where it fits / who should pick it>"
key_concepts:
  - "<concept a reader must know in this category>"
canonical_reading:
  - title: "<canonical doc/paper title>"
    url: "<url>"
aliases: ["<other written name>"]
tags: [<tag>]
updated: <YYYY-MM-DD>
sources:
  - { url: "<url>", title: "<title>", trust: 0.9 }
---

## Overview
<2-3 sentences: what this category is and the job it does.>

## Landscape
<The defacto choice, who is rising, and the real trade-offs between options.>

## Notes
<Where the category is heading; caveats a reader should keep in mind.>
