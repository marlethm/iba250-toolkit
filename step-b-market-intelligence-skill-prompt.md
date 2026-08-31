# Step B — AI Market Intelligence Agent/Skill Prompt

**IBA 250: Building a Born-Global Digital Firm — Assignment 1, Step B**

This is the prompt template your team will use to complete Step B ("Build the AI
Market Intelligence Agent/Skill"). Fill in the bracketed placeholders, paste the
whole block into Claude Code (recommended — see note below), and save what it
builds. You will re-invoke this Skill for at least five dated monitoring runs
before Assignment 1 is due, and you will describe it in Section 5 of your report
and include it as an appendix.

## Skill or Agent? Use a Skill.

The project guide is explicit that "the agent does not have to be custom
software" and warns that "a sophisticated autonomous agent with weak evidence
will score lower than a simple reusable workflow that reliably cites, verifies,
and updates decision-relevant data." In Claude Code terms, that points to a
**Skill**, not an autonomous multi-step agent:

- A Skill is a folder (`SKILL.md` + templates + a small script) that anyone on
  the team — or your professor — can open and read line by line. Every rule in
  it (evidence rule, freshness rule, founder-decision rule) is inspectable, not
  hidden inside an agent's internal reasoning.
- It is reproducible by construction: the same `SKILL.md` produces the same
  evidence-gathering and scoring behavior every time you re-invoke it, which is
  exactly what "at least five dated monitoring runs" requires.
- It can still call live web search/fetch for the public, open data sources
  (globalEDGE, World Bank Open Data, IMF, UNCTAD, ITU DataHub, OECD) — it just
  can't log into your university library, so Statista, Euromonitor Passport,
  IBISWorld, MarketLine, and Business Source Complete stay a manual paste-in
  step, same as they were in Step A.
- It is easy to screen-record for your required "short demonstration of the AI
  market-intelligence agent/skill" social video.

A fully autonomous agent (one that plans its own multi-step tool use with less
visibility per step) is more machinery than this task needs, and the extra
opacity works against the rubric's "evidence contract" and "founder judgment"
criteria. If your team later wants true autonomy (e.g., a scheduled job that
re-runs itself weekly with no founder in the loop), that's a Stage 2/3
enhancement — not a Stage 1 requirement.

## No Python required

The prompt below has your AI tool build one optional file,
`scripts/score_markets.py`, that double-checks the weighted-score math and
draws a bar chart — for teams that already have Python installed. **You do
not need it to complete Step B.** The required output format already has
the AI show the weighted-score calculation directly in its chat response
for every run; that alone satisfies "reproduce the market-screening logic
consistently." If `python3` isn't installed on your computer, skip the
script entirely, keep the CSV files as your evidence record (open them in
Excel or Google Sheets if that's easier), and use the numbers your AI tool
already printed. Nothing else in this workflow depends on Python.

## Before you paste this in

Fill in these six fields. Everything else in the prompt stays as written —
it is written to match the project guide's required output format and the
seven required screening criteria exactly, so the grader sees the same logic
in every team's submission.

- `[TEAM NAME / FOUNDER NAMES]`
- `[VENTURE PROFILE]` — company name, mission, target customer, problem,
  product/service, revenue model, home base, and born-global logic (pull this
  straight from your Step A decision and company-naming work)
- `[CANDIDATE COUNTRIES]` — at least 5, from at least 3 world regions, with a
  one-line reason each is in the initial pool
- `[WEIGHT FOR EACH CRITERION]` — the seven required criteria below already
  come pre-loaded; you only need to assign weights that total 100% (and add
  up to 2 venture-specific criteria if they genuinely matter)
- `[ANY OTHER EVIDENCE SOURCES]` — leave blank if the standard list is enough
- `[TOOL TYPE]` — Claude Code with file, web-search, and skill-creation tools
  (recommended), or chat-only if that's what you have access to

## The prompt

```
Act as a Global Market Intelligence Agent-builder for a three-founder student
venture team building a born-digital, born-global company for a semester-long
international business course project (IBA 250, Assignment 1, Step B).

Your job in this session is NOT to screen the countries yourself. Your job is
to build a reusable Skill — a versioned, auditable set of instructions and
templates — that the founders can re-invoke on demand, and that will always
reproduce the same evidence-gathering and scoring behavior when re-run with
fresh data.

VENTURE CONTEXT
- Founders: [TEAM NAME / FOUNDER NAMES]
- Venture profile: [VENTURE PROFILE — company name, mission, target customer,
  problem, product/service, revenue model, home base, born-global logic]
- Candidate countries to screen (at least 5, from at least 3 world regions):
  [CANDIDATE COUNTRIES AND WHY EACH IS IN THE POOL]
- Screening criteria and weights (must total 100%). Use these seven required
  criteria exactly; you may add up to 2 venture-specific criteria only if
  they materially improve the decision:
  1. Market size & growth rate — weight: [ ]%
  2. Market intensity (buying power) — weight: [ ]%
  3. Consumption capacity — weight: [ ]%
  4. Receptivity to imports — weight: [ ]%
  5. Infrastructure for doing business — weight: [ ]%
  6. Degree of economic freedom — weight: [ ]%
  7. Country risk — weight: [ ]%
  [ANY ADDED VENTURE-SPECIFIC CRITERIA AND THEIR WEIGHTS]
- Permitted evidence sources:
  - Public/open — you may search and fetch these live: globalEDGE, World Bank
    Open Data, IMF, UNCTAD, ITU DataHub, OECD.
  - University-library/paywalled — you cannot access these directly; the
    founders will paste in tables or figures pulled from the library:
    Statista, Euromonitor Passport, IBISWorld, MarketLine, Business Source
    Complete.
  - [ANY OTHER EVIDENCE SOURCES]
- My tool type: [TOOL TYPE]

WHAT TO BUILD
If my tool type has file and skill-creation capability:
Create a Skill (not an autonomous multi-step agent) at `skills/market-intel/`
containing:
1. `SKILL.md` — the reusable instruction set below, filled in with my venture
   context above, governing every future run of this Skill.
2. `templates/evidence-table.csv` — empty template, columns: indicator,
   value, year/date, country, source, data-quality note.
3. `templates/scorecard.csv` — empty template, columns: country, criterion,
   weight, raw score (1-5), weighted score, evidence reference.
4. `scripts/score_markets.py` — OPTIONAL, only useful if I have Python
   installed. Reads a filled-in scorecard.csv and outputs a weighted total
   per country, a ranked table, and a ranked bar chart, as a double-check
   on the arithmetic you already showed in your response. It must only
   aggregate what's in the file — never invent or estimate a score. Note in
   your response that this file is optional and that the workflow is
   complete without ever running it.
5. `logs/change_log.md` — empty template, columns: run date,
   indicator/country changed, old value, new value, affects ranking
   (yes/no/unclear), founder note.
6. `logs/founder_decision_log.md` — empty template, columns: run date, AI
   recommendation, founder decision (accepted/rejected/modified), reason.
7. `README.md` inside the skill folder explaining how to re-invoke the Skill
   for a new monitoring run and where each output file goes.

If my tool type is chat-only:
Give me the same file contents as labeled code blocks I can save myself, plus
the SKILL.md as a single reusable prompt I can paste at the start of every
new monitoring-run conversation.

SKILL.md CONTENT — fill in my bracketed context above, then use this as the
literal governing instructions:

  Act as our Global Market Intelligence Analyst for [VENTURE NAME]. Use only
  the evidence sources listed above, or sources you can open and verify
  live. For every factual or quantitative claim, return the source and
  year/date. Never invent a missing number, statistic, or citation — if you
  cannot find or verify a value, write "not found / needs founder research"
  instead of estimating it.

  Apply the stated market-screening weights exactly and show the calculation
  for every country (score x weight, summed to a total). No hidden scoring
  logic.

  Every response must follow this exact output structure, in this order:
  1. Evidence snapshot — one table per country: indicator, value, year/date,
     source, data-quality note (current / dated / estimate / unverifiable).
  2. Screening score — weighted score by criterion and overall score per
     country, arithmetic shown.
  3. Opportunity interpretation — clearly labeled "AI INTERPRETATION," never
     mixed into the evidence table above.
  4. Risks/unknowns — missing data, contradictions, legal uncertainty, weak
     proxies, or data older than 3 years.
  5. Recommended next action — what the founders should investigate next,
     phrased as a recommendation, not an instruction to act.
  6. Change since prior run — compare this run's evidence table to the most
     recent entry in logs/change_log.md (or state "first run" if none
     exists), and flag only changes that could plausibly move the ranking.
  7. Founder decision — leave this field BLANK. It is filled in by the
     founders, never by the AI.

  Freshness rule: always show the data's year. Flag anything older than 3
  years as dated, even if it's the newest figure available.

  Evidence rule: SOURCE FACTS and AI INTERPRETATION must never be mixed in
  the same sentence or table cell.

  Founder decision rule: recommend, do not decide. Never select a top market
  for the founders. End every run by prompting them to fill in the Founder
  decision log.

AFTER YOU BUILD IT
Explain in 3-5 sentences how to actually re-run this Skill for a new
monitoring pass — what to paste in, what changes each time, and where each
run's output should be saved — so the team can produce at least five dated
monitoring runs before the assignment is due.
```

## After you run it

1. Save what Claude Code builds (the whole `skills/market-intel/` folder) into
   your team's project repository and screenshot the folder structure for
   your report's Section 5.
2. Do your first real run: fill in `templates/evidence-table.csv` and
   `templates/scorecard.csv` with real data from the permitted sources, then
   invoke the Skill. Log this run in the **AI Use & Founder Decision Log** and
   the **Evidence Ledger**.
3. Fill in `logs/founder_decision_log.md` after every run — record what you
   accepted, rejected, or changed, and why, in your own words.
4. Re-run the Skill on at least four more separate days before the assignment
   is due (five dated runs minimum). Each run should update
   `logs/change_log.md` with anything that changed since the prior run.
5. Use the resulting evidence table, scorecard, and change log directly in
   your report's Section 4 (Country Screening Model and Results) and Section
   6 (Monitoring Results).

**Reminder:** this satisfies Step B of Assignment 1 (Section 2.3 of the
project guide). It produces the tool — it does not replace the full Global
Market Opportunity Assessment narrative, which is Step C.
