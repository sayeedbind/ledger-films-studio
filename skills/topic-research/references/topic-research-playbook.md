# Topic research playbook (LedgerFilmsHQ)

The research stage that runs **before** `PLAYBOOK.md`. Its job: turn live signals into a ranked shortlist and three production-ready briefs, so the production run starts from a topic that is both hot and on-brand.

---

## 0. Operating rules

1. **Live only.** Every candidate cites a source you fetched in this session, with the fetch time. Never present recollection as trend data.
2. **Browser + fetch only.** Google Trends and Reddit via the browser; RSS feeds via direct fetch. No code, no shell, no API keys, no CLI.
3. **No preflight, no approval gates.** Sweep, score, rank, brief. Ask nothing until the shortlist is ready.
4. **Parallel where possible.** Feeds are independent — fetch them together.
5. **Ad-safety gate everything.** See Section 6.
6. **Report what failed.** If a source is blocked, say so in one line. Never silently substitute.

---

## 1. The sweep (collect raw signals)

Run all of these. Full URLs are in `sources.md`.

### A. Trend heat
- Google Trends trending-now for **US, UK, CA, AU** (the target markets). Read the term, volume band, percent change and age.
- Google Trends Business category for the US.
- Keep only hits with a business, money, company, founder, market or scam angle.

### B. Current stories (news RSS)
Fetch together, parse `<title>` and `<link>`:
- Google News RSS: the broad `business` query, plus `fraud OR scandal OR ponzi`, `company collapse OR bankruptcy OR fraud`, `startup founder OR acquisition OR IPO`, `layoffs OR shutdown OR insolvency`, `crypto OR bitcoin OR exchange collapse`, `AI company OR chipmaker OR data center`.
- CNBC Business and CNBC Tech.
- WSJ US Business, BBC Business, FT, Bloomberg Markets, TechCrunch.

### C. Audience demand (Reddit)
Open the top-of-week pages for r/Entrepreneur, r/business, r/finance, r/stocks, r/wallstreetbets, r/personalfinance, r/technology. Read titles, vote counts and the top comments. Note what people are angry about, curious about, and repeating.

### D. What the channel already has
Check the LedgerFilmsHQ channel page for recent uploads so you do not propose a topic already covered. Note any strong performers to look for adjacent angles.

### E. Competitive shape (optional, browser)
If a story is hot, look at how mainstream outlets frame it. The documentary angle should go one level deeper than the news cycle: the full arc, the numbers, the lesson.

---

## 2. Extract candidates

A **candidate** is a story with a subject, a stake, and a turn. Convert raw signals into candidates with this shape:

```
Subject:   <company / founder / deal / scam / market event>
Turn:      <what happened: collapse, rise, reversal, exposure, windfall>
Stake:     <the number, in dollars or percent>
Why now:   <the live signal that makes it timely>
Source(s): <feed or page + time fetched>
```

Recurring candidate archetypes for this niche:

- **Rise and fall** — a company or founder that peaked and collapsed.
- **The deal** — an acquisition, merger or funding round that changed a market.
- **The scam** — a fraud, ponzi, or accounting cover-up.
- **The reversal** — a swing that created or destroyed a fortune in days.
- **The empire** — how one person or family built unusual wealth.
- **The playbook** — a business model that quietly out-earns its louder rivals.
- **The warning** — a company or sector showing the early signs another famous failure showed.

Discard any signal that has no subject, no stake or no turn. "Stock market falls" is a mood, not a candidate; "Nasdaq drops into correction as AI stocks shed $1 trillion" is a candidate.

---

## 3. Score every candidate

Score 1–5 on each axis. Weighted total out of 100.

| Axis | Weight | 5 means | 1 means |
| --- | --- | --- | --- |
| **Trend heat** | 20 | On Google Trends or leading a major feed today | No live signal |
| **Evergreen pull** | 15 | Will still be watchable in a year | Dead in a week |
| **Ad intent** | 20 | Money, finance, business, self-improvement — top advertiser value | Sensitive, restricted, or grim |
| **Story arc** | 20 | Clear rise, turn and fall with a lesson | Flat or confusing |
| **Fact availability** | 15 | Public figures, dates and numbers are plentiful | Thin, disputed or private |
| **Shorts potential** | 10 | One 45-second beat is obviously extractable | Nothing punchy |

```
Total = (Trend × 20 + Evergreen × 15 + AdIntent × 20 + Arc × 20 + Facts × 15 + Shorts × 10) / 5
```

Rank by total. Break ties toward the higher **Ad intent**, then the higher **Story arc**.

**Hard filters (score 0, discard):**
- Needs a real, identifiable living person's likeness without clear public-interest justification.
- Rests on a claim that would be defamatory if the drama doesn't hold.
- Depends on private data, leaked documents, or a private individual.
- Must be framed as breaking news to work.

---

## 4. Present the shortlist

Show the user a table of the **top 10**:

```
#  | Topic (working title)        | Turn                | Score | Why now (one line)
---|------------------------------|---------------------|-------|-------------------
1  | <title>                      | collapse            | 88    | <live signal, source>
...
```

Then, for each of the top 10, one line on the angle and one on the ad-safety status. Keep it tight.

Add a short **Sources used** block at the end with each source and its fetch time, and a one-line **Sources unavailable** note if any were blocked.

---

## 5. Write the three full briefs

For the top three, write a **LONG brief** and a **SHORT brief**. Use this template:

```
### 1. <Working title> — score <n>

WHY NOW
- <live signal + source + time>
- <a second, independent signal if available>

THE ARC
- Setup:  <who, where, when, the ambition>
- Rise:   <the thing that worked, the numbers>
- Peak:   <the biggest number or boldest move>
- Turn:   <the crack>
- Fall:   <the collapse>
- Lesson: <the transferable line>

LONG (16:9, ~10 min)
- Hook:       <the cold-open line, under 15 s>
- Chapters:   <5-7 chapter names>
- Key facts to verify: <dates, figures, names to confirm before scripting>
- Visual motifs: <recurring images: the tower, the ledger, the empty boardroom, the chart>
- Motion graphics: <the numbers to animate and when>

SHORT (9:16, 45-60 s)
- Hook frame: <the single most extreme image>
- Beats:      <5 beats, one line each>
- Payoff:     <the line and the number>
- Loop/CTA:   <the closing question>

AD-SAFETY
- <ok as self-contained dramatized re-enactment / needs X avoided / rate to avoid>

NEWS-ADJACENT VALUE
- <why the audience will search for this after watching>
```

---

## 6. Ad-safety gate

The channel targets the highest advertiser intent, so protect it.

**Always:**
- Frame every video as an original dramatized documentary, not news.
- Present public figures through generic, non-identifiable depictions.
- Mark disputed claims as "reported" or "allegedly".
- Keep the tone premium and factual; no gore, no sexual content, no slurs.

**Never build a topic around:**
- An allegation against a private individual.
- A tragedy, a death, or a personal medical event as the hook.
- Content that requires showing real victims.
- A story that only works if you assert an unproven crime as fact.

If a strong candidate trips a filter, look for the **safe adjacent angle** — the market, the model, or the lesson — and propose that instead.

---

## 7. Cadence

### On demand
Run whenever the user asks, or when the content calendar drops below three approved topics.

### Weekly routine

| Day | Pass |
| --- | --- |
| **Monday** | Full sweep (Section 1), fresh shortlist of 10, briefs for the top 3. |
| **Wednesday** | Watchlist check: re-score last week's runners-up that stayed hot; add any new story from the collapse/fraud/AI queries. |
| **Friday** | Shorts pass: scan the week's feeds for a single 45-second beat that stands alone; propose one Short even if no LONG is ready. |

### Data hygiene
- Trend data expires fast. Only trust a signal fetched today or yesterday.
- Re-verify every fact in a brief before the production run starts.
- Keep a running "already covered" list so the same story is not proposed twice.
- If a topic scores 88+ but facts are thin, put it on the watchlist rather than approving it.

---

## 8. Handoff to production

When the user picks a brief:
1. Confirm the format for this run — LONG, SHORT, or both.
2. Carry the hook, arc, verified facts, visual motifs and motion-graphics plan straight into `PLAYBOOK.md` Sections 2 and 4.
3. Run production. The research brief replaces the script brainstorm; the script still gets written fresh in the playbook's format.
