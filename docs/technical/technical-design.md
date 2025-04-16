# Technical Design Overview – Critical Init

## Project Structure (Unity-Compatible)

```plaintext
CriticalInit/
├── Assets/
│   ├── Scripts/
│   │   ├── Core/             # GameManager, GameLoop, SaveSystem
│   │   ├── Characters/       # Player, NPC, Race, Class, Attributes
│   │   ├── Combat/           # CombatManager, AttackLogic, Initiative
│   │   ├── UI/               # Menu, Dialogue, Inventory UI Scripts
│   │   ├── World/            # Location, Weather, TimeSystem
│   │   ├── Data/             # ScriptableObjects & JSON Parsers
│   ├── Prefabs/
│   ├── Scenes/
│   │   └── MainScene.unity
│   ├── Resources/
│   └── Art/
├── ProjectSettings/
├── Packages/
├── Tests/
│   ├── CharacterTests.cs
│   ├── CombatTests.cs
│   └── WorldTests.cs
└── README.md
```

---

## Core Systems & Responsibilities

### 🎮 GameManager.cs
- Controls game states (Menu, Playing, Paused, Combat)
- Singleton pattern

### 🧠 GameLoop.cs
- Core loop logic (for turn-based progression)
- Handles updates in text UI or Unity canvas

### 💾 SaveSystem.cs
- Manages JSON-based save/load
- Serializes player data and world state

### 👤 Character.cs (Base Class)
- Inherited by PlayerCharacter.cs and NonPlayerCharacter.cs
- Contains:
  - Name, Race, Class
  - Stats, Skills, Proficiencies
  - Inventory

### ⚔️ CombatManager.cs
- Controls initiative, turn order, action economy
- Interfaces with CombatAction and DamageCalculator

### 🌍 WorldManager.cs
- Tracks weather, time, faction rep, world state

### 📜 DialogueManager.cs (Future)
- Controls multi-path conversations and NPC responses

---

## ScriptableObjects & JSON Use
- Races, Classes, Items, Spells will be defined as data files
- This allows easy tweaking without touching code

---

## Interfaces (Example Set)
```csharp
interface IGameState {}
interface ISaveable { string Save(); void Load(string data); }
interface ICharacterAction { void Execute(); }
```

These enable extensibility, testability, and modular design.

---

## Design Patterns Used
- Singleton (GameManager)
- Strategy (CharacterAction execution)
- Factory (NPC or Quest Generation)
- Observer/Event System (UI, turn triggers)

---

## Dependencies
- Unity 2022.x or higher (LTS preferred)
- TextMeshPro for UI
- Newtonsoft.Json or Unity’s JsonUtility
- ML.NET (optional, imported later for narrative generation)

---

## Notes
- Initial development will be console-based or minimal UI for rapid prototyping.
- All system responsibilities are modular and isolated.
- All data will be version-controlled and loaded from flat files (JSON) when possible.