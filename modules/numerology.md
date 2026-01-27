# Numerology

Calculate life path numbers, cycles, challenges, and other numerological values

## Import

```typescript
import { calculateKaabalisticLifePath, calculateStraightAcrossReductionLifePath, calculateCycles, ... } from 'kaabalah/numerology';
```

## Exports

* `calculateKaabalisticLifePath`
* `calculateStraightAcrossReductionLifePath`
* `calculateCycles`
* `calculateChallenges`
* `calculateFibonacciCycle`
* `calculatePersonalCycles`
* `getDateEnergies`
* `isMasterNumber`

## Examples

### Handles years ending with 00 (including leap-day in 2000)

```typescript
import { calculateKaabalisticLifePath } from "kaabalah";

// Helper function
const dUTC = (y: number, m: number, d: number) =>
  new Date(Date.UTC(y, m - 1, d));

const a = calculateKaabalisticLifePath(dUTC(1900, 1, 1)); // Y2='00'

const b = calculateKaabalisticLifePath(dUTC(2000, 2, 29)); // leap day in a 00 year

const c = calculateKaabalisticLifePath(dUTC(2000, 1, 1)); // common 00-year master
```

### Ignores time-of-day (uses only the ISO date)

```typescript
import { calculateKaabalisticLifePath } from "kaabalah";

const a = calculateKaabalisticLifePath(
  new Date(Date.UTC(2012, 1, 12, 0, 0, 0))
);
const b = calculateKaabalisticLifePath(new Date("2012-02-12T23:59:59Z"));
```

### Handles years ending with 00 (including leap-day in 2000)

```typescript
import { calculateStraightAcrossReductionLifePath } from "kaabalah";

// Helper function
const dUTC = (y: number, m: number, d: number) =>
  new Date(Date.UTC(y, m - 1, d));

const a = calculateStraightAcrossReductionLifePath(dUTC(1900, 1, 1)); // Y2='00'

const b = calculateStraightAcrossReductionLifePath(dUTC(2000, 2, 29)); // leap day in a 00 year

const c = calculateStraightAcrossReductionLifePath(dUTC(2000, 1, 1)); // common 00-year master
```

### Ignores time-of-day (uses only the ISO date)

```typescript
import { calculateStraightAcrossReductionLifePath } from "kaabalah";

const a = calculateStraightAcrossReductionLifePath(
  new Date(Date.UTC(2012, 1, 12, 0, 0, 0))
);
const b = calculateStraightAcrossReductionLifePath(
  new Date("2012-02-12T23:59:59Z")
);
```

## Life Path Calculation Methods

### Kaabalistic Method

The `calculateKaabalisticLifePath` function uses a synthesis-based approach that:

* Preserves master numbers (11, 22, 33, 44, etc.)
* Calculates personal mythology numbers
* Provides detailed reduction steps

### Straight Across Reduction

The `calculateStraightAcrossReductionLifePath` function uses the traditional method of reducing each component (day, month, year) before summing.

## Usage Example

```typescript
import { calculateKaabalisticLifePath, calculateCycles } from 'kaabalah/numerology';

const birthDate = new Date('1990-06-15');
const lifePath = calculateKaabalisticLifePath(birthDate);

console.log(lifePath.lifePath.reducedValue);  // Life path number
console.log(lifePath.syntheses.finalSynthesis);  // Final synthesis
console.log(lifePath.personalMythologyNumbers);  // Personal mythology
```

## Live example

{% embed url="https://numerology.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
