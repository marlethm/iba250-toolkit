# Step C — Global Market Opportunity Assessment Prompt

**IBA 250: Building a Born-Global Digital Firm — Assignment 1, Step C**

This is the prompt template your team will use to complete Step C ("Complete the
Global Market Opportunity Assessment"). Fill in the bracketed placeholders, paste
the whole block into the AI tool of your choice, and keep the raw output — you'll
use it directly to write Section 3 of your report and log it in your AI Use &
Founder Decision Log.

## This is a one-time deep analysis, not a new Skill

Step B built you a reusable Skill for re-screening countries. Step C does **not**
replace or duplicate that — it's a single, deep synthesis pass that takes your
Step B scorecard as an input and builds the five things around it that a scorecard
alone can't tell you: whether *your team* is actually ready, whether *your
product* actually travels, what the *top three* countries look like at the
industry level, who your *partners* would be, and what you could *realistically
sell*. Any chat-only AI tool works fine for this step. If you already have Claude
Code open from Step B, it's convenient to run this in the same session so it can
read your Step B files directly — but it isn't required.

## Before you paste this in

Fill in these six fields. Everything else in the prompt stays as written — it
matches the project guide's six required tasks and the report template exactly.

- `[TEAM NAME / FOUNDER NAMES]`
- `[VENTURE PROFILE]` — company name, mission, target customer, problem,
  product/service, revenue model, home base, born-global logic (same as Step B)
- `[FOUNDER READINESS INPUTS]` — your team's real, specific situation: financial
  and tangible resources, relevant skills (languages, tech, marketing), how many
  hours/week each founder can realistically commit, what data access you have
  (university library databases, etc.), current customer-support capacity,
  cybersecurity/privacy capability, and which time zones your team can cover.
  Task 1 needs your team's actual situation — the AI cannot know this on its own.
- `[STEP B SCORECARD RESULTS]` — paste your most recent Step B Skill run's
  evidence table and ranked scorecard (from `runs/<date>-output.md` or
  equivalent). If you haven't done Step B yet, do that first — Task 3 below
  builds directly on it instead of re-doing the screening from scratch.
- `[PRICING / MONETIZATION ASSUMPTIONS]` — your best current thinking on price
  point(s) and how you'd monetize (subscription, freemium, per-transaction,
  etc.). If you don't have this yet, say so — the AI will propose a starting
  assumption and label it clearly as an assumption, not a fact.
- `[TOOL TYPE]` — chat-only is fine, or Claude Code if you want it to read your
  Step B files directly.

## The prompt

```
Act as our Global Market Opportunity Assessment analyst for a three-founder
student venture team building a born-digital, born-global company for a
semester-long international business course project (IBA 250, Assignment 1,
Step C). This assessment is organized around the six tasks used in the course
textbook's Global Market Opportunity Assessment chapter (Cavusgil, Knight, &
Riesenberger), adapted to a small, new venture rather than a firm with the
resources of a multinational corporation.

VENTURE CONTEXT
- Founders: [TEAM NAME / FOUNDER NAMES]
- Venture profile: [VENTURE PROFILE]
- Founder readiness inputs (real, specific — do not generalize these):
  [FOUNDER READINESS INPUTS]
- Step B market-screening Skill results (evidence table + ranked scorecard from
  our most recent run): [STEP B SCORECARD RESULTS]
- Pricing / monetization assumptions so far: [PRICING / MONETIZATION ASSUMPTIONS]
- My tool type: [TOOL TYPE]

EVIDENCE RULES (apply to every task below)
- Every country score, statistic, or forecast needs a cited source and a
  year/date. Never invent or estimate a missing number — write "not found /
  needs founder research" instead.
- Keep SOURCE FACTS and AI INTERPRETATION visibly separate — label
  interpretation explicitly, never blend it into an evidence table or cell.
- Any forecast, conversion rate, reach estimate, or monetization assumption
  that the founders (not a cited source) are supplying must be labeled
  "FOUNDER ASSUMPTION" wherever it appears.
- Do not select or rank on the founders' behalf beyond what the scoring
  method below produces. Recommend; do not decide.

TASK 1 — Organizational readiness to internationalize
Using the founder readiness inputs above, produce this table, one row per
factor, honestly assessing gaps rather than assuming a fully-resourced team:

| Readiness factor | Current status (evidence) | Gap / action to close it |
|---|---|---|
| Financial & tangible resources | | |
| Skills & competencies (languages, tech, marketing) | | |
| Time availability | | |
| Data access (library databases, tools) | | |
| Customer support capacity | | |
| Cybersecurity / privacy capability | | |
| Time-zone coverage | | |
| Commitment to international expansion | | |

TASK 2 — Suitability of the product/service for foreign markets
For our venture, explain why the offering can travel digitally, then produce
this table identifying what's universal versus what needs adaptation:

| Factor | Findings (with sources) | Adaptation needed? |
|---|---|---|
| Customer characteristics & preferences | | |
| Laws & regulations (data privacy, content, consumer protection) | | |
| Channel intermediary requirements (app stores, payment platforms) | | |
| Competitors' offerings | | |

Identify the major barriers to cross-border delivery explicitly, separate
from the table.

TASK 3 — Screen countries to identify target markets
Do NOT re-screen the countries from scratch. Reconcile and build on the
pasted Step B scorecard results above:
- Reproduce the ranked scorecard (all 7 required criteria: market size &
  growth, market intensity, consumption capacity, receptivity to imports,
  infrastructure, economic freedom, country risk — plus any venture-specific
  criteria already in use), with weights, scores, and source citations
  exactly as the Step B Skill produced them.
- If any score looks stale (older than 3 years) or any weight seems
  misaligned with what Tasks 1-2 above just revealed about our actual
  readiness or product fit, flag it explicitly as a recommendation to
  re-run the Step B Skill — do not silently change the numbers yourself.
- State the resulting top-3 country shortlist plainly.

TASK 4 — Industry market potential (for the top-3 countries only)
For each of the three strongest countries from Task 3, move from macro
indicators to industry-specific demand:

| Country | Industry/customer segment size (cited) | Growth trend (cited, w/ years) | Demand drivers | Comparable competitors/substitutes |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

TASK 5 — Choose qualified foreign business partners
For each of the top-3 countries, identify the partner types that would
reduce friction or accelerate demand for a digital venture (payment
provider, app store, marketplace, local university/incubator,
creator/influencer, reseller, cloud provider, translator/localization
provider, industry association). Name real, current organizations where you
can verify them; if you cannot verify a specific name is real and current,
describe the partner type and say so explicitly instead of inventing a name.

TASK 6 — Estimate company sales potential
For each of the top-3 countries, build a transparent, assumption-driven
funnel: reachable customers -> expected conversion rate -> paying users ->
price -> revenue, over a stated period. Provide a base case AND at least one
alternative scenario (e.g., slower adoption, stronger channel partnership).
Label every input as either a cited figure (with source) or a FOUNDER
ASSUMPTION. Do not produce a single number with no visible inputs.

OUTPUT RULES
- Follow the six tasks in order, with clear headers matching Section 3 of
  the written report template (Task 1 through Task 6).
- Every table cell is either a cited fact, a clearly labeled FOUNDER
  ASSUMPTION, or "not found / needs founder research" — never a silent guess.
- End with a short summary: the top-3 country shortlist from Task 3, and the
  single biggest open risk or unknown across Tasks 1-6 that the founders
  should resolve before Assignment 1 is due.
```

## After you run it

1. Save the raw output and log it in the **AI Use & Founder Decision Log** —
   note what you kept, changed, or rejected, especially any FOUNDER ASSUMPTION
   the AI proposed on your behalf.
2. Verify at least the highest-stakes numbers yourself (Task 3's top scores,
   Task 4's market-size figures, Task 6's revenue estimates) against the
   original sources before they go in your report — this satisfies the
   evidence-verification expectation in the rubric, not just having a citation.
3. Fill in Task 6's actual numbers using the **sales funnel calculator**
   (downloadable on this page) so the arithmetic is transparent and the
   base-case/alternative-scenario comparison is visible, not just asserted.
4. Drop this output straight into **Section 3 (Global Market Opportunity
   Assessment)** of your report, using the same six-task subheadings, and use
   Task 3's shortlist to write **Section 4 (Country Screening Model and
   Results)**.
5. Record in your **Evidence Ledger** any source you had to go find yourself
   because the AI flagged something as "not found."

**Reminder:** this satisfies Step C of Assignment 1 (Section 2.5 of the project
guide) and uses the required seven-criterion scorecard from Section 2.6. Step C
is worth the largest share of the written-report rubric (Task 3 alone is 12 of
60 points) — the accuracy and sourcing here matter more than in any other step.
