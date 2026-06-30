# CK Hunting, concept site (single page)

A single-page concept website built by Aoraki Creations for **CK Hunting**, a second-generation
big game outfitter in the Wyoming Range (Daniel / Big Piney, Wyoming). Built from the outfitter's
own real photos and copy, scraped from their existing site at http://www.ckhunting.com.

This is a **concept demo for outreach**, not affiliated or live. Every page view carries a demo badge.

## Run it
Served via `.claude/launch.json` (server name `ck-hunting`, port 8742), or:
```
python3 -m http.server 8742 --directory "demos/ck-hunting"
```
Open http://localhost:8742

## Files
- `index.html` — the whole single page (hero, hunts, ranch, fishing, gallery, plan, contact, footer)
- `styles.css` — design system (warm charcoal + buckskin + ember rust, Zilla Slab + Inter)
- `main.js` — nav, scroll reveal, gallery filter + lightbox, demo badge, demo form
- `assets/` — 23 curated real photos (renamed for clarity)
- `scrape/` — source material: `FACTS.md` (verified facts, the single source of truth), the original
  home page, the Xara asset manifest, and `img/` (all 74 photos pulled from their site)

## Honesty notes (important)
- Built using ONLY facts verified from their site (`scrape/FACTS.md`). No invented prices, dates,
  success rates, testimonials, email, or names.
- The original site's prices are labeled "2020 season," so they are shown here clearly flagged as
  **2020 rates** with a "call for current pricing" note. They are NOT presented as today's prices.
- **There is no moose photo** in their photo library, so the Moose hunt card uses valley *habitat*
  (honestly captioned), never a mislabeled animal.
- House style: no em dashes or en dashes anywhere (including source comments).

## Quality pass
Reviewed by a 4-lens adversarial pass (honesty, accessibility/HTML, code, copy/UX). Fixes applied:
keyboard-operable gallery + accessible lightbox (role=dialog, focus management, focus trap, Escape),
`scroll-padding-top` for the fixed header, footer heading hierarchy, `aria-pressed`/`aria-controls`,
progressive-enhancement reveal (content visible without JS), and copy tightening. No console errors;
verified on desktop and mobile (375px), including the mobile slide-out menu.

## Resolution caveat
The source photos are low resolution (max ~868px wide; most 560px). They hold up at the sizes used,
but for a live build we would swap in CK Hunting's full-resolution originals.

## Deployed
LIVE at **https://buckeyebait.github.io/ck-hunting/** (repo `Buckeyebait/ck-hunting`, public, GitHub
Pages from `main` root). The page carries `noindex` so the concept demo stays out of search results.
The `scrape/` working folder is gitignored and not part of the public repo.
