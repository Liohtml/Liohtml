# 🚀 How to publish this profile

Your GitHub profile README lives in a **special repo named exactly after your username**.
For you that's a repo called **`liohtml`** (i.e. `github.com/liohtml/liohtml`).

## 1. Create the special repo
1. Go to https://github.com/new
2. **Repository name:** `liohtml` (must match your username exactly — GitHub shows a 💡 "you found a secret!" hint)
3. Set it **Public**
4. ✅ Check **"Add a README file"**
5. Create.

## 2. Push these files into it
From this folder (`D:\CODEENV\PersonalRepo`):

```powershell
git init
git add README.md .github SETUP.md
git commit -m "✨ neon cyberpunk profile"
git branch -M main
git remote add origin https://github.com/liohtml/liohtml.git
git push -u origin main --force   # --force only needed if the repo already had an auto README
```

> If you created the repo *without* a README, drop `--force`.

## 3. Turn on the snake animation 🐍
The contribution-snake won't render until the workflow runs once.

1. In the repo: **Settings → Actions → General → Workflow permissions** → select **"Read and write permissions"** → Save.
2. Go to the **Actions** tab → **"Generate Snake Animation"** → **Run workflow**.
3. After ~1 min it creates an `output` branch with the SVGs. The README image then resolves automatically.

It also re-runs every 12 hours and on every push to `main`.

## 4. (Optional) Make stats count private commits
The stats card already requests `count_private=true`. To actually *show* private contributions:
`github-readme-stats` reads public data by default — that's fine for most. No action needed unless you self-host the stats instance.

---

## 🎨 Tweaks you might want
- **Theme:** every stats/streak/trophy URL uses `theme=tokyonight`. Swap for `radical`, `synthwave`, `dracula`, `catppuccin_mocha`, etc.
- **Accent colors:** the cyberpunk palette is `00F0FF` (cyan) · `BD00FF` (purple) · `FF003C` (red). Find-and-replace to recolor everything.
- **Typing lines:** edit the `lines=` query param in the `readme-typing-svg` URL (use `;` between lines, URL-encode spaces as `+`).
- **Pinned repos:** the project table is manual — reorder/add as you ship. Also pin them visually via your profile's "Customize your pins".
- **Banner text:** edit the `text=` and `desc=` params in the top `capsule-render` URL.

That's it — refresh `github.com/liohtml` and enjoy. ⚡
