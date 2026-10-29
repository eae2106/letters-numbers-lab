# Letters & Numbers Lab

A tablet activity for kindergarten readiness. It says the name of a letter or number, and the child touches it from 2 or 3 choices. The caregiver chooses between two modes:
- **Practice** gives feedback and shows the right answer.
- **Check** responds the same calm way to every answer and fills in a readiness grid.

## Privacy and safety
- **Nothing leaves the device.** There are no accounts, no analytics, no trackers, no cookies and no outside requests. All answers are saved only in the browser on the device being used.
- **No personal details.** The app never asks for a child's name, birthday or any other personal information.
- **Locked to its own files.** A Content-Security-Policy blocks the page from loading or sending anything to another site.
- **Kept out of search engines.** The page is marked noindex, and `robots.txt` disallows all crawling.
- **Data stays under the caregiver's control.** To share results, the caregiver saves a CSV file from "Readiness and records" and sends it themselves. "Delete all" removes every record from that device.

## Install on a tablet
- **iPad / iPhone:** open the address in Safari, tap Share, then tap Add to Home Screen.
- **Android:** open the address in Chrome, tap the ⋮ menu, then tap Add to Home screen (or Install app).
- After the first visit it also works offline.

## Light and dark screen
Settings → **Screen** offers three choices:
- **Auto** (the default) follows the tablet's own light or dark setting.
- **Light** and **Dark** always use that look.

The choice is saved on the device.

## Updating
Replace `index.html` and change the cache name in `sw.js`. Devices pick up the new version the next time they open the app online.
