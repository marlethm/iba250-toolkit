# Step D — Entry Mode Decision Framework Prompt

**IBA 250: Building a Born-Global Digital Firm — Assignment 2, Step D**

This is the prompt template your team will use to complete Part A of Assignment 2
("Entry mode decision framework," Section 3.2 of the project guide). Fill in the
bracketed placeholders, paste the whole block into the AI tool of your choice, and
keep the raw output — you'll use it directly to write Sections 2 and 3 of your
report and log it in your AI Use & Founder Decision Log.

## Before you start: Stage 2 has three steps, in order

Assignment 2 has three parts, and this toolkit splits them into three pages so you
can work through them one at a time without losing your place:

1. **Step D (this page)** — decide *where* you're entering (which country or
   countries carry forward from Stage 1) and *how* (your entry mode).
2. **Step E** — the quantitative political, legal, and economic analysis of the
   country or countries you selected in Step D.
3. **Step F** — the cultural analysis and comparative table for the same
   countries, plus the Stage 2 social-media requirement.

Do them in this order — Steps E and F both assume you already know which
country or countries you're analyzing, which is Step D's job to settle first.
Any chat-only AI tool works fine for all three; Claude Code isn't required
unless you want it reading your Step B/C files directly.

## Before you paste this in

Fill in these six fields. Everything else in the prompt stays as written — it
matches the project guide's entry-mode decision framework and report template
exactly.

- `[TEAM NAME / FOUNDER NAMES]`
- `[VENTURE PROFILE]` — same profile you used for Steps B and C
- `[STEP C RESULTS]` — paste your Step C output's Task 3 shortlist (top-3
  countries) and the single biggest open risk/unknown it flagged. If you've
  re-run Step B or Step C since then with updated evidence, paste the most
  recent version instead.
- `[CONTROL REQUIREMENTS]` — your team's honest, specific assessment of how
  much control you need over your brand, user/customer data, the AI
  model/workflow itself, pricing, intellectual property, and service quality
  — and why. This is not a generic answer; it depends on what's actually
  proprietary about your venture.
- `[RESOURCE & RISK CONSTRAINTS]` — your team's real capital, staffing, and
  time available, and how much uncertainty or irreversible commitment you can
  responsibly take on right now.
- `[KNOW-HOW SENSITIVITY]` — what a local partner could copy, learn, or
  misuse if you shared it with them (prompts/workflows, proprietary logic,
  user data, customer relationships) — or say "low sensitivity" if nothing
  about your venture is especially easy to copy.
- `[TOOL TYPE]` — chat-only is fine, or Claude Code if you want it reading
  your Step C files directly.

## The prompt

```
Act as our entry-mode strategy analyst for a three-founder student venture
team building a born-digital, born-global company for a semester-long
international business course project (IBA 250, Assignment 2, Step D). This
step applies the entry-mode decision framework from the course textbook
(control requirements, flexibility/resource commitment, dissemination risk)
to the country shortlist our team already built in Assignment 1.

VENTURE CONTEXT
- Founders: [TEAM NAME / FOUNDER NAMES]
- Venture profile: [VENTURE PROFILE]
- Step C country-screening results (top-3 shortlist + biggest open
  risk/unknown from our most recent run): [STEP C RESULTS]
- Our control requirements (real, specific — do not generalize these):
  [CONTROL REQUIREMENTS]
- Our resource and risk constraints: [RESOURCE & RISK CONSTRAINTS]
- Sensitivity of our know-how to disclosure/imitation: [KNOW-HOW SENSITIVITY]
- My tool type: [TOOL TYPE]

EVIDENCE RULES
- Treat the founder-supplied context above as evidence, not something to
  invent around. Every cell in the table below must be traceable to either
  that founder input or a cited, dated source — never a generic assumption
  about "most companies" or "most markets."
- Do not select or rank entry modes or countries beyond what the framework
  below produces. Recommend; do not decide. The founders make the final call.

TASK 1 — Link to Stage 1
In one short paragraph: state which country or countries from the Step C
shortlist we are carrying forward into Stage 2, explain what Stage 1 evidence
carries forward unchanged, note anything that has changed since that evidence
was gathered, and explain — without rejecting it outright — why any
shortlisted country is being deferred rather than pursued right now.

TASK 2 — Entry mode decision
Build this exact table, reasoning through each variable set using the founder
context above as evidence:

| Variable | Assessment for our firm (evidence) | Pushes toward (more/less control) |
|---|---|---|
| Strategic / control requirements: multi-domestic vs. global strategy; global concentration | | |
| Environmental / flexibility: country risk; psychic distance; demand uncertainty; competitive volatility | | |
| Transaction / dissemination risk: value and tacitness of our know-how | | |
| Conclusion: entry mode chosen and why | | |

Rules for this table:
- For a 100% digitally delivered firm, evaluate direct digital exporting as
  the default entry mode. If you recommend anything else (joint venture,
  licensing/franchising, wholly owned subsidiary), you must explicitly justify
  why direct digital exporting is insufficient for this specific venture —
  do not drift away from the digital-exporting default without a stated
  reason tied to the founder context above.
- In the Conclusion row, state plainly where this places the firm on the
  control-resource commitment continuum (wholly-owned subsidiary -> joint
  venture -> franchising/licensing -> exporting), and which specific
  activities stay centralized (kept inside the firm) versus which get
  localized or handed to a partner.

TASK 3 — Team interpretation
Add one paragraph explaining why this entry mode fits this specific venture
at this specific stage — not a generic restatement of entry-mode theory.
Reference the actual control/resource/dissemination-risk tradeoffs from the
table above.

OUTPUT RULES
- Every table cell is either evidence-based (traceable to a founder input
  above or a cited source) or explicitly labeled "not found / needs founder
  research" — never a silent guess.
- Do not just list entry modes from the textbook — explain why the chosen
  one fits this venture, using the table's own logic.
```

## After you run it

1. Save the raw output and log it in the **AI Use & Founder Decision Log** —
   note what you kept, changed, or rejected.
2. Use Task 1's output to write **Section 2 (Link to Stage 1)** of your
   report, and draw the selected countries and top reasons into **Section 1
   (Executive Decision Summary)** — you'll finish Section 1 once Steps E and
   F are done and you have the full picture.
3. Use Tasks 2-3 directly as **Section 3 (Entry Mode Decision)** of your
   report.
4. Move to **Step E** once your entry-mode table is settled — it assumes you
   already know which country or countries you're analyzing.

**Reminder:** this satisfies Part A of Assignment 2 (Section 3.2 of the
project guide). The rubric scores Entry mode decision at 10 of 60 points and
Country selection (does it properly follow from Stage 1 data, and does it
include a culturally distant Global South emerging economy) at 4 more points.
