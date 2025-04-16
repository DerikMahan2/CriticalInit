# SRD Implementation Plan – Critical Init

## 📜 Purpose
This document outlines how Critical Init will use content from the Dungeons & Dragons 5th Edition **System Reference Document (SRD)** in compliance with the **Open Game License (OGL) v1.0a**.

---

## ✅ What We Can Use from the SRD

According to the SRD and OGL v1.0a, the following **mechanical elements** are available for use:

### Character Content
- Races (Elf, Dwarf, Human, etc.)
- Classes (Fighter, Cleric, Wizard, etc.)
- Backgrounds and Traits
- Leveling and Proficiencies

### Mechanics
- Ability Scores (STR, DEX, CON, INT, WIS, CHA)
- Combat rules (initiative, saving throws, action economy)
- Equipment lists
- Spell lists and mechanics
- Conditions (Blinded, Stunned, etc.)

### Game Systems
- XP tables
- Magic and spellcasting rules
- Item descriptions (SRD-approved only)

---

## ❌ What We Will Not Use

We will **not** use any Wizards of the Coast trademarks or copyrighted settings:

- Named lore (e.g., Faerûn, Forgotten Realms, Baldur’s Gate)
- Trademarked creatures (e.g., Beholders, Mind Flayers, Owlbears)
- Iconic characters or locations
- Logos or branding from Wizards of the Coast or D&D

All references will remain **generic**, and any lore or story material will be 100% original.

---

## 📄 License Attribution (Required)

This project will include a `legal/srd-compliance.md` file containing:
- The full text of the **Open Game License (OGL) v1.0a**
- A section listing which SRD elements are used
- Proper attribution as required by the license

---

## 🛠 Implementation Strategy

- All SRD-derived content will be modular and **stored in external JSON or ScriptableObjects** (e.g., `races.json`, `spells.json`) so it can be isolated or replaced if needed.
- Any changes to SRD mechanics will be documented and clearly distinguished as **homebrew**.
- An `SRDContent` namespace will be used for any code interfacing with SRD data.

---

## Notes
- Future commercial release will maintain SRD/OGL compliance and may evolve toward a dual-license structure if needed.
- This strategy ensures flexibility while remaining legally protected and professionally structured.