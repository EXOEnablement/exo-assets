# EXO Portal — Architecture clarification (Nick, 2026-11-27, voice)

Nick clarified the portal is NOT one shared space. Separate places, by audience:

## 1. Coach portal — Nick only (private backend)
- For Nick alone. This is where the current portal prototype belongs.
- Holds everything: private coach notes, journal-tier material shared with him,
  full session records, scoring, focus tracking, buyer-report preparation.
- Nobody else logs in here. Ever. Me-only access is the requirement, not a setting.

## 2. SDR manager area — login, separate place
- SDR managers log in to THEIR OWN place, distinct from the coach backend.
- They see their team: aggregate progress, onboarding journey status, shared-tier
  information only.
- They never see: Nick's private notes, coachee journal content, or anything from
  the coach backend beyond what Nick deliberately publishes into their view.
- (Nick was still setting out the full structure when this was captured —
  a coachee/SDR-facing place may follow as a third zone. Do not assume its
  shape until Nick states it.)

## Design consequence
The current public-URL prototype (localStorage, no logins) cannot deliver this
split. The real build needs authenticated, role-separated spaces:
coach (Nick only) vs manager (per-team login) at minimum, with the privacy
tiers enforced by the system, not by habit. Hosting/auth route still to be
chosen within the £0-first constraint; GDPR posture from spec v1 still open
before any real data.

## Also pending
- Nick said he is sending the full prompt for the Trust Heatmap and that it
  "should come into consideration as well" for the portal. Incorporate it
  when it arrives; do not reconstruct it from memory or invent its contents.
