# CRAFT platform - UPDATE 175 (compact deploy build)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (100 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged (no new ones).
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena` and 17 lines from `[HANGMAN] Mounted at /hangman` to `[TREASUREGRID] Mounted at /treasuregrid`.
   Saved settings under `app/data/` are never overwritten.

## What is new in 175
* **Games 33-100 quality pass:** every setting audited and tested (no dead settings), shared timing / scoring / hint / session settings verified in the real engine, 1,890 screens rendered without errors.
* **One-screen fit:** each game's stage now scales itself to fit the phone screen - nothing is pushed off the bottom.
* **More customization** for the 50 newest games: region filters, option counts, grid sizes, question types, ranges, currencies and more (all "0 = by difficulty").
* Test mode fixes (Word Rush, Odd One Out, Hangman, Team Arena start-up).

Full details: `CHANGES_UPDATE_175.md` (inside the unpacked `app/` folder).
