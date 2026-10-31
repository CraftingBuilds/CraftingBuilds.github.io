---
layout: page
title: Crafting Builds Core
description: "Documentation for the GitHub Pages scaffolding that powers CraftingBuilds.github.io."
permalink: /atlas/core/
kicker: Root Repository
---
## Mission Statement

The root repository overview is documented in the project README:
[README.md](https://github.com/CraftingBuilds/CraftingBuilds.github.io/blob/main/README.md)

This atlas page summarizes the repository structure and documentation scaffolding used to publish the site.

## Layout & Includes

- `_layouts/default.html` — the celestial frame used by every Jekyll page.
- `_layouts/page.html` — nested layout that provides chapter headers for atlas entries.
- `_includes/nav.html` — navigation bar that sources its links from `_config.yml`.
- `_includes/project-card.html` — reusable component used to render the atlas cards on the homepage.

## Styling Assets

- `assets/css/style.css` defines the shared theme for both the Jekyll and Apache exports.
- Google Fonts `Unica One` and `Space Grotesk` provide headings and body typography.

## Collections

The configuration exposes two primary collections ready for additional content:

- `astro-arith` — publishable lessons and reference pages for Astrology Arith(m)etic.
- `grimoire` — ritual schematics and spells prepared for future publishing.

Use the `defaults` block in `_config.yml` to automatically attach the `page` layout to new markdown files placed inside these collections.
