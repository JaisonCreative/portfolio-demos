# Gem Keno — playable prototype

A mobile keno game with slot reels on top, by Jaison Rivera Creative Studio. This repo hosts the embeddable version for the portfolio case study.

`index.html` shows only the game inside a phone frame. The page background is transparent and the frame has no drop shadow, so it sits directly on a dark section. The phone scales down to fit whatever size the embed box is.

## Files

```
index.html     The game (phone frame only, transparent page)
sound/         The game's sounds as MP3 files
.nojekyll      Tells GitHub Pages to serve the files as they are
```

## Publish with GitHub Pages

1. Create a new repo (for example `gem-keno`) and upload everything in this folder. Keep `sound/` next to `index.html`.
2. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, then pick `main` and `/ (root)`, and save.
3. After a minute the game is live at `https://<your-username>.github.io/gem-keno/`.

## Embed in Framer

- Add an **Embed** component and set its URL to the Pages link.
- Size: width 440 and height 900 on desktop. On tablet and phone, width 100% and height 880.
- No border and no background on the embed. The game draws its own phone frame.
- After you push an update, hard-refresh the Framer page (Ctrl+Shift+R), because Pages and browsers cache the old file.

## Sounds

| File | When it plays |
|---|---|
| `drop.mp3` | Each ball lands in the draw tray |
| `catch.mp3` | One of your numbers is drawn |
| `tick.mp3` | Repeats while the reels spin |
| `stop.mp3` | A reel lands |
| `column.mp3` | A column scores; the game raises its pitch for each column, left to right |
| `win.mp3` | Any paying round |
| `bigwin.mp3` | Big win (15× the total bet) or more |
| `gem.mp3` | A gem bonus pays |

- To use a recorded sound, replace its file with an MP3 of the same name. Keep the sounds short; `tick.mp3` repeats every 92 ms.
- The game sets each sound's volume, so files normalized to full level work fine.
- If a file is missing or can't be decoded, the game plays its built-in synthesized version instead.
- The MP3s only load when the page is served from the web (GitHub Pages or a local server). If you open `index.html` straight from your drive, the built-in sounds play.
- Sound starts after the first tap, because browsers block audio until then. The speaker button in the game mutes it.
