# Changelog — Letters & Numbers Lab

Version numbers follow **MAJOR.MINOR.PATCH**:
- **MAJOR** changes when an update breaks old records or changes how things work.
- **MINOR** changes for new features, which arrive switched off or on safe defaults.
- **PATCH** changes for fixes only.

Each version is a git tag (`v1.2.0`) and has its own pull request.

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
