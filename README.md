# BOP Expenses – Deployment Guide

## Files in this folder
```
index.html      ← the entire app
manifest.json   ← PWA metadata
sw.js           ← service worker (offline support)
icon-192.png    ← app icon
icon-512.png    ← app icon (large)
```

## Deploy to GitHub Pages (one time)

1. Go to github.com → New repository
   - Name it something like `bop-expenses`
   - Set to **Public**
   - Click "Create repository"

2. Upload all 5 files from this folder to the repository
   (use the "uploading an existing file" link on the repo page)

3. Go to **Settings → Pages**
   - Source: `Deploy from a branch`
   - Branch: `main` / `(root)`
   - Click **Save**

4. Wait ~60 seconds. Your app URL will be:
   `https://YOUR-USERNAME.github.io/bop-expenses/`

## Install on your Android phone

1. Open the URL above in **Chrome** on your Android phone
2. Chrome will show a banner: "Add to Home Screen" → tap it
   (Or: Chrome menu → "Add to Home Screen")
3. The app installs like a native app

## First run

1. Get an Anthropic API key from console.anthropic.com
   (You'll need to add a small amount of credit – receipt extraction
    uses claude-haiku which costs roughly $0.001 per receipt)
2. Enter the key in the app's setup screen – it stays on your phone only

## Updates

When you want to update the app, just replace files in the GitHub repo.
The service worker will pick up changes on next app open.
