# Daylight — F1 Race Control Redesign

This package updates the existing Daylight PWA with the approved Max Verstappen / F1-inspired visual theme.

## Preserved
- Existing `daylight-pwa-data-v1` localStorage key and data shape
- Tasks, priorities, due dates, completion, editing and deletion
- Monday-first weekly task board, navigation, scheduling and unscheduled tasks
- Habits and streaks
- Focus timer and session history
- Daily reflections
- JSON backup export/import and local data deletion
- Local-only storage and service-worker offline support
- SVG app icon (`icon.svg`) referenced from both `index.html` and `manifest.json`

## Deploy
Replace `index.html`, `manifest.json`, `sw.js`, and `icon.svg` in the repository root, and add `race-hero.png`. Commit and push to `main`. The service-worker cache name is bumped so the redesigned shell is refreshed after deployment.

## Important
The app does not migrate, clear, or rename localStorage. Existing data remains under `daylight-pwa-data-v1`. Export a JSON backup before deployment as a precaution.
