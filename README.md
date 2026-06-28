<div align="center">

# ✦ LUMINARY

### *Weave Light With Your Hands*

> A real-time hand-tracking art experience built entirely in the browser. No installs. No frameworks. Just your hands and light.

</div>

---

## ✨ What Is Luminary?

**Luminary** is an interactive, browser-based art tool that uses your webcam and hand-tracking to let you paint, weave, and sculpt with light — in real time. Pick a mode, raise your hands, and watch the magic happen.

It uses [MediaPipe Hands](https://mediapipe.dev/) for precise finger landmark detection and HTML5 Canvas for all rendering. Zero dependencies, zero backend — just one HTML file.

---

## 🎮 Modes

### 🕸 Neural Web
Physics-driven glowing strings connect your fingertips across both hands. The strings vibrate, bounce, and shimmer based on how fast you move — the faster you wave, the more the strings ripple. Sparks trail from your fingertips as you move through the air.

### ✦ Mirror Draw
Paint with light in the air using your index finger. Your left hand is mirrored symmetrically across the canvas, creating perfect neon mandalas and patterns. Gesture controls let you clear the canvas or cycle colors without touching anything.

**Gestures:**
- ✊ **Pinch** — Clear the canvas
- ✌️ **Peace sign** — Cycle to the next color

### 🌊 Fluid Ink 
Your fingers disturb a living ink simulation. Every fingertip spawns glowing vapor particles that drift, curl, and dissipate like luminous smoke in liquid — driven by a curl noise field.

---

## 🎨 Controls

| Control | Action |
|---|---|
| Color swatches | Pick a base color |
| **MULTI** toggle | Enable rainbow multicolor mode |
| Size slider | Adjust brush / string thickness |
| **CLEAR** | Wipe the canvas |
| **SAVE** | Download the current frame as a PNG |
| **EXIT** | Return to mode selection |

---

## 🚀 Getting Started

### Option 1 — Live (No Setup)
Just open the deployed GitHub Pages link:
**[bhavikaa-guptaa.github.io/Luminary](https://bhavikaa-guptaa.github.io/Luminary/)**

### Option 2 — Run Locally
```bash
git clone https://github.com/bhavikaa-guptaa/Luminary.git
cd Luminary
# Open index.html in any modern browser
open index.html
```

> **Note:** Camera access requires HTTPS or localhost. If opening directly from the filesystem doesn't work, serve it locally:
> ```bash
> python3 -m http.server 8080
> # Then visit http://localhost:8080
> ```

---

## 🛠 Tech Stack

| Technology | Role |
|---|---|
| **MediaPipe Hands** | Real-time hand landmark detection (21 points per hand) |
| **HTML5 Canvas** | Triple-layered rendering (draw, trail, overlay) |
| **WebGL / Canvas 2D** | Gradient rendering, composite blend modes |
| **Orbitron + Share Tech Mono** | Cyberpunk HUD typography |
| **Vanilla JS** | Physics simulation, particle systems, gesture recognition |

---

## 🏗 Architecture

Luminary uses **three stacked canvas layers** for efficient rendering:

```
┌─────────────────────────────────┐
│  overlay-canvas  (z:4)          │  ← Live fingertip cursors, anchors, sparks
│  trail-canvas    (z:3)          │  ← Motion trails (reserved)
│  draw-canvas     (z:2)          │  ← Persistent art (strings, ink, drawings)
│  <video>         (z:1)          │  ← Mirrored webcam feed
└─────────────────────────────────┘
```

String physics uses a spring simulation per pair of connected fingertips — each string has two independent control points with velocity, damping, and impulse response to hand movement speed.

---

## 📸 Screenshots

| Neural Web | Mirror Draw | Fluid Ink |
|---|---|---|
| Glowing strings between fingertips | Symmetric neon mandala painting | Vapor trails drifting in curl noise |

---

## 🔒 Privacy

Luminary runs **entirely in your browser**. No video, images, or hand data are ever sent to any server. All processing happens locally on your device in real time.

---

## 🤝 Contributing

Contributions, ideas, and new mode suggestions are welcome! Feel free to open an issue or submit a pull request.

---

## 📄 License

MIT License — free to use, modify, and share.

---

<div align="center">

Made with ✦ and a lot of neon glow

*raise your hands and let there be light*

</div>
