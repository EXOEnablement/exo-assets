# Public diagnostic form — v3 redesign (2026-11-27, Nick's direction)

Nick corrected the concept on a voice call: the ICP calculator is FOR NICK,
not for grading prospects. He does not believe in giving a potential client
a score — it doesn't make sense and it's off-brand.

## v3 design (live)
- The page is a diagnostic FORM: "Tell me about your SDR team."
- Visitor answers the same 9 questions + optional name / company / email / note.
- The score (Fit /70, Urgency /30) is computed internally and is NEVER shown
  to the visitor — no number, no breakdown, no verdict label.
- The visitor gets a HUMAN message back, built from their answers:
  - Acknowledges what's solid ("The need is real...")
  - Names what's still missing, from their lowest areas, in plain words
  - Suggests 2-3 conversation topics specific to their answers
    (e.g. shared call scorecard, ramp/attrition, 30-60-90, manager cover,
    first-SDR readiness for pre-hire, honest not-for-you for no-outbound)
- Send route today: visitor can copy their summary (answers in words) and
  send it to Nick on LinkedIn. Nick's internal score is included only in
  the private payload, never in the copied text or on screen.

## OPEN ITEM — automatic delivery
For submissions to land in Nick's inbox automatically, the form needs a
form-inbox endpoint tied to a destination email address. Nick's business
email address is not on file (only that it's Mail.com). Once Nick gives the
address, wire SEND_ENDPOINT in icp-calculator.html (one line) to a free
form-inbox service (e.g. FormSubmit) — first submission triggers a one-time
activation email Nick clicks once. Until then, copy + LinkedIn is the route,
and the page says so honestly: nothing is collected unless the visitor
chooses to send it.
