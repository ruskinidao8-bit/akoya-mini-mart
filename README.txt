AKOYA MINI MART POS — PWA

Files:
- index.html              Main POS application
- manifest.json           Installable PWA settings
- service-worker.js       Offline app-shell caching
- icons/                  App icons

How to test:
1. Serve this folder over HTTPS or localhost. Service workers do not work from file://.
2. Open index.html through the local web server.
3. Use the browser's Install option or the Install AKOYA POS button.
4. After the first successful load, the app shell is cached for offline use.

Data:
The current POS continues to use its existing localStorage data. Google Sheets sync remains available when internet access is present.

Important:
Offline use keeps data on the device. Back up/sync regularly because browser storage is not a substitute for a database backup.
