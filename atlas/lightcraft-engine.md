---
layout: page
title: Lightcraft Submodule
description: "Documentation and instructions for the Lightcraft git submodule bundled with this repository."
permalink: /atlas/lightcraft-engine/
kicker: Submodule
---
## Embedded README

{% capture submodule_readme %}{% include_relative ../Lightcraft/README.md %}{% endcapture %}
{{ submodule_readme | markdownify }}

## Working with the Submodule

1. **Initialize** — `git submodule update --init --recursive`
2. **Pull updates** — inside `Lightcraft/`, run `git checkout main && git pull`
3. **Commit linkage** — commit submodule pointer changes from the root repository so deployments track the desired revision.

## Integration Points

- The Jekyll atlas references this README directly for live documentation.
- The Apache export mirrors this summary so offline deployments still expose Lightcraft context.
- `_data/submodules.yml` flags Lightcraft as `active`, ensuring site navigation highlights it as ready-to-use infrastructure.
