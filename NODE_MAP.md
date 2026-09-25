# Paths of Ruin — Node Map (26 Nodes)

## Graph Overview

```
                        [NORTH]
                            │
        B4 NORTH_RIDGE ── B2 BORDER_FORT
         │                    │
        B9 FORGOTTEN_VAULT    │
         (DEAD END)           │
                              │
                              B1 CROSSROADS
                             ╱      │      ╲
                    (from A3)   B3 RIVERFORD  B5 HOLLOW_PASS
                                    │            │
                              C2 SHRINE_ASH      │
                                    │         B6 SUNKEN_MARSH
                                    │            │
                                    │         C4 WAR_CAMP ── C8 WARLORD'S_REST
                                    │            │        (DEAD END)
                              C3 MERCHANT_CAMP   │
                                    │            │
                                    └──────┬─────┘
                                           │
                              C1 HEARTLAND_GATE
                             ╱      │      ╲
                    C6 CATHEDRAL_STEP C5 SIEGEWORKS
                          │              │
                          │           (C9 DRAGONFALL
                          │            DEAD END)
                          │              │
                          └──────┬───────┘
                                 │
                           C7 BATTLEFIELD
                                 │
                           D1 GODSWARD
                                 │
                           D2 LIGHTFALL
                                 │
                        [E1 → E2 → E3 CAPITAL]
                        
        B8 OLD_QUARRY (DEAD END, off B6)
```

---

## Region 1: The Wastes (Demon King Territory)

| ID | Node | Terrain | Hero | Notes |
|----|------|---------|------|-------|
| A1 | THE_RIFT | Obsidian crater | — | Tutorial 1. The summoning site. |
| A2 | ASHFIELDS | Ash plain, burning vents | — | Tutorial 2. Demon army intro. |
| A3 | FIRST_LIGHT | Border meadow | **Jax** | Tutorial 3. Scripted encounter — kill or corrupt. **Permanent consequence.** |

### Tutorial Hero: Jax (Recommendation)
Jax is the tutorial's living choice:
- **Corrupt him:** He joins immediately. Camp gains music. His "you're still in there, right?" line lands as your first corrupted ally.
- **Kill him:** Permadeath is taught by loss. His plot fragments (morale, music, the war's emotional truth) redistribute to Rafael (performer grief → resolve).
- **Why Jax:** Friendly, curious, narratively plausible vanguard scout. His corruption reaction ("reaching for the old you") sets the emotional tone for every recruitment after.

**Connections:** A1→A2→A3→B1 (linear, mandatory)

---

## Region 2: The Borderlands

| ID | Node | Terrain | Hero | Movement |
|----|------|---------|------|----------|
| B1 | CROSSROADS | Dirt crossroads, neutral ground | — | Hub. First real branch. |
| B2 | BORDER_FORT | Stone fort, walls | **Suki** | Territorial. Holds until defeated, then retreats to C1. |
| B3 | RIVERFORD | River crossing, bridges | **Marcus** | Strategic. Ambush AI. Flanks player's next node. |
| B4 | NORTH_RIDGE | Snowy ridge, elevation | **Elena** | Territorial (research). Retreats to C2 when threatened. |
| B5 | HOLLOW_PASS | Canyon pass, chokepoints | **Greta + Keith** | Aggressive. They *advance toward* B1 if player dawdles. |
| B6 | SUNKEN_MARSH | Swamp, water tiles | **Damien** | Territorial (broods). Holds. |
| B7 | MILL_TOWN | Village, buildings, civilians | **Tomás + Mei** | Defensive. Protect civilians. If civilians harmed, Tomás turns Aggressive permanently. |
| B8 | OLD_QUARRY | Pits, rock cover | **Aisha** | **DEAD END.** Strategic. Lurks. High-value Thief gear on the node. |
| B9 | FORGOTTEN_VAULT | Sealed vault interior | — | **DEAD END.** No hero start. Shop + rare items. NPC guardians. |

**Connections:**
- B1 → B2, B3, B5
- B2 → B4
- B4 → C2, B9
- B3 → C2, C3
- B5 → B6, (B1 back-edge for Greta/Keith pursuit)
- B6 → C4, B8
- B7 → C3 (Tomás/Mei retreat path if village threatened)

---

## Region 3: The Heartland

| ID | Node | Terrain | Hero | Movement |
|----|------|---------|------|----------|
| C1 | HEARTLAND_GATE | Great wall fortress | **Yuki + Nia** | Convergence. Yuki Defensive (holds gate), Nia Strategic (retreats to C5 on approach). Rivals sharing a wall — tension dialogues. |
| C2 | SHRINE_OF_ASH | Temple, healing circles | **Brother Leo** | Territorial (sanctuary). Never retreats. Capturable strongpoint — healing node if you hold it. |
| C3 | MERCHANT_CAMP | Tents, market | **Lila** | Strategic (intelligence hub). Flees to C4 if approached directly. |
| C4 | WAR_CAMP | Military camp, palisades | **Roland** | Defensive fortress. Keith retreats here if B5 falls. Suki also regroups here. |
| C5 | SIEGEWORKS | War machines, industrial | **Wei** | Territorial (his engines). Holds until C1 falls, then retreats to C7. |
| C6 | CATHEDRAL_STEP | Cathedral plaza, holy ground | **Sister Maria** | Defensive (sacred duty). Holds. If Brother Leo corrupted, becomes **Aggressive** — hunts the player. |
| C7 | BATTLEFIELD | Scarred open field | **Rafael** | Mobile. Moves *toward* whichever adjacent node has the most heroes (he follows the drama). |
| C8 | WARLORD'S_REST | Tavern, warm interior | — | **DEAD END.** No hero start. Shop + rumor encounters. Heroes *present at adjacent nodes* may appear here in camp-like vignettes. |
| C9 | DRAGONFALL | Mountain peak, ancient bones | — | **DEAD END.** No hero start. Legendary weapon for the MC. Guardian boss fight (NPC). |

**Connections:**
- C2, C3, C4 → C1 (three-way convergence — the mid-game funnel)
- C1 → C6, C5
- C6 → C7
- C5 → C7, C9
- C4 → C8, D1 (back route — skips C7, but lightly defended? No: guarded by Roland if alive)
- C7 → D1

---

## Region 4: The Holy Reach

| ID | Node | Terrain | Hero | Movement |
|----|------|---------|------|----------|
| D1 | GODSWARD | Radiant causeway, sky exposure | — | Convergence of C7 and C4. **Trigger event:** entering D1 forces Twin Converter into Pursuit regardless of chapter counter — their back is against the Goddess's sanctum. They stop running and stand. |
| D2 | LIGHTFALL | Massive gate, waterfalls of light | **Twin Converter** | Phase-gated. TC starting position. Effectively unreachable until D1 (region gating does the avoid-phase work). |

**Connections:** D1 → D2 → E1

---

## Region 5: The Capital (Endgame, Chapters 21–23)

| ID | Node | Terrain | Heroes | Notes |
|----|------|---------|--------|-------|
| E1 | THRESHOLD | Capital plaza | All surviving uncorrupted heroes | Chapter 21. The last stand — everyone you've spared is here. |
| E2 | SANCTUM | Inner temple, radiance | Twin Converter + elites | Chapter 22. TC's last fight — unless corrupted earlier. |
| E3 | THE_GODDESS | Throne of light | The Goddess | Chapter 23. Final confrontation. Ending determined by: corrupted roster, deaths, romance, TC status. |

---

## Hero Starting Positions (Summary)

| Hero | Start | Pattern | Retreat Route |
|------|-------|---------|---------------|
| Jax | A3 | Tutorial scripted | — |
| Suki | B2 | Territorial | C1 → C4 |
| Elena | B4 | Territorial | C2 (stays with shrine) |
| Marcus | B3 | Strategic | Flanks to player's next node |
| Greta | B5 | Aggressive | Advances! C1 if unchecked |
| Keith | B5 | Aggressive | C4 (to Roland) |
| Damien | B6 | Territorial | Holds (no retreat) |
| Tomás | B7 | Defensive | C3 if village falls |
| Mei | B7 | Defensive | C3 if village falls |
| Aisha | B8 | Strategic (dead end) | Shadows player after quarry |
| Yuki | C1 | Defensive | D1 (command retreat) |
| Nia | C1 | Strategic | C5 → C7 |
| Brother Leo | C2 | Territorial (holds) | Never retreats |
| Lila | C3 | Strategic | C4 → shadows player |
| Roland | C4 | Defensive | D1 if war camp falls |
| Wei | C5 | Territorial | C7 |
| Sister Maria | C6 | Defensive | Aggressive if Leo corrupted |
| Rafael | C7 | Mobile | Follows hero density |
| Twin Converter | D2 | **Phased:** Avoid→Random→Pursuit | D1 entry forces Pursuit |

---

## Node Density Math

- 26 nodes total; one playthrough visits ~20 (3 tutorial + 17 main-game chapters)
- 6 nodes skipped per run → replay value through path divergence
- 3 dead ends (B8, B9, C8) + C9 = 4 optional detours with high-value rewards
- Skippable heroes per run: ~6 (varies by path)

---

## Design Notes

1. **Greta/Keith aggression pressure:** If the player camps or backtracks, Hollow Pass heroes advance. The tutorial's passivity is punished — the war doesn't wait.
2. **Mill Town civilians:** Optional objective. Protecting them keeps Tomás/Mei defensive (cornerable, corruptible). Harming them enrages Tomás (Aggressive, buffed stats, unrecruitable by corruption until calmed post-battle via Leo... if Leo's alive).
3. **Shrine of Ash as anchor:** Capturable healing node. Strategic reason to take the north-center path even when rushing.
4. **Warlord's Rest vignettes:** Adjacent heroes appear in non-combat scenes — rumor-delivery device for Twin Converter mystery fragments.
5. **Dragonfall:** The MC's legendary weapon (Apostle-tier). Locked behind the C5 side path, forcing a choice: siege engines (Wei) or the weapon.
6. **C4 back route:** Roland's war camp connects directly to D1 — a "honorable path" where the player fights through the fortress chain (B2→B4→C2→C3→C4→D1) facing defenders in sequence. Slow, heavily defended, but skips C1 entirely.

---

*Designed by Yrn, 2026-09-25. Caleb to review, adjust, and break as needed.*
