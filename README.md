# CRAFT platform - UPDATE 173

**What changed in this update**
* **Snake Arena is removed** (it needed instant steering, which does not work with TikTok's chat delay).
* **31 new games** were added. Every viewer plays for themselves, and all rounds are slow enough for chat delay.

| Group | New games |
|---|---|
| Numbers & maths | What's Next · Missing Signs · Make The Target · Sum Pyramid · Number Translator · Unit Switch · Which Day · Number Spotter · Emoji Equation |
| Pictures & logic | Clock Reader · Count It · Odd Emoji Out · Pattern Finish · Colour Trap · Line Them Up |
| Word games | Word Search · Word Mine · One Letter Off · Fill The Gap · Bookends · Spell Check |
| Geography | Capital Call · Continent Sort · City Finder · Malaysia Towns · Where In The World |
| Quizzes | Trivia Time · Fact Or Fib · Clue Ladder · Finish The Saying · Closest Guess |

The full list with web addresses is in `CHANGES_UPDATE_173.md` (inside the unpacked `app/` folder).

## Deploy (same as always)
1. Upload ALL files in this folder to your GitHub repository (replace the old ones).
2. Render redeploys by itself. Build Command `npm install`, Start Command `npm start` (unchanged).
3. No new settings and no new packages. Your saved settings and records are kept.
4. In the Render log you should see `[launcher] unpacked ... files` and then one `Mounted at /...` line per ARCADE game, ending with `[CLOSESTGUESS] Mounted at /closestguess`.

| File | Purpose |
|---|---|
| `package.json` | list of packages + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the whole platform (80 games, compressed) |
| `.env.example` | reference for the environment variables |
| `.gitignore` | keeps `app/`, `node_modules/` and saved data out of git |
| `README.md` | this file |
