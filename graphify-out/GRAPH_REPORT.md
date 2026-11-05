# Graph Report - happy-birthday  (2026-11-05)

## Corpus Check
- Corpus is ~5,045 words - fits in a single context window. You may not need a graph.

## Summary
- 32 nodes · 40 edges · 7 communities (5 shown, 2 thin omitted)
- Extraction: 98% EXTRACTED · 2% INFERRED · 0% AMBIGUOUS · INFERRED: 1 edges (avg confidence: 0.75)
- Token cost: 69,227 input · 0 output

## Community Hubs (Navigation)
- Celebration Effects
- Candles, Mic & Music
- Particle Engine & Reasons
- Story Flow & Finale Heart
- Page Overview
- Love Letter
- Canvas Sizing

## God Nodes (most connected - your core abstractions)
1. `parts particle array` - 6 edges
2. `firework()` - 6 edges
3. `openGift()` - 5 edges
4. `celebrate()` - 5 edges
5. `COLORS palette` - 4 edges
6. `confetti()` - 4 edges
7. `heartBurst()` - 4 edges
8. `balloons()` - 4 edges
9. `toggleMusic()` - 4 edges
10. `show() screen switcher` - 4 edges

## Surprising Connections (you probably didn't know these)
- `confetti()` --shares_data_with--> `parts particle array`  [EXTRACTED]
  index.html → index.html  _Bridges community 2 → community 0_
- `heartParticles()` --shares_data_with--> `parts particle array`  [EXTRACTED]
  index.html → index.html  _Bridges community 2 → community 3_
- `firework()` --implements--> `Parametric heart curve`  [EXTRACTED]
  index.html → index.html  _Bridges community 0 → community 3_
- `writeLetter()` --calls--> `firework()`  [EXTRACTED]
  index.html → index.html  _Bridges community 0 → community 5_
- `blow() candle` --calls--> `heartBurst()`  [EXTRACTED]
  index.html → index.html  _Bridges community 2 → community 1_

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Canvas particle system sharing parts array** — index_parts, index_loop, index_confetti, index_firework, index_heartburst, index_heartparticles, index_sparkle_trail [EXTRACTED 1.00]
- **Interaction-gated screen progression** — index_intro, index_opengift, index_blow, index_celebrate, index_reason_cards, index_openenvelope, index_writeletter, index_show [INFERRED 0.85]
- **Personalisation constants** — index_intro_const, index_words, index_reasons, index_message [EXTRACTED 1.00]

## Communities (7 total, 2 thin omitted)

### Community 0 - "Celebration Effects"
Cohesion: 0.36
Nodes (6): balloons(), celebrate(), COLORS palette, confetti(), firework(), openGift()

### Community 1 - "Candles, Mic & Music"
Cohesion: 0.33
Nodes (6): blow() candle, Mic blow detector, playSong(), SONG note table, toggleMusic(), WORDS (one per candle)

### Community 2 - "Particle Engine & Reasons"
Cohesion: 0.33
Nodes (6): heartBurst(), loop() render loop, parts particle array, Reason flip cards, REASONS, Pointer sparkle trail

### Community 3 - "Story Flow & Finale Heart"
Cohesion: 0.40
Nodes (5): Parametric heart curve, heartParticles(), intro(), INTRO lines, show() screen switcher

### Community 4 - "Page Overview"
Cohesion: 0.67
Nodes (3): Happy Birthday interactive page, prefers-reduced-motion support, Six-screen story flow (intro, surprise, cake, reasons, letter, finale)

## Knowledge Gaps
- **10 isolated node(s):** `INTRO lines`, `WORDS (one per candle)`, `REASONS`, `MESSAGE (love letter text)`, `resize() canvas` (+5 more)
  These have ≤1 connection - possible missing edges. (Counts symbols only; 13 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `firework()` connect `Celebration Effects` to `Particle Engine & Reasons`, `Story Flow & Finale Heart`, `Love Letter`?**
  _High betweenness centrality (0.261) - this node is a cross-community bridge._
- **What connects `INTRO lines`, `WORDS (one per candle)`, `REASONS` to the rest of the system?**
  _10 weakly-connected nodes found - possible missing edges._
- **Why does `parts particle array` connect `Particle Engine & Reasons` to `Celebration Effects`, `Story Flow & Finale Heart`?**
  _High betweenness centrality (0.176) - this node is a cross-community bridge._
- **Why does `openGift()` connect `Celebration Effects` to `Candles, Mic & Music`, `Particle Engine & Reasons`, `Story Flow & Finale Heart`?**
  _High betweenness centrality (0.158) - this node is a cross-community bridge._