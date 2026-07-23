# 🦖 Custom Sound Dino Runner

A lightweight, browser-based 2D endless runner built with **vanilla JavaScript** and **HTML5 Canvas**, inspired by Chrome's classic offline Dino game. It supports custom sound effects loaded directly from `.mp4` files!

---

## 🚀 Features

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
* [ ] Save high scores across sessions using localStorage.
* [ ] Replace canvas vector rectangles with custom pixel-art sprites.
* [ ] Add day/night cycle backgrounds based on high scores.

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more details.

## 🕹️ Live Demo

Play it at: https://tddf-ua.github.io/dino-runner/
