# ACL Rehab Tracker — personal, phone-first app

A free, mobile-first web app built from `ACL_Rehabilitation_Weekly_Tracker.xlsx`. It is designed for one person and stores data locally in the browser on the device where it is used. No account, database or cloud sync is included.

## Included
- Original 33 exercises from the four spreadsheet blocks, with additional optional library suggestions in each block.
- Clinical-style movement schematics on exercise cards (simple visual cues, not technique instruction).
- Approval status for each exercise: Not yet approved, Approved or Retired. New and existing items default to Not yet approved.
- Editable physio-prescribed sets, reps, holds, resistance, side instructions and notes; dosage fields remain blank until entered.
- Add your own exercise to any of the four blocks.
- Day-by-day weekly planner and completion ticks.
- Pain, swelling, stiffness and free-text symptom log.
- Seven-day completion graph and symptom history.
- Per-exercise video URL field plus a YouTube search shortcut.
- Local browser save and JSON export/import backup.

## Use on iPhone
For an installable home-screen app and reliable offline support, deploy the folder to a free HTTPS static host (for example GitHub Pages or Cloudflare Pages), open its HTTPS address in Safari, then choose Share → Add to Home Screen. The hosting serves the app files only; your rehab records remain in local browser storage on that iPhone. There is no cross-device sync.

You can also open `index.html` directly for a quick preview, but local-file browser behaviour is less reliable for saving and offline app features.

## Backup
Use Settings → Export backup regularly. Import that JSON file to restore your data. Local browser data can be lost if website data is cleared or the app is opened under a different browser/origin.

## Important clinical boundary
This app is a record-keeping and planning tool, not a rehabilitation prescription. The additional exercises are optional library ideas only. They are not recommendations to start or progress them. Leave every item as **Not yet approved** until your physiotherapist confirms it is suitable for your current stage and specifies the dosage, frequency, range and progression. Impact and plyometric work must remain specifically cleared by your clinical team. The schematics are simplified visual cues, not a substitute for a clinician demonstration or a reliable exercise video.
