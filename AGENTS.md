# AGENTS.md

## Overview
Vanilla HTML5 Canvas clone of Asteroids. All game logic, rendering, and input live
in a single plain-script file `game.js`, loaded via `<script src="game.js">` in
`index.html`. No dependencies, no bundler, no build step.

## Run / verify
- No package.json, tests, or lint exist. Verification is manual in a browser:
  `npx serve .` → http://localhost:3000, or open `index.html` directly.

## Gotchas
- Canvas size is hardcoded in TWO places that must stay in sync:
  `width="800" height="600"` in `index.html` and `W`/`H` at the top of `game.js`.
- `game.js` is a classic script, not an ES module — do not add `import/export`.
- UI strings are in Spanish (e.g. `GAME OVER`, `NIVEL`, `PUNTAJE`); keep new text Spanish.
- Input uses `e.code` (`ArrowLeft`, `ArrowUp`, `Space`); those codes get `preventDefault`.
- README mentions power-ups and an "estrella fugaz" asteroid type, but the current
  code has neither — trust `game.js` over the README.
