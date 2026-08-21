# Step A — AI-Assisted Venture Brainstorming Prompt

**IBA 250: Building a Born-Global Digital Firm — Assignment 1, Step A**

This is the prompt template your team will use to complete Step A ("Use AI for structured idea generation"). Fill in the bracketed placeholders, paste the whole block into the AI tool of your choice, and keep the raw output — you'll log it in your **AI Use & Founder Decision Log** and cite it in your report.

Do not ask an AI tool for "a good business idea." That produces generic, unscored, unverifiable output. This prompt forces constraints, structure, and evidence instead.

---

## Before you paste this in

Fill in these five fields. Everything else in the prompt stays as written.

- `[TEAM NAME / FOUNDER NAMES]` — who's asking
- `[FOUNDER SKILLS, LANGUAGES, PRIOR EXPERIENCE]` — what your team actually brings (coding, design, a second language, an industry you've worked in, etc.)
- `[INDUSTRY, INTEREST AREA, OR PROBLEM SPACE]` — optional. Leave as "open" if you have no starting point, or narrow it (e.g., "education," "personal finance," "small-business tools") if you do
- `[WEEKS AVAILABLE TO PROTOTYPE]` — how much of the semester you realistically have before Assignment 1 is due
- `[TOOL TYPE]` — note whether your AI tool can create files and run code (e.g., Claude with file/code tools, ChatGPT with Code Interpreter) or is chat-only. This changes how it should hand you Task 2's folder and script.

---

## The prompt

```
Act as a startup ideation and market-screening advisor for a three-founder
student team building a born-digital, born-global venture for a semester-long
international business course project.

TEAM CONTEXT
- Founders: [TEAM NAME / FOUNDER NAMES]
- Skills, languages, and relevant experience: [FOUNDER SKILLS, LANGUAGES, PRIOR EXPERIENCE]
- Interest area (leave open if none): [INDUSTRY, INTEREST AREA, OR PROBLEM SPACE]
- Time available to build a working prototype: [WEEKS AVAILABLE TO PROTOTYPE]
- My tool type (has file/code capability, or chat-only): [TOOL TYPE]

HARD CONSTRAINTS — every idea must satisfy all four
1. Digitally deliverable: the core product/service can be delivered entirely
   through software, with no physical shipping required to serve a customer.
2. Potentially scalable across borders: nothing about the idea limits it to one
   country (e.g., no dependence on a single country's physical infrastructure,
   license, or regulator).
3. Solves a definable customer problem: name the customer and the specific pain
   point. Reject ideas where the "problem" is vague or the customer segment is
   "everyone."
4. Feasible for a student team to prototype in the time available: a working
   demo (even a simple one) must be realistic given our skills and weeks above.

TASK 1 — GENERATE IDEAS
Generate at least 5 distinct venture ideas that satisfy all four constraints.
For each idea, provide:
- Working name
- One-sentence pitch
- Target customer (be specific — not "small businesses," but e.g. "solo
  freelance graphic designers in emerging-market cities")
- The customer problem in one sentence
- Why it is digitally deliverable
- Why it is plausible cross-border (which regions/segments might it fit
  beyond one home market, and why)
- Rough revenue model

TASK 2 — SET UP A RESEARCH FOLDER AND ANALYSIS SCRIPT
For each of the 5+ ideas, list 2-3 data points that would help us judge
"global scalability," "customer problem severity," and "data availability" in
the decision matrix in Task 3 (e.g., market size for the target segment,
digital adoption rate, number of visible competitors). For each data point,
name where we could actually find it: our university library databases
(Statista, Euromonitor Passport, IBISWorld, MarketLine, Business Source
Complete) or public sources (World Bank Open Data, ITU DataHub, OECD,
globalEDGE). Do not invent values — only propose what to look for and where.

If my tool type above has file and code capability:
- Create a project folder structure for me: a top-level folder with
  /data/raw (for exported files or pasted tables from library databases),
  /data/sources (a running log: source name, URL/database, date accessed,
  what it's for), and /analysis (scripts and outputs).
- Write a Python script that reads a simple CSV I'll fill in (columns: idea
  name, criterion, raw score 1-5, weight) and outputs: a normalized weighted
  score per idea, a ranked bar chart, and a printed summary table. I will
  fill in the actual scores after I do the research — do not fabricate data
  to fill the template.

If my tool type above is chat-only:
- Give me the same folder structure as a checklist I can create manually in
  Google Drive or on my computer, and give me the same Python script as a
  code block I can run myself in Google Colab once I have real data.

TASK 3 — DECISION MATRIX
Build a decision matrix with the 5+ ideas as rows and these criteria as
columns: customer problem (severity/clarity), global scalability,
differentiation, feasibility for our team, data availability, and founder
interest. Leave every score cell blank for us to fill in after research —
do not assign scores yourself. Suggest a starting weight (must total 100%)
for each criterion and explain the logic for each weight in one sentence.

TASK 4 — COMPETITOR CHECK
For each idea, name 2-3 obvious existing competitors or substitutes (real
products/companies, not hypothetical ones) that already address a similar
problem. For each, state in one or two sentences what would be genuinely
different about our offering. If you are not confident a named competitor is
real and current, say so explicitly instead of guessing.

TASK 5 — PROS AND CONS
For each of the 5+ ideas, list 3-4 pros and 3-4 cons, covering at minimum:
market/customer risk, technical/build risk, and competitive risk.

OUTPUT RULES
- Do not pick a winner. Present all ideas neutrally with their matrix,
  competitor notes, and pros/cons, then stop. The founders — not the AI —
  make the final selection, and that decision and its reasoning will be
  recorded separately.
- Flag anywhere you are uncertain, guessing, or lack current information
  instead of filling the gap with an invented fact.
- Format the response with clear headers per idea plus one combined table
  for the decision matrix.
```

---

## After you run it

1. Save the raw output and log it in the **AI Use & Founder Decision Log** (tool used, prompt summary, what you kept/changed).
2. Do the actual research named in Task 2 using UA library databases and the public sources listed, and record each source in the **Evidence Ledger**.
3. Fill in the decision matrix with real scores tied to that evidence — not the AI's guesses.
4. As a team, discuss and select one idea. Write down *why*, in your own words. This decision must be attributed to the founders.
5. Move to naming the company and checking domain/social availability, then on to Step B (the AI Market Intelligence Agent/Skill).

**Reminder:** this satisfies Step A of Assignment 1 (Section 2.2 of the project guide). It is not a substitute for the Global Market Opportunity Assessment or the country-screening scorecard — those come in Step C.
