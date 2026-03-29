# 02 — Setup

## 1. Clone the Workshop Repo

```bash
git clone https://github.com/Ammly/cyber-defender-snake-workshop.git
cd cyber-defender-snake-workshop
```

## 2. Create Your Project Files

```bash
mkdir cyber-defender-snake && cd cyber-defender-snake

# Mac / Linux
touch index.html style.css game.js

# Windows (PowerShell)
New-Item index.html, style.css, game.js
```

Copy `lessons.json` from the repo root into your `cyber-defender-snake/` folder.

```
cyber-defender-snake/
├── index.html
├── style.css
├── game.js
└── lessons.json   ← copy from repo root
```

## 3. Open in VS Code

```bash
code .
```

## 4. Install Live Server

`Ctrl+Shift+X` → search **Live Server** → Install (by Ritwick Dey).

Right-click `index.html` → **Open with Live Server**.

Your browser opens at `http://127.0.0.1:5500` — it auto-refreshes on every save.

## 5. Verify Copilot

Check the VS Code status bar for the Copilot icon. If it's crossed out: `Ctrl+Shift+P` → **Copilot: Sign In**.

> No Copilot? Use [claude.ai](https://claude.ai) — paste the same prompts from `copilot-prompts.md`.

## ✅ Ready when

- [ ] Browser shows a blank page at `localhost:5500`
- [ ] Copilot icon is active in status bar
- [ ] `lessons.json` is in your project folder

---

→ **[03-build.md](./03-build.md)**