# Paths of Ruin — Overworld & Hero Movement System

## Core Concept

The overworld is a **directed graph of nodes**. Each node represents a specific battle map with hardcoded terrain and layout. The 19 heroes **move between nodes** according to their own logic — they are not statically placed.

**The heroes ARE the plot.** Story beats trigger based on:
- Which heroes are present at a node when you arrive
- Which heroes are missing (dead, corrupted, or elsewhere)
- The state of relationships between present heroes

## Node Structure

- **26 nodes total** — slightly more than the 19 heroes, ensuring some nodes are empty or NPC-only
- Each node = one chapter battle
- Node connections are **directed** (you can go B→E but not E→B)
- **Dead end nodes** exist — nodes that connect nowhere except back the way you came. Places to corner heroes or be cornered.
- Some nodes are **mandatory** (story gates)
- Some nodes are **optional** (recruitment opportunities, item shops)
- Convergent nodes allow paths to merge
- **NPC encounters** fill empty nodes when no hero is present (heroes move, so any node CAN have a hero)

## Hero Movement Rules

Heroes exist as **entities on the graph**, not fixed to nodes:

1. **Starting positions** — Each hero begins at a specific node
2. **Movement triggers** — Heroes move between connected nodes:
   - After each battle (all surviving enemy heroes move 1 node)
   - When certain story conditions are met
   - When other heroes are corrupted/killed (some heroes pursue, some flee)
3. **Movement patterns** — Each hero has tendencies:
   - **Aggressive:** Moves toward the player/front lines
   - **Defensive:** Holds position or retreats toward the capital
   - **Strategic:** Moves to cut off player paths or protect key nodes
   - **Territorial:** Stays within a region unless forced out
   - **Avoidant:** Moves away from the player
   - **Random:** No predictable pattern

### Chapter Counter

**"Chapter" is defined by heroes defeated or converted.** The game advances its internal chapter counter each time a hero is killed or corrupted by the player. This means:
- Skipping nodes doesn't advance the chapter counter (no hero defeated)
- Dead end nodes that force NPC fights don't advance the counter
- The Twin Converter's phase transitions are tied to this counter, not raw map progress

## Player Agency

The player controls:
- **Which node to advance to** from their current position
- **Which optional nodes to visit** (skipping costs potential recruits)
- **When to use Apostle's Touch** in battle (corrupting a hero removes them from enemy movement)

The player does NOT control:
- **Enemy hero movement** (determined by AI/ scripted patterns)
- **Which heroes appear at a node** (depends on timing and prior movement)
- **Hero deaths off-screen** (heroes can die in battles you skip)

## Dynamic Encounters

### Example: Roland (Knight, defensive)
- Starts at Node C (frontier fort)
- If player goes B→E, Roland stays at C until player approaches, then retreats to F
- If player goes C directly, Roland defends C with local garrison
- If Roland's friend Keith is corrupted, Roland becomes **aggressive** and pursues the player

### Example: Marcus (Thief, strategic)
- Starts at Node D (bandit territory)
- Always tries to flank — moves to nodes adjacent to the player's path
- If player skips D, Marcus ambushes at a later convergence node (F or G)
- If corrupted early, stops moving entirely (becomes player unit)

### Twin Converter (special — phased movement)

The Twin Converter has a **three-phase movement pattern** tied to the chapter counter (heroes defeated/converted):

| Phase | Chapter Range | Behavior | Description |
|-------|--------------|----------|-------------|
| **Phase 1: Avoid** | 1–10 | **Avoidant** | Actively moves away from the player. Never appears at the player's node. |
| **Phase 2: Random** | 11–15 | **Random** | No longer avoiding, but not pursuing. Appearances are unpredictable. |
| **Phase 3: Pursuit** | 16+ | **Aggressive** | Actively hunts the player. Will appear at the player's node. |

**Key mechanic:** The Twin Converter can **uncorrupt** heroes the player has already recruited. This creates urgency — the longer you wait to deal with them, the more of your army they can revert.

**Forced encounter:** By Chapter 16+, the Twin Converter is in full pursuit and **will** encounter the player.

## Consequences of Skipping

- **Missed recruitment:** Heroes at skipped nodes may die in off-screen battles
- **Changed compositions:** Heroes who survive skipped nodes move elsewhere, changing later battles
- **Story divergence:** Some heroes carry key plot information; missing them locks/unlocks story beats

## Node Types

| Type | Description |
|------|-------------|
| **Frontier** | Early nodes, lightly defended, 1-2 heroes |
| **Fortress** | Heavily defended, 3-4 heroes, optional |
| **Convergence** | Merge points where multiple paths meet, high hero density |
| **Dead End** | Nodes that only connect back the way you came. High risk, high reward. |
| **Capital Gate** | Final main-game nodes, all surviving heroes deployed |
| **Capital** | Endgame chapters (21-23), story-mandatory |

---

*Started: 2026-08-26*
