# ⚡ Anime Assault: NYC

**A neon-soaked twin-stick arena shooter, packed into a single HTML file.**

No build step, no dependencies, no installs — double-click `index.html` (or host it anywhere) and it runs instantly on desktop and mobile.

> The anime invaders have flooded the neon streets. You and your best friend are the city's last line of defense. Blast them back to the multiverse!

---

## 🎮 Features

- **Single-file game** — the entire game (HTML, CSS, and JavaScript) lives in one `index.html` with zero external dependencies or build tools.
- **AI companion** — a friend character fights at your side, auto-targeting the nearest enemy. If they go down, they revive automatically after a short cooldown.
- **Wave-based survival** — a fresh wave of enemies rolls in every 30 seconds, with difficulty and enemy health scaling the longer you survive.
- **Three enemy types** — basic **Chibi** grunts, fast **Sprinters** (unlocked after 15s), and tanky **Tanks** (unlocked after 40s).
- **Combo scoring** — chain kills to build a score multiplier (up to x8) before it decays.
- **Pickups** — collect hearts to heal or trigger a screen-clearing **Nova Bomb**.
- **Juicy feedback** — screen shake, hit-stop, particle bursts, muzzle flashes, and a parallax neon NYC skyline.
- **Synthesized audio** — all sound effects are generated in real time with the Web Audio API (no audio files needed), plus a mute toggle.
- **Local Hall of Fame** — your top 8 high scores are saved in the browser via `localStorage`.
- **Fully responsive** — desktop mouse/keyboard controls and dual virtual joysticks for touch devices, with safe-area support for notched phones.

## 🕹️ How to Play

Just open the game — no setup required:

1. Clone or download this repository.
2. Open `index.html` in any modern browser (double-click it, or drag it into a browser window).

To run it from a local server instead (useful for some browsers' autoplay/audio policies):

```bash
git clone https://github.com/RuHRabin/Anime-Assault-Game.git
cd Anime-Assault-Game
python3 -m http.server 8000
# then visit http://localhost:8000 in your browser
```

You can also enable **GitHub Pages** on this repo (Settings → Pages → deploy from `main`) to play it directly from a public URL.

## 🎯 Controls

| Action | Desktop | Touch |
|---|---|---|
| Move | `WASD` or Arrow keys | Left thumb — virtual joystick |
| Aim | Mouse | Right thumb — virtual joystick |
| Fire | Click or `Space` | Right thumb (moving the aim stick fires) |
| Pause | `P` or `Esc` | Pause button (top-right) |
| Mute | `M` | Mute button (top-right) |
| Restart | `R` | Restart button on Game Over screen |

## 👾 Enemies

| Type | Behavior | Unlocks |
|---|---|---|
| **Chibi** | Standard grunt, moderate HP and speed | From the start |
| **Sprinter** | Low HP, but fast and erratic | After 15 seconds |
| **Tank** | High HP, slow, hits hard | After 40 seconds |

Enemy health scales up the longer a run goes on, and spawn rate increases over time, so survival gets progressively tougher.

## ✨ Scoring & Pickups

- Killing enemies builds a **combo**; every 5 kills increases your score multiplier, up to **x8**. The combo resets if you go a few seconds without a kill.
- Defeated enemies have a chance to drop a pickup:
  - ❤️ **Heart** — restores HP.
  - 💥 **Nova Bomb** — damages every enemy on screen.
- Final score, wave reached, kill count, and best combo are shown on the Game Over screen, and your best runs are saved to the local leaderboard.

## 🛠️ Tech Stack

- **Vanilla JavaScript** — no frameworks or libraries.
- **HTML5 Canvas** — for all rendering (background, characters, bullets, particles, UI effects).
- **Web Audio API** — procedurally generated sound effects.
- **`localStorage`** — persists local high scores between sessions.

## 📁 Project Structure

```
Anime-Assault-Game/
├── index.html   # The entire game — markup, styles, and logic
└── LICENSE      # MIT license
```

## 📄 License

Released under the [MIT License](LICENSE).
