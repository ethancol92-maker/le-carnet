# Hosting Le Carnet as an installable app — GitHub Pages walkthrough

You need a real HTTPS URL for "Add to Home Screen" and PWABuilder to work — a
downloaded file on your phone isn't enough. GitHub Pages is free and takes
about 5 minutes.

## 1. Create a GitHub account (skip if you have one)
https://github.com/join

## 2. Create a new repository
- Click the "+" top-right → "New repository"
- Name it something like `le-carnet` (repo can be Public or Private — Public
  is required for free GitHub Pages)
- Don't add a README — leave it empty
- Click "Create repository"

## 3. Upload the files
- On the new repo's page, click "uploading an existing file"
- Drag in all 8 files from the `le-carnet-pwa` folder you downloaded:
  `index.html`, `app.html`, `manifest.json`, `sw.js`, `icon-192.png`,
  `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png`
- Scroll down, click "Commit changes"

## 4. Turn on Pages
- Go to the repo's **Settings** tab → **Pages** (left sidebar)
- Under "Build and deployment" → Source: **Deploy from a branch**
- Branch: **main**, folder: **/ (root)** → Save
- Wait ~1 minute, then refresh — GitHub will show you the live URL, something
  like `https://yourusername.github.io/le-carnet/`

## 5. Install it on Android
- Open that URL in Chrome on your phone
- Tap the **⋮** menu → **Add to Home screen** (or Chrome may prompt you
  automatically)
- It now opens full-screen with its own icon, like any other app, and works
  offline after the first load

## 6. (Optional) Get a real .apk
- Go to https://www.pwabuilder.com
- Paste your GitHub Pages URL, let it scan the site
- Go to the "Android" package option → download the signed `.apk`/`.aab`
- Side-load the `.apk` directly on your phone, or use the `.aab` to publish
  to the Play Store later if you ever want to

Any time you want to update the app, just re-upload the changed file(s) to
the same repo — GitHub Pages updates automatically within a minute or two,
and your installed home-screen app will pick up the change next time it's
opened with a connection (the service worker checks for updates each load).
