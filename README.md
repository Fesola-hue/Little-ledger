# Little Ledger

A small, free budget PWA. Enter a month's income, add or edit categories and their percentages, then check in with rough totals. It starts with four categories, but you can add more or remove them. Data stays in that browser on that device. A 6–12 digit PIN can encrypt it locally; backup and restore are available in **Edit split**.

## Deploy on Vercel

Import this repository in Vercel and deploy. `vercel.json` points Vercel to the ready-built `dist` directory; no build command, database, login, or paid service is required. The app needs HTTPS for installation and PIN encryption; Vercel provides HTTPS on its deployment URLs.

To install on a phone, open the deployed URL in the browser and use **Add to Home Screen** or **Install app**. Browser support and menu wording vary.

**If you already use another Little Ledger URL:** save a backup from that app first. Browser storage is tied to the origin, so a new Vercel URL starts with an empty budget. Open the new URL and restore the backup there. Keep the PIN if the backup is encrypted.

## Run locally

Serve `dist` with any static server, for example `python3 -m http.server 8000 -d dist`, and open `http://localhost:8000`. A production installation should use HTTPS.

## Files

- `dist/index.html`: app, styles, and behavior
- `dist/guide.html`: beginner handbook
- `dist/sw.js`, `dist/manifest.webmanifest`, `dist/icon*`: offline PWA support
- `vercel.json`: static Vercel deployment configuration

The app is open source under the MIT license. It does not use analytics or a server to collect budgets.
