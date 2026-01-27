# Core

Tree of Life system for building correspondences across different esoteric systems

## Import

```typescript
import { TreeOfLife, BaseNode, SPHERES, ... } from 'kaabalah/core';
```

## Exports

* `TreeOfLife`
* `BaseNode`
* `SPHERES`
* `SPHERES_DATA`
* `HEBREW_LETTERS_DATA`

## Examples

### Add nodes and links, retrieving relations correctly

```typescript
import { TreeOfLife, SPHERES, SPHERES_DATA } from "kaabalah";

const treeOfLife = new TreeOfLife();

const kether = treeOfLife.addSphere({
  sphere: SPHERES.KETHER,
  data: SPHERES_DATA.KETHER,
  relatedNumber: 1,
});
const chokhmah = treeOfLife.addSphere({
  sphere: SPHERES.CHOKHMAH,
  data: SPHERES_DATA.CHOKHMAH,
  relatedNumber: 2,
});

const path11 = treeOfLife.addPath({
  leftSphere: kether,
  rightSphere: chokhmah,
  relatedNumber: 1,
});
```

### Correctly link nodes

```typescript
import { TreeOfLife, BaseNode, SPHERES, SPHERES_DATA, HEBREW_LETTERS_DATA } from "kaabalah";

const treeOfLife = new TreeOfLife();

const chokhmah = treeOfLife.addSphere({
  sphere: SPHERES.CHOKHMAH,
  data: SPHERES_DATA.CHOKHMAH,
  relatedNumber: 2,
});
const binah = treeOfLife.addSphere({
  sphere: SPHERES.BINAH,
  data: SPHERES_DATA.BINAH,
  relatedNumber: 3,
});

const path14 = treeOfLife.addPath({
  leftSphere: chokhmah,
  rightSphere: binah,
  relatedNumber: 4,
});

treeOfLife.addLetters({
  path: path14,
  letters: [
    {
      letter: "Aleph",
      type: LetterTypes.HEBREW_LETTER,
      data: HEBREW_LETTERS_DATA.ALEPH,
    },
    { letter: "A", type: LetterTypes.LATIN_LETTER },
  ],
});

const air = treeOfLife.upsertNode(
  new BaseNode({ id: "Air", type: WesternAstrologyTypes.WESTERN_ELEMENT })
);
treeOfLife.link(path14, air);

const jupiter = treeOfLife.upsertNode(
  new BaseNode({ id: "Jupiter", type: WesternAstrologyTypes.PLANET })
);
treeOfLife.link(path14, jupiter);

const theEmperor = treeOfLife.addTarotArkAnnu({
  node: path14,
  tarotArkAnnu: "The Emperor",
  data: { type: "major" },
  relatedNumber: 14,
});
```

### Correctly remove nodes

```typescript
import { TreeOfLife, SPHERES, SPHERES_DATA } from "kaabalah";

const treeOfLife = new TreeOfLife();

const chokhmah = treeOfLife.addSphere({
  sphere: SPHERES.CHOKHMAH,
  data: SPHERES_DATA.CHOKHMAH,
  relatedNumber: 2,
});
const binah = treeOfLife.addSphere({
  sphere: SPHERES.BINAH,
  data: SPHERES_DATA.BINAH,
  relatedNumber: 3,
});

const path14 = treeOfLife.addPath({
  leftSphere: chokhmah,
  rightSphere: binah,
  relatedNumber: 4,
});

treeOfLife.removeNode(chokhmah);
```

## Tree of Life Structure

The Tree of Life consists of:

* **10 Sephiroth (Spheres)**: Kether, Chokhmah, Binah, Chesed, Geburah, Tiphareth, Netzach, Hod, Yesod, Malkuth
* **22 Paths**: Connecting the Sephiroth, associated with Hebrew letters
* **Correspondences**: Links to tarot, astrology, numerology, and more

## Usage Example

```typescript
import { TreeOfLife, SPHERES, SPHERES_DATA } from 'kaabalah/core';

const tree = new TreeOfLife();

// Add spheres
const kether = tree.addSphere({
  sphere: SPHERES.KETHER,
  data: SPHERES_DATA.KETHER,
  relatedNumber: 1
});

// Get related nodes
const related = tree.related(kether);
```

## Live example

{% embed url="https://archetypes.kaabalah.com" %}

***

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
