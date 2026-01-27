# Ifa

Calculate Odu numbers based on dates for Ifa divination

## Import

```typescript
import { calculateOdu } from 'kaabalah/ifa';
```

## Exports

- `calculateOdu`

## How Odu Calculation Works

The Odu numbers are calculated from a date by:

1. Splitting the date (DD/MM/YYYY) into left and right digit columns
2. Summing each column and reducing to 1-16
3. Calculating directional values:
   - **North**: Sum of left column
   - **South**: Sum of right column
   - **East**: North + South
   - **West**: North + South + East
   - **Center**: Sum of all directions

## Usage Example

```typescript
import { calculateOdu } from 'kaabalah/ifa';

const odu = calculateOdu(new Date('1990-06-15'));
console.log(odu.north);  // North direction Odu
console.log(odu.center); // Center/synthesis Odu
```

---

If you find this package useful, you can support it on Ko-Fi too (or just star the repo):

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
