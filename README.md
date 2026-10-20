# Punch Person — PWA starter

A mobile-friendly, separate-page Progressive Web App starter for personal routines, timers, attendance, goals, reports, and a friends UI.

## Current features
- Home dashboard and separate navigation pages
- Editable activity schedule, starting with 04:00 wake-up and a 04:00–08:00 morning block
- Configurable bedtime and display name in Settings
- Focus timer with start/pause/reset and completion flow
- Wake-up clock-photo selection and preview
- Attendance calendar, weekly reflection, goals, activity breakdown, CSV export
- Local friend list UI and sample progress comparison
- Installable PWA manifest and service-worker offline shell

## Important limitations
This starter stores routine metadata and check-in records in browser `localStorage` on the current device. It does **not** implement secure login, cross-device synchronization, real invitation links, server-side photo storage, scheduled background notifications, or verified photo timestamps. The photo picker is a front-end flow only; do not use it as proof of identity or time. Friend progress is local/demo data until a backend is connected.

## Run locally
Because service workers and PWA installation require a secure context, use HTTPS hosting or localhost. You can preview `index.html` directly, but install/offline features will not fully work from a `file://` URL.

For local testing with Python:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000` in a browser.

## Deploy
Upload the contents of this folder to a static HTTPS host. To support real invited friends, accounts, private evidence and multi-device sync, connect an authentication/database/storage backend and enforce per-user permissions before collecting any personal data.
