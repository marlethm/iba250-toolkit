# Step E — Political, Legal, and Economic Environment Prompt

**IBA 250: Building a Born-Global Digital Firm — Assignment 2, Step E**

This is the prompt template your team will use to complete Part B of
Assignment 2 ("Political, legal, and economic analysis," Section 3.3 of the
project guide). This step assumes you've already done **Step D** and know
which country or countries you're analyzing. Fill in the bracketed
placeholders, paste the whole block into the AI tool of your choice, and keep
the raw output — you'll use it directly to write Section 4 of your report.

## Numbers and graphs, not adjectives

The project guide is explicit: a narrative like "Country X has a stable
economy and good technology" does not satisfy this step. Every claim needs a
cited indicator, a value, and a year/date. The prompt below is built around
that requirement — it will not let the AI get away with vague descriptions,
and you shouldn't accept vague descriptions from it either.

## Get the files

Download the prompt, and download the starter kit — empty CSV templates for
the required ten-row table and the figures each country needs, plus an
optional charting script so the two required graphs per country (and the one
cross-country comparison figure) come from real numbers you can verify, not
a picture the AI drew from nothing.

- Download: `step-e-political-legal-economic-analysis-prompt.md` (this page)
- Download: `country-context-starter-kit.zip`

## Before you paste this in

Fill in these five fields, then paste the whole block below into your AI
tool.

- `[TEAM NAME / FOUNDER NAMES]`
- `[VENTURE PROFILE]` — same profile you used for Steps B, C, and D
- `[SELECTED COUNTRIES]` — the country or countries you settled on in Step D
  (at least one must be an emerging-market economy in the Global South,
  meaningfully different from the United States in cultural context)
- `[ANY OTHER EVIDENCE SOURCES]` — leave blank if the standard list is enough
- `[TOOL TYPE]` — chat-only is fine, or Claude Code if you want it reading
  your Step D files directly

## The prompt

```
Act as our political, legal, and economic country analyst for a
three-founder student venture team building a born-digital, born-global
company for a semester-long international business course project (IBA 250,
Assignment 2, Step E). This step produces the quantitative country analysis
that Step D's entry-mode decision depends on being accurate.

VENTURE CONTEXT
- Founders: [TEAM NAME / FOUNDER NAMES]
- Venture profile: [VENTURE PROFILE]
- Selected countries (from Step D): [SELECTED COUNTRIES]
- Permitted evidence sources:
  - Public/open — search and fetch these live: World Bank Open Data, World
    Bank Worldwide Governance Indicators (WGI), IMF, OECD, national
    statistics agencies and central banks for the countries above, and each
    country's relevant data-privacy/consumer-protection regulator or
    official legal-database site.
  - University-library/paywalled — you cannot access these directly; the
    founders will paste in tables or figures pulled from the library:
    Statista, Euromonitor Passport, IBISWorld, MarketLine, Business Source
    Complete.
  - [ANY OTHER EVIDENCE SOURCES]
- My tool type: [TOOL TYPE]

EVIDENCE RULES
- A narrative claim with no number, source, and year/date does not count as
  evidence — "stable economy" or "good technology" is not acceptable on its
  own. Every quantitative or legal claim needs a cited source and a
  year/date.
- Never invent or estimate a missing number or legal fact — write "not found
  / needs founder research" instead.
- Keep SOURCE FACTS and AI INTERPRETATION visibly separate — label
  interpretation explicitly, never blend it into a table cell.
- Do not select or rank countries beyond what Step D already decided — this
  step analyzes the countries already chosen; it does not re-screen them.

TASK 1 — Country tables
For EACH selected country, produce this exact ten-row table:

| Dimension / indicator | Findings with indicators (cite source & year) | What our firm must do to start operations |
|---|---|---|
| Political system / governance | | |
| Rule of law / contract environment | | |
| Data privacy | | |
| Consumer / advertising / IP | | |
| GDP / growth | | |
| Inflation / GDP per capita | | |
| Internet penetration | | |
| Digital payments | | |
| Taxes / registration for foreign digital services | | |
| Country-risk summary | | |

Minimum quantitative evidence per country (check off all of these — do not
skip any):
- At least eight decision-relevant indicators total across the table, each
  with its value, year/date, source, and a plain-language interpretation.
- At least one indicator/source for political/institutional conditions.
- At least two economic indicators (e.g., GDP per capita, growth, inflation,
  exchange-rate conditions, unemployment, income, or purchasing power).
- At least two digital/market-access indicators relevant to THIS venture
  specifically — not generic "internet exists" statements.
- At least one legal/regulatory issue directly connected to our actual
  product (data privacy, consumer protection, digital-services taxation, AI
  regulation, advertising, IP, platform rules, or cross-border payments).

After each country's table, add a one-sentence "So what?" statement
explaining how that evidence would change a real launch decision — not a
restatement of the table.

TASK 2 — Figure data (for the required graphs)
You cannot draw an image in this chat, so instead produce the underlying
data table for each required figure, with a one-line caption, so the
founders can chart it themselves (the starter kit's script or Excel/Google
Sheets both work):
- Two figures per country: pick the two indicators from Task 1 that most
  clearly affect our launch decision and that have a trend worth showing
  (e.g., internet penetration over several years, or an economic indicator
  over time) — for each, give (year, value, source) rows.
- One cross-country comparison figure: pick the two or three indicators most
  decision-relevant to THIS venture specifically, and give (country,
  indicator, value, year, source) rows comparing the selected countries
  side by side.

TASK 3 — Business Environment Synthesis
Do a short PESTLE analysis, or complete this table identifying the three
business-environment factors your team should monitor most closely during
the first year of operations:

| Area | Rating (1-5) | Strongest evidence | Main opportunity/risk | What our firm must do |
|---|---|---|---|---|
| Political/institutional environment | | | | |
| Legal/regulatory environment | | | | |
| Economic environment | | | | |
| Digital infrastructure/readiness | | | | |
| Payments/market access | | | | |
| Overall launch environment | | | | |

If more than one country was selected, build one of these rating rows per
country (or a combined comparison table like the worked example's), not a
single blended rating that hides which country drives which risk. Explain
why a meaningful change in each monitored factor could alter the
market-entry decision.

OUTPUT RULES
- Use country subheadings so each country's table, figures, and "so what"
  statement are clearly separated.
- Every table cell is either a cited fact or "not found / needs founder
  research" — never a silent guess.
- End with a short team-interpretation paragraph per country (and, if
  multiple countries, one comparative paragraph) stating which evidence most
  changes the launch decision.
```

## After you run it

1. Save the raw output and log it in the **AI Use & Founder Decision Log** —
   note anything you had to verify, correct, or find yourself because the
   AI flagged it as "not found."
2. Turn Task 2's figure data into actual charts — two per country plus the
   cross-country comparison — using the starter kit's optional script (if
   you have Python) or Excel/Google Sheets. A data table alone does not
   satisfy "include at least two sourced graphs/figures" — the guide wants
   a chart.
3. Verify the highest-stakes figures yourself (anything that would change
   whether you launch at all) against the original source before they go in
   your report.
4. Drop this output straight into **Section 4 (Political, Legal, and
   Economic Environment)** of your report, with the figures inserted after
   each country's table.
5. Move to **Step F** — the cultural analysis builds on the same selected
   countries and feeds directly off this step's launch-relevant findings.

**Reminder:** this satisfies Part B of Assignment 2 (Section 3.3 of the
project guide). The rubric scores Political, legal & economic analysis at 14
of 60 points — the single largest criterion in Assignment 2 — plus
Start-of-operations requirements at 6 more points. Together that's a third of
the assignment's grade, so the sourcing here matters more than in any other
step of Stage 2.
