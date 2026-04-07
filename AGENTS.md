# AGENTS.md

## What this repo is

`dexsword/RiftAIWebPresence` is a single-file static site: one `index.html` with all CSS and JavaScript inlined. Hosted on GitHub Pages at `https://dexsword.github.io/RiftAIWebPresence/`. There is no build step, no package manager, no framework, no test suite, and no CI.

## Critical context

- `/root/riftweb/index.html` **is the real source file** — it has been replaced with the actual site HTML (not the GitHub blob page that was here previously).
- To fetch the latest upstream version: `curl -o index.html https://raw.githubusercontent.com/dexsword/RiftAIWebPresence/main/index.html`
- The repo has exactly one file (`index.html`) plus `AGENTS.md`. GitHub Pages serves `index.html` from the root of `main`.

## Editing

- All styles are in a single `<style>` block in `<head>`. No external stylesheet.
- All scripts are in a single `<script>` block at the bottom of `<body>`. No bundler.
- Fonts: `Syne` (headings/numbers) and `DM Sans` (body) — loaded from Google Fonts.
- CSS custom properties on `:root` — never hardcode hex values, use the variables.
- Key variables: `--ink`, `--gold`, `--gold-light`, `--gold-pale`, `--accent`, `--surface`, `--border`, `--r`, `--r-lg`, `--banner-h`, `--nav-h`.

## Key URLs hardcoded in the file

- Discord invite: `https://discord.com/oauth2/authorize?client_id=1457128015397130470`
- Ko-fi: `https://ko-fi.com/dexsword`
- GitHub Pages URL: `https://dexsword.github.io/RiftAIWebPresence/` (in og:url meta tag)

## No commands to run

There is no `npm install`, `build`, `test`, or `lint` command. Validate changes by opening `index.html` directly in a browser.

## Deploying

Push to `main` — GitHub Pages auto-deploys from the root of `main`. No workflow file needed.

To enable GitHub Pages on a fresh clone (one-time setup):
1. Go to `https://github.com/dexsword/RiftAIWebPresence/settings/pages`
2. Source → "Deploy from a branch"
3. Branch → `main`, folder → `/ (root)`
4. Save — site is live at `https://dexsword.github.io/RiftAIWebPresence/` within ~60 seconds.
