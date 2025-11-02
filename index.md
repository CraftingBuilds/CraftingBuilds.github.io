---
layout: default
title: Crafting Builds Observatory
description: "A cosmic interface cataloguing every file, folder, and submodule orbiting the CraftingBuilds GitHub Pages repository."
---
<section class="hero">
  <span class="hero__eyebrow">Cartography for the Craft</span>
  <h1 class="hero__title">Map the Metaphysical Builds</h1>
  <p class="hero__description">
    Explore every document, ritual framework, and experimental subsystem maintained inside this repository.
    From astrology codices to Lightcraft engines, the observatory keeps each artifact illuminated.
  </p>
  <div class="hero__actions">
    <a class="button button--primary" href="{{ '/atlas/' | relative_url }}">Open the Atlas</a>
    <a class="button button--secondary" href="{{ '/atlas/submodules/' | relative_url }}">Review Submodules</a>
  </div>
  <p class="hero__note">There may be more logs in the fire than the constellations displayed here—new repositories ignite once they are forged for public view.</p>
</section>

<section aria-labelledby="projects-title">
  <h2 id="projects-title" class="section-title">Repository Chapters</h2>
  <div class="data-grid">
    {% for project in site.data.projects %}
      {% include project-card.html project=project %}
    {% endfor %}
  </div>
  <p class="section-footnote">All active CraftingBuilds repositories are woven into this grid. Expect additional embers to surface as private experiments mature.</p>
</section>

<section class="section-panel" aria-labelledby="highlights-title">
  <h2 id="highlights-title">Highlights from the Temple</h2>
  <div class="section-panel__grid">
    <article class="highlight-card">
      <h3>Astrology Arith(m)etic</h3>
      <p>A structured codex of planetary mechanics and astrological pedagogy. Ideal for training AI or meditative study.</p>
      <a href="https://github.com/CraftingBuilds/Astrology-Arithm-etic" target="_blank" rel="noopener">Source Repository</a>
    </article>
    <article class="highlight-card">
      <h3>Grimoire Collection</h3>
      <p>Ritual schematics and spiritual tooling catalogued for quick invocation. Pair with the Lightcraft engine for praxis.</p>
      <a href="https://github.com/CraftingBuilds/RitualGrimoire-Stellar-Shield" target="_blank" rel="noopener">Stellar Shield Blueprint</a>
    </article>
  </div>
</section>
