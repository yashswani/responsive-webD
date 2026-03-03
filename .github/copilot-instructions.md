<!--
Repository: responsive-webD
Purpose: Short, actionable instructions to help AI coding agents be productive in this repo.
Keep this file concise (20–50 lines) and specific to the codebase layout and conventions.
-->

# Copilot instructions for responsive-webD

This repository is a small static HTML/CSS exercise site. Most work is done in self-contained folders (e.g. `1.3 Markers/`, `2.4 HTML CSS Quiz/`). Use these notes to make edits, run previews, and follow repository conventions.

Key facts
- Project type: static site (HTML + CSS). There is no build system, no package.json, and no tests detected.
- Layout: each exercise folder contains an `index.html` and a `styles.css` (note: some folders use `style.css` or `styles.css`; check the exact filename before editing).
- Top-level `index.html` exists and several subfolders follow the pattern `X.Y Name/` (spaces and dots are part of folder names).

Developer workflows (how to preview and debug)
- Quick preview in VS Code: use the Live Server extension or open the folder in an editor and right‑click an `index.html` -> "Open with Live Server".
- From a terminal (macOS zsh) run a quick static server at repository root:
  - python: `python3 -m http.server 8000` and open http://localhost:8000
  - node: if Node is available: `npx serve .`
- Browser devtools are primary debugging tools (no JS frameworks or bundlers present).

Project-specific patterns and notes (do not change unless necessary)
- File naming: many directories use `styles.css` but at least one (`2.4 HTML CSS Quiz/`) uses `style.css` — edits must reference the file actually linked by that folder's `index.html`.
- Relative linking: pages link CSS and assets using relative paths inside each folder. When moving files, update relative links accordingly.
- Folder names contain spaces and leading numeric prefixes (e.g. `1.3 Markers`). When scripting or writing paths, surround in quotes or escape spaces.

Examples (use these as templates when making changes)
- To edit the Marker exercise: open `1.3 Markers/index.html` and `1.3 Markers/styles.css`.
- To preview entire site: run `python3 -m http.server` from the repository root and open http://localhost:8000/index.html.

When to ask for human help
- If a requested change would introduce a build system, Node dependencies, tests, or server-side logic — ask for clarification before proceeding.
- If new assets are added, confirm whether they should be placed in a new `assets/` folder or inside the exercise folder.

Where to look for relevant files
- Exercise sources: top-level folders like `1.1 Cat Pics/`, `1.2 Menu/`, `2.1 Rothko Painting/`, etc.
- Main entrypoints: `index.html` at repo root and each exercise's `index.html`.

Success criteria for edits
- HTML pages render in a modern browser without console errors.
- CSS edits are limited to the exercise folder unless the change is intended to affect the whole repo—mention this in commit message.

If anything above is unclear or you want the file to include more detailed examples (live-server config, exact CSS filename list, or commit message templates), tell me which section to expand.
