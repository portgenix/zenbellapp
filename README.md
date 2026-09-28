# ZenBell landing page

Single static page (`index.html`, no build step) for zenbell.app's marketing site — real
screenshots and the promo reel under `assets/`, both taken from the app itself.

## Publish via GitHub Pages

```bash
cd zenbell-landing
git init
git add .
git commit -m "ZenBell landing page"
git branch -M main
git remote add origin git@github.com:<you>/<repo>.git
git push -u origin main
```

Then in the repo's **Settings → Pages**, set Source to `Deploy from a branch`, branch `main`,
folder `/ (root)`. The site will be live at `https://<you>.github.io/<repo>/` within a minute or
two (root-level repos named `<you>.github.io` instead get served at the bare domain).

## Editing

- All content and styling lives in `index.html` — no framework, no build tool.
- Store links (`apps.apple.com/...`, `play.google.com/...`) and the Privacy Policy link near the
  bottom are the only hardcoded external URLs; update them if either ever changes.
- Light/dark mode is CSS-only (`prefers-color-scheme` + a `data-theme` override hook), matching
  the same token-based approach as the app's own theme system.
- `assets/screenshots/` and `assets/video/reel.mp4` are pulled from `takecare/marketing/` in the
  main app repo — replace them there and re-copy/resize if the app's UI changes enough that these
  go stale.
