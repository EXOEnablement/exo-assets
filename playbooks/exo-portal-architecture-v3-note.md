# EXO Portal — Architecture v3 (Nick, 2026-11-27, voice — supersedes v2 note)

Three separate places, by audience. One system, role-separated logins,
privacy enforced by the system, not by habit:

## 1. Coach portal — Nick only (private backend)
For Nick alone. Everything lives here: private coach notes, full session
records, scoring, focus tracking, Trust Heatmap reviews, report preparation.
Nobody else logs in here. Ever.

## 2. SDR manager area — login, separate place
Their own team only: aggregate progress, onboarding journey status,
shared-tier information, and the manager-side Heatmap reflection
(where could better follow-ups have deepened trust?). Never Nick's private
notes, never coachee journal content.

## 3. SDR area — login, separate place
The rep's own space: their onboarding journey and checklists, their focus
skill, shared session notes and tasks, their curated resources, their
self-assessments, their journal (visible to them; shared with Nick only as
the tier allows), and their own Trust Heatmap results with the rep-side
reflection prompt (which of your questions created the most curiosity?).
Positioned as craft development, NOT surveillance — the rep sees what the
system holds on them.

## Trust Heatmap — now a portal consideration (Nick, 2026-11-27)
Full master prompt supplied by Nick via Google Doc
(Doc ID 188uhJrF43U8wSguz0ibR4odhzLX7gH9tNxnonwKArbc), saved privately at
scorecards/trust-heatmap-master-prompt.md. Core model:
- Rep Question Quality Score 0-100 (high-value open/outcome +10, purposeful
  closed +1, generic/scripted 0)
- Prospect Curiosity Score 0-100 (high-trust +15, tactical +5, neutral 0,
  defensive -10)
- Classification: Red <55 trust breakdown, Yellow 56-75 fragile,
  Green >75 trust building
- Coaching reflection prompts per role: Rep / Manager / Both
Portal mapping: analysis/scoring sits in the coach backend; managers get
their reflection view; SDRs get their own results + rep reflection.
Prototype v1.1 (live, coach side only): manual score entry, band
classification on the two-score average, evidence notes, reflection prompts,
history per person, colour counts (no content) in the buyer report.
Automated transcript analysis is NOT built — scores are entered from a
review run outside the portal (e.g. with the master prompt in an AI tool).
