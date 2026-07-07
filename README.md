# 3D Painter

A simplified, kid-friendly texture painter built with Three.js. Loads a single 3D model (Cannon) as a plain grey mesh and lets you paint directly on it with a brush, eraser, paint bucket, and color wheel.

## Local Testing

Run the app locally from this folder:

```text
serve-local.bat
```

(or `.claude/serve.ps1` if you don't have Python installed). It starts a local server; open:

```text
http://127.0.0.1:3000/
```

Keep the terminal window open while testing. Close it to stop the server.

## GitHub Pages

This project can run directly from GitHub Pages. After committing and pushing:

1. Open the repository on GitHub.
2. Go to **Settings** > **Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder.
5. Save.

## Model

The app loads a single FBX model from the repository:

```text
models/model7/cannon_lp.fbx
```

Keep the file in this path, or update `MODEL_CONFIG` in `index.html`.

## Features

- **Brush** / **Eraser** with three hardness levels (hard, mid, soft)
- **Paint Bucket** with Full Object / Face / UV Shell fill modes
- **Color Wheel** (hue ring + saturation/value triangle) and **Color Picker** (eyedropper)
- **Undo** (Ctrl+Z), up to 10 steps
- Backface-aware painting (strokes never bleed through to hidden surfaces)

## Controls

- **LMB** / touch: paint
- **RMB**: orbit
- **MMB**: pan
- **Scroll** / pinch: zoom
- **Ctrl+Z**: undo
- **R**: reset camera

## Notes

- Do not open `index.html` directly with `file://`; browsers block model loading that way.
- GitHub Pages or any static web host is enough.
- The FBX file is served as-is; the app does not compress, convert, or re-export it.
