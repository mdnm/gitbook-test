# Quickstart

## Usage Examples

### Core Library

```typescript
import { createTree } from 'kaabalah/core';

const tree = createTree({
  system: 'kaabalah',
  parts: ['westernAstrology', 'tarot'],
});

const gematriaResult = calculateGematria('kaabalah', tree);

console.log(gematriaResult);
```

### Direct Module Imports (Tree-Shakable)

```typescript
// Only import what you need
import { calculateLifePath } from 'kaabalah/numerology';
import { getBirthChart } from 'kaabalah/astrology';
import { calculateGematria } from 'kaabalah/kaabalah';
import { getRandomSpread } from 'kaabalah/tarot';

// Calculate life path number
const lifePath = calculateLifePath(new Date('1990-01-15'));

// Generate a birth chart (with Swiss Ephemeris)
const birthChart = getBirthChart({
  date: new Date('1990-01-15T12:30:00Z'),
  latitude: 40.7128,
  longitude: -74.0060,
  timezone: -5
});

// Calculate Hebrew gematria
const gematriaValue = calculateGematria('kaabalah');

// Get a tarot spread
const spread = getRandomSpread(3, true);
```

---

If you find this package useful, you can support it on Ko-Fi too (or just star the repo):

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
