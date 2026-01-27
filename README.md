---
description: Welcome to your team’s developer platform
layout:
  width: wide
  title:
    visible: false
  description:
    visible: false
  tableOfContents:
    visible: false
  outline:
    visible: false
  pagination:
    visible: false
  metadata:
    visible: true
metaLinks:
  alternates:
    - https://app.gitbook.com/s/2AwfWOGBWBxQmyvHedqW/
---

# Developer Platform

<h2 align="center">Kaabalah</h2>

<p align="center">The de-facto library for any esoteric calculations and tooling</p>

```
npm install kaabalah
```

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><h4><i class="fa-leaf">:leaf:</i></h4></td><td><strong>AGPL-3.0 license</strong></td><td>Get started with the developer platform in 5 minutes.</td><td><a href="https://template.gitbook.com/space-product-docs">https://template.gitbook.com/space-product-docs</a></td><td><a href=".gitbook/assets/no-code.jpg">no-code.jpg</a></td></tr><tr><td><h4><i class="fa-server">:server:</i></h4></td><td><strong>Tree-Shakable</strong></td><td>Learn more about hosting the developer platform.</td><td><a href="https://template.gitbook.com/space-product-docs">https://template.gitbook.com/space-product-docs</a></td><td><a href=".gitbook/assets/hosted.jpg">hosted.jpg</a></td></tr><tr><td><h4><i class="fa-terminal">:terminal:</i></h4></td><td><strong>API reference</strong></td><td>Browse, test, and implement APIs.</td><td><a href="https://template.gitbook.com/space-api-reference">https://template.gitbook.com/space-api-reference</a></td><td><a href=".gitbook/assets/api-reference.jpg">api-reference.jpg</a></td></tr></tbody></table>

{% columns %}
{% column %}
### Get started in 5 minutes

Setting up your first calculation should be the easiest part of getting started. With clear APIs, copy-paste-ready examples, and quick setup, you’ll be up and running in minutes—not hours.

No guesswork, no complexity—just your first successful calculation, fast.

<a href="https://github.com/mdnm/kaabalah" class="button primary" data-icon="rocket-launch">Get started</a> <a href="https://github.com/mdnm/kaabalah" class="button secondary" data-icon="terminal">API reference</a>
{% endcolumn %}

{% column %}
{% code title="index.js" overflow="wrap" %}
```javascript

// Import the SDK
import { createTree } from 'kaabalah/core';

// Initialize the tree
const tree = createTree({
  system: 'kaabalah',
  parts: ['westernAstrology', 'tarot'],
});

// Calculate the gematria of a name
const gematriaResult = calculateGematria('kaabalah', tree);

console.log(gematriaResult);

```
{% endcode %}
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column %}
<figure><img src="https://gitbookio.github.io/onboarding-template-images/placeholder.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
### Learn more about the developer platform

Read guides, watch tutorials, and learn more about working with the developer platform and integrating it with your own stack.

<a href="https://github.com/mdnm/kaabalah" class="button primary" data-icon="book-open">Guides</a> <a href="https://github.com/mdnm/kaabalah" class="button secondary" data-icon="book">Documentation</a>
{% endcolumn %}
{% endcolumns %}

<h2 align="center">Join a community of over 3,000 developers</h2>

<p align="center">Join our Discord community or create your first PR in just a few steps.</p>

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><h4><i class="fa-discord">:discord:</i></h4></td><td><strong>Discord community</strong></td><td>Join our Discord community to post questions, get help, and share resources with over 3,000 like-minded developers.</td><td><a href="https://kaabalah.com/" class="button secondary">Join Discord</a></td><td></td></tr><tr><td><h4><i class="fa-github">:github:</i></h4></td><td><strong>GitHub</strong></td><td>Our product is 100% open source and built by developers just like you. Head to our GitHub repository to learn how to submit your first PR.</td><td><a href="https://github.com/mdnm/kaabalah" class="button secondary">Submit a PR</a></td><td></td></tr></tbody></table>
