# Astrology

Generate birth charts and planetary positions using Swiss Ephemeris

## Import

```typescript
import { getBirthChart, HouseSystem } from 'kaabalah/astrology';
```

## Exports

- `getBirthChart`
- `HouseSystem`

## Examples

### should calculate a birth chart

```typescript
const options: BirthChartOptions = {
        date: new Date(2024, 2, 25, 12, 0, 0),
```

### should handle timezone conversion correctly

```typescript
const options: BirthChartOptions = {
        date: new Date(2024, 2, 25, 8, 0, 0),
```

### should handle different house systems

```typescript
const baseOptions: BirthChartOptions = {
        date: new Date(2024, 2, 25, 12, 0, 0),
```

### should handle edge cases and invalid inputs

```typescript
const baseOptions: BirthChartOptions = {
        date: new Date(2024, 2, 25, 12, 0, 0),
```

## House Systems

The library supports multiple house systems:

- `HouseSystem.PLACIDUS` - Most commonly used
- `HouseSystem.KOCH` - Koch system
- `HouseSystem.EQUAL` - Equal house system
- `HouseSystem.WHOLE_SIGN` - Whole sign houses

## Usage Example

```typescript
import { getBirthChart, HouseSystem } from 'kaabalah/astrology';

const chart = await getBirthChart({
  date: new Date('1990-06-15T12:30:00'),
  latitude: 40.7128,
  longitude: -74.0060,
  houseSystem: HouseSystem.PLACIDUS,
  timeZoneSettings: { timeZone: 'America/New_York' }
});

console.log(chart.planets.sun);  // Sun position
console.log(chart.houses.ascendant);  // Ascendant
```

---

If you find this package useful, you can support it on Ko-Fi too (or just star the repo):

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
