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
yarn add kaabalah
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

### Practical next steps

* If the terminology feels foreign, start with [Concepts and terminology](../getting-started/concepts-and-terminology.md).
* If you want copy-paste workflows, jump to [Practical recipes](../getting-started/practical-recipes.md).
* If you’re doing astrology in the browser, read [WebAssembly Integration](../guides/webassembly.md).

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
