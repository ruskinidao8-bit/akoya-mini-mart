# AKOYA MINI MART POS

Installable offline-first Progressive Web App (PWA) for AKOYA MINI MART.

## Features
- POS sales, purchases, expenses, suppliers and products
- Local-first storage for offline operation
- Google Sheets synchronization when online
- Installable as an app on supported browsers/devices
- Responsive portrait and landscape layout

## Run locally
A service worker requires `localhost` or HTTPS. Do not open `index.html` directly with `file://`.

### Python
```bash
python3 -m http.server 8080
```
Then open `http://localhost:8080/`.

## GitHub Pages
This repository includes a GitHub Actions workflow that publishes the PWA to GitHub Pages.

1. Create a GitHub repository, for example `akoya-mini-mart-pos`.
2. Upload all files in this folder to the repository root.
3. In GitHub, open **Settings → Pages** and set the source to **GitHub Actions**.
4. Push to `main`; the workflow publishes the app.
5. Open the generated HTTPS Pages URL and use the browser's **Install** option.

If the repository is private, the repository/source remains private, but GitHub Pages access depends on the repository/account plan and Pages settings. Do not put passwords, API keys, or private credentials in this repository.

## Offline data
The POS currently keeps its operational data in browser local storage. Google Sheets remains the backup/sync destination when configured. Regular sync/backups are recommended because browser storage can be cleared by the browser/device.

## Google Sheets
Keep the Google Sheet itself private. The POS only needs the Apps Script Web App URL configured in the Sync section. Do not place the spreadsheet ID or credentials directly in the frontend.
