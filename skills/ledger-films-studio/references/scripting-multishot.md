# Multishot prompt format (LedgerFilms)

Adapts the VideoExpress Scripting Skill. **Attribution:** the multishot method and prompt format are from the VideoExpress Scripting Skill by Brent Wesley (ratava), licensed CC BY-NC 4.0. Keep this attribution if you redistribute.

Upstream: https://github.com/ratava/videoexpress-scripting-skill

## When to use it

Use the multishot format when **one generation should contain several hard cuts** — a montage beat, a rapid rise sequence, a collapse montage. For a single continuous shot, write one flowing paragraph instead.

## The tagged block template

```
[REFERENCE USE]
Reference Photo 1 = [character master name]. Reference Photo 2 = [location reference].

[IDENTITY / CONTINUITY]
[Paste the verbatim Character Bible line for every subject in frame.]
[Paste the verbatim Location block.]

[SCENE]
[Place], [time of day], [period/era]. [One line of context.]

[ACTION]
Shot 1: [beat 1 in cause-and-effect order]
Shot 2: [beat 2]
Shot 3: [beat 3]

[CAMERA]
Total duration: [n] s. Shot 1: [one named move + end framing]. Shot 2: [move + end]. Shot 3: [move + end].
Hard cuts between shots.

[LIGHT AND IMAGE]
Cinematic AI-illustrated documentary art, painterly digital illustration with photographic lighting, rich dark teal-and-amber palette, volumetric light, shallow depth of field, film grain, no text, no watermark.
[Lighting for this beat.]

[PRODUCTION SOUND]
[Transient only, or "silent — music handled on track 3".]

[NEGATIVES]
No text, no watermark, no logos, no extra limbs, no real-person likeness, no duplicated subjects.
```

## Worked example

```
[REFERENCE USE]
Reference Photo 1 = Arthur Vale. Reference Photo 2 = Vale Tower rooftop.

[IDENTITY / CONTINUITY]
Arthur Vale — 52, thinning grey hair, heavyset, charcoal three-piece suit, plain gold wedding band, tired eyes, default expression a tight smile.
Vale Tower rooftop — glass parapet, helipad marking left of frame, city skyline behind, dusk, warm interior light spilling from the stairwell door.

[SCENE]
Vale Tower rooftop, dusk, 1998. The night before the takeover.

[ACTION]
Shot 1: Arthur walks to the parapet, looking down at the city he owns.
Shot 2: He sets a leather briefcase on the parapet and opens it.
Shot 3: He looks at the unsigned papers inside, then closes it.

[CAMERA]
Total duration: 8 s. Shot 1: slow push-in ending on his back and the skyline. Shot 2: tilt down ending on the open case. Shot 3: rack focus from the papers to his eyes. Hard cuts.

[LIGHT AND IMAGE]
Cinematic AI-illustrated documentary art, painterly digital illustration with photographic lighting, rich dark teal-and-amber palette, volumetric light, shallow depth of field, film grain, no text, no watermark. Golden-hour rim light, cool blue shadow fill.

[PRODUCTION SOUND]
Wind only.

[NEGATIVES]
No text, no watermark, no logos, no extra limbs, no real-person likeness, no duplicated subjects.
```

## Rules that keep the look consistent

- Quotation marks in a prompt mean **speech**. LedgerFilms videos are third-person narrated, so dialogue is rare — keep narration in the TTS field, not the motion prompt.
- Two speakers per clip maximum if dialogue is used.
- Positive anchors beat prohibitions; describe what you want.
- Auto-enhance and image-prompt enhancement stay **OFF**.
- Reuse the same **STYLE ANCHOR** sentence in every single prompt, image and video.
- Chaining: the last frame of one clip is the first frame of the next when continuity matters — or generate fresh from the master to avoid drift.
