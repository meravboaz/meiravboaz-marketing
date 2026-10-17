# Website changelog: meiravboaz.co.il

Newest first.

- 2026-10-17: Added a hero headline at the bottom of the main image on `index.html` (approved by Merav after screenshot previews): h2 "המוח לא יוצא לפנסיה..." and the subtitle "קורס מוסיקה למבוגרים בנס ציונה: שרים, מנגנים, זוכרים ונהנים, בקבוצה קטנה וחמה." Plain text on the image with a text shadow, no background box (Merav asked to remove it). Placed above the floating WhatsApp button on phones. Chosen over competitor-style wording ("מאמנת את המוח כמו שריר", "החיים מתחילים בגיל 60"); avoids health claims.
- 2026-10-17: Call buttons on computers (Merav reported they tried to open an app): on mouse devices, "call me" buttons now scroll to the contact section and highlight the number line; clicking a number itself copies it and shows "המספר הועתק ✓". Phones and tablets dial as before. Code is in `index.html` <head>, after the conversion listener; phone clicks are still counted as conversions. Tested live on desktop and in mobile emulation.
- 2026-10-17: Added Google Ads conversion events to `index.html` (one click listener after the gtag config): WhatsApp taps → `AW-18449420494/_vn4CKH8kKAdEM6hr91E`, phone taps → `AW-18449420494/s4wwCKT8kKAdEM6hr91E`. Kids page left without them so show inquiries don't mix with course leads. Visitors see no change. Tested on the live site: both clicks sent conversion hits.
- 2026-10-17: Checked video loading on the live site: videos have `preload="none"` and only `data-src`; they load only after a click on play. Scrolling the whole page loaded ~1 MB and no .mp4 (the 3 videos total ~32 MB).
- 2026-10-10: Added Meta Pixel `1102922088890690` (PageView) to `index.html` and `Kids.html`: the script in <head>, the noscript fallback right after <body>.
- 2026-10-10: Added a hidden HTML comment to `index.html` to test the GitHub → Netlify deploy. Visitors see no change. Deploy succeeded.
- 2026-10-10: Moved the site from manual Netlify uploads to GitHub (`meravboaz/meiravboaz-site`). Netlify now deploys automatically on every push to `main`.
- 2026-10-04: Last manual upload (included the Google Ads tag AW-18449420494).

## Open items
- Planned (2026-10-17): replace the hero photo with a slow 3-image crossfade (1. circle laughing, 2. ribbons/movement, 3. recorders close-up), strongest image first, still image for reduced-motion. Frames picked from Merav's WhatsApp videos were too small (848px), so Merav will film the current course in 4K and send originals (not via WhatsApp).
- Kids page (`Kids.html`) still shows placeholder text for the three show names and descriptions (`[שם המופע הראשון]` and so on).
- Email taps aren't tracked (only WhatsApp and phone were requested).
- Add Meta `Contact` events for WhatsApp, phone and email taps, so Meta counts leads and not just page views.
