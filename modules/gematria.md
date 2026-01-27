# Gematria

Calculate Hebrew gematria values for names and words, with reverse gematria lookup

## Import

```typescript
import { calculateGematria, reverseGematria } from 'kaabalah/gematria';
```

## Exports

* `calculateGematria`
* `reverseGematria`

## Examples

### Handle O at start (AYIN = 70) vs elsewhere (VAV = 6)

```typescript
import { reverseGematria } from "kaabalah";

// O at start = 70
const resultO = reverseGematria({ targetVowels: 70, maxLength: 1 });

// AO = A(1) + O(6) = 7 vowels (O not at start)
const resultAO = reverseGematria({
  targetVowels: 7,
  targetConsonants: 0,
  minLength: 2,
  maxLength: 2,
});
```

### Handle ending letter values

```typescript
import { reverseGematria } from "kaabalah";

// C at end = 500 (Kaph sofit), C in middle = 20
// AC = A(1) + C(500) = 501 synthesis, 1 vowel, 500 consonants
const resultAC = reverseGematria({
  targetConsonants: 500,
  targetVowels: 1,
  minLength: 2,
  maxLength: 2,
});
const acResult = resultAC.results.find((r) => r.letters === "AC");

// M at end = 600 (Mem sofit)
const resultAM = reverseGematria({
  targetConsonants: 600,
  targetVowels: 1,
  minLength: 2,
  maxLength: 2,
});
```

### Include digraphs when includeDigraphs is true

```typescript
import { reverseGematria } from "kaabalah";

// SH = 300
const resultWithDigraphs = reverseGematria({
  targetConsonants: 300,
  maxLength: 2,
  includeDigraphs: true,
});
```

### Exclude digraphs when includeDigraphs is false

```typescript
import { reverseGematria } from "kaabalah";

const resultWithoutDigraphs = reverseGematria({
  targetConsonants: 300,
  maxLength: 2,
  includeDigraphs: false,
});
// SH should not be present, but X (300) should be
```

### Set hasMore when more results exist

```typescript
import { reverseGematria } from "kaabalah";

const result = reverseGematria({
  targetSynthesis: 10,
  maxResults: 1,
  maxLength: 5,
});
// There are many ways to reach synthesis of 10
```

## How Gematria Works

Latin letters are mapped to Hebrew letter values:

* Vowels (A, E, I, O, U, W, Y) have specific values
* Consonants map to Hebrew consonant values
* Position-dependent values (e.g., O at start = 70, elsewhere = 6)
* Final letter forms (sofit) when at word end

## Usage Example

```typescript
import { calculateGematria, reverseGematria } from 'kaabalah/gematria';

// Calculate gematria for a name
const result = calculateGematria('DAVID');
console.log(result.synthesis.originalSum);  // Total value
console.log(result.vowels.originalSum);     // Vowels value
console.log(result.consonants.originalSum); // Consonants value

// Find words with specific values
const matches = reverseGematria({
  targetSynthesis: 25,
  maxLength: 5
});
```

### Live example

{% embed url="https://gematria.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
