# Zivon

An original interactive robot character (inspired by the friendly-service-robot genre — its own design, not a copy of any existing character), built as self-contained HTML/CSS/JS + SVG with **no build step and no dependencies**. Just open the files.

## Live demos

> Served via GitHub Pages at `https://<user>.github.io/<repo>/<file>`.

| Page | What it is |
|------|-----------|
| [`index.html`](index.html) | **Zivon** — the interactive character. Eyes track your cursor; click moods to change eyes, mouth & hands; type a line and Zivon speaks it (lip-synced); 11 expressions; a Milky-Way background; an eye-color hue slider; and a cyan ↔ ember theme toggle. |
| [`index-orange.html`](index-orange.html) | The same demo, booting in the **orange “ember”** theme. |
| [`gallery.html`](gallery.html) | 3D model viewer ([`zivon_robot.glb`](zivon_robot.glb)) + the rendered interaction states in [`renders/`](renders/). |

Everything is pure SVG / canvas + the Web Speech API — **no external libraries**.

## Run locally
```bash
# any static server works; the voice (Speak) needs http(s), not file://
python3 -m http.server 4599
# → http://localhost:4599/index.html
```

## How it's built
- **`index.html`** is a single self-contained file: the robot is live SVG; animation, cursor-tracking, expressions, the speech (Web Speech API + lip-sync) and the procedural Milky-Way canvas are all inline JS.
- The **3D model** (`zivon_robot.glb`) was built procedurally in Blender, with eye **morph targets** preserved, so it can be animated the same way in three.js / model-viewer.

A `.nojekyll` file is included so GitHub Pages serves every file as-is.

---
*Original character design — not a reproduction of any copyrighted character.*
