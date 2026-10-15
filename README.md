# spa-chairs

A six-chair timer for the VR massage spa. Staff tap a chair on any phone; every phone
shows it running and flashes red when its time is up. No sign-in, no laptop.

**Open:** `https://quicksketcherz.github.io/spa-chairs/#<room>`. The part after `#` is the room code;
every phone with the same link shares the same chairs. The **QR** button on the page shows the link
for the next phone. Open it in Safari, then Share → Add to Home Screen.

- The dot next to "Spa chairs": green **live** = synced.
- Tap a box to start (5:00). Tap a running box twice to stop early. Amber from 1:00, red when up.
  Tap a red box = seen; tap again after reseating = next guest.
- **− / +** minutes for all six. **Layout** = tap two boxes to swap. Long-press the tally to reset it.

The chairs live in Firebase Realtime Database (project `spa-chairs`), under `rooms/<room>`.
Rules: nothing can be listed; a room can be read and written only by someone who knows its code.
The room code is never in this repo, so keep the link to the staff.

Source of truth: `spa-chair-timer/web/index.html` in the private TD-SKETCHES26 repo.
