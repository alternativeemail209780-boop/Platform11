# CRAFT platform - UPDATE 171 (compact deploy build)

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

## What's new in 171
* **TEAM ARENA** - Platforms 8, 9 and 10 merged into one: 33 formats (7 word duels brought back: Codedle, Shapedle, Colorblindle, Colordle, Structle, Comparable, Linedle),
  +192 trivia questions, +4 question kinds (missing vowels, odd one out, secret code, emoji decoder) in every quiz format.
* **HANGMAN** - unlimited tries, uses all Word Shuffle categories.
* **16 new ARCADE games** - Emoji Decoder, Missing Vowels, Odd One Out, Math Blitz, Secret Code, Word Rush, Name Them All, Peekaboo,
  Chat vs Bot Tic-Tac-Toe, Crowd Connect 4, Maze Runner, Snake Crowd, Higher or Lower, This or That, Simon Says, Treasure Grid.
* Full details: `CHANGES_UPDATE_171.md` (inside the unpacked `app/` folder).

New games live at `/<game id>/`, e.g. `/hangman/`, `/emojidecoder/`, `/vowels/`, `/oddoneout/`, `/mathblitz/`, `/secretcode/`, `/wordrush/`, `/namethemall/`, `/peekaboo/`,
`/tictactoe/`, `/connect4/`, `/mazerunner/`, `/snakechat/`, `/higherlower/`, `/thisorthat/`, `/simonsays/`, `/treasuregrid/`.
