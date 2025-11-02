---
layout: page
title: Submodule Registry
description: "Status dashboard for every submodule declared in CraftingBuilds.github.io."
permalink: /atlas/submodules/
kicker: Linked Repositories
---
## Active Links

| Name | Path | Status | Description |
| --- | --- | --- | --- |
{% for module in site.data.submodules %}| [{{ module.name }}]({{ module.url }}) | `{{ module.path }}` | {{ module.status | capitalize }} | {{ module.description }} |
{% endfor %}

## Usage Notes

- Submodules are tracked so that both the GitHub Pages build and the Apache export can surface their documentation.
- The Lightcraft module is initialized within this repository to expose its README and assets.
- RitualGrimoire-Stellar-Shield is registered and ready for initialization when shielding schematics need to be pulled locally.

## Command Reference

```bash
# initialize every submodule
git submodule update --init --recursive

# update a single module
cd Lightcraft && git pull && cd ..
```
