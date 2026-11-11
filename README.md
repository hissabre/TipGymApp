# TIP

TIP is a personal workout app that runs in your phone's browser and installs to your home screen. Version 1.0.

- 261 animated exercises: free weights, machines, cables, bands, bodyweight, cardio, mobility, stretching and yoga
- Train now: pick a body part, your equipment and the minutes; the workout builds itself; swap anything
- Follow along: guided sets, a rest timer, a progress staircase, a screen that stays on, and a touch lock
- Plans: 9 multi-week programs that add load, reps or time from what you log
- Stretch: guided sessions with animated poses and steps
- Photos: weekly progress photos with an alignment guide, a before/after slider and a timelapse
- Progress: XP levels, badges, streaks, strength levels for your body weight, a calendar, "weight moved" comparisons, and recovery and strain from Apple Health

All data stays on your phone. Nothing is uploaded.

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

## Apple Health

A web app can't read Apple Health directly, so TIP offers two ways in:

**1. Full import (recommended first).** On your iPhone open Health → tap your picture → Export All Health Data → Export → Save to Files. In TIP go to Settings → Apple Health → Import Health export and choose the `export.zip`. TIP reads the last 12 months of sleep, HRV, resting heart rate, steps, active calories, body weight, height and workouts, right on your phone. Nothing is uploaded.

**2. Daily sync with a Shortcut (optional).** Build a shortcut that opens
`https://YOUR-USERNAME.github.io/tip/#health=` followed by URL-encoded JSON like
`{"date":"2026-11-09","sleep":7.2,"hrv":58,"rhr":54,"steps":8400}`.
Settings → Apple Health → "Daily sync with a Shortcut" lists the steps. Sleep may be in hours, minutes or seconds. Add a Shortcuts Automation to run it every morning.

TIP uses this to show a daily recovery score (HRV vs your 30-day baseline, resting heart rate, sleep), a strain score, insights, and Health workouts on the calendar. Low recovery holds back weight increases automatically.

## Keeping the screen on

During a workout TIP keeps the screen awake (Settings → You → Keep screen on). The lock button in Follow along blocks accidental taps; press and hold to unlock.
