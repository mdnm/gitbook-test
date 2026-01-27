---
description: >-
  A comprehensive TypeScript library for numerology, astrology, kaabalah, and
  tarot
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: false
  pagination:
    visible: true
  metadata:
    visible: true
metaLinks:
  alternates:
    - https://app.gitbook.com/s/2AwfWOGBWBxQmyvHedqW/
---

# Introduction

<p align="center"><strong>The de-facto library for esoteric calculations and tooling</strong></p>

```bash
npm install kaabalah
```

## Modules

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>🔢 Numerology</strong></td><td>Life path, cycles, challenges, and personal mythology calculations</td><td><a href="modules/numerology.md">numerology.md</a></td></tr><tr><td><strong>✡️ Gematria</strong></td><td>Hebrew letter values with reverse gematria lookup</td><td><a href="modules/gematria.md">gematria.md</a></td></tr><tr><td><strong>🌟 Astrology</strong></td><td>Birth charts and planetary positions via Swiss Ephemeris</td><td><a href="modules/astrology.md">astrology.md</a></td></tr><tr><td><strong>🃏 Tarot</strong></td><td>78 cards with meanings, spreads, and interpretations</td><td><a href="modules/tarot.md">tarot.md</a></td></tr><tr><td><strong>🐚 Ifa</strong></td><td>Odu calculations based on dates for Ifa divination</td><td><a href="modules/ifa.md">ifa.md</a></td></tr><tr><td><strong>🌳 Core</strong></td><td>Tree of Life system linking all esoteric correspondences</td><td><a href="modules/core.md">core.md</a></td></tr></tbody></table>

## Quick Start

{% columns %}
{% column %}
#### Get started in 5 minutes

Setting up your first calculation is easy. With clear APIs, copy-paste-ready examples, and quick setup, you'll be up and running in minutes.

<a href="docs/getting-started.md" class="button primary">Get Started</a> <a href="reference/api.md" class="button secondary">API Reference</a>
{% endcolumn %}

{% column %}
{% code title="example.ts" overflow="wrap" %}
```typescript
import { calculateGematria } from 'kaabalah/gematria';
import { calculateKaabalisticLifePath } from 'kaabalah/numerology';

// Calculate gematria for a name
const gematria = calculateGematria('DAVID');
console.log(gematria.synthesis.originalSum); // 25

// Calculate life path from birth date
const lifePath = calculateKaabalisticLifePath(new Date('1990-06-15'));
console.log(lifePath.lifePath.reducedValue);
```
{% endcode %}
{% endcolumn %}
{% endcolumns %}

## Features

{% columns %}
{% column %}
#### Tree-Shakable

Import only what you need. Each module is independently tree-shakable for optimal bundle size.

```typescript
// Only imports gematria module
import { calculateGematria } from 'kaabalah/gematria';
```
{% endcolumn %}

{% column %}
#### TypeScript First

Full TypeScript support with comprehensive type definitions for all functions and return values.

```typescript
import type { TarotCard, GematriaResult } from 'kaabalah';
```
{% endcolumn %}
{% endcolumns %}

## Learn More

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>📚 Documentation</strong></td><td>Complete guides and tutorials for all modules</td><td><a href="docs/getting-started.md">getting-started.md</a></td></tr><tr><td><strong>🔧 WebAssembly</strong></td><td>Swiss Ephemeris WASM integration guide</td><td><a href="guides/webassembly.md">webassembly.md</a></td></tr><tr><td><strong>📖 API Reference</strong></td><td>Detailed API documentation for all exports</td><td><a href="reference/api.md">api.md</a></td></tr></tbody></table>

### New to esoterism?

Start here:

* [Concepts and terminology](getting-started/concepts-and-terminology.md)
* [Practical recipes](getting-started/practical-recipes.md)

## Community

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>GitHub</strong></td><td>100% open source. Star the repo, report issues, or submit PRs.</td><td><a href="https://github.com/mdnm/kaabalah" class="button secondary">View on GitHub</a></td></tr></tbody></table>

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
