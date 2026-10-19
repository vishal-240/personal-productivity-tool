# APEX — F1 Race Control Productivity PWA

A responsive F1-inspired redesign of the existing local-first productivity app.

## Preserved behavior
- Existing localStorage key `daylight-pwa-data-v1` and data shape (intentionally unchanged so existing browser data remains available)
- Tasks, priorities, due dates, completion, editing/deletion, and Monday-first weekly board
- Habits, streaks, focus timer/session history, and daily reflections
- JSON backup export/import and local data deletion
- Local-only storage and service-worker offline shell
- Existing SVG app icon and its references

## Deploy
Replace `index.html`, `manifest.json`, `sw.js`, and `icon.svg` in the repository root, and add/replace `race-hero.png`. Commit the files to `main` and wait for GitHub Pages to deploy.

## Important
The storage key is intentionally still `daylight-pwa-data-v1`; do not change it during this rebrand. Export a JSON backup before deploying as a precaution. Browser data remains local to each browser/device and is not automatically synchronized.
