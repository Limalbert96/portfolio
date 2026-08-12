# Albert Lim — Personal Brand Site

Live at **https://limalbert96.github.io/portfolio/**

A single-file interactive site (`index.html` + `albert.jpg`). No build step, no dependencies. Hosted free on GitHub Pages.

## What this is

A personal brand experience built to show, not just tell: animated particle background, custom cursor, an interactive "Handoff Tax" calculator that quantifies the cost of a broken presales to postsales handoff, and the full story of full lifecycle technical ownership.

## How it got deployed (the one-time setup, already done)

1. Created a public repo at `github.com/Limalbert96/portfolio` (empty, no README/license).
2. Initialized git in this folder and pushed:
   ```bash
   git init
   git add .
   git commit -m "Albert Lim personal brand site"
   git branch -M main
   git remote add origin https://github.com/Limalbert96/portfolio.git
   git push -u origin main
   ```
3. Authenticated with GitHub CLI (`gh auth login`) so pushes work without juggling tokens.
4. Turned on Pages: repo **Settings > Pages > Source: Deploy from a branch > Branch: `main` / root**.

GitHub Pages rebuilds automatically on every push. Changes go live in about a minute.

## Making changes later (this is all you need)

Edit `index.html`, then run these three commands from this folder:

```bash
cd ~/Documents/alim_workspace/portfolio
git add .
git commit -m "describe what changed"
git push
```

Refresh the live URL a minute later to see it. That is the entire loop.

## Handy extras

Check status (what changed since last push):
```bash
git status
```

See the live site URL / open the repo:
```bash
gh repo view --web
```

Undo local edits to a file before committing (revert to last pushed version):
```bash
git checkout -- index.html
```

If a push ever asks for a password again, re-link GitHub CLI once:
```bash
gh auth setup-git
```

## Files

- `index.html` — the entire site (HTML, CSS, JS inline)
- `albert.jpg` — hero headshot
- `README.md` — this file
