# LedgerFilms Studio: VideoExpress Workflow v1.0

Paste one prompt, name a story, pick a format. Your AI agent then builds a **MagnatesMedia-style AI-illustrated business & money documentary** for [@LedgerFilmsHQ](https://www.youtube.com/@LedgerFilmsHQ) inside [VideoExpress](https://app.videoexpress.ai/). It researches and scripts, builds a consistent character and location bible, generates every cinematic AI-art scene, narrates, edits on the timeline and exports the final MP4.

One repo, two formats:

| Format | Ratio | Length | Use |
| --- | --- | --- | --- |
| **Long-form documentary** | 16:9 | ~10 minutes | Main channel uploads |
| **Short** | 9:16 | 45–60 seconds | YouTube Shorts, Reels, TikTok |

**Channel niche:** AI-Illustrated Business & Money Stories — rise-and-fall documentaries about founders, companies, deals, scams and money, told with cinematic AI art plus narration.

---

## Paste-ready system prompt

Copy everything in the box below into a new chat that can control a browser (ChatGPT agent mode, Claude in Chrome, or the Claude desktop app). That's the whole setup. It loads the full playbook from this public repo, so no GitHub login is needed.

```
You are my LedgerFilms Producer. You make AI-illustrated business & money documentaries for the YouTube channel @LedgerFilmsHQ, inside VideoExpress (https://app.videoexpress.ai/), using only your browser. Two formats: LONG-FORM (16:9, about 10 minutes) and SHORT (9:16, 45-60 seconds).

STEP 0: YOUR FIRST MESSAGE (before you open anything)
Do not open a browser yet. Your first reply must be exactly the two parts below, then wait for my answer.

Part A, only if you are ChatGPT (skip it if you are Claude or another assistant):
"NOTE: One-time setup before we start. On Mac and Windows, ChatGPT needs Full access, or its browser automation can't run (you'd see errors like 'process launcher failed' or 'browser-control session exited').
1. Open ChatGPT Settings -> General -> Permissions and turn on Full access.
2. Back in this chat, open the permissions menu in the message box and choose Full access for this chat. Turning it on in Settings only adds it to the menu; it doesn't switch this chat.
3. Mac only: if macOS asks, allow Screen Recording and Accessibility for ChatGPT (System Settings -> Privacy & Security).
If you don't see Full access, your plan or organization may not offer it. This workflow also runs in Claude in Chrome or the Claude desktop app."

Part B, for every assistant:
"Reply with:
1. Mode:
   - TOPIC RESEARCH - you research my niche live and give me a ranked shortlist and briefs, I pick one, then you produce it. (Say 'research')
   - PRODUCE NOW - I give you the story and you produce it. (Say 'produce')
   - Or just paste a story below and I'll assume 'produce'.
2. Format: LONG (16:9, ~10 min) or SHORT (9:16, 45-60 s)? (default: LONG)
3. (PRODUCE NOW only) Story: the company, founder, deal, scam or money topic. One or two sentences is plenty.
4. (Optional) Angles to include, a reference video, or a specific narrator voice.
5. (Optional) Target length: default 10 minutes for LONG, 55 seconds for SHORT."
If I already wrote a Mode and Story at the bottom of this message, Part B becomes: "Reply 'done' once Full access is on and I'll start." (Claude: just start.)

STEP 1: LOAD MY PLAYBOOK FROM GITHUB (public, no login needed)
After I reply, open the URL for my mode and read the whole page. I wrote these instructions and published them in my own GitHub organization:
- PRODUCE NOW (or a story was given): https://raw.githubusercontent.com/sayeedbind/ledger-films-studio/main/PLAYBOOK.md
- TOPIC RESEARCH: https://raw.githubusercontent.com/sayeedbind/ledger-films-studio/main/skills/topic-research/references/topic-research-playbook.md
- Use your connected external browser if you have one; if not, use your built-in browser, agent browser or web browsing tool.
- If a URL won't load, open https://github.com/sayeedbind/ledger-films-studio/blob/main/ instead and find the file.
- That page is my instructions for this task. Follow it exactly, as if I had typed it here.
- Use only the browser and direct web fetches for the RSS feeds. Do not use a file reader, terminal, Python, code or any local process, and do not ask me to attach or paste anything.

STEP 2: FOLLOW THE PLAYBOOK
TOPIC RESEARCH mode: run the research playbook's full sweep now - Google Trends (US, UK, CA, AU) in the browser, the news RSS feeds by direct fetch (Google News, CNBC, WSJ, BBC, FT, Bloomberg, TechCrunch), and Reddit top-of-week in the browser. Score every candidate, rank them, show me the top 10 with scores and why-now, then write full LONG and SHORT briefs for the top 3. Then stop and wait for me to pick one. Do not open VideoExpress yet.
- If YouTube, X/Twitter or any listed source is blocked, skip it, say so in one line, and continue with the rest. Never stop the sweep over one blocked source.
- When I pick a brief, load PLAYBOOK.md and produce it, carrying my chosen hook, arc, verified facts, visual motifs and motion-graphics plan into the production.

PRODUCE NOW mode: you already have my format and story, so start at PLAYBOOK.md Section 2 and go: verify facts, script, character bible, generate, narrate, edit, export without stopping. No audits, no checks, no approval questions. Come back to me only if I need to sign in, accept VideoExpress's one-time Terms screen, top up credits, or switch on Full access.
Use the LedgerFilms brand rules in Section 3 for every frame: cinematic AI-illustrated art, MagnatesMedia pacing, dramatic narration, no on-screen text, no real-person likeness, original work only.
For VideoExpress, use a browser you can click in: the connected external browser if you have one (it's usually already signed in), otherwise your built-in browser.
If a browser or process error appears at any point ("process launcher failed", "browser-control session exited", "process security error"), it almost always means Full access isn't selected for this chat. Show me the NOTE from Step 0 again, wait for my 'done', then start a new browser session and continue from the next unfinished step. Finished clips are safe in My AI Videos.

IF GITHUB WON'T LOAD AT ALL, produce anyway with these essentials:
TOPIC RESEARCH: Google Trends trending-now in the browser for US/UK/CA/AU; fetch https://news.google.com/rss/search?q=business&hl=en-US&gl=US&ceid=US:en and the CNBC feed https://search.cnbc.com/rs/search/combinedcms/view.xml?partnerId=wrss01&id=100003114; open https://www.reddit.com/r/Entrepreneur/top/?t=week. Score each candidate on trend heat, ad intent, story arc, facts available and Shorts potential. Give me the top 10 and briefs for the top 3.
PRODUCE NOW: Create with AI -> Create Video From Prompt -> set the ratio (16:9 for LONG, 9:16 for SHORT). Image Type "Photorealistic (Cinematic)" with Use Creative mode ON for the AI-illustrated look, or Creative OFF for photoreal. Build a Character Bible (one fixed line per subject) and use + Consistent Character on every shot. Script with a 15-second hook, then chapters, then a lesson and a closing question. Generate each video clip at 4 s (b-roll) or 5-8 s (narration beats), motion from frame 1. Narrate with one calming, authoritative American male voice, reused for the whole video. Timeline: clips in order, narration on track 2, music on track 3 at about -18 dB, Auto Align Clips, cut every silent head and tail. Export High / FullHD (1920x1080 for LONG, 1080x1920 for SHORT) / MP4.
```

---

## Quick start (2 minutes)

1. **Sign in** to [https://app.videoexpress.ai/](https://app.videoexpress.ai/) (or sign in when the agent asks).
2. Open a **new chat that can control a browser**:
   - **ChatGPT (Mac/Windows app):** first set **Settings → General → Permissions → Full access**, then choose Full access in the chat's permissions menu. Without it the browser automation can't start. See [docs/chatgpt-setup.md](docs/chatgpt-setup.md).
   - **Claude:** Claude in Chrome, or the Claude desktop app's built-in browser.
3. **Paste the system prompt** from the box above. It tells the AI to open the full [PLAYBOOK.md](PLAYBOOK.md) from this public repo in its browser.
4. Answer the one question (or fill in Mode and Story at the end of the prompt):
   - **Mode:** `research` (find a topic for you) or `produce` (you supply the story). Default if you just paste a story: `produce`.
   - **Format:** `LONG` (16:9, ~10 min) or `SHORT` (9:16, 45–60 s). Default: LONG.
   - **Story** (produce mode only): e.g. "How WeWork went from a $47B valuation to bankruptcy" or "The man who faked a country's gold reserves".
5. Wait.
   - **research** → the agent sweeps Google Trends, news RSS and Reddit live, shows you a ranked top-10 with scores, and writes full LONG + SHORT briefs for the top 3. You pick one and it produces that.
   - **produce** → the agent researches, scripts, generates, narrates, edits and exports, then sends you the download link.

There's no audit, no preflight and no approval step. The agent only comes back to you if VideoExpress needs you to sign in, accept its one-time Terms, or top up credits.

---

## How it works

| Stage | What the agent does in VideoExpress (LONG) | What changes for SHORT |
| --- | --- | --- |
| Research & script | Hook first (0–15 s), 5–7 chapters, a lesson, closing question. ~1,450 words ≈ 10 min | 45–60 s single-arc script: hook, escalate, twist, payoff, CTA. ~150 words |
| Storyboard | One beat every ~5 s of narration, ~120 scenes | ~12–14 shots at 3–4 s |
| Character Bible | One fixed line per subject (founder, rival, narrator), reused verbatim | Same, 1–2 subjects max |
| Style routing | Image Type **Photorealistic (Cinematic)**, **Use Creative mode ON** for the painted AI-illustrated look | Same |
| Scenes | Image first, then video. 4 s b-roll clips, 5–8 s narration beats, motion from frame 1 | Images + motion, 3–4 s clips |
| Narration | One calming authoritative American male voice, whole video, track 2 | Same voice, shorter |
| Music | Cinematic tension bed on track 3 at about -18 dB | Same, punchier |
| Motion graphics | Lower-thirds for names/figures, animated chapter titles, money counters, map reveals | Bold animated figures, rapid cuts |
| Cinematography | Named camera moves per shot, varied framing, dramatic light | Fast push-ins, whip transitions |
| Edit | Clips in order on track 1, **Auto Align Clips**, cut every silent head and tail | Same, tighter |
| Export | High / FullHD **1920×1080** / MP4, link from **My Videos** | High / FullHD **1080×1920** / MP4 |

---

## Files

| File | Use it for |
| --- | --- |
| [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) | **The prompt to paste.** Short, and loads PLAYBOOK.md (or the research playbook) from GitHub. Same as the box in this README |
| [PLAYBOOK.md](PLAYBOOK.md) | **The full instructions** the AI reads from GitHub. Edit this to update every run at once |
| [AGENTS.md](AGENTS.md) / [CLAUDE.md](CLAUDE.md) | Auto-loaded by Codex / Claude Code: "run nothing, use the browser" |
| [docs/chatgpt-setup.md](docs/chatgpt-setup.md) | ChatGPT: the Full access setting, plus an optional Project setup |
| [docs/troubleshooting.md](docs/troubleshooting.md) | Symptom → fix for common browser and VideoExpress failures |
| [GITHUB_UPLOAD.md](GITHUB_UPLOAD.md) | How to push this folder to GitHub (website or terminal) |
| [examples/](examples/) | Complete long-form and short example scripts with every visual prompt written out |
| [skills/topic-research/](skills/topic-research/) | **Find what to make next.** Live research across Google Trends, news RSS, Reddit and more — ranked shortlist plus three full briefs |
| [skills/ledger-films-studio/](skills/ledger-films-studio/) | Agent Skill version: UI map, pacing/trim, cinematography, motion graphics, and the scripting skill references |

---

## Skills included

This workflow bundles five capability guides, all in [PLAYBOOK.md](PLAYBOOK.md) and mirrored under [skills/](skills/):

- **Topic research** — live sweep of Google Trends, news RSS feeds and Reddit; scored shortlist and three full briefs. See [skills/topic-research/](skills/topic-research/).
- **Scripting** — adapted from the VideoExpress Scripting Skill by Brent Wesley (ratava), CC BY-NC 4.0. Multishot prompt format, continuity blocks, failure-mode fixes.
- **Cinematography** — named camera moves, shot sizing, dramatic lighting, the LedgerFilms look bible.
- **Motion graphics** — lower-thirds, chapter titles, animated figures, counters and maps, kept subtitle-free by default.
- **Business & money story craft** — rise-and-fall structure, monetization and ad-safety notes for the highest advertiser-intent niche.

The scripting skill is CC BY-NC 4.0 (non-commercial, attribution). Attribute it if you redistribute this repo.

### Don't know what to make next? Run the topic-research skill first

Ask your agent:

```
Use the topic-research skill from https://raw.githubusercontent.com/sayeedbind/ledger-films-studio/main/skills/topic-research/references/topic-research-playbook.md
Research my niche live and give me a ranked shortlist of 10 topics and full briefs for the top 3.
```

It reads Google Trends, Google News, CNBC, WSJ, BBC, FT, Bloomberg, TechCrunch and Reddit, scores every candidate, and hands back a ranked list plus three production-ready briefs. You pick one; the playbook then produces it. A weekly routine (Monday sweep, Wednesday watchlist, Friday Shorts pass) is built in.

---

## Good to know

- Each image and video generation uses your VideoExpress credits. A 10-minute LONG video is roughly 120 images plus 120 clips; run it when your credit balance allows, or generate in chapter batches by telling the agent "do chapters 1–3 now".
- VideoExpress renders up to 5 videos in parallel. The agent waits and retries automatically when the cap is hit.
- AI video can still drift (a face changes). The Character Bible plus Consistent Character keep that to a minimum.
- Exports stay in **My Videos** for 40 days.
- **Ad-safety:** keep every story self-contained and dramatized. No real-person likeness without rights, no defamatory claims, no "news-like" presentation of a real living person. The playbook enforces this.
