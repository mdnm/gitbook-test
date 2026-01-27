# Tarot

78 tarot cards with meanings, spreads, and interpretations

## Import

```typescript
import { ARKANNUS, majorArcana, shuffleTarotDeck } from 'kaabalah/tarot';
```

## Exports

* `ARKANNUS`
* `majorArcana`
* `shuffleTarotDeck`

## Card Structure

The `ARKANNUS` array contains all 78 tarot cards with the following structure:

```typescript
type TarotCard = {
  number: number
  tarotCard: string
  tarotCardFilename: string
  egyptianCardName?: string
  meaning: string
  papusMeaning?: string
  type: 'major' | 'minor' | 'daat+royalship'
  deck: string
  suit?: string
  isInverted?: boolean
}
```

## Card Types

* **Major Arcana** (1-22): The 22 trump cards
* **Da'at Royalship** (23-26, 37-40, 51-54, 65-68): Court cards for each suit
* **Minor Arcana** (27-36, 41-50, 55-64, 69-78): Pip cards for each suit

## Suits

* Wands (Fire)
* Cups (Water)
* Swords (Air)
* Pentacles (Earth)

## Usage Example

```typescript
import { ARKANNUS, shuffleTarotDeck } from 'kaabalah/tarot';

// Get all major arcana
const majorArcana = ARKANNUS.filter(card => card.type === 'major');

// Shuffle and draw 3 cards
const shuffled = await shuffleTarotDeck(ARKANNUS, true);
const spread = shuffled.slice(0, 3);
```

### Live example

{% embed url="https://tarot.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
