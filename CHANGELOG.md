# DraftBound 2.0 changelog

Reinstall note: manifest id/start_url/scope and icon paths changed. Existing home-screen installs keep working and update via the service worker (new cache `draftbound-v2`), but for the new icon and install name, remove and re-add to the home screen. Saved profiles are migrated automatically (legacy demo data becomes sample data, custom persona becomes a persona list, flat data is wrapped in a roster). Save a backup first as a precaution.

| File | What | Why |
| --- | --- | --- |
| app/index.html | Rebuilt UI and outputs: overview with readiness check, recruiter details, sample mode, persona toggle and unlimited personas, model picker, bio drafting, new share cards (square/story/wide, QR), one-page PDF, 3 website styles, version stamp | Make the app and everything it exports credible to coaches |
| app/index.html | Fixes: multi-athlete data mix-up, accent not restored on load, duplicate functions, unescaped HTML, PDF/xlsx read as text, chained edit modals closing | Pre-existing bugs found in audit |
| app/index.html | Removed all "always-live link" and Gemini claims; videos are links only | Accuracy; hosting is up to the user |
| app/sw.js | New. Cache `draftbound-v2`, network-first HTML, cache-first assets | Offline and clean updates; version tied to About text |
| app/manifest.json | New in /app: id, start_url, scope "./", maskable icons, screenshots | Installable, correct scope |
| app/icon-192.png, icon-512.png | New safe-zone icons | Maskable-safe |
| app/shot-narrow-1/2.png, shot-wide.png | Simulated screenshots (sample data) | Rich install UI |
| index.html | New landing: honest copy, real alt text, app output screenshots, footer with copyright and contact | Remove placeholders and claims |
| assets/*.jpg | Compressed (7.0MB to under 400KB each); added out-card/out-sheet/out-site | Page speed; show real outputs |
| README.md, docs/*.svg | Rewritten with diagrams | Accurate docs |
| Removed | root manifest.json, download, .keep files, app/README.md, app/assets/* | Stale or duplicate |

Deviation: landing photos live in `/assets/` (target layout had none).
Limitation: videos are links, not uploads.
