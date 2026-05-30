# QA — ЕК-Дент д-р Елена Колева

## Gate 1 — source/fact audit
- PASS business name/category: sheet + Titul/Oink/Zlatna Firma.
- PASS address: Titul and Oink — ул. „проф. д-р Васил Златарски“, 1799 ж.к. Младост 2, София.
- PASS phone: sheet and Titul — +359 87 814 7471.
- PASS coordinates: Oink — 42.64245620, 23.37000350.
- PASS Google Maps CID: Titul — 3228267660040785342.
- PASS hours: Titul — Mon 09:00–17:30, Tue 09:00–17:00, Wed 09:00–17:30, Thu 09:00–17:00, Fri 09:00–17:00, Sat/Sun closed.
- PASS testimonials: real public excerpts from Titul/Zlatna Firma, original language retained.
- PASS no invented prices/certifications/awards/treatments/guarantees. No public review counts used.

## Gate 2 — visual-result image audit
- PASS not a visual-result business. Dentist/clinic page does not require before-after/work-result images.

## Gate 3 — testimonial audit
- PASS Google/Titul public review excerpts manually reviewed via fetched profile.
- PASS cards use real reviewer names/text. Star rows used only for reviews presented from 5-star public review context.
- PASS no anonymous fake cards, rating-only cards, review themes, AI summaries, or review counts.

## Gate 4 — copy audit
- PASS Bulgarian copy pass completed. Removed source/audit language from customer-facing page. Copy is direct, dental-specific, and local.

## Gate 5 — link/schema/SEO-head audit
- PASS title, description, robots, canonical, OG tags, twitter card present.
- PASS exactly one H1.
- PASS Dentist schema includes NAP, geo, phone, opening hours, sameAs, canonical URL.
- PASS tel/maps/Facebook/nav anchors present.

## Gate 6 — image/layout audit
- PASS no fake/stock clinic/staff photos. No rejected unrelated Bing thumbnail used.
- PASS brand SVG is vector/graphic only, not presented as clinic photo.
- PASS no duplicate photo subjects.

## Gate 7 — map/local SEO audit
- PASS bottom Google Maps/local SEO block directly above footer.
- PASS exactly one visible navigation CTA/link in map block.
- PASS iframe uses Google Maps CID embed: `https://maps.google.com/maps?cid=3228267660040785342&output=embed`.

## Gate 8 — responsive visual QA
- PASS desktop and mobile screenshots generated locally with Playwright: `artifacts/ek-dent-elena-koleva-desktop.png`, `artifacts/ek-dent-elena-koleva-mobile.png`.
- PASS map-specific viewport screenshots generated after scrolling to iframe: `artifacts/ek-dent-elena-koleva-map-section.png`, `artifacts/ek-dent-elena-koleva-map-section-mobile.png`.
- 2026-05-30 correction: replaced CID-based lazy map iframe with eager coordinate-based embed (`42.6424562,23.3700035`) after mobile full-page QA showed a blank map area before scroll.
- PASS footer icon row uses consistent SVG icon buttons.
- PASS sticky mobile call CTA present.

## Gate 9 — final live QA
- PASS GitHub Pages returned HTTP 200.
- PASS live HTML contains business name, testimonial phrase, phone CTA, map/contact block, Dentist schema, canonical, and OG tags.

## Notes / blockers
- 2026-05-30 correction: Dean supplied the correct Facebook page: https://www.facebook.com/p/ЕК-Дент-100063898398260/?locale=bg_BG . The site/schema/footer now use this page instead of the previously surfaced wrong Facebook id.
- Public staff/clinic photos were not accessible from autonomous sources. Correct Facebook page fetch/mobile/mbasic routes hit logged-out or unsupported-browser walls and did not expose usable images; old business.site returned 404. Page intentionally avoids fake portraits or stock clinic photos.
- Sheet row 21 website/Facebook field updated after Dean supplied the correct page.
