# Domi — playable embed

The Domi mobile domino prototype, packaged as an embed for the portfolio site: only the game inside the phone frame, on a transparent page with no drop shadow, so it sits directly on the dark section behind it.

Design, UI/UX and art direction by Jaison Rivera — [jaisonrivera.com](https://jaisonrivera.com)

## Files

```
index.html                     the game in the phone frame (portraits are built in)
.nojekyll                      tells GitHub Pages to serve files as they are
sound/
  music/<track>.mp3            9 seamless loops
  sfx/<pack>/<sound>.mp3       4 sound packs × 8 sounds
```

## Publish on GitHub Pages

1. Upload everything in this folder to a new repo (for example `domi`). Keep `sound/` next to `index.html`.
2. Go to **Settings → Pages**, set Source to *Deploy from a branch*, choose `main` and `/ (root)`, and save.
3. After a minute the game is live at `https://<your-username>.github.io/domi/`.

## Framer embed

- Add an **Embed** with that URL. Recommended size: **440 × 900**.
- The phone scales down to fit any embed size and keeps its frame at every size.
- The page is transparent, so whatever is behind the embed shows around the phone.
- After pushing a change, wait a minute, then hard-refresh (Ctrl+Shift+R). Pages and browsers cache old files.

## Sounds

| File | Plays when |
|---|---|
| `click` | Buttons, menus and equipping items |
| `flip` | A boneyard tile flips over |
| `place` | A tile is placed on the table |
| `hit` | A tile matches (pitch rises as the streak grows) |
| `miss` | A tile doesn't match |
| `tier` | A new pay level is reached |
| `win` | A paying run or a winning hand |
| `tick` | Counters and small ticks |

Sound packs: `classic` (default), `marimba`, `arcade`, `coins`.
Music: `lounge`, `brass`, `night` (free), `cumbia`, `salsa`, `rail` (earned), `chip`, `velvet`, `marble` (shop).

- **Swap a sound:** replace the file with an MP3 of the same name. The game sets the volume itself.
- **Swap a music track:** replace the MP3 with the same name. The built-in loops repeat without a gap. A different file loops from start to end, so give it a clean loop point.
- **Fallback:** if a file is missing or still loading, the game plays its built-in version. The MP3s only load from the web (GitHub Pages or a local server), not when `index.html` is opened from your drive.

Credits are play money only. Nothing can be cashed out, and shop purchases are demos.
