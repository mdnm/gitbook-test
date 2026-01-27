# Gematria

Calculate Hebrew gematria values for names and words, with reverse gematria lookup

## Import

```typescript
import { calculateGematria, reverseGematria } from 'kaabalah/gematria';
```

## Exports

- `calculateGematria`
- `reverseGematria`

## Examples

### should calculate correct values for letter %s

```typescript
const result = calculateGematria(input as string);
```

### should calculate missing letters

```typescript
calculateGematria("ABCDEFGHIJKLMNOPQRSTUVWXYZ", { missing: true
```

### should calculate letter percentages

```typescript
calculateGematria("KAABALAH", { percentages: true
```

### should correctly handle multiple words

```typescript
const { consonants, vowels
```

### should correctly return the included letters

```typescript
const { includedLetters
```

## How Gematria Works

Latin letters are mapped to Hebrew letter values:

- Vowels (A, E, I, O, U, W, Y) have specific values
- Consonants map to Hebrew consonant values
- Position-dependent values (e.g., O at start = 70, elsewhere = 6)
- Final letter forms (sofit) when at word end

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

---

If you find this package useful, you can support it on Ko-Fi too (or just star the repo):

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
