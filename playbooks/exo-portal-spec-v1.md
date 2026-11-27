# EXO Portal — Spec v1 (INTERNAL ONLY)

**Status:** Exploration draft, 2026-11-27. Not a locked commitment.
**Visibility rule (Nick, 2026-11-27):** The two reference platforms named in this document must NEVER be referenced in anything visible to the public — no website copy, no proposals, no decks, no social posts. They are private design references only. Any public-facing derivative of this spec must have those names and any identifying details removed first.

## Purpose
A working portal/app for EXO Enablement coaching delivery: somewhere Nick runs onboarding and coaching engagements, and SDRs/managers work between sessions. Built by tailoring an open-source base, not bought off the shelf and not copied from proprietary products.

## Base candidate: Frappe LMS (AGPL-3.0)
Already provides (plumbing we do not build):
- Courses with chapters and lessons
- Live-class batches / cohorts
- Quizzes and assignments
- Certificates
- Self-hostable, Docker install, actively maintained (v16.x, Nov 2026)

## Behaviour references (INTERNAL ONLY — see visibility rule)
Studied for behaviour patterns only. No code, design assets, copy or branding may be taken from either.

Reference A — a sales-coaching platform Nick used and rated highly:
- Team overview + individual overview: coach sees who needs coaching, on what, at a glance, then drills down
- Every coaching session tied to ONE focus skill; session holds notes, linked materials, and tasks created from the session
- Tiered privacy: coaching notes visible only to coach + coachee; journal entries visible only to the coachee
- Focus area + target date + progress curve over the working period
- Self-assessments managed and compared over time by the rep
- Personal goals tracked alongside company goals; explicitly positioned as NOT a surveillance tool

Reference B — an enterprise coaching app Nick used (LHH stablemate):
- One-stop coachee app: scheduling, video sessions, resources, coach messaging in one place
- Coach-curated resources per person (hand-picked articles/worksheets/media), not a dumped library
- Built-in measurement: assessments in-app, progress reporting on a monthly cadence
- AI assistant delivering between-session reflection nudges, responses shared with the coach — AI as amplifier between human sessions

## The EXO layer (what we design and build on top of the base)
1. Coaching session record: date, participants (1:1 or group), ONE focus skill, agreements/insights notes, tasks out of the session with owners and due dates.
2. Privacy tiers: (a) shared coach+coachee notes, (b) coachee-only journal, (c) Nick-only private notes. Manager/employer views see aggregate progress only — never private notes or journal content. This is the "protect the experience" principle in product form: the portal is not a surveillance tool.
3. Coaching plan per coachee: goals (theirs and the team's), focus areas, review dates.
4. Focus tracker: one active focus skill per person, target date, simple progress view over time (self-rating + coach rating + evidence from call scorecards).
5. Self-assessment: repeatable EXO scorecard a rep completes at intervals and compares against their own previous results.
6. Curated resources: Nick assigns specific resources to specific people; no generic library dump as the default experience.
7. Between-session prompts: scheduled reflection nudges between sessions; responses visible to Nick (and, in time, an AI assist drafting the prompt — human-reviewed before sending).
8. Onboarding journeys: EXO onboarding stages (day one, week one, month three, promotion readiness) as structured cohort programmes in the base LMS, with the coaching layer running alongside.
9. Measurement for the buyer: engagement-level reporting (sessions held, focus progress, assessment movement) that a manager can read in minutes — proof, not vanity metrics.

## EXO principles baked in
- Hard on the problem, invested in the person: the portal surfaces what needs work without exposing the person.
- Craft over volume: one focus at a time; depth over activity counts.
- Human + AI partnership: AI assists between sessions; it does not coach in Nick's place.
- Simple, repeatable, scalable.

## Phases (proposed, not agreed)
1. Stand up Frappe LMS in a test environment; Nick uses it as a coachee and as a coach; verdict on fit.
2. Brand/theme it (burgundy/black/gold, EXO logo system).
3. Design the coaching layer (items 1–7 above) as customisations; estimate effort honestly before building.
4. Pilot with one real engagement before any client-facing claims are made about it.

## Open questions
- Hosting: self-host cost vs managed Frappe hosting, within Nick's £0-first budget constraint.
- Does the AGPL licence fit how Nick wants to offer this to clients? (AGPL obligations if the portal is offered as a service — needs a proper check before client use.)
- Client data: coaching notes are sensitive; data protection/GDPR posture to settle before any real coachee data goes in.
