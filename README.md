# GROUND ZERO — WOLF-01

Upgraded directly from the original Winter Arc source. Includes workout mission plan, character blueprint, baseline body measurements, run/walk interval presets, signature kimbap-inspired meal check-in, existing activity logs, daily sequence, calendar, journal and offline PWA assets.

## Preserve data
The app deliberately uses the original `winter-arc-iron-wall-v1` browser localStorage key to read your existing data, **if you install this update at the exact same website origin and browser storage context**. Hosting it at a different address or opening a local file will not migrate iPhone data automatically. Export your existing Winter Arc backup first; if using a different origin, use System > Import Backup in the new app. Never uninstall, clear site data, or erase the old app before verifying the data appeared.

## Deploy
Upload all files to the same HTTPS site used for Winter Arc, with index.html at root; hard refresh or reopen after service worker update. When running on a new site, open online once to install cache and use Safari > Share > Add to Home Screen.

## Limitation
iOS may pause browser speech when the screen locks. A native running interval app is recommended for dependable lock-screen cues. No account/cloud sync.