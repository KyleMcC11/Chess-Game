# Culloden 1746: Celtic vs Red Coats 3D Chess

A single-page 3D chess game — Jacobite Highlanders (White) vs British Red Coats (Black) —
built with Three.js for the 3D board/pieces and chess.js for the rules. Play against the
built-in AI commander or pass-and-play, with clan lore for each Jacobite piece.

## Play it

Live site (GitHub Pages): https://kylemcc11.github.io/Chess-Game/

## Run it locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server
```

then open http://localhost:8000

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole game (board, UI, lore, game logic) |
| `js/three.min.js` | Three.js 0.147 — vendored locally (last build with a global `THREE`) |
| `js/chess.min.js` | chess.js 0.10.3 — vendored locally (old `in_check()` / `game_over()` API this game uses) |

Fonts (Cinzel + Inter) load from Google Fonts; if they are blocked the game still
works with fallback fonts.

## Deploy (GitHub Pages)

Push this folder to the repo, then in GitHub go to **Settings → Pages →
Build and deployment → Source: Deploy from a branch → Branch: `main`, `/(root)`**.
No build step, no Jekyll config needed.
