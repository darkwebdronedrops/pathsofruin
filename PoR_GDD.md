# Paths of Ruin — Game Design Document

**Working Title:** Paths of Ruin  
**Genre:** Tactical RPG (Fire Emblem-style grid combat)  
**Platform:** TBD (PC primary)  
**Status:** Concept Phase  

---

## 1. Overview

Twenty students from a single classroom are isekai'd into a fantasy world at war.

- **The 19** are summoned by the Goddess. They each receive a unique divine blessing.
- **You** are summoned by the Demon King. Your blessing is **Apostle's Touch** — the power to corrupt anyone you defeat.

### The War

The Demon King seeks **dominion over the continent**. The Goddess and her empire have been at war with monsterkind for generations, fighting over resources and territory.

**This is not a moral conflict.** Neither side is inherently good or evil:
- The Monster side is "monstrous" because they fight and kill humans
- The Human side is "good" because they fight monsters and are human
- The player is human, yet fights for the Demon King
- The war itself is about **resources and territory**, not righteousness

**Mind control** (used by two of the heroes) is simply a tool of war — as is corruption.

The game spans 23 chapters of grid-based tactical combat. Deaths are permanent. The plot requires only **you** to survive — everyone else is optional, recruitable, or expendable.

---

## 2. Core Loop

1. **Tactical Combat** — Grid-based, turn-based battles against the Goddess's heroes
2. **Corruption Decision** — For each enemy: kill for full XP, or use Apostle's Touch to recruit them at their current HP
3. **Army Management** — Recruited enemies join immediately in-combat, creating protection and XP-sharing dilemmas
4. **Camp & Relationships** — Between battles, manage relationships, trigger scenes, and prepare for the next fight
5. **Permadeath** — Anyone who dies in combat is gone forever, including recruited allies

---

## 3. Combat System

### 3.1 Apostle's Touch (Corruption)

The MC has two attack modes:

| Mode | Damage | Effect | XP |
|------|--------|--------|-----|
| Normal Attack | Weapon damage | Standard combat | Standard XP |
| Apostle's Touch | **0** | Deals Corruption equal to weapon stats | **+1 XP only** |

**Recruitment Condition:** When an enemy's accumulated Corruption ≥ their current HP, they are immediately converted to your side.

**Recruitment Properties:**
- Unit joins **in the current battle** at its present HP and stats
- Not added to a roster — they're on the field, right now
- Enemy AI ceases; unit becomes player-controlled
- Must be protected for the rest of the battle or they die permanently

### 3.2 The Choice

Every enemy presents a decision:
- **Kill** — Full XP, loot, no risk of losing the unit later
- **Corrupt** — +1 XP only, but gain a new party member at their current HP

**Risk/Reward:**
- Recruited units absorb XP from kills (shared pool)
- Low-HP recruits are fragile and require protection
- High-HP recruits are powerful but took longer to corrupt
- Apostle's Touch grants almost no XP, slowing MC progression

### 3.3 XP & Leveling

- **XP Range:** 1–99 XP per level
- **Level-Up:** 100 XP triggers level up; the 100th XP becomes 1 XP at the next level
- **Apostle's Touch:** Always grants exactly +1 XP, regardless of outcome

This creates tension: corruption slows your MC's growth while expanding your army.

### 3.4 Permadeath

- All deaths are **permanent**
- Plot does **not** require anyone but the MC to survive
- Game continues even if all recruitable characters die
- Some content (camp scenes, relationship dialogue) becomes inaccessible if specific characters die

**MC Death:** Game over. The Demon King does not resurrect you.

**Save System:**
- **Battle saves** — Save during combat (standard)
- **Chapter saves** — Save between chapters
- **Optional Iron Man Mode** — For players who want true permadeath with no reloading

---

### 3.5 Corruption Visuals

When a unit is corrupted:
- **Map sprite** — Changes to the player's team color
- **Portrait** — Eyes turn red
- No body horror or visual degradation — corruption is presented as a tool, not a defilement

---

## 4. Characters

### 4.1 The MC

- **Gender:** Player-selected (Male/Female)
- **Replaces one of two possible characters** depending on gender choice, keeping the 10M/10F ratio
- **Power:** Apostle's Touch (corruption)
- **Backstory:** Ordinary student, pulled by the Demon King instead of the Goddess

### 4.2 The 19 (Goddess's Heroes)

- **20 total characters** including MC
- **19 distinct, named characters** with unique:
  - Combat class/build
  - Divine blessing (special power)
  - Personality and backstory
  - Relationship arcs with other characters
- **Special dialogue** with MC for each character
- **Relationship dialogue** between specific pairs/triples

### 4.3 The Twin Converter

At character generation, the MC replaces **one of two possible characters** based on gender selection. The character **not replaced** becomes a special enemy:

- They possess a power analogous to Apostle's Touch: **the ability to uncorrupt**
- They can revert corrupted heroes back to the Goddess's side
- If you corrupt this character, you gain **two converter characters** (MC + them)
- This creates a strategic arms race: who can convert faster?

### 4.3 Character Relationships

**Romance System:**
- **3 romanceable characters** (for the MC)
- Other characters can form relationships with each other:
  - Romantic pairings
  - Deep friendships
  - Rivalries

**Camp Scenes:**
- Trigger based on **character presence + relationship level**
- Example: "If you have [Character A] and [Character B] at Relationship Level 3, a camp scene triggers"
- Some scenes require specific characters to be alive and recruited

---

## 5. Army Composition

### 5.1 Demon Army Hirelings

- Generic demon units available as filler
- Weaker than the 19 heroes but expendable
- Can be hired between battles

### 5.2 Corrupted Heroes

- The 19 heroes who were converted via Apostle's Touch
- Retain their divine blessings and classes
- Can die permanently just like anyone else
- Can potentially be **uncorrupted** by the Twin Converter (the character not replaced at char gen)
- Once the Twin Converter is themselves corrupted, you have **two corruption sources**

### 5.3 Boss Recruitment

- Major enemy heroes (bosses) can also be corrupted
- Bosses who join bring unique classes/powers
- Some bosses may have special recruitment conditions

---

## 6. Structure

### 6.1 Three-Act Structure

The game is divided into three narrative and mechanical sections:

#### Act I: The Tutorial (Chapters 1–3)

**Chapter 1 — The Real World**
- Opens in the classroom. All 20 students are introduced.
- Player selects MC gender, replacing one of two characters.
- Brief interactive scenes establishing classroom dynamics and relationships.
- The isekai event: light, summoning, separation.

**Chapter 2 — The Summoning**
- MC awakens in the Demon King's realm. First combat against monsters.
- Exposition delivered through combat: tutorial mechanics, Apostle's Touch demonstration.
- Demon King explains the war, the Goddess, your power.

**Chapter 3 — First Blood**
- First encounter with the Goddess's heroes. Tutorial corruption.
- Demonstrates the core choice: kill or corrupt.
- Establishes the Twin Converter as antagonist.

#### Act II: The Main Game (Chapters 4–20)

- **Overworld map** with branching paths
- Player chooses which regions/battles to engage
- Path choice determines:
  - Which heroes appear as enemies (and can be corrupted)
  - Which heroes may die before you reach them
  - Terrain types, enemy composition, rewards
- Some heroes appear in multiple paths; others are path-locked
- Demon army hirelings available between battles
- Camp and relationship management between chapters

#### Act III: The Endgame (Chapters 21–23)

- Assault on the **enemy capital** (Goddess's stronghold)
- All surviving heroes are deployed in defense
- Final confrontation with the **Twin Converter**
- Multiple endings based on:
  - Who was corrupted
  - Who died
  - MC's romance
  - Whether the Twin Converter was recruited

### 6.2 Total Chapters

- **23 chapters** total
- Chapters 1–3: Tutorial
- Chapters 4–20: Main game (overworld path choices)
- Chapters 21–23: Endgame (capital assault)

### 6.3 Overworld Map

- **Node-based** map with connected regions
- Each node = one chapter/battle
- Some nodes are **optional** (recruitment opportunities)
- Some nodes are **mandatory** (story progression)
- Node selection determines:
  - Which heroes appear
  - Which terrain
  - Enemy army composition
  - Available rewards

### 6.4 Progression

- MC grows through normal combat XP
- Army grows through corruption (immediate) or hirelings (between battles)
- Relationship levels advance through camp interactions and battle proximity

---

## 7. Open Questions / TODO

- [x] What happens if MC dies? **Game over. No resurrection.**
- [x] Can corrupted heroes be "uncorrupted" or saved? **Yes — via the Twin Converter.**
- [ ] What does the Demon King provide besides the initial summon? Guidance? Resources?
- [x] How are the 19 distributed across the 23 chapters? **Tutorial (3) → Main game with overworld paths (17) → Endgame (3). Some may die before you reach them based on path choices.**
- [ ] Does the MC have a class system, or is Apostle's Touch the only differentiator?
- [ ] Equipment/gear system depth?
- [x] What does "corruption" look like visually/narratively? **Team color swap + red eyes. Not body horror.**
- [x] Ending structure — multiple endings based on who lives/dies/who you romance? **Yes — corrupted roster, deaths, romance, and Twin Converter status all factor in.**
- [ ] Camp scene scope — how many? Fully written or procedural/generated?
- [ ] What is the Twin Converter's class/build?

---

## 8. Design Pillars

1. **Every enemy is a choice** — Kill or corrupt? XP now or unit forever?
2. **Permanence matters** — Death is real. Loss is real. The story adapts.
3. **Relationships are systemic** — Characters interact with each other, not just the MC.
4. **The Demon King is not evil by default** — Corruption is a tool, not a moral failing.
5. **Player agency over plot** — The story requires only you. Everything else is optional.

## 9. Class System

### 9.1 Base Classes (10 total)

| Base Class | Stat Modifiers / Abilities |
|-----------|---------------------------|
| **Fencer** | +10% crit |
| **Thief** | Open locks, +1 Move |
| **Fighter** | +2 CON |
| **Knight** | -1 Move, +20% DEF growth |
| **Cavalier** | +2 Move, -5% all growths |
| **Priest** | +10% LCK growth |
| **Mage** | Critical hits are x4 instead of x3 |
| **Warlock** | -10% SKL growth, +4 ATK |
| **Bard** | Double SPD bonus when attacked |
| **Apostle** (MC only) | Corruption ability, +5% all growths |

### 9.2 Advanced Classes (10 total)

Base classes share advanced classes in a chain:

| Base Class Pair | Advanced Class |
|----------------|----------------|
| Fencer / Apostle | Hero |
| Fencer / Thief | Assassin |
| Thief / Fighter | Pirate |
| Fighter / Knight | Barbarian |
| Knight / Cavalier | Dragoon |
| Cavalier / Priest | Paladin |
| Priest / Mage | Sage |
| Mage / Warlock | Archmage |
| Warlock / Bard | Shaman |
| Bard / Apostle | Saint |

### 9.3 Class Change Rules

- **Base class abilities persist** through class change
- Example: Thief → Assassin keeps lockpicking and +1 Move
- Example: Fencer → Assassin keeps +10% crit
- Two units of the same advanced class can play completely differently depending on their base class

### 9.4 Three-Layer Ability System

Every character has **3 layers** of abilities:
1. **Base class** — shared with all of that base class
2. **Advanced class** — shared with all of that advanced class
3. **Unique ability** — character-specific only

This means a corrupted enemy brings their full build: base + advanced + unique.

---

## 10. Stats & Growth

### 10.1 Stat Caps (Base Classes)

| Stat | Base Cap | Notes |
|------|---------|-------|
| **HP** | 60 | Never class-limited |
| **LCK** | 30 | Never class-limited |
| **ATK** | 20 | |
| **SKL** | 20 | |
| **SPD** | 20 | |
| **DEF** | 20 | |
| **RES** | 20 | |

### 10.2 Level-Up Stats (7 rolled)

On level up, the following stats are randomly rolled based on growth percentages:
- HP, ATK, SKL, SPD, LCK, DEF, RES

### 10.3 Derived / Function Stats

These are **not** rolled on level up:
- **HIT** — calculated function
- **CRIT** — calculated function
- **MOVE** — modified by class
- **CON** — modified by class

---

*Document started: 2026-08-17*  
*Last updated: 2026-08-17*
