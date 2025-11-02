---
layout: page
title: Repository Atlas
description: "A guided walkthrough of every folder, document, and ritual dataset contained in CraftingBuilds.github.io."
permalink: /atlas/
kicker: Navigational Chart
---
## Directory Overview

| Location | Purpose | Key Artifacts |
| --- | --- | --- |
| `/` | Core GitHub Pages source housing layouts, includes, and global assets. | `_layouts/`, `_includes/`, `index.md` |
| `/LightCraft` | Internal notespace that grounds the LightCraft narrative inside this repository. | `README.md` |
| `/Lightcraft` | Git submodule mount that exposes the external Lightcraft engine. | `README.md` |
| `/assets` | Shared visual system for both the Jekyll site and Apache export. | `css/style.css` |

## Project Cards

{% for project in site.data.projects %}
### {{ project.name }}
- **Category:** {{ project.category }}
- **Summary:** {{ project.summary }}
{% if project.local_url %}- **Local Chapter:** [Open the detail page]({{ project.local_url | relative_url }}){% endif %}
{% if project.repository %}- **Repository:** [View on GitHub]({{ project.repository }}){% endif %}
{% if project.tags %}- **Tags:** {{ project.tags | join: ', ' }}{% endif %}
{% endfor %}

## Submodule Snapshot

The site tracks each registered submodule so that both the Jekyll build and the Apache export can reference their source.

| Submodule | Status | Path | Remote |
| --- | --- | --- | --- |
{% for module in site.data.submodules %}| {{ module.name }} | {{ module.status | capitalize }} | `{{ module.path }}` | [{{ module.url }}]({{ module.url }}) |
{% endfor %}

## Public Repository Directory

Every active CraftingBuilds repository is cross-linked for quick navigation. Some experiments stay in ember-form until they are ready for public release, so expect the constellation to continue expanding.

| Repository | Focus | Link |
| --- | --- | --- |
{% assign public_repos = site.data.projects | where_exp: 'item', "item.repository" %}{% for project in public_repos %}| {{ project.name }} | {{ project.summary }} | [Visit]({{ project.repository }}) |
{% endfor %}

> There may be more logs in the fire than what you see here—some works are incubating privately or awaiting their own repositories.

## External Knowledge Streams

- [Astrology Arith(m)etic](https://github.com/CraftingBuilds/Astrology-Arithm-etic) — foundational cosmic logic repository.
- [RitualGrimoire-Stellar-Shield](https://github.com/CraftingBuilds/RitualGrimoire-Stellar-Shield) — protective construct schematics ready to initialize as a submodule.
- [CraftingBuilds GitHub Organization](https://github.com/CraftingBuilds) — jump into the larger ecosystem of metaphysical tooling.
