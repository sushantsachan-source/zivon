# Zivon

An original interactive robot character (inspired by the friendly-service-robot genre — its own design, not a copy of any existing character), built as self-contained HTML/CSS/JS + SVG with **no build step and no dependencies**. Just open the files.

## Live demos

> After enabling GitHub Pages (see below), these live at `https://<user>.github.io/<repo>/<file>`.

| Page | What it is |
|------|-----------|
| [`index.html`](index.html) | **Zivon** — the interactive character. Eyes track your cursor; click moods to change eyes, mouth & hands; type a line and Zivon speaks it (lip-synced); 11 expressions; Milky-Way background; eye-color hue slider; cyan ↔ SpeakX theme toggle; a performed pitch + an excited finale. |
| [`index-orange.html`](index-orange.html) | The same demo, booting in the **SpeakX (orange) “ember”** theme. |
| [`zivon-presents.html`](zivon-presents.html) | **Zivon presents** — Zivon narrates a deck slide-by-slide (synced expressions, captions, voice picker, playback controls) and answers spoken/typed questions. |
| [`aura-icon.html`](aura-icon.html) | **Aura** — an interactive 3D icon: a breathing field of points, each wired to a glowing core. Drag / hover / click. `?hue=`, `?bare=1`, `?bg=0` params. |
| [`pulse-icon.html`](pulse-icon.html) | **Pulse** — a 3D heartbeat core that fires a shockwave on every beat. |
| [`pulse-aura.html`](pulse-aura.html) | Combined **Pulse & Aura** orb with live equation sliders. |
| [`pulse-aura-icons.html`](pulse-aura-icons.html) | Side-by-side gallery of the Pulse and Aura icons. |
| [`gallery.html`](gallery.html) | 3D model viewer ([`zivon_robot.glb`](zivon_robot.glb)) + rendered interaction states. |

Everything is pure canvas / SVG + the Web Speech API — **no external libraries** (the embedded pitch deck loads fonts/icons from a CDN).

## Run locally
```bash
# any static server works; some features (mic, cross-frame control) need http, not file://
python3 -m http.server 4599
# → http://localhost:4599/index.html
```

## Publish to GitHub Pages
1. Create a repo and push this folder.
2. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / root**.
3. Your site goes live at `https://<user>.github.io/<repo>/` (homepage = `index.html`).

A `.nojekyll` file is included so Pages serves every file as-is.

---
*Original character design. The 3D model lives in its own Blender collection; the marketing deck/PPT are kept out of this repo via `.gitignore`.*
