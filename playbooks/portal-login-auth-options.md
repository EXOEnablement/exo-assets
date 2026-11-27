# Portal login — what was built, and the real-auth decision still open

Date: 2026-11-27. Status: front door live; NO real authentication yet.

## What was built (live on exoenablement.github.io)
- `login.html` — "Portal login" front door in the premium design system,
  linked from the shared top nav on every page (homepage, diagnostic,
  portal, login). Three role doors matching the agreed architecture:
  1. **Coach** (Nick only) — links through to the existing portal
     prototype (`portal.html`), labelled honestly as pilot access.
  2. **SDR Manager** — no working login; states access is by invitation
     and opens when coaching starts, with a LinkedIn contact route.
  3. **SDR** — same invitation treatment.
- The page states plainly that there are no passwords yet, deliberately:
  a fake login box that pretends to be secure would be worse than none.
- The shared top nav (sliding gold glider + "What I do" mega-panel) was
  rolled onto `icp-calculator.html` and `portal.html`; both pages'
  backgrounds aligned to the premium #140109. Existing functionality
  untouched: the diagnostic form and the portal's localStorage app work
  as before.
- Nothing about this is real access control. `portal.html` remains a
  public, unlisted URL holding data only in the visitor's own browser.

## The decision Nick still has to make BEFORE any client logs in
Real role-separated logins (coach / manager / SDR, per
exo-portal-architecture-v3) need an auth provider. Free-tier candidates:

- **Supabase Auth** — email/password + magic links, Postgres-backed user
  table with row-level security; best fit if the portal's data moves to
  Supabase too (one system for auth + data, generous free tier).
- **Firebase Auth** — Google's auth (email, magic link, social) with a
  Spark free tier; best fit if the portal stays a static site and just
  needs identity + simple role claims.
- **Cloudflare Access** — gates URLs by email/SSO in front of the site
  with no code; best fit for protecting the coach-only prototype quickly,
  weakest fit for in-app roles (manager vs SDR views).

Recommendation to discuss: Supabase if portal data is going server-side
anyway; Cloudflare Access as a stopgap gate for the coach prototype in
the meantime. Do not build a hand-rolled password check.

## Standing caveat — GDPR
No real coachee data goes into any of this until the auth route AND the
GDPR/data-protection posture are settled. The prototype's localStorage
model keeps data on Nick's own machine only, which is why piloting it
solo is acceptable and client use is not.
