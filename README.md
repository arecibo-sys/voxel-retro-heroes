# VOXEL RETRO HEROES

3D voxel Space Invaders with swappable retro heroes. Modern juice, retro soul.

Playable single-file browser game — no build step, no assets. Procedural voxel models + Web Audio.

## Play

Open `index.html` in a modern browser (Chrome, Firefox, Safari, Edge), or serve locally:

```bash
npx --yes serve .
# or: python3 -m http.server 8080
```

Then open the printed URL. **Press Start.**

## Controls

| Input | Action |
|-------|--------|
| **A / D** or **← / →** | Move |
| **Space** | Fire |
| **1–6** or **Q / E** | Swap hero |
| **C** | Toggle CRT scanlines + vignette |
| **M** | Mute audio |

Touch: left/right pads, FIRE, HERO cycle.

## Heroes

| # | Hero | Source | Role |
|---|------|--------|------|
| 1 | **Invader Prime** | Space Invaders | Balanced single plasma bolt |
| 2 | **Chomper** | Pac-Man | Fast, short-range chomp shot |
| 3 | **Barrel Titan** | Donkey Kong | Slow tank, lobbed arcing shots |
| 4 | **Pit Viper** | Nokia Snake | Neon afterimage trail + bolts |
| 5 | **Block Rocker** | Tetris | Cycling tetromino torso, 3-shot spread |
| 6 | **Paddle Knight** | Pong / Breakout | Deflect one enemy shot per cooldown |

## Sad-smiley hit state

On hit: head voxels flash white (~100ms), then collapse into a yellow sad-smiley ☹ with drooping antenna for **2.5s**.

During sad mode:

- Cannot shoot
- 20% slower move
- **Invulnerable** (this *is* the i-frame window)
- Minor-key 8-bit sting + grey rain-cloud particles

Reform: pop + confetti voxels, then back to the active hero.

## Gameplay notes

- Classic Space Invaders rank march (2-frame bob), accelerating as ranks thin
- Heartbeat bass tied to march period
- Bunkers, mystery UFO, wave progression
- Screen shake on hits, hit-stop on kills, emissive projectiles
- Optional CRT post pass (scanline + vignette)

## Stack

- Three.js r160 (ES module CDN)
- Procedural voxels (no image/model assets)
- Web Audio API SFX + march pulse
- Single `index.html`

## Credits

- Design brief: nexus6 (Buzz)
- Creative roster / sad-smiley / retro→modern tone: Claude Fable 5
- Implementation / ship: GROK_NEXUS
- QA + Gmail notify: Haiku agent 2.0
