# 🦖 Custom Sound Dino Runner

A lightweight, browser-based 2D endless runner built with **vanilla JavaScript** and **HTML5 Canvas**, inspired by Chrome's classic offline Dino game. It supports custom sound effects loaded directly from `.mp4` files!

This repository hosts two versions of the runner as separate pages:

| Page | Description | Live URL |
| :--- | :--- | :--- |
| **Classic Dino** ([index.html](index.html)) | The original block-sprite runner with custom `.mp4` jump/crash sounds. | https://tddf-ua.github.io/dino-runner/ |
| **Mochi Backyard Runner** ([mochi/index.html](mochi/index.html)) | A reskin starring Mochi the calico cat running through a backyard, dodging potted plants and hanging figs. | https://tddf-ua.github.io/dino-runner/mochi/ |

---

## 🚀 Classic Dino: Features

* **Physics Engine**: Smooth gravity and jumping mechanics.
* **Dynamic Obstacles**: Randomized ground-level cactuses and flying pterodactyls.
* **Progressive Difficulty**: Game speed automatically increases as your score builds.
* **Custom Audio Effects**: Native browser audio handling using custom `.mp4` clips for jump and game-over triggers.
* **Zero Dependencies**: Pure HTML5, CSS3, and JS—no frameworks or build tools required.

---

## 🎮 Controls

| Action | Key Input |
| :--- | :--- |
| **Jump** | `Spacebar` or `Up Arrow` (`↑`) |
| **Restart Game** | `Spacebar` or `Up Arrow` (`↑`) on Game Over |

---

## 📁 Repository Structure

To ensure sound effects load correctly, maintain the following directory layout:

```text
dino-runner/
├── index.html       # Combined HTML, CSS, and JS game engine
├── jump.mp4         # Audio/video clip triggered on jump
└── crash.mp4         # Audio/video clip triggered on collision
```

**Note on Audio Paths:**
If you move audio files to a subfolder (e.g., `assets/`), update the audio setup lines in `index.html`:

```javascript
const jumpSound = new Audio('assets/jump.mp4');
const crashSound = new Audio('assets/crash.mp4');
```

## 🛠️ Local Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/TDDF-UA/dino-runner.git
   cd dino-runner
   ```

2. **Run the Game**
   * Double-click `index.html` to open it directly in any modern web browser.
   * *(Optional)* Serve using VS Code's **Live Server** extension or Python's HTTP server:
     ```bash
     python -m http.server 8000
     ```

## 🎙️ Replacing Sound Effects

You can replace the sound effects with your own recorded voices or sound clips:

1. Record short sound effects on your device.
2. Save/export the clips as **jump.mp4** and **crash.mp4**.
3. Place them in the same directory as `index.html`.
4. Refresh the browser page to play with your new sounds!

## 💡 Future Improvements (Roadmap)

Feel free to fork this repository and submit Pull Requests! Here are some fun ideas to add:

* [ ] Add duck/crouch mechanic (Down Arrow) for dodging high-flying pterodactyls.
* [ ] Save high scores across sessions using localStorage (already implemented in the Mochi Backyard Runner page below).
* [ ] Replace canvas vector rectangles with custom pixel-art sprites.
* [ ] Add day/night cycle backgrounds based on high scores.

---

## 🐱 Mochi Backyard Runner

An 8-bit retro side-scroller reskin of the classic runner, starring Mochi the calico cat running through a backyard. Lives at [`mochi/index.html`](mochi/index.html), served as its own page at https://tddf-ua.github.io/dino-runner/mochi/.

### Features

* **Custom Pixel-Art Sprites**: Mochi running (2-frame cycle) and jumping poses, potted plant obstacles (basil, roses, lavender), a fig tree with hanging figs, and a scrolling backyard background.
* **Mobile & Touch Support**: Tapping the canvas jumps or restarts the game; `touch-action: none` and `preventDefault()` stop unwanted scrolling/zooming while playing on a phone.
* **Responsive Scaling**: Canvas scales fluidly to fit the screen while preserving its 3:1 aspect ratio, including a native Fullscreen Mode toggle.
* **Persistent High Score**: Best score is saved across sessions via `localStorage` (`mochi_runner_highscore`).
* **Transparent Sprites**: Near-white pixels (RGB > 215) in the sprite PNGs are converted to transparent alpha at load time in-browser, so no pre-processing step is required to view the game — though a standalone `fix_sprites.py` (Python + Pillow) exists for baking transparency into the source PNGs directly, for anyone editing the art assets.

### Directory Layout

```text
dino-runner/
└── mochi/
    ├── index.html            # Mochi game engine, styles, and logic
    ├── Mochi_background.png  # Seamless scrolling backyard background
    ├── Mochi_run1.png        # Mochi running frame 1
    ├── Mochi_run2.png        # Mochi running frame 2
    ├── Mochi_jump.png        # Mochi jumping pose
    ├── Mochi_basil.png       # Potted Basil obstacle
    ├── Mochi_roses.png       # Potted Roses obstacle
    ├── Mochi_lavender.png    # Potted Lavender obstacle
    ├── Mochi_figtree.png     # Background Fig Tree
    └── Mochi_fig.png         # Hanging Fig obstacle
```

Note: this version of the game plays silently — it does not use the `jump.mp4`/`crash.mp4` audio effects from the classic page.

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more details.

## 🕹️ Live Demos

* Classic Dino: https://tddf-ua.github.io/dino-runner/
* Mochi Backyard Runner: https://tddf-ua.github.io/dino-runner/mochi/
