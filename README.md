# MMXM Trader's Desk

An installable, offline web app (PWA) for the MMXM Traders mentorship:
24 lessons, a step-by-step trading playbook, 11 short explainer videos, a glossary,
and a guided 3-step trade journal.

## Publish on GitHub Pages

1. Create a new repository and upload everything in this folder (keep `.nojekyll`).
2. Repository **Settings → Pages → Build and deployment**:
   Source = *Deploy from a branch*, Branch = `main`, Folder = `/ (root)`. Save.
3. Wait about a minute, then open `https://<your-username>.github.io/<repo-name>/`.
4. Install it:
   - iPhone/iPad (Safari): Share → **Add to Home Screen**
   - Android / Chrome / Edge: menu → **Install app**

After the first visit the app works offline (lessons, playbook, videos, journal).

## Journal data

Journal entries and screenshots are saved **in your browser on that device** (IndexedDB).
They are never uploaded to GitHub. Use **Journal → Export** to back up, and **Import**
to restore or move entries to another device.

## Updating

Replace the files and push. The service worker cache name in `sw.js` (`mmxm-v2`)
should be bumped (e.g. `mmxm-v3`) on each release so devices pick up the new version.

## Files

- `index.html` – the whole app (content, diagrams, journal)
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png` – install metadata
- `sw.js` – offline cache
- `videos/` – explainer videos (`v1`–`v11`) and poster images
