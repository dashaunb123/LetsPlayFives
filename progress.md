Original prompt: when a player pack is opened show the starting lineup at the top when its time to pick so the user has a good idea of what to pick

- Added a compact `CURRENT STARTERS` panel to the pack modal and only surface it during the player-pack pick phase.
- Hid the reel once a player-pack result lands so the lineup sits at the top during the actual decision step.
- Added hover highlighting so mousing over a draft option lights up the matching starter slot by position.
- Changed the player-pack burst handoff so the five cards stay in their fanned spread, flip over in place, and can be picked directly from that burst layout.
- Reverted the later starter-panel graphic redesign and kept the simpler compact lineup strip.
- Shifted the player-pack fan downward when the starters panel is visible so the pick cards stop covering that UI.
- Tightened the pack-rip burst by hiding the torn flap after the rip completes and shortening the pack linger/explode timing.
- Rebuilt the burst pack as separate wrapper pieces (lower shell + opened mouth cavity + flap) so the rip reads like a physical pack instead of one flat rectangle.
- Simplified the season recap to record, total cash accumulated, packs opened, and the final lineup, and added a lifetime cash-earned tracker for the recap.
- Added looping background music from `LP5SOUNDTRACK.mp3` that starts when a run begins and stops at the season recap/main menu.
- Hardened soundtrack startup so the game uses a hidden audio element, waits for the Web Audio context to resume before `play()`, and falls back cleanly if the lowpass graph cannot be created.
- Added a tense reel end-phase: the rarity wheel slowly zooms in, the surrounding modal blurs instead of the wheel itself, and the soundtrack lowpasses as the result approaches.
- Removed the soundtrack lowpass/filter layer entirely after it interfered with playback; the wheel tension beat now keeps the zoom/blur visuals while music stays plain looping audio.
- Did a code-level sanity check only; no browser automation was run because testing was not requested.
