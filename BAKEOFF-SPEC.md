# Engine Test — Exact Build Spec (agreed 2026-10-21)

Every engine (Godot, Unity, Flutter) builds THIS, identically. Judged on: build time,
AI mistakes to fix, animation feel, and look (crisp text, board glow in the dark).

## The flow
1. Leo's phone (home screen). Player taps the **Tenraku** app icon → app opens.
2. Black Box board (below). Player fires the two scripted probe shots.
3. Player finishes → **notification banner** drops over the app. It cannot be
   dismissed or skipped; tapping it is the only way forward.
4. Banner tap → out to the phone, first scene plays in Messages (Sarah, the good
   morning). Scene completes → back to the phone; Tenraku icon ready to relaunch.

## The exact puzzle — Black Box, "L"
- **Board: 8×8.** Rows numbered 1–8 top→bottom, columns 1–8 left→right.
  32 rim firing points (8 per side).
- **5 hidden motes**, placed to spell an **L** — vertical bar of four in column 3,
  foot pointing right at the bottom:
  **(3,3), (4,3), (5,3), (6,3), (6,4)** in (row, column).

```
col:   1 2 3 4 5 6 7 8
row 1  . . . . . . . .
row 2  . . . . . . . .
row 3  . . ● . . . . .
row 4  . . ● . . . . .
row 5  . . ● . . . . .
row 6  . . ● ● . . . .
row 7  . . . . . . . .
row 8  . . . . . . . .
```

## Scripted probe shots (machine-verified with the canonical ray walk)
1. **Top, column 3** → straight down the bar → **H** (absorbed by the mote at (3,3)).
2. **Top, column 2** → travels down column 2, bends 90° left at the corner of the
   (3,3) mote → **exits Left, row 2**. (The signature corner-deflection.)

## Full outcome table for this layout (all 32 entries, verified)
Notation: T/B/L/R + number = rim point (e.g. T3 = top column 3, L2 = left row 2).
- **Hits (10):** T3, B3, B4, L3, L4, L5, L6, R3, R4, R6
- **Deflected (5 pairs, 10 entries):** T2↔L2, T4↔R2, T5↔R5, B2↔L7, B5↔R7
- **Straight through (6 pairs, 12 entries):** T1↔B1, T6↔B6, T7↔B7, T8↔B8, L1↔R1, L8↔R8
- **Reflections (0):** this layout produces no R results.

## Scene content for step 4 (from the GDD's Stage 1 "Spark", content reused,
structure is the new one): Sarah's message — *"We're pregnant! 💕 Can't wait to
tell our families tonight."* — plus the ultrasound photo in the phone and the
calendar item *4:00 PM Hackathon AI Demo*. Phone state: bright morning, 100% battery.
