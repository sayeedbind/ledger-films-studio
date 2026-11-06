# Sources (verified working, 2026-11-06)

Every source below was tested from this environment. Use the stated access method. Re-test if a source starts failing; the access map is part of the skill.

## Access methods

- **browser** — open the URL in a browser tab. The page renders and its text is readable.
- **fetch** — retrieve the URL with a direct HTTP request. Works for RSS/XML endpoints. Prefer this: it returns structured, complete data in one call with no rendering.
- **blocked** — do not rely on it. List it in the report as unavailable.

---

## 1. Google Trends — browser

| Purpose | URL |
| --- | --- |
| Trending now, US, past 24 h | `https://trends.google.com/trends/trendingsearches/daily?geo=US` |
| Trending now, UK | `https://trends.google.com/trends/trendingsearches/daily?geo=GB` |
| Trending now, CA / AU | `...geo=CA` / `...geo=AU` |
| Rising finance searches | `https://trends.google.com/trends/trendingsearches/daily?geo=US&category=3` (Business) |

Readable fields per trend: the term, search volume band ("200K+"), the change ("1,000%"), the age ("14 hours ago"), and related queries.

**Note:** the page redirects to `https://trends.google.com/trending?geo=US`. That is expected; read the rendered text.

**Use it for:** raw search heat. Mostly mainstream. Filter hard for business/money relevance — a good hit is something like "tax brackets 2027", "stock market", or a named company.

---

## 2. News RSS feeds — fetch

All of these returned live items on the test date. `fetch` them, then parse `<title>` and `<link>` tags.

### Google News RSS — the workhorse

Build any query. 80–100 items per feed.

```
https://news.google.com/rss/search?q=QUERY&hl=en-US&gl=US&ceid=US:en
```

Ready-made niche queries:

| Angle | Query |
| --- | --- |
| Broad business | `business` |
| Collapse / failure | `company+collapse+OR+bankruptcy+OR+fraud` |
| Scam / fraud | `fraud+OR+scandal+OR+ponzi+OR+embezzlement` |
| Founders / deals | `startup+founder+OR+acquisition+OR+IPO+OR+merger` |
| Layoffs / decline | `layoffs+OR+shutdown+OR+insolvency` |
| Money / markets | `stock+market+OR+interest+rates+OR+inflation` |
| Billionaires | `billionaire+OR+fortune+OR+wealth` |
| Crypto | `crypto+OR+bitcoin+OR+exchange+collapse` |
| AI business | `AI+company+OR+chipmaker+OR+data+center` |

URL-encode: spaces as `+`, `OR` literal, `&` as `%26` if inside the query.

### Publisher feeds

| Source | URL | Items | Angle |
| --- | --- | --- | --- |
| CNBC — Business | `https://search.cnbc.com/rs/search/combinedcms/view.xml?partnerId=wrss01&id=100003114` | ~30 | Mainstream business, strong on markets |
| CNBC — Tech | `https://search.cnbc.com/rs/search/combinedcms/view.xml?partnerId=wrss01&id=19854910` | ~30 | AI, chips, big tech |
| WSJ — US Business | `https://feeds.a.dj.com/rss/WSJcomUSBusiness.xml` | ~20 | Deals, corporate moves |
| BBC — Business | `https://feeds.bbci.co.uk/news/business/rss.xml` | ~54 | Global, explains impact for a general audience |
| FT | `https://www.ft.com/?format=rss` | ~12 | High-signal finance |
| Bloomberg — Markets | `https://feeds.bloomberg.com/markets/news.rss` | ~20 | Markets, macro |
| TechCrunch | `https://techcrunch.com/feed/` | ~20 | Startups, funding, founder stories |

**Use them for:** the specific, named, current stories — the raw material for a documentary. RSS gives a headline, a source and a link, which is exactly what a topic shortlist needs.

---

## 3. Reddit — browser

| Subreddit | URL |
| --- | --- |
| r/Entrepreneur | `https://www.reddit.com/r/Entrepreneur/top/?t=week` |
| r/business | `https://www.reddit.com/r/business/top/?t=week` |
| r/finance | `https://www.reddit.com/r/finance/top/?t=week` |
| r/personalfinance | `https://www.reddit.com/r/personalfinance/top/?t=week` |
| r/technology | `https://www.reddit.com/r/technology/top/?t=week` |
| r/stocks | `https://www.reddit.com/r/stocks/top/?t=week` |
| r/wallstreetbets | `https://www.reddit.com/r/wallstreetbets/top/?t=week` |

Swap `t=week` for `t=month` or `t=day`. Read the rendered body: post titles, upvote counts, comment counts and the top comments.

**Use Reddit for:** audience demand — what people are already arguing about, asking about, and feeling. A story Reddit is angry or fascinated by has proven emotional pull. Reddit comments are excellent for finding the "why people care" line.

**Blocked:** `old.reddit.com` (login required) and Reddit's `.json` API (403). Use `www.reddit.com` HTML only. `.rss` endpoints are also 403.

---

## 4. Blocked or unreliable in this environment

Do not build the workflow around these. Note them as unavailable if relevant.

| Source | Symptom |
| --- | --- |
| YouTube (search, trending, homepage) | Returns an empty body — bot/consent wall |
| X / Twitter | Redirects to a login onboarding page |
| Reuters, Forbes, Business Insider, MarketWatch, Bloomberg (site), Yahoo Finance, The Verge | Fail to load through the server, or return an empty body |
| BBC, FT, TechCrunch (sites, not feeds) | Site load fails; use the RSS feeds instead |
| news.google.com (site, not RSS) | Fails to load; use the Google News RSS instead |

**Substitute for YouTube:** use Google News RSS queries to find which business stories are being covered, and Reddit to see which have a video-hungry audience. You can also read a channel's public page in the browser for format reference, but do not depend on YouTube search or trending.

---

## Fetch hygiene

- Set a normal browser User-Agent on fetches: `Mozilla/5.0`.
- Take several feeds in one pass; they are independent, so fetch them together.
- Record the fetch time for every source used. Trend data is only valid with a timestamp.
- If a feed returns 0 items, treat it as broken and move on — do not report it as "no news".
