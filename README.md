# Tenraku (転落)

Tenraku is a light-based puzzle game in development for mobile. Its puzzles are
built on light and colour — beams, filters and the RGB/CMY colour system —
across five core puzzle types drawn from the Nikoli / Simon Tatham tradition:
Light Up, Black Box (presented in-game as "Black Lights"), Masyu,
Hashiwokakero (Bridges) and Mid-Loop.

The game is presented entirely on a phone screen: the puzzles live inside the
in-story game app, while the story of Leo — a developer whose life unravels
across a job, a merger and a firing — is told through the phone's other apps
between puzzle clusters.

## What's in this repository

This is the project's design vault and prototype library:

- `PROGRESS.md` — current design status and open questions
- `BAKEOFF-SPEC.md` — engine bake-off specification and results
- `core-library.html` / `core-five.html` — the core puzzle library and the
  five chosen puzzle types, with sourced board art in `core-library-assets/`
- `proto.html`, `proto2.html` — early playable prototypes
- `cmy-light-puzzles.html`, `actual-puzzles.html` — colour/light mechanic
  prototypes, including the prism rule (a clear prism splits white light into
  one beam per colour present; a coloured prism first absorbs its complement)
- `blackbox-toy.html` — a playable Black Box teaching board
- `dominosa-small.html` — a reserve puzzle-type prototype
- `nikoli-tatham-ip-checklist.md` — IP/fidelity notes on the puzzle sources
- `ROADMAP.md` — the Part 1 build plan

## How to view the prototypes

No build step: open any `.html` file in a web browser.

## Status

Part 1 is in design and prototyping: roughly 50 levels (about 10 per core
puzzle type) and 12 story scenes across four chapters. The planned production
engine is Unity (C#), picked from the engine bake-off in `BAKEOFF-SPEC.md`
(the same test slice built in Flutter, Unity and Godot) — a different stack
from my Godot/JavaScript projects. Browser prototyping continues while the
Unity build is set up. This repository holds the design and the browser
prototypes. See `ROADMAP.md` for the plan.

## License

MIT — see `LICENSE`.
