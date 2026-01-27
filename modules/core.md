# Core

Tree of Life system for building correspondences across different esoteric systems

## Import

```typescript
import { TreeOfLife, BaseNode, SPHERES, ... } from 'kaabalah/core';
```

## Exports

- `TreeOfLife`
- `BaseNode`
- `SPHERES`
- `SPHERES_DATA`
- `HEBREW_LETTERS_DATA`

## Examples

### should add nodes and links, retrieving relations correctly

```typescript
const treeOfLife = new TreeOfLife();
    const kether = treeOfLife.addSphere({
```

### should throw an error when trying to link unknown nodes

```typescript
const treeOfLife = new TreeOfLife();
```

### should correctly link nodes

```typescript
const treeOfLife = new TreeOfLife();
    const chokhmah = treeOfLife.addSphere({
```

### should correctly remove nodes

```typescript
const treeOfLife = new TreeOfLife();
    const chokhmah = treeOfLife.addSphere({
```

## Tree of Life Structure

The Tree of Life consists of:

- **10 Sephiroth (Spheres)**: Kether, Chokhmah, Binah, Chesed, Geburah, Tiphareth, Netzach, Hod, Yesod, Malkuth
- **22 Paths**: Connecting the Sephiroth, associated with Hebrew letters
- **Correspondences**: Links to tarot, astrology, numerology, and more

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

---

If you find this package useful, you can support it on Ko-Fi too (or just star the repo):

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/matmoura19)
