# Site Redesign Package

This folder contains the redesigned game pages, the new shared design system, the
new homepage, and a new resume page. Drop these files into your local repo,
preserving paths, and they'll land in the right places.

## How to push to GitHub

```bash
# 1. Make a branch from your current main
git checkout -b redesign/game-pages

# 2. From the root of this release folder, copy everything into your repo
#    (replace ~/path/to/ifishbw.github.io with your local path)
cp -R . ~/path/to/ifishbw.github.io/

# 3. Push the branch
cd ~/path/to/ifishbw.github.io
git add .
git commit -m "Redesign: game pages, resume, shared design system"
git push -u origin redesign/game-pages
```

Then open a PR on GitHub and review before merging to main.

## What's inside

### New pages
- `index.html` — new homepage (replaces existing root index.html)
- `resume/index.html` — new clean resume route
- `kintsugi/index.html` — Kintsugi (rebuilt)
- `copy-1/kintsugi/index.html` — Scroll of Doom (rebuilt, renamed from Rune Combat)
- `copy-2/kintsugi/index.html` — The Bloody Cross (rebuilt)
- `copy-3/kintsugi/index.html` — Bones Whisper (rebuilt)
- `copy-4/kintsugi/index.html` — Timeline LA (rebuilt, renamed from Paradox)
- `copy-1/copy-4/kintsugi/index.html` — Shrimp Out (rebuilt, renamed from Mantis Shrimp Boxing)

### Shared design system
- `assets/site.css` — design tokens, components, layout used by all game pages
- `assets/site.js` — nav scroll behavior + reveal animations

### Asset folders (readable filenames)
- `assets/kintsugi/` — core-loop, screenshot, state-diagram
- `assets/bloody-cross/` — dialogue-system, art-sorrowful, art-sorrowful-thorns
- `assets/scrolls-of-doom/` — combat-system, rune-types, rune-signage, in-game
- `assets/bones-whisper/` — level-design
- `assets/shrimp-out/` — state-machine
- `assets/resume/` — resume.pdf, resume.png

## Optional cleanup (after merge)

These are orphaned by the new pages — safe to delete when you're confident:
- `copy-1/copy-1/copy-4/kintsugi/` (old resume route)
- `assets/static/` (Webstudio CSS)
- `assets/entries/` (Webstudio JS)
- `assets/chunks/` (Webstudio JS)
- Old hashed asset filenames (e.g. `assets/CoreLoop_Kint_AG8J0Z1BU3WpgQF3PcZoG.png`) — replaced by readable names in `assets/<game>/`

## Notes

- All asset paths use relative URLs (e.g. `../assets/site.css`) so they work on
  GitHub Pages without needing a base path.
- Game pages link to the homepage via `/` and to anchors like `/#portfolio` —
  these resolve to root on GitHub Pages.
- Resume nav link points to `/resume` (the new clean route).
