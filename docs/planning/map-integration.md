# Map Integration Strategy – Critical Init

## Purpose
This document outlines the strategy for integrating external, procedurally generated maps—specifically from [https://watabou.github.io](https://watabou.github.io)—into Critical Init using Unity.

Watabou’s tools provide beautiful and free-to-use maps that we can leverage for world-building, city layouts, dungeons, and more.

---

## Primary Tools from Watabou
- **Medieval Fantasy City Generator**
- **One Page Dungeon**
- **Procgen Arcana**

---

## Supported Export Formats
| Format | Usage                     | Notes                                |
|--------|---------------------------|--------------------------------------|
| PNG    | Visual map or background  | Easy to import and render            |
| SVG    | Vector layout             | Optional: could be parsed for shape  |
| JSON   | Structural map data       | Optional: for procedural parsing     |

---

## Integration Options

### 🔹 1. Static Visual Map (Phase 1)
Use PNGs as backgrounds or overlays:
- Drag the exported PNG into `Assets/Maps/`
- Create a `SpriteRenderer` in the scene
- Set the image as the sprite
- Adjust camera to match the size and position

Best used for:
- World maps
- Menu screens
- Dungeon entrances

### 🔹 2. Interactive Gameplay Map (Phase 2)
Use exported PNGs or tile-based references to create:
- Unity Tilemaps
- Prefab-based scenes (based on visual reference)
- Manual or semi-automated tile painting

Steps:
- Use tools like [Tiled](https://www.mapeditor.org/) to convert PNG to tile layout (optional)
- Slice the PNG in Unity and assign to a tile palette
- Paint the layout using Unity’s Tilemap system
- Add colliders and triggers to designated areas

### 🔹 3. Procedural Import via JSON (Phase 3 or 4)
Parse JSON exports to reconstruct maps dynamically in Unity:
- Write a parser for Watabou JSON structure
- Generate tilemaps, positions, or prefabs from that data
- Potential for ML-enhanced map evolution based on player behavior

---

## File Organization (Recommended)
```
Assets/
├── Maps/
│   ├── Visual/
│   │   └── world-map-town1.png
│   ├── Interactive/
│   │   └── dungeon1-tilemap.png
│   └── JSON/
│       └── watabou-city-001.json
```

---

## Future Integration Ideas
- Mini-map system (using world PNGs)
- ML-generated adjustments to city/dungeon layouts
- Tying quests/NPCs to map nodes
- Weather overlays based on region

---

## Attribution & Usage
Watabou maps are publicly available and licensed under permissive terms for non-commercial and even commercial use. We will ensure attribution is included if required by the tool.

---

## Placement
📁 Place this file in: `docs/planning/map-integration.md`

---

This strategy ensures Critical Init remains visually rich while still building toward procedural and ML-driven world interaction.

