# ACL Rehab & Performance – Version 7

A personal, phone-first rehabilitation and training planner. It is a record-keeping and scheduling tool, not a clinical decision system.

## Main areas
- Overview: today's planned exercises, completion, symptoms and training log totals.
- Weekly plan: add and remove exercises by day, add Peloton / Speediance / swimming sessions, choose rest days, and generate a draft week.
- Exercise library: five blocks (activation/mobility, strength/stability, single-leg/functional, plyometrics/impact, stretching/mobility); edit names/descriptions, replace images, delete user-added exercises, retire built-in items, and record physio approval and dosage.
- Physio review: clinical profile, exercise approval, sets/reps/holds/resistance, weekly frequency, priority, auto-plan inclusion, range, restrictions, progression criteria, review date, clinical notes, JSON export and printable review sheet.
- Training hub: Peloton, Speediance and swimming settings, clinical-clearance gates, workout logging, RPE and performance notes, and 70.3 goal.
- Progress: pain, swelling, stiffness, fatigue, sleep and next-morning response history.
- Settings: backup and restore.

## iPhone Duo / Safari
- Responsive for narrow outer display, unfolded inner display, landscape and desktop widths.
- Bottom navigation scrolls horizontally on narrow screens.
- Uses safe-area insets, 16px form controls to avoid unwanted iOS zoom, Apple touch icon, PWA manifest and standalone display mode.
- Open the HTTPS website in Safari, Share → Add to Home Screen, then enable Open as Web App.
- On iPhone Duo, test both folded and unfolded layouts. Safari's outer-screen controls may reserve part of the visible area; the page uses responsive sizing and safe-area padding rather than assuming a fixed screen shape.

## Data and privacy
- No account, cloud database or sync. App records stay in browser storage on the device.
- Custom exercise images are stored in IndexedDB to reduce pressure on localStorage.
- Export a JSON backup before browser resets, clearing website data, or changing devices. Import the backup to restore records and custom images.
- Updating the GitHub Pages files at the same website origin should preserve the existing browser data. Do not clear Safari website data during an update.

## Auto-planner rules
- Exercise sessions are scheduled only when the exercise is marked Approved, included in Generate Week, and assigned a weekly frequency.
- Peloton, Speediance and swimming sessions are scheduled only when their training mode has an explicit Approved for planning clearance and a weekly target. Swimming also requires its own clearance.
- Priority, recent completed sessions, workload distribution and selected rest days influence placement.
- The generator does not decide medical priority, prescribe a frequency, increase load, or grant clinical clearance. Physio/user-entered settings control eligibility and targets.
- Generated weeks are drafts and must be reviewed with the treating physiotherapist.

## Clinical safety
Only enter exercise dosage, range, resistance, progression and restrictions after agreement with your surgeon or physiotherapist. The Stretching & Mobility block is a candidate library for discussion, not a prescribed routine. Hamstring stretching should be specifically reviewed in the context of the hamstring graft. Plyometrics and impact remain gated by clinical approval.

## Update on GitHub Pages
Upload all files from this package to the existing repository, including the complete `assets` folder and the app icons, then commit the changes. Keep `index.html`, `app.js`, `exercises.json`, `manifest.webmanifest`, `sw.js`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, and `assets/` at the repository root. The service worker cache version is incremented to refresh the new release.

## Version 8 – Hydrotherapy (Block 7)

Added eight illustrated hydrotherapy library entries:
1. Forward water walking
2. Backward water walking
3. Lateral water walking
4. Supported marching
5. Pool calf raises
6. Supported mini-squat
7. Standing hamstring curl
8. Deep-water aqua jogging (later-stage option; flotation belt)

The existing Block 6 number is intentionally left open for future expansion, so Hydrotherapy appears as Block 7 as requested. All hydrotherapy entries default to Not yet approved, and their sets/reps/holds/frequency remain blank until entered with the physio.

Hydrotherapy is an optional adjunct to land-based ACL rehabilitation. The pool is the preferred environment because depth, temperature, footing, handrails and resistance can be controlled. Do not use sea water as a replacement for a therapy pool. Any shallow sea walking should be considered only if the clinician explicitly approves it and the location is calm, sheltered, shallow, with safe entry/exit and a companion. Avoid currents, waves, slippery/uneven footing and cold-water exposure. Do not enter water until wounds are fully healed and the surgical team has confirmed swimming is safe.


## Version 9 – Hydrotherapy as a separate recovery area

Hydrotherapy is no longer shown as an exercise-library block or included in the weekly auto-planner. It has a dedicated Hydrotherapy & Recovery tab with its own approval and prescription fields, session date/duration/notes logging, and session history. It is treated as occasional optional recovery work rather than a weekly target. The exercise entries remain part of the shared clinical data and can be reviewed in the Hydrotherapy section.
