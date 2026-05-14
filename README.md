# Stinger Protocol 

A high-speed, zero-dependency HTML5 arcade shooter featuring time-dilation mechanics, procedural deep-space environments, and a heavy emphasis on "game feel." 

Built entirely in vanilla JavaScript using the HTML5 Canvas API, this project serves as an exercise in building highly optimized, garbage-collection-free game loops and custom physics engines from scratch without relying on heavy frameworks like Unity or Godot.

## ✨ Core Features

* **Time Dilation (Chronos System):** A custom physics time-scale implementation. Successfully parrying projectiles slows the global engine tick rate to 15% while allowing the player to move at 50% speed, creating tactical "bullet time" windows.
* **Zero-Garbage Object Pooling:** Uses O(1) round-robin object pools for hundreds of projectiles, particles, and enemies to ensure a locked 60 FPS without browser garbage collector stuttering.
* **Procedural Environments:** Dynamically renders parallax celestial bodies (gas giants, nebulas, dying suns) and drifting space debris completely through math and canvas composite operations—no external image assets required.
* **Twin-Stick & Touch Support:** Fully responsive control schemes featuring WASD + Mouse for desktop, and multi-touch virtual analog sticks for mobile devices.
* **Dynamic Wave Scaling:** An escalating threat director that spawns 7 distinct enemy "Xenotypes" (Hives, Pulsars, Phantoms) with unique trigonometric movement and attack patterns.

## 🎮 Controls

**Desktop (Keyboard & Mouse):**
* **WASD:** Move Ship
* **Mouse:** Aim
* **Left Click:** Fire Weapon
* **Right Click:** Deploy Parry Shield
* **Spacebar:** Phase / Dodge (I-Frames)

**Mobile (Touch):**
* **Left Half of Screen:** Drag to Move (Virtual Analog)
* **Right Half of Screen:** Drag to Aim & Fire (Virtual Analog)
* **Bottom Left / Right Corners:** Tap to Dodge / Parry

## 🛠️ Technical Implementation

This game was built to explore native browser rendering limitations and custom math-based animation. 

* **Rendering:** `CanvasRenderingContext2D` with heavy use of `globalCompositeOperation` and `shadowBlur` for glowing neon aesthetics.
* **Math & Movement:** Uses `Math.atan2` for precise directional aiming and trigonometric functions (`Math.sin`, `Math.cos`) for organic enemy movement patterns, procedural chain-lightning calculations, and particle drift.
* **State Management:** Custom finite state machines handling player i-frames, weapon cooldowns, and enemy staggering.

## 🚀 How to Play

No build steps, no dependencies, no server required. 

1. Clone or download this repository.
2. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3. Click **Start Journey** to begin the game loop.
