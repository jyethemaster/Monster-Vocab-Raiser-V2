# Woordentrainer — complete GitHub Pages PWA

## Upload
Upload **all six files** from this folder to the **root** of your GitHub repository:
- `index.html`
- `manifest.json`
- `sw.js`
- `icon-192.png`
- `icon-512.png`
- `icon-512-maskable.png`

There is no `icons/` folder. The HTML and manifest both point to the root-level PNG files.

## Publish
In GitHub, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then save. Open the published HTTPS Pages URL.

## Notes
- `index.html` is the uploaded vocabulary game with its game logic and monster reactions preserved. Its icon references have been corrected to root-level files.
- `manifest.json` uses relative paths, so it works from a GitHub Pages project URL (including a repository subpath).
- `sw.js` caches the app shell and uses a new cache version to replace the earlier cache.
- Service workers and PWA installation require HTTPS (GitHub Pages provides HTTPS).
