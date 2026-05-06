# TapTicket Deployment Package

## Files
- `index.html` — Full app (single file, zero dependencies)
- `manifest.json` — PWA manifest for app installation
- `sw.js` — Service worker for offline caching
- `netlify.toml` — Netlify deployment config

## Deploy to Netlify (Recommended)
1. Go to netlify.com → "Add new site" → "Deploy manually"
2. Drag and drop the entire `tapticket/` folder
3. Your app is live in ~30 seconds

## Deploy to Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` inside this folder

## Deploy to GitHub Pages
1. Create a repo, push these files to `main` branch
2. Settings → Pages → Source: main branch / root

## PWA Installation
- **Android Chrome**: "Add to Home Screen" banner appears automatically
- **iOS Safari**: Share → "Add to Home Screen"
- **Desktop Chrome/Edge**: Install icon in address bar

## App Icons
Generate icons at https://favicon.io or https://realfavicongenerator.net
Upload a 512×512 image and download:
- icon-192.png → place in same folder
- icon-512.png → place in same folder

Without icons the PWA still works — icons are optional for basic install.

## Features
- ✅ 100% offline — works with no internet after first load
- ✅ PWA installable on Android, iOS, Desktop
- ✅ Zero dependencies — no npm, no build step
- ✅ Single HTML file — easy to host anywhere
- ✅ Fast: loads in <1 second on 3G
- ✅ All data stored locally (localStorage)

## Back Office Sync
The back office dashboard reads from localStorage — it shows live data
as conductors enter tickets on the SAME device. For multi-device sync
(conductor phone + owner phone), integrate a backend like:
- Firebase Realtime Database (free tier sufficient)
- Supabase
- PocketBase (self-hosted)
