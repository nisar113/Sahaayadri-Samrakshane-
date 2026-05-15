# Deploying Forest_Guard Web UI to GitHub Pages

This repo contains a static web UI (root `index.html`, `app.js`, `styles.css`). The included GitHub Actions workflow will publish these static files to the `gh-pages` branch so GitHub Pages can serve the site.

Quick steps:

1. Push this repository to GitHub (replace placeholders):

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

2. After pushing, GitHub Actions will run and publish to `gh-pages` branch. You can monitor the workflow under the Actions tab.

3. Visit Settings → Pages and confirm the site is served from the `gh-pages` branch. The URL will be:

```
https://<your-username>.github.io/<your-repo>/
```

Notes:

- If your site requires a Node backend, GitHub Pages is not suitable; consider Render or Railway for server-side deployments.
- The `server.js` file in this repo is a small static server for local testing only.
