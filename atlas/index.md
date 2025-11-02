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
- **Local Chapter:** [Open the detail page]({{ project.local_url | relative_url }})
- **Repository:** [View on GitHub]({{ project.repository }})
{% if project.tags %}- **Tags:** {{ project.tags | join: ', ' }}{% endif %}
{% endfor %}

## Submodule Snapshot

The site tracks each registered submodule so that both the Jekyll build and the Apache export can reference their source.

| Submodule | Status | Path | Remote |
| --- | --- | --- | --- |
{% for module in site.data.submodules %}| {{ module.name }} | {{ module.status | capitalize }} | `{{ module.path }}` | [{{ module.url }}]({{ module.url }}) |
{% endfor %}

## Public Repository Network

Every beacon listed here reflects a public CraftingBuilds repository. Where you see gaps, trust that there may be more logs in the fire waiting to emerge or projects still coalescing before they are minted as repositories.

| Repository | Focus | Portal |
| --- | --- | --- |
{% for repo in site.data.repositories %}| {{ repo.name }} | {{ repo.focus }} | [Visit on GitHub]({{ repo.url }}) |
{% endfor %}

## External Knowledge Streams

- [Astrology Arith(m)etic](https://github.com/CraftingBuilds/Astrology-Arithm-etic) — foundational cosmic logic repository.
- [RitualGrimoire-Stellar-Shield](https://github.com/CraftingBuilds/RitualGrimoire-Stellar-Shield) — protective construct schematics ready to initialize as a submodule.
- [CraftingBuilds GitHub Organization](https://github.com/CraftingBuilds) — jump into the larger ecosystem of metaphysical tooling.
