# Gorillas: Reborn

## What this is

A faithful, self-contained recreation of the classic **QBasic `GORILLAS.BAS`**
(1991) — the exploding-banana artillery duel that shipped with MS-DOS 5. Two
gorillas stand atop a randomly generated city skyline and lob explosive bananas
at each other; you pick an **angle** and a **velocity**, mind the wind, and try to
knock the other gorilla off the rooftops. And yes — you can bonk the sun.

It runs entirely in the browser with no build step, no dependencies, and no
network calls. Everything on screen — the skyline, the gorillas, the tumbling
banana, the reactive sun — is drawn at runtime with canvas primitives.

## What this is not

- **Not a copy of Microsoft's game.** No original code, art, text, or assets.
  Every line and every drawing here is original, inspired by the 1991 game and the
  early-PC era. See the trademark note in `LICENSE`.
- **Not multiplayer over a network.** Two players share one keyboard (hotseat), or
  you play against a built-in computer opponent.
- **Not online, and nothing to install.** One file, one browser, no accounts, and
  no data leaves the machine.

## At a glance

| | |
|---|---|
| **Type** | Turn-based artillery duel |
| **Players** | 2 hotseat, or 1 vs. the computer |
| **Physics** | Angle/velocity aiming, gravity, per-round wind |
| **Skyline** | Randomly generated and fully destructible |
| **Gravity** | Selectable — Moon, Earth, Jupiter |
| **Match length** | First to N rounds (1–9) |
| **Facts panel** | 52 rotating retro-computing facts |
| **Session length** | ~5–15 minutes per match |
| **Tech** | Vanilla HTML/CSS/JS + canvas. No build, no dependencies |
| **Port** | 8000 |

## Features

- **Destructible skyline.** A randomly generated city each round; explosions punch
  real craters into the buildings, changing the board as you duel.
- **Real projectile physics.** Angle and velocity aiming, gravity, and a per-round
  wind (shown by the arrow along the baseline) that curves the banana in flight.
- **A live aim indicator** that shows your angle before you fire, plus the reactive
  sun that ducks and gapes when you hit it.
- **Pixel gorillas** with a ready-arm aiming pose and the traditional arms-up
  victory dance.
- **A beatable computer opponent** that simulates shots and tightens its aim after
  each miss — or **hotseat 2-player** for two people at one keyboard.
- **Selectable gravity** (Moon / Earth / Jupiter) and match length (first to 1–9).
- **A "Did You Know?" panel** that rotates through 52 facts about QBasic, MS-DOS,
  pre-Windows PCs, early microprocessors, and 4/8-bit game consoles.

## How to use it

1. Open the game and choose your opponent (the computer or a second player), the
   gravity, and how many rounds it takes to win.
2. On your turn, set the **Angle** and **Velocity** sliders — the dashed arrow
   shows where you're aiming — and watch the wind arrow at the bottom.
3. Press **Fire!** (or **Enter**) to lob the banana. Land it on the other gorilla
   to win the round.
4. Buildings crater where bananas land, reshaping the skyline. First to the target
   number of rounds wins the match.

**Controls** — Angle and Velocity sliders, then **Fire!** or press **Enter**.

## Run it locally

From the repository folder:

```
python -m http.server 8000
```

Then open **http://localhost:8000**. Any static file server works — or just open
`index.html` directly in a browser. There is no build step and nothing to install.

## Project structure

```
gorillas/
├── index.html   The entire game — physics, rendering, AI, UI, and the facts panel
├── README.md
└── LICENSE
```

Everything lives in one self-contained `index.html`: the projectile physics and
destructible terrain, the pixel sprites, the computer opponent, the interface, and
the rotating retro-computing facts.

## License

Dual-licensed — MIT for the code, CC BY-NC-SA 4.0 for the written game content.
See [LICENSE](LICENSE), including the trademark note on "QBasic", "GORILLAS", and
"MS-DOS".
