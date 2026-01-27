# Astrology

Generate birth charts and planetary positions using Swiss Ephemeris

### WebAssembly usage

This library uses the Swiss Ephemeris for astrological calculations, find the integration guide here:

{% content-ref url="../guides/webassembly.md" %}
[webassembly.md](../guides/webassembly.md)
{% endcontent-ref %}

## Import

```typescript
import { getBirthChart, HouseSystem } from 'kaabalah/astrology';
```

## Exports

* `getBirthChart`
* `HouseSystem`

## House Systems

The library supports multiple house systems:

* `HouseSystem.PLACIDUS` - Most commonly used
* `HouseSystem.KOCH` - Koch system
* `HouseSystem.EQUAL` - Equal house system
* `HouseSystem.WHOLE_SIGN` - Whole sign houses

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

## Live example

{% embed url="https://astrology.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
