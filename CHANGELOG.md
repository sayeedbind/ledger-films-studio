# Changelog

## 1.0.0 (2026-11-06): LedgerFilms Studio

First release. Consolidates four upstream workflows into one repo tuned for the LedgerFilmsHQ channel.

### Added
- **`README.md`** — overview, the paste-ready system prompt, quick start, the LONG/SHORT comparison table, and a skills list.
- **`SYSTEM_PROMPT.md`** — the short paste-in prompt. Loads `PLAYBOOK.md` from this public repo. Includes the ChatGPT Full access note and a no-GitHub fallback.
- **`PLAYBOOK.md`** — the full instruction set:
  - the LedgerFilms brand bible (art style anchor, palette, lighting, motifs, never-do list, ratio safe areas),
  - research and script structure for LONG (~1,450 words, 7-section beat sheet) and SHORT (~150 words, single arc),
  - the VideoExpress LONG pipeline (character bible, locations, storyboard, images, video, narration, music, assembly, motion graphics, dead-air trim, Auto Align, smoke test),
  - the SHORT deltas,
  - **cinematography** rules (shot sizes, named camera moves, lighting, lens language, cutting rhythm),
  - **motion graphics** kit and rules,
  - delivery, recovery, and file map.
- **`skills/ledger-films-studio/`** — agent skill with `SKILL.md` and five references: UI map, pacing/trim, cinematography, motion graphics, and the multishot prompt template.
- **`docs/chatgpt-setup.md`**, **`docs/troubleshooting.md`**.
- **`examples/long-form-example.md`**, **`examples/short-example.md`** — full worked scene maps.
- **`AGENTS.md`**, **`CLAUDE.md`**, **`.gitignore`**.

### Sources
Adapted from, and structured after, the following:
- `sayeedbind/realistic-mini-dramas` — repo structure, zero-preflight browser-only philosophy.
- `sayeedbind/historical-documentary-video-workflow` — documentary pipeline, narration reuse, timeline trim.
- `sayeedbind/videoexpress-stickman-story-agent` — character master, location blocks, continuity and recovery rules.
- `sayeedbind/videoexpress-two-character-agent` — authorization scope, consistency and cropping-safety rules.
- `ratava/videoexpress-scripting-skill` (Brent Wesley, CC BY-NC 4.0) — multishot prompt format, continuity blocks, failure-mode fixes, browser-workflow guidance.

### Changes from the sources
- Niche retuned to AI-Illustrated Business & Money Stories for @LedgerFilmsHQ.
- Added a **dual-format** model: LONG 16:9 ~10 min and SHORT 9:16 45–60 s, in one playbook.
- Added a **cinematography** reference and a **motion graphics** reference.
- Added the **LedgerFilms brand bible** with a fixed style anchor and ad-safety rules.
- One narrator voice, no presenter intro.
