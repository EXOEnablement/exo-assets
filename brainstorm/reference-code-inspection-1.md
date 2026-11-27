# Reference site code inspection #1 — Nooks (2026-11-27)

Priority task set by Nick 2026-11-27: inspect publicly served code of reference
sites, learn the techniques, rebuild ORIGINAL equivalents for EXO.
Line held: techniques/structure learned — no proprietary code, copy or assets taken.
Reference never named in anything public.

## What their page actually loads (from the live homepage HTML)
- Platform: **Webflow** (cdn.prod.website-files.com assets, Webflow JS + jQuery).
  NOT a custom React/Next build — a very polished Webflow site.
- Animation engine: **GSAP 3.15 + ScrollTrigger + SplitText + CustomEase**,
  served from Webflow's own CDN. This is the motion layer:
  split-text headline reveals, scroll-triggered entrances, eased movement.
- Nav/dropdown: custom JS files ("logomenu" scripts) + Webflow interactions —
  the sliding highlight and one-sheet panel are custom JS on top of Webflow.
- Utilities: Finsweet Attributes (list behaviours), Plyr (video), Fancybox
  (lightboxes), Intellimize (A/B personalisation), Intercom-style chat widget.
- Fonts: loaded via Google WebFont loader (Lato in the loader config; display
  type defined in their CSS).

## What this means for EXO (static GitHub Pages stack)
- We do NOT need Webflow. Hand-coded HTML/CSS/JS + the same open animation
  library gets the same feel on our stack, at £0.
- **GSAP + ScrollTrigger are free to use commercially** (and SplitText became
  free with GSAP 3.13+). We can load them from a public CDN and write our own
  animations: headline reveals, bento/panel scroll entrances, smoother nav.
  That is the single biggest lever for "stagnant" -> "alive".
- Already rebuilt as originals from layout inspection alone:
  sliding gold nav glider, one-sheet "What I do" panel, proof bento,
  numbered stage pills with switching panels, dark dot-grid panel.
- Next from this inspection: add a GSAP motion pass to the homepage
  (scroll-triggered rises on bento/stage/dark panel, subtle hero reveal),
  written from scratch, then check it doesn't hurt readability or mobile.

## Copyright-free imagery — status
- Generic image search and Openverse were checked 2026-11-27: results were
  either unverifiable licences (blogs/Getty) or irrelevant (sports coaching).
  REJECTED — nothing will be embedded from unverified sources.
- Route: Pexels / Unsplash only (their licences allow free commercial use),
  each image recorded with its source page before use. Shortlist still to be
  built for: bento photo card, dark-panel scattered photos.
- Note: GitHub connector pushes text only, so photos must be embedded as
  data-URIs (like the logo) or hotlinked from the licence source — embedding
  keeps the site self-contained but inflates page size; keep images small.

## Still to inspect under this priority task
- Orum (product dropdown structure — partly done from Nick's description).
- EZRA UK (structure only; behaviour-reference rules already apply).
