Here’s a `README.md` file for your **DropScore Player Viewer** project:

---

# 🏀 DropScore Player Viewer

**DropScore** is a browser-based fantasy NBA playoff drafting and scoring app. It lets users create leagues, run snake-style drafts, track fantasy points through the playoffs, and see who comes out on top. It supports saving previous drafts and exporting data for backup or analysis.

---

## 🔧 Features

- 🐍 **Snake-style NBA Playoff Draft**
- 📈 **Live Draft Board & Leaderboard**
- 🧠 **Points-based scoring per player**
- 💾 **Save and view previous drafts (stored locally)**
- ⬇️⬆️ **Export/import drafts (CSV & JSON)**
- 🔄 **Undo last pick**
- 🎉 **Winner reveal with sound effects**
- 📱 **Fully client-side – no backend required**

---

## 🚀 How to Use

1. **Open `index.html`** in a browser.
2. Click **"Start New Draft"** or **"View Previous Drafts"**.
3. For a new draft:
   - Name your league.
   - Choose number of draft rounds.
   - Set number of teams (2–12).
   - Enter team names.
   - Draft players in a snake order.
4. Track player points and view the **leaderboard** when the draft ends.

---

## 🧪 Data Source

Player data is fetched from a [Sheety](https://sheety.co/) API URL:

```
https://api.sheety.co/8bc8ea9aa07e26b76e867fe4d92cee28/nbaPlayoffData/sheet1
```

Each player object includes:
- `playerName`
- `team`
- `points`
- `eliminated` (boolean)

---

## 🧠 How Draft Works

- Players draft in a **snake format**: Team A → B → C → C → B → A...
- Draft continues for the selected number of rounds.
- Each player can only be drafted once.
- Teams accumulate points based on their players' total playoff points.
- Once complete, a **leaderboard** and **final rosters** are shown.

---

## 💾 Draft Persistence

- Previous drafts are stored in `localStorage`.
- You can:
  - 🔍 View past leaderboards and rosters.
  - ⬇️ Export a draft to **CSV** or **JSON**.
  - ⬆️ Import JSON to restore saved drafts.
  - 🗑️ Delete individual drafts.

---

## 📂 Project Structure

All functionality is in a **single HTML file**:
- **HTML**: Structure and UI.
- **CSS**: Inlined styling.
- **JavaScript**: Handles all logic including:
  - Draft flow
  - API fetching
  - Dynamic UI rendering
  - State tracking
  - LocalStorage persistence
  - CSV/JSON export & import

---

## 🔊 Media

Includes an applause sound (`applause-8.mp3`) played when a draft ends.

---

## 📸 Image Handling

Player headshots are loaded from:

```
https://cdn.nba.com/headshots/nba/latest/260x190/{PlayerName}.png
```

Fallback image is used if not found.

---

## 📌 Requirements

- Modern browser (Chrome, Firefox, Edge, Safari)
- Internet connection (for player API + headshots)

---

## 📤 Deployment

No build or server required. Simply host or open `index.html` directly.

To deploy on GitHub Pages:
1. Push this file to a GitHub repo.
2. Go to **Settings → Pages**.
3. Select your branch and `/root` or `/docs`.
4. Visit the generated GitHub Pages link.

---

## 🙌 Credits

- NBA stats powered via [Sheety](https://sheety.co/)
- UI designed with inline HTML/CSS
- Audio from [SoundJay](https://www.soundjay.com/)

---

## 🛠️ Future Ideas

- Real-time multiplayer draft syncing
- Mobile optimization
- Dark/light theme toggle
- Player stats history view
- Authentication + cloud storage

---

Let me know if you'd like this as a downloadable file or want it customized further!
