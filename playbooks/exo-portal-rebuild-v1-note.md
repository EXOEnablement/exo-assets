# EXO Portal — rebuild v1 (2026-11-27)

Nick declined the Frappe Cloud trial account and asked Toni to rebuild it instead.
Built: a working EXO Portal prototype as a single-page web app, live (unlisted)
at https://exoenablement.github.io/portal.html — deliberately NOT linked from
the public homepage until Nick pilots it (spec phase 4).

Implements the spec's EXO layer on the LMS-style base behaviours:
- People/cohorts with the four onboarding stages and per-stage checklists
- One active focus skill per person, target date, self + coach ratings, progress bar
- Coaching session log tied to the focus skill, with privacy tiers
  (shared / coach-only private / coachee journal)
- Tasks created from sessions, with owners implicit by person and due dates
- Between-session reflection prompt per person
- Repeatable self-assessment (6 areas, 1-5) with movement vs first score
- Curated resources assigned per person with a why
- Buyer report: aggregate only (sessions, open tasks, journey %, assessment
  movement) — no private notes or journal content; copyable summary
- Export/import JSON backup

Honest limits of this rebuild:
- Data is stored ONLY in the user's browser on that device (localStorage).
  It is a one-person working prototype, not a multi-user hosted portal:
  no logins, no sync, no client access yet. Real client data / GDPR posture
  from the spec's open questions still applies before any real coachee use.
- It is an original EXO build informed by the spec — it is not Frappe code
  and contains no reference-platform names or assets.
