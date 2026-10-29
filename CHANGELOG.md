# Changelog — Letters & Numbers Lab

Version numbers follow **MAJOR.MINOR.PATCH**:
- **MAJOR** changes when an update breaks old records or changes how things work.
- **MINOR** changes for new features, which arrive switched off or on safe defaults.
- **PATCH** changes for fixes only.

Each version is a git tag (`v1.2.0`) and has its own pull request.

## [1.4.0] — 2026-10-29
### Added
- **Child profiles.** Tap the child's name on the home screen to change it. Each child has their own records, settings, readiness grid and background.
  - A nickname and a picture are enough.
  - Existing data becomes "Child 1" automatically, and nothing is lost.
  - Deleting a child asks first and removes only that child's records.
  - CSV exports cover the current child, with a `profile` column.
  - Backups hold every child. Older backups still restore, into Child 1.
- **Backgrounds.** Settings → Background offers Plain (the default), Sky, Sand, Forest or **My photo**.
  - Each comes in a light and a dark version.
  - The cards stay solid, so letters never sit on top of a picture.
  - Photos are shrunk on the tablet (to 1600 px), softened and dimmed, and kept on the tablet for that child only. They aren't included in backups.
  - Records note the background (`background` column).
- **Session timer (Practice only).** Settings → Session timer offers Off (the default), 3, 5 or 10 minutes.
  - A shrinking circle shows the time left, and Pause stops the clock.
  - When time is up, the turn in progress finishes; then Next ends the session with "Time is up. Nice work!".
  - Check never shows the timer.

## [1.3.0] — 2026-10-29
### Added
- **Celebrations (Practice only).** Settings → Celebrations offers three levels, and the default is **Off**:
  - **Off:** no celebration.
  - **Calm:** a soft chime, a one-time glow, and a star in a jar of 5.
  - **Lively:** Calm plus a confetti burst of about 1 second.
- **Star jar.** When the jar fills, a gentle chord and glow play, then the jar empties for the next round.
- **Celebrate every right answer, every 2nd or every 3rd.** Celebrating less often over time keeps the focus on the letters.
- **Guardrails:**
  - Nothing happens on wrong taps or repeat taps; each question can be celebrated only once.
  - No flashing, no looping and no rising-pitch sounds.
  - The tablet's Reduce Motion setting turns off all movement.
  - **Check never celebrates.**
- **Extra taps after answering.** Every touch is counted. The readiness page shows the average and gives a gentle warning if he may be tapping for the effects.
  - The CSV gains `taps` and `celebration` columns.

## [1.2.0] — 2026-10-29
### Added
- **Voices.** Settings → Voice offers four:
  - US female (built in)
  - US male
  - UK female
  - UK male

  The extra voices download once when picked and then work offline. The UK voices say "zed" for Z. Every record notes which voice asked the question.
- **Backup & restore.** Readiness and records → Save backup produces a `.json` file with every record and setting.
  - **Restore from backup** adds any missing records.
  - It never duplicates or deletes records, and it refuses files that aren't from this app.
- **Answer time.** Each answer records how long it took after the question finished.
  - The records table has a new Time column.
  - The readiness page shows the typical answer time.
  - The CSV gains `latency_ms`, `voice` and `version` columns.
- **Storage protection.** The app asks the browser not to clear its storage.
- **Version shown** at the bottom of Settings.

### Changed
- The service worker cache is now `lnl-v3-1.2.0`. Voice packs are kept in their own `voicepacks-1` store, so app updates don't delete them.

## [1.1.0] — 2026-10-29
### Added
- **Dark mode.** Settings → Screen offers Auto, Light or Dark. Auto follows the tablet's own setting.

## [1.0.0] — 2026-10-28
### Added
- First public version:
  - Practice and Check modes.
  - Uppercase, lowercase, 0–10 and 0–20.
  - 2 or 3 choices.
  - Readiness grid.
  - CSV export.
  - Works offline and installs to the home screen.
  - Locked to its own files.
