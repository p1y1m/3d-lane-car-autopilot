# 3D Lane Car Autopilot (Three.js)

**Author:** Pedro Yanez Melendez  

## Overview
A **responsive 3D lane-based car game** built with **Three.js**, featuring **manual driving** and a **robust rule-based autopilot** that avoids obstacles reliably in real time.  
Playable on **desktop, tablet, and mobile** via GitHub Pages.

> ⚠️ This project uses a **deterministic autopilot (rules + geometry)**.  
> It does **not** include reinforcement learning or model training.

---

## Live Demo
👉 https://p1y1m.github.io/3d-lane-car-autopilot/

---

## Features
- Manual & Auto modes (toggle at runtime)
- Strong obstacle avoidance without ML
- Speed control (0–100)
- Responsive UI (desktop, iPad, mobile)
- Single-file deployment (`index.html`)
- No backend, no build tools

---

## Controls

### Desktop
- Left / Right: change lane (Manual)
- Up: increase speed (Manual & Auto)
- R: restart after crash

### Mobile / Tablet
- ⬅ / ➡: change lane (Manual)
- ⬆: increase speed
- Tap screen: restart after crash

---

## Autopilot Logic (High Level)
The Auto mode uses:
- Lane awareness (3 fixed lanes)
- Nearest obstacle per lane
- Time-to-collision heuristics
- Safe-lane selection with hysteresis
- Debounced lane switching

This rule-based approach outperforms basic RL in this environment because it is fully observable, deterministic, and low-dimensional.

---

## Tech Stack
- JavaScript (ES Modules)
- Three.js
- HTML + CSS
- GitHub Pages

---

## Repository Structure
/
├── index.html   # Entire game (logic + rendering + UI)
└── README.md

---

## Deployment (GitHub Pages)
1. Upload `index.html` to repository root
2. Go to Settings → Pages
3. Source: main branch / (root)
4. Open the generated GitHub Pages URL

---

## Why No Reinforcement Learning?
For this problem:
- Rules are simpler
- Behavior is predictable
- Performance is better and more stable
- No training, no tuning, no policy export

RL would be useful only for partial observability, noisy perception, or complex dynamics.

---

## License
MIT — free to use, modify, and deploy.
