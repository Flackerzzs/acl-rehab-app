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


## Version 10 – Stretching and hydrotherapy image repair

The live GitHub repository was missing the requested image files: direct checks of `assets/block5-01.jpg` and `assets/hydro-01.jpg` on the published repository returned 404. This release includes the complete assets folder plus explicit `stretch-01.jpg`…`stretch-07.jpg` and `hydrotherapy-01.jpg`…`hydrotherapy-08.jpg` files. The app references these explicit names and pre-caches them in a newly versioned service worker. If an image still fails to load, a visible movement-reference fallback is shown instead of a broken-image icon.

**Important upload instruction:** upload the complete `assets` folder from this ZIP, not only the files at the top level. On GitHub, use Add file → Upload files and drag the `assets` folder itself (containing all image files) into the upload area. Commit the update.


## Version 11 – Running and Speediance physio register

- Added Running as a future training mode with session type, duration, weekly frequency, effort ceiling, clearance gate, and clinician-entered return-to-run criteria. It defaults to Not cleared and is excluded from automatic weekly planning unless explicit clearance and frequency are entered.
- Added 23 previously recorded Speediance exercises across Upper, Rehab Lower 1 and Rehab Lower 2, including historical loads, sets and reps where available. Each entry can be edited and marked To review / Approved / Modify / Avoid with physio notes.
- One Rehab Lower 2 unilateral exercise was cropped/unidentified in the original record; it is deliberately labelled for confirmation rather than guessed.
- The printable physio review sheet now includes the Speediance exercise register.
- Running is a planning/logging placeholder only. The app does not determine when running is safe or prescribe return-to-run progression.


## Version 12 – Running and Speediance exercise library refinement

This release contains a future Running training mode (default Not cleared) and the user's 23 previously recorded Speediance exercises across Upper, Rehab Lower 1 and Rehab Lower 2. Historical loads and rep schemes are retained for discussion only. The unidentified 10 kg unilateral movement in Rehab Lower 2 remains explicitly flagged for the user/physio to identify. The printable physio review report includes these entries.


## Version 13 – Physio session journal and interface refinement

- Added a dedicated Physio Sessions page with date, clinician, appointment type, next appointment, focus, observations, treatment, exercise changes, home programme, restrictions, goals, questions and personal notes.
- Sessions can be edited, deleted, viewed chronologically, and printed as a session-history report.
- Visit records are stored in the existing local app state and included in JSON backup/restore.
- Added compact session summary metrics and progressive disclosure: detailed fields are tucked into expandable sections.
- Refined typography, spacing, cards, form controls, page headings and bottom navigation for phone screens. The bottom navigation can scroll horizontally where all tabs do not fit.
- Simplified repeated explanatory copy while retaining key clinical safety messages and backup guidance.


## Version 14 – Dark appearance and exercise navigation icon

- Replaced the Exercises bottom-navigation plus symbol with a custom kettlebell SVG, keeping the Physio symbol distinct.
- Added automatic Dark Mode support using the device/browser `prefers-color-scheme` setting. The app follows the iPhone's system appearance rather than adding a separate in-app theme switch.
- Added dark variants for cards, forms, inputs, selectors, navigation, exercise illustrations, tags, charts and session records.
- Updated the web app manifest and service-worker cache version for the dark appearance.


## Version 15 – Flackys ACL Rehab dashboard and mobile fixes

- Renamed the app to Flackys ACL Rehab in the page title and web app manifest.
- Fixed the weekly-plan training session picker: dark background, constrained form controls, two-column layout on wider phones and single-column layout on narrow phones; buttons and inputs stay within the card.
- Reworked the bottom navigation to an eight-column inline grid so all tabs fit the phone width without horizontal overflow.
- Added a surgery-date-based recovery day/week counter and a broad educational graft-remodelling phase card on the home page.
- Added a graft anatomy illustration and a collapsible explanation with clinical-source links. The phase is an educational estimate only and is not a measurement of graft strength or readiness.
- Added individual exercise thumbnails to the Speediance exercise register, using generated upper-body illustrations and existing movement reference illustrations for lower-body movements.
