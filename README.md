# Daylight v2 — Weekly Task Board

## What changed
- Added a Monday-first weekly task board with previous/next week navigation.
- Add a task directly to a selected day.
- Complete tasks from the board.
- View and schedule active tasks without due dates.
- Uses the existing `daylight-pwa-data-v1` localStorage key and existing task objects. No database reset or migration is performed.
- Service worker cache name changed to `daylight-shell-v2` so the browser can fetch the updated app shell.

## Critical safe-update steps
1. On each device, open the currently working Daylight app and use **Export backup (JSON)**.
2. Keep each backup separately labelled, e.g. `daylight-before-weekly-board-windows.json` and `daylight-before-weekly-board-iphone.json`.
3. Upload the updated files in this folder to the root of the existing `personal-productivity-tool` repository, replacing the same-named files. Do not delete the repository or clear website data.
4. Wait for GitHub Pages deployment to finish. GitHub says a site change can take up to 10 minutes to appear: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
5. On Windows, open the live site and hard refresh with Ctrl+F5. Test first with a harmless task, then confirm existing tasks/habits/reflections remain.
6. On iPhone, open the Home Screen app while online and refresh/reopen it. If the old version remains, open the same site in Safari, reload it, then close and reopen the Home Screen app. The service worker cache version has been bumped.
7. Verify the board on both devices. If any data appears missing, stop editing and import that device's own backup. Do not import the Windows backup over iPhone data or vice versa unless you deliberately want to replace that device's dataset.

## Privacy and storage
- This is a static web app with no account, analytics or external API calls.
- GitHub Pages source code is publicly readable in a public repository. Never commit task backups or personal data.
- Each browser/device stores data separately. This update intentionally keeps the same localStorage key.
- Local browser storage is not encrypted; keep device access protected and backups private.

## Weekly board behavior
- Week begins Monday.
- Tasks with due dates appear on their date.
- Tasks without a due date can be shown in the unscheduled panel and assigned a date.
- Existing tasks are not duplicated by this update.
- Dates use local calendar dates.
