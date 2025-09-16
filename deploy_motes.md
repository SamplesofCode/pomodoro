# Deploy Notes – ADHD Pomodoro PWA

Whenever you update **HTML, CSS, or JS**, you must bump the cache name in
`service-worker.js` to force clients to pull the new files.

---

## Steps for every release

1. **Update cache version**
   - Open `service-worker.js`
   - Change:
     ```js
     const CACHE = 'pomodoro-v0-3-1';
     ```
     to the next version (e.g., `'pomodoro-v0-3-2'`).

2. **Commit & push**
   - `git add .`
   - `git commit -m "Release v0.3.2 (UI fix + new styles)"`
   - `git push`

3. **Verify GitHub Pages deploy**
   - Open https://samplesofcode.github.io/pomodoro
   - Force-refresh in the browser (Ctrl+Shift+R or ⌘+Shift+R).

4. **Verify PWA update**
   - Close the installed app (swipe it away).
   - Reopen → new version should be active.

---

## Tips

- **Always bump the cache** when UI changes (HTML, CSS, JS).
- **Icons/manifest** rarely change, but if you do update them, also bump the cache.
- To test, check DevTools → Application → Service Workers → "Skip Waiting" to see the new worker activate instantly.
- Consider syncing `CACHE` string with repo tag version for clarity.

---

_Last updated: 2025-09-16_