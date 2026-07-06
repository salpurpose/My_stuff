# Put the Cash Flow tool on your iPhone (free, no Mac, no App Store)

This turns the tool into a home-screen app on your iPhone using a **PWA** ("Add to Home
Screen"). You host these files once on **GitHub Pages** (free), then install it from Safari.

Everything in this `pwa` folder is what gets uploaded:
`index.html`, `manifest.webmanifest`, `sw.js`, `icon-180.png`, `icon-192.png`, `icon-512.png`.

---

## Part 1 — Host it on GitHub Pages (do once, ~10 min, all in a web browser)

1. Go to **github.com** and create a free account (skip if you have one).
2. Click **+** (top-right) → **New repository**.
   - Repository name: `cashflow-tool` (or any name)
   - Set it to **Public**
   - Click **Create repository**
3. On the new repo page, click **Add file → Upload files**.
   - Drag in all six files from this `pwa` folder.
   - Scroll down, click **Commit changes**.
4. Click **Settings** (top of the repo) → **Pages** (left sidebar).
   - Under **Source**, choose **Deploy from a branch**.
   - Branch: **main**, folder: **/ (root)** → click **Save**.
5. Wait about 1 minute, then refresh. GitHub shows your live link, which looks like:
   **`https://YOUR-USERNAME.github.io/cashflow-tool/`**

That link is your app. (Bookmark it.)

---

## Part 2 — Install it on your iPhone (do once)

1. Open **Safari** on your iPhone (this only works in Safari, not Chrome).
2. Go to your link: `https://YOUR-USERNAME.github.io/cashflow-tool/`
3. Tap the **Share** button (the square with an up-arrow).
4. Scroll down and tap **Add to Home Screen** → **Add**.
5. You now have a **Cash Flow** icon on your home screen. Open it — it runs full-screen like a
   real app and works **offline** after the first open.

---

## Important tips

- **Enter your budget inside the installed app.** The home-screen app has its own private storage,
  separate from the Safari tab. Whatever you type stays **only on your iPhone** — nothing is uploaded.
- **Back up occasionally.** Use the app's **Export data (.json)** button now and then and save the
  file (e.g. to Files or email it to yourself). iPhones can clear an app's storage if it goes unused
  for a long time; the export is your safety net. Use **Import data (.json)** to restore.
- **The GitHub link is public, but your money data is not.** Only the app's code is public; your
  numbers never leave your phone. If you'd rather the link be hard to find, use an unusual repository
  name.

---

## Updating the app later (if you change the tool)

1. Copy the latest `cashflow-tool.html` over this folder's `index.html` (replace it).
2. Open `sw.js` and change `cashflow-v1` to `cashflow-v2` (bump the number). This makes iPhones
   pick up the new version instead of the cached old one.
3. On GitHub: **Add file → Upload files**, drop in the changed files, **Commit changes**.
4. On your iPhone, open the app (while online) once to let it update.
