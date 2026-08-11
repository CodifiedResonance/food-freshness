# PROVISION — Leeds Provision Network

GitHub Pages-ready Progressive Web App package.

**Core line:** Provision is the live map of what a place can provide.

## Deploy

1. Create a GitHub repository (for example `provision`, `food-freshness` or `fresh-select`).
2. Upload **the contents of this folder to the repository root**. Do not upload the enclosing folder as an extra level.
3. Commit to `main`.
4. In **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
5. Wait for the Pages URL to go live, then open it in Chrome on Android.

The package deliberately uses relative paths (`./`) so it works on a GitHub project Pages URL such as `https://USERNAME.github.io/REPOSITORY/` without editing the manifest.

## PWA files

- `manifest.webmanifest` — app identity, start URL, standalone display, icons.
- `service-worker.js` — offline app-shell caching and navigation fallback.
- App icons are deliberately at the repository root so GitHub web upload cannot silently omit an `icons/` folder.
- `.nojekyll` — makes GitHub Pages serve the static package directly.
- `index.html` — PROVISION itself, linked to the manifest and service worker.

## Verify after deployment

In Chrome desktop: **DevTools → Application → Manifest**. Confirm the manifest loads, icons resolve, and the service worker is activated under **Application → Service workers**.

On Android Chrome: load the live HTTPS Pages URL, use it once, then open Chrome's menu. You should be offered **Install app** or **Add to Home screen**, depending on Chrome's UI/version.

This package also includes an in-app **Install** button. Chrome only exposes it once the PWA is considered installable.

## Important: this package is deliberately flat

Every required PWA file is at the repository root. If you are replacing an earlier version, upload **all files in this package**, including every PNG. The old `icons/` and `assets/` directories are no longer required.

After GitHub Pages deploys, refresh the live page once or twice. The new service worker cache is `provision-leeds-v2.1.0`. The in-app **Install** control stays visible in the browser until Provision is installed.
