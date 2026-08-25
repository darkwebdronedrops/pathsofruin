# Paths of Ruin — Overworld & Hero Movement System

## Core Concept

The overworld is a **directed graph of nodes**. Each node represents a specific battle map with hardcoded terrain and layout. The 19 heroes **move between nodes** according to their own logic — they are not statically placed.

**The heroes ARE the plot.** Story beats trigger based on:
- Which heroes are present at a node when you arrive
- Which heroes are missing (dead, corrupted, or elsewhere)
- The state of relationships between present heroes

## Node Structure

```
Example branching (simplified):

    [Start] ──┬──→ [B] ──┬──→ [E] ──┬──→ [H]
              │          │          │
              ├──→ [C] ──┼──→ [F] ──┼──→ [I]
              │          │          │
              └──→ [D] ──┴──→ [G] ──┴──→ [J]
```

- Each node = one chapter battle
- Node connections are **directed** (you can go B→E but not E→B)
- Some nodes are **mandatory** (story gates)
- Some nodes are **optional** (recruitment opportunities, item shops)
- Convergent nodes (E, F, G) allow paths to merge

## Hero Movement Rules

Heroes exist as **entities on the graph**, not fixed to nodes:

1. **Starting positions** — Each hero begins at a specific node (varies by playthrough seed or is fixed)
2. **Movement triggers** — Heroes move between connected nodes:
   - After each battle (all surviving enemy heroes move 1 node)
   - When certain story conditions are met
   - When other heroes are corrupted/killed (some heroes pursue, some flee)
3. **Movement patterns** — Each hero has tendencies:
   - **Aggressive:** Moves toward the player/front lines
   - **Defensive:** Holds position or retreats toward the capital
   - **Strategic:** Moves to cut off player paths or protect key nodes
   - **Territorial:** Stays within a region unless forced out

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

### Example: Twin Converter (special)
- Starts at the capital (final nodes)
- Moves **toward the player** each chapter
- Can uncorrupt heroes the player has already recruited
- Appears at whatever node the player is at after Chapter 15 (forced encounter)

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
| **Capital Gate** | Final main-game nodes, all surviving heroes deployed |
| **Capital** | Endgame chapters (21-23), story-mandatory |

---

*Started: 2026-08-26*
