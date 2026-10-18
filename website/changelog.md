# Website changelog: meiravboaz.co.il

Newest first.

- 2026-10-18: Hero subtitle changed to plural, approved by Merav after screenshot previews: "קורסי מוסיקה למבוגרים בנס ציונה: שרים, מנגנים, זוכרים ונהנים, בקבוצות קטנות וחמות."
- 2026-10-17: Added caption for testimonial video 3 (`v4.mp4`, seated in purple, 1:03): "בשבילי, זה היה ללמוד שפה חדשה וממש נהניתי" – סבטלנה, רחובות (Merav's wording). Merav also sent a second, vertical selfie video of Svetlana; undecided which to keep (garden video looks better; content is Merav's call).
- 2026-10-17: Testimonial videos section (`index.html`), approved by Merav after screenshot previews: added a caption under the carousel that follows the active video. Video 1 (`v1.mp4`, standing in a garden): "אני מגיעה לחוג שמחה ויוצאת מאושרת" – פיפי, חולון. Video 2 (`v2.mp4`, close-up with glasses): "המשתתפים מחכים מדי שבוע למפגש הבא ולתכנית ההמשך" – אביבה, מזכרת בתיה. Video 3 (`v4.mp4`, seated in purple) has no caption yet (space kept, hidden).
- 2026-10-17: `videos/v2.mp4` (Aviva) audio raised from -26.3 to -14.5 LUFS, peak -0.5 dBFS, to match the other two videos; video stream unchanged. Removed the hidden "העלו סרטון בשם videos/vN.mp4" placeholder text that crawlers and screen readers read.
- 2026-10-17: Added a hero headline at the bottom of the main image on `index.html` (approved by Merav after screenshot previews): h2 "המוח לא יוצא לפנסיה..." and the subtitle "קורס מוסיקה למבוגרים בנס ציונה: שרים, מנגנים, זוכרים ונהנים, בקבוצה קטנה וחמה." Plain text on the image with a text shadow, no background box (Merav asked to remove it). Placed above the floating WhatsApp button on phones. Chosen over competitor-style wording ("מאמנת את המוח כמו שריר", "החיים מתחילים בגיל 60"); avoids health claims.
- 2026-10-17: Call buttons on computers (Merav reported they tried to open an app): on mouse devices, "call me" buttons now scroll to the contact section and highlight the number line; clicking a number itself copies it and shows "המספר הועתק ✓". Phones and tablets dial as before. Code is in `index.html` <head>, after the conversion listener; phone clicks are still counted as conversions. Tested live on desktop and in mobile emulation.
- 2026-10-17: Added Google Ads conversion events to `index.html` (one click listener after the gtag config): WhatsApp taps → `AW-18449420494/_vn4CKH8kKAdEM6hr91E`, phone taps → `AW-18449420494/s4wwCKT8kKAdEM6hr91E`. Kids page left without them so show inquiries don't mix with course leads. Visitors see no change. Tested on the live site: both clicks sent conversion hits.
- 2026-10-17: Checked video loading on the live site: videos have `preload="none"` and only `data-src`; they load only after a click on play. Scrolling the whole page loaded ~1 MB and no .mp4 (the 3 videos total ~32 MB).
- 2026-10-10: Added Meta Pixel `1102922088890690` (PageView) to `index.html` and `Kids.html`: the script in <head>, the noscript fallback right after <body>.
- 2026-10-10: Added a hidden HTML comment to `index.html` to test the GitHub → Netlify deploy. Visitors see no change. Deploy succeeded.
- 2026-10-10: Moved the site from manual Netlify uploads to GitHub (`meravboaz/meiravboaz-site`). Netlify now deploys automatically on every push to `main`.
- 2026-10-04: Last manual upload (included the Google Ads tag AW-18449420494).

## Open items
- Subtitles inside the testimonial videos (WebVTT track, not burned in): blocked 2026-10-17 because the fal account (used for Hebrew transcription) is out of credits, and transcription models can't be downloaded in the cloud workspace. Options: Merav tops up fal, or she supplies the text and timing is aligned by speech pauses.
- Video 3 (`v4.mp4`, Svetlana): could be trimmed from 63 s to about 40 s; Merav may swap it for her newer selfie video (quieter audio at -24 LUFS, vertical, ceiling lamp in frame).
- Planned (2026-10-17): replace the hero photo with a slow 3-image crossfade (1. circle laughing, 2. ribbons/movement, 3. recorders close-up), strongest image first, still image for reduced-motion. Frames picked from Merav's WhatsApp videos were too small (848px), so Merav will film the current course in 4K and send originals (not via WhatsApp).
- Kids page (`Kids.html`) still shows placeholder text for the three show names and descriptions (`[שם המופע הראשון]` and so on).
- Email taps aren't tracked (only WhatsApp and phone were requested).
- Add Meta `Contact` events for WhatsApp, phone and email taps, so Meta counts leads and not just page views.
