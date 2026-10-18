# Space Cab for CHGame

Space Cab, Vampirics and filmote's Pokitto tribute to *Space Taxi*, ported
to the CHGame handheld: fly your cab between the platforms, pick up the
fares and drop them off, and watch your fuel.

## Controls

| Button | Action |
|---|---|
| A | Thruster |
| B | Landing gear |
| LEFT / RIGHT | Steer |
| START | Pause; hold 3 s for the CHGame menu |

## Building

Needs Python 3 (with Pillow and ziglang, for the simulator), arduino-cli and
the CHGame board package, as any CHGame game (`chgame/tools/README.md`).
`cl` (Git Bash) and `cl.cmd` (Windows) run the vendored CHGame tools on the
sketch:

| Command | What |
|---|---|
| `./cl build` | the release image |
| `./cl upload` | onto the board |
| `./cl run SpaceCab/tools/scripts/smoke.txt out/smoke` | a script in the simulator |
| `./cl test` / `./cl check` | the host tests / everything that needs no board |

## Credits and licence

- **The game:** [Space Cab](https://github.com/Press-Play-On-Tape/SpaceCab_Pokitto)
  for the Pokitto, graphics by Vampirics and code by filmote (Press Play On
  Tape), with thanks to Pharap. It is free software under the
  **GNU General Public License v3**, and so is this port: see
  [LICENSE](LICENSE) and [SpaceCab/NOTICE](SpaceCab/NOTICE).
  `SpaceCab/src/game/` holds the game's sources, changed for CHGame (each
  change is commented), and its levels come from the SpaceCab_V1.0.2
  release.
- **Font:** `SpaceCab/src/game/Font3x5.cpp` is the Pokitto library's
  font3x5 (Aurélien Rodot's Gamebuino font, LGPL 3).
- **Not included:** the Pokitto version's recorded voices and theme tune.
  CHGame's piezo plays short tones in their place.
- **The CHGame libraries and tools** in `chgame/` are under their own
  GPL-compatible licences ([chgame/LICENSE](chgame/LICENSE),
  [chgame/NOTICE](chgame/NOTICE)).

*Space Taxi* (1984) is John F. Kutcher's. This port is unofficial and not
endorsed by the original authors.
