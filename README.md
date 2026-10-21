# WINTER ARC — PROJECT IRON WALL

An offline-capable iPhone-friendly web app prototype for the 90-day training launch (Oct 21, 2026–Jan 18, 2027).

## Features
- Daily sequential mission checklist, editable under SYSTEM
- Voice-led walk/jog interval timer with walk duration, jog duration and rounds
- Timestamp-backed timing (correct elapsed duration after background / screen-lock suspension)
- Full-body strength log with weekly split, exercise/weight/reps/sets
- Daily mobility checks
- Recording checklist and private journal
- Optional body metrics and monthly-progress notes
- Local backup export/import as JSON; no cloud account required
- Offline use after HTTPS installation + initial visit (service worker)

## Install on iPhone
1. Deploy the **contents** of this folder to a secure HTTPS static site (e.g. GitHub Pages). Keep `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg` together.
2. In iPhone Safari, open the HTTPS app URL, Share → Add to Home Screen.
3. Open the Home Screen app once while online to cache assets.
4. Try Airplane Mode after cache is ready to verify offline operation.

## Critical limitation (not hidden)
No iPhone web app can *guarantee* spoken timers continue when Safari/PWA is locked/backgrounded. This app calculates interval elapsed time from real timestamps and catches up upon resuming, but iOS can suspend JavaScript speech and timers. Use a native app (Intervals Pro / Seconds Pro) for reliable locked-screen spoken cues. A native Swift/iOS audio-session implementation is the next step for the exact requested behavior.

## Backups and media
App data stays in localStorage. Back up under SYSTEM → EXPORT BACKUP frequently. Clearing Safari data or reinstalling can lose data. Recording files live in Apple Photos, not the app; create an album and verify cloud backups independently.

## Testing checklist
- Start interval with audible cues, lock iPhone for 2+ minutes, unlock and confirm clock catches up. Background cues are NOT guaranteed.
- Add a lift and cardio log, reload and check persistence.
- Check one daily task; reload and verify state.
- Export JSON, import and verify values.
- Install over HTTPS, load once, then check offline reload.
- Test iPhone dark-mode appearance, Safari Add to Home Screen, call interruptions.