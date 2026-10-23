# Tenraku — Part 1 Roadmap

Part 1 scope: ~50 levels (~10 per core puzzle type), ~12 story scenes across
four chapters (The Job, The Merger, The Firing, The Dark), 3–4 hours of play,
paid mobile release. The scene at 3:32 AM bookends the beginning and the end.

## Design (this repository)

- [ ] Map the five core puzzle types onto the four chapters
- [ ] Finish the level-design pass for each type: 2 teaching / 4 working /
      2 remix / 2 mastery levels per type
- [ ] Verify every generated Black Lights layout: every hidden light can
      affect a beam, and a strong solve fits the probe allowance
- [ ] Lock the prism-mechanic level set (clear vs coloured prisms, decoys,
      gates, feed-the-prism colour control)
- [ ] Finalise the 12 scene scripts as phone-app sequences (Messages, Mail,
      Calendar, Photos)

## Build (production engine not yet chosen)

- [ ] Decide the production engine: complete the bake-off in
      `BAKEOFF-SPEC.md` (same test slice in Flutter, Unity and Godot;
      prototyping currently iterates in Flutter while the decision is open)
- [ ] Phone home screen and app shell (Tenraku app icon, scripted
      notification banners that gate progress between clusters)
- [ ] Playable implementations of the five core puzzle types
- [ ] Level/cluster flow with scene transitions (ordinary app open/close)
- [ ] Diegetic music via Leo's music app as the soundtrack
- [ ] Save/progress system for Part 1

## Polish and release prep

- [ ] Playtest rounds per chapter; difficulty pass on prism levels
- [ ] Icon/screenshot pass; store listing for a Part 1 release
