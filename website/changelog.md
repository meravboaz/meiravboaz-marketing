# Website changelog: meiravboaz.co.il

Newest first.

- 2026-10-17: Added Google Ads conversion events to `index.html` (one click listener after the gtag config): WhatsApp taps → `AW-18449420494/_vn4CKH8kKAdEM6hr91E`, phone taps → `AW-18449420494/s4wwCKT8kKAdEM6hr91E`. Kids page left without them so show inquiries don't mix with course leads. Visitors see no change. Tested on the live site: both clicks sent conversion hits.
- 2026-10-17: Checked video loading on the live site: videos have `preload="none"` and only `data-src`; they load only after a click on play. Scrolling the whole page loaded ~1 MB and no .mp4 (the 3 videos total ~32 MB).
- 2026-10-10: Added Meta Pixel `1102922088890690` (PageView) to `index.html` and `Kids.html`: the script in <head>, the noscript fallback right after <body>.
- 2026-10-10: Added a hidden HTML comment to `index.html` to test the GitHub → Netlify deploy. Visitors see no change. Deploy succeeded.
- 2026-10-10: Moved the site from manual Netlify uploads to GitHub (`meravboaz/meiravboaz-site`). Netlify now deploys automatically on every push to `main`.
- 2026-10-04: Last manual upload (included the Google Ads tag AW-18449420494).

## Open items
- Kids page (`Kids.html`) still shows placeholder text for the three show names and descriptions (`[שם המופע הראשון]` and so on).
- Email taps aren't tracked (only WhatsApp and phone were requested).
- Add Meta `Contact` events for WhatsApp, phone and email taps, so Meta counts leads and not just page views.
