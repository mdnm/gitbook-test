# Gematria

Calculate Hebrew gematria values for names and words, with reverse gematria lookup

## Import

```typescript
import { calculateGematria, reverseGematria } from 'kaabalah/gematria';
```

## Exports

* `calculateGematria`
* `reverseGematria`

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

## Live example

{% embed url="https://gematria.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
