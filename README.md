# 🃏 Rummy Scorer

A mobile-friendly Progressive Web App (PWA) to track scores during Rummy card games. Install it on your iPhone home screen for a native app experience.

🔗 **Live App:** [ajayashok1.github.io/Rummy](https://ajayashok1.github.io/Rummy)

---

## 📲 How to Install on iPhone

1. Open the link above in **Safari**
2. If it opens in WhatsApp browser, tap **⋯ → Open in Safari**
3. Tap the **Share button** (□↑) at the bottom
4. Tap **⋯ More**
5. Tap **Add to Home Screen**
6. Tap **Add ✓**

The app will appear as an icon on your home screen!

---

## 🚀 Version History

### v3.0 — Current
*Dark Saffron Theme · Card Suits · Game History · Improved UX · Rule Enforcement*

#### ✨ New Features

**🎨 Dark Saffron Theme**
- Rich dark saffron/burnt orange background with warm golden spotlight
- Subtle card suit symbols (♠ ♥ ♦ ♣) scattered across the background
- Saffron-orange accents on titles, borders, buttons, and highlights
- Dark card surfaces with saffron borders for a premium card-game feel

**📅 Game Date & History**
- Current date shown on setup screen and game screen headers
- Each game records the date and time when it starts
- Games are automatically saved when they end (winner declared) or when starting a new game
- New **Past Games** tab on the setup screen to browse all previous games
- Tap any past game to expand and view the full round-by-round scorecard
- Delete individual game records with confirmation
- Stores up to 50 past games in localStorage

**🔍 Bigger Avatars & Names**
- Setup avatars 64px, leaderboard avatars 56px — much larger and clearer
- Player names, scores, and hints all bumped up in font size for mobile readability

**📷 Photo Compression**
- Uploaded photos are now resized to 120x120px thumbnails and compressed as JPEG at 70% quality
- Reduces each photo from ~2-5MB to ~3-5KB, preventing localStorage overflow
- Fixes the issue where photos would silently fail to load

#### 🔧 Gameplay Changes

**Simplified Score Input**
- Quick-score buttons reduced from 9 options to just **0, 25, 100** plus manual input
- Cleaner, less cluttered score entry

**Single Zero Per Round**
- Only 1 player can score 0 (win) per round — entering multiple zeros shows a validation error

**Rejoin Cap at 170**
- Eliminated players can only rejoin if the highest active player's score is 170 or below
- If any active player exceeds 170, the Rejoin button is disabled with a message

**New Game Player Choice**
- When starting a new game, a second prompt asks whether to keep the same players or reset
- No more accidentally losing your player setup

---

### v2.0
*Photo Avatars · Team Management · Mid-Game Features · Casino Theme*

#### ✨ New Features

**👤 Photo Avatars**
- Tap any player avatar to upload a photo from your camera roll
- Or choose an emoji instead
- Photos appear on the leaderboard, score input, round history and saved teams

**➕ Add Player Mid-Game**
- Add a new player at any point during a game
- They join from the current round with 0 points
- Past rounds show `—` for the new player in history

**🔄 Rejoin After Elimination**
- Eliminated players can rejoin the game
- Their starting score is set to the highest active player's score at that moment

**💾 Team Management**
- Save your regular group of players as a named team
- Load a saved team instantly from the Saved Teams tab
- Edit a saved team — rename, change avatars, add or remove members
- Delete saved teams with inline confirmation (no popup)
- Duplicate team names are blocked (case-insensitive)

**🎨 Casino Theme**
- Rich green felt background with subtle texture
- Gold accents on titles, labels, buttons and highlights
- Dark card surfaces with gold borders — like a real card table
- Classic casino / playing card aesthetic

#### 🐛 Bug Fixes
- **Score validation** — typing invalid characters (e.g. `220-`, letters, symbols) now shows an inline warning `⚠️ Numbers only (e.g. 25)` with a red border. The value is preserved so the user can correct it. Saving is blocked until all scores are valid whole numbers.
- **Inline delete confirmation** replaces browser `confirm()` dialog which was blocked in some environments.

---

### v1.0
*Initial Release*

#### ✨ Features
- Add 2–8 players with emoji avatars
- Track scores across unlimited rounds
- Quick-score buttons (0, 10, 20, 25, 30, 40, 50, 80, 100)
- Auto-elimination when a player exceeds 220 points
- Live leaderboard sorted by score
- Round history table
- Undo last round
- Celebration banners for round winners and eliminations
- Scores saved locally — survive page refresh
- PWA support — installable on iPhone home screen

---

## 🎮 How to Play

- **Cutoff:** 220 points — exceed this and you're eliminated
- **Round winner:** Player with 0 points wins the round 🏆
- **Game winner:** Last player remaining under the cutoff wins
- **Rejoin:** Eliminated players can rejoin with the highest active player's score (only if max active score ≤ 170)
- **One winner per round:** Only 1 player can score 0 in a single round

---

## 🛠 Built With

- Vanilla HTML, CSS, JavaScript — no frameworks
- LocalStorage for score and team persistence
- PWA meta tags for home screen installation
