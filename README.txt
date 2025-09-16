ADHD Pomodoro – Minimal (v0.3 PWA)
==================================

What this is
------------
A single-page, offline-first Pomodoro timer tailored for ADHD:
- Flexible intervals (presets + custom)
- Planner with Today/Tomorrow tasks and carry-over
- Active task links to session logs
- Daily/All CSV exports for logs, JSON export/import for tasks
- Works offline via service worker (PWA)

How to deploy to GitHub Pages
-----------------------------
1) Create a new repo on GitHub (public or private with Pages enabled).
2) Upload the contents of this folder (index.html, manifest.webmanifest, service-worker.js, icons/, VERSION.txt, README.txt).
3) In your repo: Settings → Pages → Set Source to the default branch (usually 'main'), folder: / (root).
4) Wait for the Pages URL (e.g., https://USERNAME.github.io/REPO/).
5) Open that URL in Chrome/Edge/Android Chrome:
   - You should see an "Install app" option (address bar or ⋮ menu).
   - On iOS Safari: Share → Add to Home Screen.

Notes
-----
- All assets use relative paths ('./') so it will work from your REPO subpath.
- If you change what the service worker caches, bump 'CACHE' in service-worker.js (e.g., 'pomodoro-v0-4').
- Avoid external scripts/fonts so it works fully offline.
- Mobile browsers may throttle timers in the background; keep the screen on during focus blocks if you need precise beeps.

Security/Privacy
----------------
- Data is stored locally in your browser (localStorage). No network is used by the app itself.
- Import/Export are manual file actions initiated by you.

License
-------
MIT
