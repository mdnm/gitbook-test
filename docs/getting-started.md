# Getting Started

Kaabalah is a comprehensive TypeScript library for numerology, astrology, kaabalah, and tarot calculations.

## Installation

{% tabs %}
{% tab title="npm" %}
```bash
npm install kaabalah
```
{% endtab %}

{% tab title="pnpm" %}
```bash
pnpm install kaabalah
```
{% endtab %}

{% tab title="yarn" %}
```bash
yarn kaabalah
```
{% endtab %}
{% endtabs %}

## Quick Example

```typescript
import { createTree } from 'kaabalah/core';

const tree = createTree({
  system: 'kaabalah',
  parts: ['westernAstrology', 'tarot'],
});
```

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
