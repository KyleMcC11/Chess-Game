# Culloden 1746 → Louisbourg 1758 → Quebec 1759 — Wikipedia & Campaign Edition

The completed expanded edition of the chess game. All 8 Jacobite regiments (a2–h2)
and all 8 Hanoverian regiments (a7–h7) with campaign service, Wikipedia links,
back-rank commanders, floating regiment badges, veteran highlights, and the
phone layout (compact header, Info bottom sheet, pinch zoom).

## What is in this zip

- `culloden_chess_3d.html` — the complete game, standalone
- `js/three.min.js` + `js/chess.min.js` — the two libraries, vendored locally
  (only needed if your folder does not already have a `js/` folder with them)

## Install — replace the current game (main page)

From inside your `Chess-Game` folder:

```
unzip -o ~/Downloads/chess-game-louisbourg.zip
cp culloden_chess_3d.html index.html
git add .
git commit -m "Louisbourg/Quebec edition: campaign badges, Wikipedia links, veteran highlights"
git push
```

If the push is rejected with "fetch first" (because a workflow commit landed on
GitHub since your last pull), run `git pull --rebase` first, then `git push` again.

## Install — keep as a second page instead

If you want the original game to stay as the main page, skip the `cp` line —
just add the file and push. The new edition then lives at
`https://kylemcc11.github.io/Chess-Game/culloden_chess_3d.html`:

```
unzip -o ~/Downloads/chess-game-louisbourg.zip
git add .
git commit -m "Add Louisbourg/Quebec edition as second page"
git push
```

## Notes

- Nothing changes on the live site until you push.
- Two CSS bugs from the draft are fixed (an unclosed comment that would have
  swallowed the badge styles, and a rule missing its `*` selector).
- Three.js + chess.js load from the local `js/` folder, so the game works even
  if a CDN is down. Tailwind still loads from its CDN, with the needed styles
  also baked into the file as a fallback.
- Play-test before calling it done: one move, one capture, one promotion, and
  the Louisbourg & Quebec Vets button. Those flows reuse the proven engine from
  the first game, but they were verified by screenshot/DOM checks, not by live
  clicking.
