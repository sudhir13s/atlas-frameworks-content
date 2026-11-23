---
id: use-case/<slug>
type: use-case
slug: <slug>
schema_version: 3.0              # the schema's current version; the schema refuses any other
title: "<Human Readable Title>"
label: "<Short label for the goal list>"
order: <int>                       # display order on the getting-started page
goal: "<One sentence: what the finished system does.>"
stages:                            # 2 to 4 lanes of the system map, in order
  - id: <stage-slug>
    name: "<Stage name>"
    note: "<One sentence: when this part of the system runs.>"
blocks:                            # ordered by where they sit in the system
  - id: <block-slug>               # unique in this record
    stage: <stage-slug>            # one of stages[].id
    name: "<Block name>"
    purpose: "<One sentence: what this block does in this system.>"
    options:                       # 1 to 5; the first is the default, exactly one default
      - record: framework/<slug>   # an Atlas record: framework/, model/ or benchmark/
        choice: default            # default | alternative
        when: "<One sentence: why it is the default.>"
      - name: "<Tool name>"        # only when the Atlas has no record yet: name + url, no record
        url: "<maker url>"
        choice: alternative
        when: "<One sentence: when to pick this instead.>"
    how_to_choose:                 # 1 to 4 short bullets
      - "<How the choice follows from the reader's situation.>"
    browse:                        # optional: where the full list lives in the Atlas
      label: "<All vector databases>"
      record: framework-category/<slug>   # framework-category/, task-group/ or task/
learn_next:
  - title: "<resource title>"
    url: "<url>"
    kind: doc                      # video | course | paper | doc | docs | blog
related_use_cases: [use-case/<other-slug>]
tags: [<tag>]
updated: <YYYY-MM-DD>
sources:
  - { url: "<url>", title: "<title>", trust: 0.9 }
---

## Overview
<2-3 sentences: what you are building and the shape of the system.>
