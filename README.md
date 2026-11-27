# Monthly Budget

A simple, phone-friendly monthly budget app. Set your income and category budgets, log expenses as you go, and see what's left to spend each day. It installs to your home screen with its own icon and works offline.

Your data is stored **only on your device** (in the browser's local storage). Nothing is sent anywhere. Use **Plan → Export backup** now and then, and **Import backup** to move to a new phone.

## Put it on GitHub Pages

1. On GitHub, click **New repository**. Name it, for example, `monthly-budget`, and make it **Public**. (Pages on private repos needs a paid plan.)
2. On the new repo's page, click **uploading an existing file**. Drag in everything from this folder, including the `icons` folder, then click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source** to *Deploy from a branch*, then pick branch **main** and folder **/ (root)**. Click **Save**.
4. Wait a minute or two, then refresh the page. GitHub shows your site's address, something like
   `https://YOUR-USERNAME.github.io/monthly-budget/`

Prefer the command line?

```bash
cd monthly-budget
git init -b main
git add .
git commit -m "Monthly Budget app"
git remote add origin https://github.com/YOUR-USERNAME/monthly-budget.git
git push -u origin main
```

Then do step 3 above.

## Install it on your phone

- **iPhone (Safari):** open your site's address, tap the **Share** button, then **Add to Home Screen**.
- **Android (Chrome):** open the address, tap the **⋮** menu, then **Install app** (or **Add to Home screen**).

It opens full screen like a normal app and keeps working without a connection.

## Updating the app

After you change any file, open `sw.js` and bump `VERSION` (for example `budget-v1` → `budget-v2`) before you upload. Phones then pick up the new version the next time the app is opened online. Updating the app doesn't touch your saved data.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app: layout, styles and code |
| `manifest.webmanifest` | App name, colours and icons used when installing |
| `sw.js` | Service worker that makes it work offline |
| `icons/` | App icons for home screens, plus favicons |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
