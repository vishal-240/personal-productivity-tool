# Daylight — Personal Productivity PWA

A beginner-friendly, local-first productivity web app for desktop and iPhone.

## Included
- Tasks with priority and due date
- Daily habits and simple streaks
- Focus timer with session history
- Daily reflection
- JSON export/import
- Delete-all-data action
- Responsive layout and basic offline app-shell caching

## Privacy notes
- App records are stored in `localStorage` in the browser profile where the app is opened.
- The app code does not call external APIs or include analytics/advertising SDKs.
- Browser storage is not an encrypted vault. Anyone with access to the unlocked browser/device profile may be able to access it.
- Exported backups are plain JSON. Keep them somewhere private.
- Local data does not automatically sync between Windows and iPhone.
- The timer may be suspended or delayed if iOS puts Safari in the background. Keep the app open for reliable timing.
- This starter has not undergone a professional security audit.

## Run on Windows for local testing
1. Install Python 3 from https://www.python.org/downloads/ if needed.
2. Extract the ZIP to a folder.
3. Open that folder in File Explorer.
4. Click the address bar, type `cmd`, and press Enter.
5. Run:
   `python -m http.server 8000`
6. On the same laptop, open `http://localhost:8000` in your browser.

To test from an iPhone on the same Wi-Fi, find your laptop's local IPv4 address using `ipconfig`, then open `http://YOUR-LAPTOP-IP:8000` in iPhone Safari. This local HTTP test is for development only; service workers/PWA installation generally require HTTPS or localhost, so this address may not support offline installation. Do not expose the server to public Wi-Fi/internet.

## Install on iPhone Home Screen
For a reliable installable PWA, host these files on an HTTPS static host. A no-cost option may be available on services such as GitHub Pages, but check their current terms and configure the repository carefully.
1. Publish the files to an HTTPS static site.
2. Open the HTTPS site in Safari on iPhone.
3. Tap Share.
4. Choose Add to Home Screen. If shown, enable Open as Web App.
5. Open the new Home Screen icon and test adding a sample task.
6. Export a backup and test import before relying on the app.

## Important storage detail
`localStorage` is origin-specific. Data created on `localhost` on Windows, a hosted domain on Windows, and that hosted domain on iPhone are separate stores. Installing the same website on iPhone does not transfer your Windows browser data. Use the app's export/import feature to move a backup manually.

## Limitations
- No cloud sync, account, calendar integration, recurring task scheduler, or push notifications.
- Habits are daily check-ins; streaks are calculated from consecutive calendar days.
- Timer completion is most reliable while the app remains open.
- Service-worker caching is a starter offline shell, not a guarantee that every browser lifecycle/offline state will behave identically.
