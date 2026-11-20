# CRAFT platform - UPDATE 172 (compact deploy build)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (50 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged (no new ones).
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena` and 17 lines from `[HANGMAN] Mounted at /hangman` to `[TREASUREGRID] Mounted at /treasuregrid`.
   Saved settings under `app/data/` are never overwritten.

## What's new in 172
No game treats the whole chat as ONE player any more. Six ARCADE games were rebuilt so every viewer plays and scores for themselves (same ids and URLs):

* **TIC TAC TACTICS** (`/tictactoe/`) - find the winning or blocking square; first right answer scores.
* **CONNECT 4 TACTICS** (`/connect4/`) - find the winning or blocking column; first right answer scores.
* **MAZE RUNNER** (`/mazerunner/`) - every viewer has their own runner and races to the flag.
* **SNAKE ARENA** (`/snakechat/`) - every viewer steers their own snake in a shared arena.
* **HIGHER OR LOWER** (`/higherlower/`) - every viewer keeps their own streak.
* **THIS OR THAT** (`/thisorthat/`) - an A/B fact quiz, right answers score, fastest gets a bonus.

Full details: `CHANGES_UPDATE_172.md` (inside the unpacked `app/` folder).
