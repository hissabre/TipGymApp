# TIP

Personal workout app: generated workouts by body part, equipment and time, follow-along programs, guided stretching and yoga, and progressive overload tracking. Runs fully in the browser; data stays on your phone.

## Put it online (GitHub Pages)

1. On github.com, create a new public repository, for example `tip`.
2. Click **Add file → Upload files** and drag in everything from this folder (`index.html`, `manifest.webmanifest`, `sw.js`, `README.md` and the `icons` folder). Commit.
3. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute your app is live at `https://YOUR-USERNAME.github.io/tip/`.

## Install it on your phone

- **iPhone (Safari):** open the link, tap **Share → Add to Home Screen**.
- **Android (Chrome):** open the link, tap **⋮ → Install app** (or Add to Home screen).

It opens full-screen with the TIP icon and keeps working offline after the first visit.

## Updating

Upload the new `index.html` over the old one. To make phones pick it up right away, change `tip-v1` to `tip-v2` in `sw.js` and upload that too.

## Your data

Workouts are saved in the phone's browser storage. Use **Settings → Export backup** now and then, and keep the file somewhere safe. Deleting the home-screen app or clearing Safari data erases it.

## Progress photos

Photos are stored on your phone only (in the app's private storage). They are never uploaded and are not part of the backup file. The live camera with the alignment guide works in the installed app; if your browser blocks the camera, TIP opens your phone's camera app instead.
