---
id: framework/<slug>
type: framework
slug: <slug>
schema_version: 1.2
title: "<Project name>"
kind: framework                    # framework | library | tool; omit until someone has judged it
category: framework-category/<slug>
subcategory: <finer-grouping>
tagline: "<one line>"
description: "<what it is>"        # omit description and the body for a record with no prose yet
best_for: "<who should pick it>"
not_ideal_for: "<who should not>"
key_features: ["<feature>"]
use_cases: ["<use case>"]
pros: ["<pro>"]
cons: ["<con>"]
language: <main implementation language>
languages_supported: [<language>]
maintained_by: "<who maintains it>"
license_spdx: Apache-2.0           # or `license_note: "<licence text as the source gives it>"` when compound or proprietary
github_url: "<url>"
docs_url: "<url>"
website_url: "<url>"
maturity: production               # experimental | stable | production
backing:
  type: corporate                  # corporate | foundation | community
  orgs: ["<organization>"]
alternatives: [framework/<slug>]
ecosystem_connections: [framework/<slug>]
registry_signals:                  # owned by the jobs; numbers that change
  github_stars: <int>
  downloads_monthly: <int>
  latest_version: "<version>"
  latest_release_date: "<YYYY-MM-DD>"
  observed_at: "<YYYY-MM-DD>"
  source: "<url>"
aliases: ["<owner/repo>"]
locked: [description, kind]        # field paths no job may change
tags: [<tag>]
updated: <YYYY-MM-DD>
sources:
  - { url: "<url>", title: "<title>" }
---

## Overview
<What the project is and what it is for; the description, verbatim.>
