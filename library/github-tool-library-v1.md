# EXO GitHub Tool Library — v1

**Built:** 2026-11-27 · **Source:** live GitHub searches + repo checks run by Toni, 2026-11-27.
**Purpose:** a standing log of open-source projects that can help build EXO Enablement — what each one is, and exactly how EXO would use it.

## Rules for this library

- **Licence is the gate.** Only genuinely open-source-licensed code (MIT, AGPL, GPL, Apache etc.) can be rebuilt or tailored for EXO. Anything "source-available" or "fair-code" is flagged — usable as a hosted/self-hosted tool within its terms, **not** a codebase to build on.
- **Stars and activity are as of 2026-11-27** and will drift. "Updated" means the repo itself was touched that week — a proxy for "alive", not a quality guarantee.
- **Status key:** `Vetted` = checked in depth already · `Identified` = found and summarised, licence/activity checked at headline level · `Watch` = interesting pattern, not usable yet · `Avoid` = checked, verdict is no.
- Nothing here is adopted until Nick says so. This is a library, not a shopping list.

---

## 1. Portal & learning delivery (the EXO Portal)

### Frappe LMS — `frappe/lms`
- **What:** full open-source LMS — courses, cohorts/batches, quizzes, assignments, progress.
- **EXO use:** the standing base candidate for the real portal (coach / manager / SDR role places). Already the reference in the portal spec v1.
- **Licence:** AGPL-3.0 (verified in earlier portal research). **Stars:** ~3,500 · Python · updated 2026-11-26.
- **Status:** `Vetted` — Nick declined a Frappe Cloud trial; direction is rebuild-the-patterns, so treat as architecture reference + candidate base.

### Pupilfirst — `pupilfirst/pupilfirst`
- **What:** LMS built for asynchronous, coach-reviewed schools — students submit artefacts, coaches review and level them up.
- **EXO use:** the closest living pattern to EXO's cohort model (EXO Foundations free cohort + Team Sprint): submit-artefact → coach gate → level-up. Worth studying before building Track A/B/C flows.
- **Licence:** to verify before any reuse. **Stars:** ~1,000 · Ruby · updated 2026-11-27.
- **Status:** `Identified` — high pattern value, small project; study, don't adopt blindly.

### Chamilo — `chamilo/chamilo-lms`
- **What:** long-running accessibility-focused LMS (PHP).
- **EXO use:** backup LMS option only; heavier and more traditional than EXO's direction.
- **Licence:** GPL-family (verify). **Stars:** ~1,000 · updated 2026-11-26.
- **Status:** `Identified` — low priority.

### SkillTree (NSA skills-service) — `NationalSecurityAgency/skills-service`
- **What:** a gamification service for learning: skills, levels, XP, badges, designed to plug into other apps.
- **EXO use:** pattern source for the portal's player-profile layer — visible levels/attributes growth tied to the one focus skill, personal not leaderboard. Exactly the grown-up gamification Nick specified.
- **Licence:** to verify (NSA projects are usually Apache-2.0). **Stars:** ~700 · updated 2026-11-26.
- **Status:** `Identified` — study the skill/level model when the portal gamification layer gets built.

### Level-Up — `cjmellor/level-up`
- **What:** small Laravel package that adds XP, levels and achievements to a PHP app.
- **EXO use:** only relevant if the portal ever goes the Laravel route — a ready-made levelling mechanic instead of hand-rolling one.
- **Licence:** to verify. **Stars:** ~680 · updated 2026-11-22.
- **Status:** `Watch`.

---

## 2. CRM & pipeline (running the business)

### Frappe CRM — `frappe/crm`
- **What:** modern open-source CRM from the same house as Frappe LMS.
- **EXO use:** the natural pairing if the portal goes Frappe — one stack for delivery (LMS) and pipeline (CRM): prospects scored against the ICP rubric, deals, follow-ups.
- **Licence:** AGPL-family (verify). **Stars:** ~4,000 · Vue · updated 2026-11-27.
- **Status:** `Identified` — strongest CRM candidate because of the LMS pairing.

### Twenty — `twentyhq/twenty`
- **What:** the big open-source Salesforce alternative — modern UI, very active.
- **EXO use:** standalone CRM option if EXO doesn't go Frappe. Probably more CRM than a solo operator needs today.
- **Licence:** to verify (has commercial enterprise parts). **Stars:** ~61,600 · TypeScript · updated 2026-11-27.
- **Status:** `Identified`.

### EspoCRM — `espocrm/espocrm`
- **What:** mature, lightweight, genuinely simple CRM (PHP).
- **EXO use:** the low-drama option — prospect tracking and follow-ups without a platform project attached.
- **Licence:** GPLv3 (verify). **Stars:** ~3,700 · updated 2026-11-27.
- **Status:** `Identified`.

### Krayin — `krayin/laravel-crm`
- **What:** free Laravel CRM for leads and sales management.
- **EXO use:** alternative CRM if a Laravel stack ever happens (pairs with Level-Up above).
- **Licence:** MIT (verify). **Stars:** ~24,200 · updated 2026-11-27.
- **Status:** `Identified`.

### Monica — `monicahq/monica`
- **What:** a *personal* CRM — remembers people: last contact, notes, reminders to follow up.
- **EXO use:** relationship layer, not pipeline: recommenders, sponsors, past clients, warm contacts. Fits how Nick actually sells — through people.
- **Licence:** AGPL-3.0 (**verified 2026-11-27**). **Stars:** ~25,900 · updated 2026-11-27.
- **Status:** `Identified` — genuinely different job from a sales CRM; could run alongside one.

---

## 3. Booking & scheduling

### Cal.com — `calcom/*`
- **What:** the open-source Calendly — booking pages, availability, reminders.
- **EXO use:** discovery-call booking link for the site and LinkedIn, replacing back-and-forth emails.
- **Licence:** mixed (open core + enterprise parts — verify before self-hosting).
- **Status:** `Identified — vetting incomplete`: the repo has been renamed/restructured and headline checks didn't resolve cleanly on 2026-11-27. Verify the current repo and licence before adopting. The hosted free tier may be the pragmatic route anyway.

### Someday — `rbbydotdev/someday`
- **What:** tiny free availability picker built on Google Apps Script.
- **EXO use:** zero-infrastructure fallback for "pick a time" links.
- **Licence:** to verify. **Stars:** ~1,100 · updated 2026-11-21.
- **Status:** `Watch`.

---

## 4. Forms, diagnostics & feedback

### Formbricks — `formbricks/formbricks`
- **What:** open-source survey/experience platform (the Qualtrics alternative).
- **EXO use:** structured feedback and benchmarking data — post-sprint buyer surveys, EXO Foundations applications, cohort feedback — beyond what the diagnostic form does.
- **Licence:** mixed AGPL + commercial (**flagged NOASSERTION on GitHub — read terms before building on it**). **Stars:** ~13,300 · updated 2026-11-27.
- **Status:** `Identified`.

### HeyForm — `heyform/heyform`
- **What:** clean open-source form builder.
- **EXO use:** quick standalone forms (applications, intake) with a nicer front end than the current form route.
- **Licence:** to verify. **Stars:** ~9,100 · updated 2026-11-26.
- **Status:** `Identified`.

### OpnForm — `OpnForm/OpnForm`
- **What:** simpler open-source form builder.
- **EXO use:** same job as HeyForm, lighter weight.
- **Licence:** to verify. **Stars:** ~4,000 · updated 2026-11-27.
- **Status:** `Watch`.

---

## 5. Money: invoicing, quotes, expenses

### Invoice Ninja — `invoiceninja/invoiceninja`
- **What:** invoicing, quotes, projects and time tracking for freelancers/small businesses.
- **EXO use:** client invoices and quotes for sprints and fractional work.
- **Licence:** **source-available (Elastic License) — NOT open source. Flagged:** fine to use as a tool (incl. its hosted plans), never a codebase to build on.
- **Stars:** ~10,600 · updated 2026-11-27.
- **Status:** `Identified` — practical tool, licence-flagged.

### InvoicePlane — `InvoicePlane/InvoicePlane`
- **What:** simple self-hosted invoices, clients, payments (PHP).
- **EXO use:** the genuinely-open-source invoicing fallback if Invoice Ninja's licence is a problem.
- **Licence:** to verify. **Stars:** ~3,300 · updated 2026-11-25.
- **Status:** `Identified`.

### TaxHacker — `vas3k/TaxHacker`
- **What:** self-hosted AI accounting helper — analyses receipts/invoices/transactions with an LLM.
- **EXO use:** sole-trader expense wrangling — photograph receipts, get categorised records for the accountant/tax return.
- **Licence:** to verify. **Stars:** ~6,900 · updated 2026-11-27.
- **Status:** `Watch` — appealing, young project; don't trust it with real finances until vetted properly.

---

## 6. Contracts & signing

### Documenso — `documenso/documenso`
- **What:** open-source DocuSign alternative — send, sign, track documents.
- **EXO use:** client agreements for Team Sprints and fractional engagements, tender paperwork. Has both a Zapier app and an n8n node (found in search), so it plugs into EXO's existing glue.
- **Licence:** AGPL core + commercial parts (verify split). **Stars:** ~15,900 · updated 2026-11-27.
- **Status:** `Identified` — high practical value for a business about to sign its first clients.

---

## 7. Audience: email & publishing

### Listmonk — `knadh/listmonk`
- **What:** high-performance self-hosted newsletter/mailing-list manager, single binary.
- **EXO use:** own the EXO mailing list (manifesto readers, cohort applicants, past clients) with no per-subscriber SaaS bill.
- **Caveat:** needs a real SMTP sending service — Mail.com free can't do this (Premium-only SMTP, and Nick won't pay for Mail.com). Pairs with a proper sending domain if/when Google Workspace happens.
- **Licence:** AGPL-3.0 (verify). **Stars:** ~24,500 · updated 2026-11-27.
- **Status:** `Identified` — right tool, blocked on the email decision, not on the software.

### Ghost — `TryGhost/Ghost`
- **What:** publishing platform with memberships and newsletters built in.
- **EXO use:** alternative home for EXO long-form writing (manifesto, onboarding series) with email capture built in, instead of bolting a list onto the static site.
- **Licence:** MIT (verify). **Stars:** ~55,900 · updated 2026-11-27.
- **Status:** `Identified` — a direction decision (own platform vs LinkedIn-first), not a tooling gap.

---

## 8. Automation glue

### n8n — `n8n-io/n8n`
- **What:** visual workflow automation with AI nodes — connects forms, email, CRMs, spreadsheets.
- **EXO use:** the solo-operator force multiplier: diagnostic submission → score → CRM row → follow-up draft; cohort applications → spreadsheet → emails. Zapier already connects some of this; n8n is the self-hosted, no-per-task-cost version.
- **Licence:** **fair-code (Sustainable Use License) — NOT open source. Flagged:** free to self-host for your own business use; not a codebase to build a product on.
- **Stars:** ~212,400 · updated 2026-11-27. Huge template ecosystem (multiple 20k+★ template collections found in search).
- **Status:** `Identified` — probably the single highest-leverage tool in this library for a one-person business.

---

## 9. Website analytics

### Umami — `umami-software/umami`
- **What:** privacy-first, cookie-free website analytics.
- **EXO use:** see whether the site/diagnostic actually gets used — pages, referrers (LinkedIn), diagnostic completions — with no cookie banner and no Google Analytics.
- **Licence:** MIT (**verified 2026-11-27**). **Stars:** ~40,400 · updated 2026-11-27.
- **Status:** `Identified` — clean fit for the current static site.

### Plausible — `plausible/analytics`
- **What:** the other privacy-first analytics option.
- **EXO use:** same job as Umami; heavier to self-host (Elixir + ClickHouse).
- **Licence:** AGPL (verify). **Stars:** ~30,000 · updated 2026-11-27.
- **Status:** `Identified` — Umami wins for EXO on simplicity.

---

## 10. Client communication

### Chatwoot — `chatwoot/chatwoot`
- **What:** open-source live-chat / shared-inbox / omnichannel support desk.
- **EXO use:** later-stage: website chat + one inbox for client messages once volume justifies it. Overkill today.
- **Licence:** mixed (GitHub flags NOASSERTION — MIT core + enterprise parts; verify). **Stars:** ~40,700 · updated 2026-11-27.
- **Status:** `Watch`.

### Plane — `makeplane/plane`
- **What:** open-source project management (Jira/Linear alternative).
- **EXO use:** only if EXO's own delivery tracking outgrows current tools — internal ops, not client-facing.
- **Licence:** AGPL-family (verify). **Stars:** ~63,300 · updated 2026-11-27.
- **Status:** `Watch` — solving a problem EXO doesn't have yet.

---

## 11. AI sales roleplay — searched, verdict: not yet

Every sales-roleplay / cold-call-practice repo found on 2026-11-27 (20+ results) has **0–2 stars** — student projects and weekend toys, e.g. `olivia-outsorcy/mockcalls`, `sarvagyajain299/cold-call-trainer`, `GoodHand-Off/ai-sales-roleplay`.

- **Verdict:** nothing on GitHub is production-usable for client delivery. Do **not** base EXO coaching or the free cohort on these.
- **Use instead:** the patterns only (AI prospect persona + rubric scorecard) if EXO ever builds its own — and commercial tools (e.g. Hyperbound, which Nick already has history with) for anything client-facing.
- **Status:** `Avoid` (as products) / `Watch` (as a category — re-check in 6 months).

---

## 12. Visitor identification & enrichment (commercial — added 2026-11-27, not GitHub)

*Not open source and never will be: the value is the proprietary identity data, not the code. Logged because Nick asked; checked against vendor pages and independent comparisons on 2026-11-27.*

### RB2B — visitor identification (person-level)
- **What:** a pixel on the site that names individual visitors — name, LinkedIn, job title, business email on paid plans — pushed to Slack/CRM/webhooks.
- **The catch for EXO:** person-level ID is **US-only** (RB2B's own FAQ; it geofences). UK/EU visitors resolve to **company level only** (via Demandbase). Nick's ICP is UK/EMEA, so for EXO this is a company-level tool wearing a person-level costume.
- **Maths:** person-level match ~15–20% of *US* traffic on Starter/Pro, 35–45% on Pro+. Pricing: free tier (company-level only since Jan 2026), Starter $79/mo, Pro from $149/mo. Below roughly 5,000 B2B visits/month, identification isn't the constraint — traffic is.
- **Legal:** naming individuals is the legally fraught end of UK/EU GDPR + ePrivacy; company-level sits on much firmer legitimate-interest ground.
- **Brand:** covertly naming visitors, then auto-sequencing them, is the "faster, bigger" pattern EXO exists against — and it clashes with the portal's anti-surveillance positioning.
- **Status:** `Parked` — revisit only if EXO gets meaningful US traffic.

### Company-level identification (EU-suited alternatives)
- **Leadfeeder** — reverse-IP company ID, EU-built (data stored in the EU), free plan exists, paid from ~€79/mo. Naming saga: Leadfeeder merged with Echobot and rebranded as **Dealfront** in 2023, then flipped back to **Leadfeeder** on 24 Mar 2026 (legal entity still Dealfront Group GmbH); the visitor product is now called **Web Visitors**, with an Intent Score per visiting company. **Albacross** — from €59/mo. **Snitcher** — from $49/mo.
- **EXO use if ever:** "a target-account company visited the pricing/diagnostic page" as a *signal* for human follow-up — not an auto-sequence trigger.
- **Status:** `Watch` — only worth it once site traffic is real; Umami first, to see the traffic honestly.

### FullEnrich — waterfall enrichment (different job from RB2B)
- **What:** takes people you *already* have (name + company, or LinkedIn URL) and cascades 20–25 data providers until it finds a verified work email or mobile. Claims ~84% EMEA email find rate; charged only on verified hits (email 1 credit, mobile 10). From $29/mo. Pushes to HubSpot; also has an official MCP server for AI agents.
- **EXO use:** directly attacks a known EXO problem — the Apollo free-plan data ceiling (List 2 scoring capped at 65/100 on Apollo data alone). Waterfall enrichment of ICP lists could lift contact-data coverage beyond any single source, Apollo included.
- **Status:** `Identified — genuinely interesting`. The one tool in this section that fits EXO's current stage and geography.

---

## Priority shortlist (Toni's ranking, for Nick to confirm or reorder)

1. **n8n** — automation glue; saves a solo operator hours weekly. Licence-flagged but usable.
2. **Umami** — site analytics, MIT, trivial fit, answers "is any of this working?"
3. **Documenso** — signing for first clients and tenders.
4. **Frappe LMS + Frappe CRM** — the portal/pipeline stack decision, already in motion.
5. **Listmonk** — audience ownership, waiting on the email/domain decision.
6. **Pupilfirst + SkillTree** — pattern libraries for the portal's cohort loop and gamification layer.

## Still to vet (named, not yet checked)
- Mautic (marketing automation), Activepieces (n8n alternative, MIT core), Cal.com's current repo/licence, Monica vs a simple spreadsheet for relationships, form licence checks (HeyForm/OpnForm).

*Library v1 — update in place as tools are vetted, adopted or rejected. Rejections stay in the log with their reason, so we don't re-search dead ends.*
