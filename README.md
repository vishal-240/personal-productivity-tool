# APEX — Personal Productivity

A privacy-first, local-only productivity PWA with an F1 race-control theme. Deploy the files in this folder to GitHub Pages or serve them from any static host.

## Pages
- **Home / Race Control** — balanced daily overview, today's progress, top five active tasks, and quick actions.
- **Tasks / Race Plan** — task management, priorities, due dates, filters, and a Monday-first weekly board.
- **Focus Stint** — timestamp-based focus timer with pause/resume and saved partial/interrupted sessions. Focus time is accumulated by actual active elapsed seconds and segmented by local calendar date.
- **Consistency** — habit checklist and streaks.
- **Telemetry & Debrief** — optional mood and energy check-ins (1–5), daily prompts, Monday–Sunday weekly review, and 7/30/90-day analytics.
- **Settings & Data** — JSON backup/import and local data deletion.

## Privacy and storage
All application data is stored in `localStorage` under the legacy key `daylight-pwa-data-v1` so existing installations continue to work. No account, backend, remote analytics, or automatic cross-device sync is used. Browser local storage is not encrypted; keep exported backups somewhere safe.

## Compatibility and history
Existing tasks, habits, focus sessions, and quick-review notes remain supported. Older JSON backups can still be imported; new backups also include daily check-ins, snapshots, and weekly reviews. Daily snapshots begin from the day the updated app is used; the app does not fabricate historical mood, energy, or progress data. Tasks are counted as planned for a day when their due date is that day.

Focus timing uses timestamps rather than relying only on interval ticks. Mobile browsers, especially iOS Safari, may suspend background work, so the app reconciles elapsed time on visibility changes and reloads; no browser timer can guarantee uninterrupted execution in the background.

## Install / update
1. Upload `index.html`, `manifest.json`, `sw.js`, `icon.svg`, and `race-hero.png` to the repository root.
2. Deploy/refresh GitHub Pages.
3. Open the app and allow the service worker update to activate. Export a JSON backup before major changes.
