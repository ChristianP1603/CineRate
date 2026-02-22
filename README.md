# 🎬 CineRate — Shared Film Rating Tool

A beautiful, serverless film rating tool for you and your friends. No login required. All data stored in a shared **GitHub Gist** (free, git-backed).

## ✨ Features
- 🎬 **Film Search** via TMDb API (free) — posters, overviews, genres, runtime
- ➕ **Manual Add** — add films without TMDb if needed
- ⭐ **1–5 Star Ratings** with optional text reviews
- 👥 **See who rated what** — user avatars and attribution on every film
- 🔁 **Duplicate Detection** — if a friend already added the film, it opens directly
- 📊 **Stats & Breakdowns** — average scores, rating distribution per film
- 🔄 **Real-time Sync** via GitHub Gist API
- 🟢 **Sync Status** indicator in the header
- 🎨 **Dark Cinema Theme** — glassmorphism, smooth animations

## 🚀 Setup (One-Time)

### Step 1 — Create a Shared GitHub Gist
1. Go to [gist.github.com](https://gist.github.com) (any group member can do this)
2. Create a **secret** gist
3. Filename: `cinerate.json`
4. Content:
```json
{"films":[]}
```
5. Click **Create secret gist**
6. Copy the **Gist ID** from the URL: `gist.github.com/<username>/<GIST_ID>`

### Step 2 — Create a GitHub Personal Access Token
1. Go to [github.com/settings/tokens](https://github.com/settings/tokens) → **Generate new token (classic)**
2. Give it a name like `CineRate`
3. Select scope: ✅ **gist**
4. Generate & copy the token (`ghp_...`)
> Each friend creates their own token — never share tokens!

### Step 3 — Get a Free TMDb API Key (Optional but recommended)
1. Create a free account at [themoviedb.org](https://www.themoviedb.org)
2. Go to Settings → API → Request an API Key (choose "Developer")
3. Copy your **API Key (v3 auth)**

### Step 4 — Open CineRate
1. Open `index.html` in your browser
2. Fill in: your name, the shared Gist ID, your token, and optionally your TMDb key
3. Share the **Gist ID** with friends — they each do steps 2–4 with their own token

## 🌐 Hosting on GitHub Pages (Optional)
To access via URL (e.g. on mobile):

```bash
git init
git add index.html README.md
git commit -m "Initial CineRate setup"
# Create a repo on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/cinerate.git
git push -u origin main
```
Then enable GitHub Pages in repo Settings → Pages → main branch → root.

## 📁 Project Structure
```
FilmRating/
└── index.html    ← The entire app, one file
└── README.md     ← This file
```

## 🔒 Privacy Notes
- Each friend's GitHub token is stored only in **their own browser** (localStorage)
- The Gist is "secret" (unlisted, but not encrypted — anyone with the URL can read it)
- No passwords, no accounts, no server costs
