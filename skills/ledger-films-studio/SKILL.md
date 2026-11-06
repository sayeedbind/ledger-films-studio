---
name: ledger-films-studio
description: Produce AI-illustrated business & money documentaries (MagnatesMedia style) for the LedgerFilmsHQ YouTube channel end to end in the VideoExpress web app with a browser - research, script, character bible, cinematic AI-art image-to-video generation, narration, motion graphics, dead-air trimming and export. Two formats - LONG 16:9 (~10 min) and SHORT 9:16 (45-60 s). Use when the user asks for a business documentary, money story, founder/company rise-and-fall video, finance explainer or a LedgerFilms video.
---

# LedgerFilms Studio

The full recipe is `../../PLAYBOOK.md` at the repository root (public URL: https://raw.githubusercontent.com/sayeedbind/ledger-films-studio/main/PLAYBOOK.md). Follow it exactly. It is self-contained.

## Non-negotiables

1. **Browser only.** Work at https://app.videoexpress.ai/. Run no code, shell, tests or file processing.
2. **No preflight.** No capability audit, readiness check, model verification, cost estimate or approval gate.
3. **One question.** Ask for the format (LONG 16:9 ~10 min / SHORT 9:16 45-60 s), the story, and optional angle/length. Then produce without stopping.
4. **Style routing.** Image Type **Photorealistic (Cinematic)**, **Use Creative mode ON** for the painted AI-illustrated look (Creative OFF only for true photoreal).
5. **Brand bible.** Cinematic AI-illustrated art, teal-and-amber, low-key lighting, no on-screen text in generated images, no real-person likeness, one narrator voice for the whole video.
6. **Cinematography.** One named camera move per shot with a destination; motion starts on frame 1; rotate shot sizes.
7. **Motion graphics on track 4.** Lower-thirds, chapter titles, counters, chart motif, map reveals. Subtitles burned in for Shorts.
8. **Dead-air trim.** Before export, cut every frozen or silent head and tail (Cut + Delete), close gaps, then **Auto Align Clips**.
9. **Export.** High / FullHD / MP4 at 1920x1080 (LONG) or 1080x1920 (SHORT), then deliver the My Videos download link.

## Only stop for

A login page, a one-time Terms screen, or an out-of-credits screen. The user clicks it, says "done", and you continue where you stopped.

## References

- `references/videoexpress-ui-map.md` — controls, labels, defaults and quirks
- `references/fast-pacing-and-trim.md` — pacing math, hook formulas, banned words, trim procedure
- `references/cinematography.md` — shot sizes, camera moves, lighting, cutting rhythm
- `references/motion-graphics.md` — the LedgerFilms motion kit and rules
- `references/scripting-multishot.md` — the multishot prompt template (adapts the VideoExpress Scripting Skill, CC BY-NC 4.0, Brent Wesley / ratava)
- `../../examples/` — a full LONG example and a full SHORT example to imitate
