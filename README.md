# Woordentrainer — GitHub + installable phone app

This repository includes the vocabulary game and its Progressive Web App (PWA) files:
- `index.html` — the game
- `manifest.json` — app name, display mode and icon declarations
- `sw.js` — service worker for offline caching
- `icons/` — 192 px, 512 px and maskable app icons

## Publish it from GitHub

1. Create a new **public** GitHub repository.
2. Upload all files and the `icons` folder to the repository's top level (keep the folder structure).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Wait for GitHub Pages to publish the site. Open the Pages URL once in Chrome while online. This lets the service worker install and cache the app shell.

## Install on Android / Chrome

1. Open the GitHub Pages URL in Chrome on your phone.
2. Open Chrome's menu (⋮).
3. Tap **Install app** or **Add to Home screen** (wording depends on Chrome version).
4. Launch Woordentrainer from the new home-screen icon.

After the first successful load, the service worker caches the app shell for offline use.

## Download a local copy instead

You can also use the repository's **Code → Download ZIP** option, extract it, and open `index.html`. The game itself is self-contained and works as a local HTML file. However, browsers do not allow service workers to run from `file://` URLs, so the PWA install prompt and service-worker offline caching require the HTTPS GitHub Pages URL (or localhost during development).
