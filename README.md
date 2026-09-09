# 3D Painter
 
![Three.js](https://img.shields.io/badge/Three.js-black?logo=three.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-blue)
 
A lightweight, kid-friendly texture painting tool built with [Three.js](https://threejs.org/). It loads a single 3D model (a cannon) as a plain grey mesh and lets users paint directly on its surface using a brush, eraser, paint bucket, and color wheel — all running in the browser, no installation required.
 
🔗 **Live demo:** [gabrielpradovieira.github.io/3D-Painter](https://gabrielpradovieira.github.io/3D-Painter/)
 
---
 
## Features
 
- **Brush / Eraser** — three hardness levels (hard, mid, soft)
- **Paint Bucket** — Full Object, Face, or UV Shell fill modes
- **Color Wheel** — hue ring + saturation/value triangle, plus a color picker (eyedropper)
- **Undo** — up to 10 steps (`Ctrl+Z`)
- **Backface-aware painting** — strokes never bleed through to hidden surfaces
## Controls
 
| Input | Action |
|---|---|
| LMB / touch | Paint |
| RMB | Orbit |
| MMB | Pan |
| Scroll / pinch | Zoom |
| `Ctrl+Z` | Undo |
| `R` | Reset camera |
 
## Getting Started
 
### Run locally
 
From the project folder, run:
 
```
serve-local.bat
```
 
(or `.claude/serve.ps1` if Python isn't installed). This starts a local server at:
 
```
http://127.0.0.1:3000/
```
 
> Keep the terminal window open while testing — closing it stops the server.
 
> ⚠️ Do not open `index.html` directly via `file://` — browsers block model loading that way. A local server or static host is required.
 
### GitHub Pages Deployment
 
This project runs directly from GitHub Pages:
 
1. Push your changes to the repository.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder.
5. Save.
## Model
 
The app loads a single FBX model from the repository:
 
```
models/model7/cannon_lp.fbx
```
 
Keep the file in this path, or update `MODEL_CONFIG` in `index.html`.
 
## Project Structure
 
```
.
├── .claude/       # Local server scripts and Claude-related configs
├── curves/        # Animation curve presets
├── images/        # Static assets and textures
├── libs/          # Third-party libraries
├── models/        # 3D models (FBX)
├── vendor/        # Vendored dependencies
├── index.html     # App entry point
└── serve-local.bat
```
 
## Tech Stack
 
- [Three.js](https://threejs.org/) — 3D rendering engine
- Vanilla JavaScript / HTML5
- GitHub Pages — static hosting
## Notes
 
- The FBX file is served as-is; the app does not compress, convert, or re-export it.
- Any static web host is sufficient — GitHub Pages is not a hard requirement.
---
 
## Author
 
**Gabriel Vieira** — [@gabrielpradovieira](https://github.com/gabrielpradovieira)
 
