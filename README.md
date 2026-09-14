# Shelf Life

A delivery-to-clearance expiry tracker for stores. Log deliveries, track items as they approach their expiry date, and see wastage trends before stock has to be cleared out or thrown away.

## Features

- Store accounts with sign in / sign up, backed by Firebase Authentication
- Per-store data synced to the cloud via Firestore, so any device can log in and see the same stock
- Log, edit, and filter deliveries (by category and delivered-date range)
- Bulk catalog import and on-demand catalog lookups
- Password strength hint on signup and self-service password reset via a recovery email
- Owner dashboard comparing wastage across stores
- Export to Excel
- Installable as a PWA (works offline-first, has app icons and a manifest)

## Running it locally

This is a single static page with no build step. Any static file server works, for example:

```bash
npx serve .
```

Then open the printed local URL in your browser.

> Note: sign-in and data sync require a Firebase project. The Firebase config is set in `index.html` — point it at your own project to run the app end-to-end.

## Tech stack

- Plain HTML/CSS/JavaScript — no framework, no bundler
- [Firebase](https://firebase.google.com/) (Auth + Firestore) for accounts and data sync
