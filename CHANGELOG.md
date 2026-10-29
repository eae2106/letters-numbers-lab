# Changelog — Letters & Numbers Lab

Version numbers follow **MAJOR.MINOR.PATCH**:
- **MAJOR** changes when an update breaks old records or changes how things work.
- **MINOR** changes for new features, which arrive switched off or on safe defaults.
- **PATCH** changes for fixes only.

Each version is a git tag (`v1.2.0`) and has its own pull request.

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
