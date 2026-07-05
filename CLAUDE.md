# CLAUDE.md — handlogic-web (v1 — LIVE PRODUCTION)

**This repo IS the live site at handlogic.io.** GitHub Pages serves the repo
root of `main` directly — **a push to main is a deploy**, live within minutes.
No build step, no staging. The `CNAME` file makes the custom domain work; never
delete it.

## What's here
Static HTML/CSS/JS: `index.html` plus per-app pages (logicdesk, logictray,
logicvoice, logiccontent, privacy-policy), one shared `handlogic.css`, and
assets (icons, OG images, `robots.txt`, `sitemap.xml`).

## Working on it
```bash
python3 -m http.server 8642    # serve locally (matches .claude/launch.json)
```
Edit files directly — no bundler, no npm. Keep styling in the shared
`handlogic.css`; global selector changes affect every page.

## Gotchas
- **v2 replacement in progress** at `~/Developer/handlogic-web-v2` (React +
  Vite, branch `codex/site-v2`, not yet deployed). Until v2 ships, this repo
  stays the production site — content fixes go here.
- The older prototype in `~/Developer/HandLogic/website-prototype/` is a design
  reference only; don't sync changes from there blindly.
- New pages: keep the nav rule — "HandLogic" first in the top menu and in the
  footer, and update `sitemap.xml`.
