**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 1: `# Sogni Video Brief 01 — "Morning Chai Reset" (Seedance 2.5 test render)`
- line 7: `- line 155: `- The published asset carries the exact string `AI-generated` as a reel-native``
- line 16: `**`sogni-video-brief-01`** — "Sogni Video Brief 01 — Aarohi Morning Chai (5s`
- line 17: `9:16)". AAR-19 copies prompts from THAT document. This document is retained as`
- line 25: `(AAR-16 cost band). The publish master must be 1080×1920 (AAR-13 §3);`
- line 44: `**Model:** Seedance 2.5 via Sogni (`videoModel=seedance2-5`)`
- line 55: `reads as a real morning. This is the low-risk first render: static camera,`
- line 70: `| Resolution | 720p (720×1280) | 1080×1920 (Reels minimum per AAR-13 §3) |`
- line 71: `| Aspect ratio | 9:16 vertical | 9:16 vertical |`
- line 76: `The 9:16 vertical aspect is mandatory — this asset is an Instagram Reel.`
- …and 7 further line(s) in this document reference the same superseded formats.

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# Sogni Video Brief 01 — "Morning Chai Reset" (Seedance 2.5 test render)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 16: `3. **Overlay numeric spec (Refpack Stage A):** the `AI-generated` overlay is`
- line 155: `- The published asset carries the exact string `AI-generated` as a reel-native`
- line 190: `- [ ] Exact string `AI-generated` overlaid, lower-right, high contrast,`
- line 205: `"AI-generated visual; caption and storytelling by Aarohi's team."`
- line 206: `- [ ] Caption carries all storytelling; nothing except the `AI-generated``

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**STATUS — SUPPLEMENTARY ANNEX, NOT THE RENDER CONTRACT.** A parallel run of
this same issue posted the canonical brief first:
**`sogni-video-brief-01`** — "Sogni Video Brief 01 — Aarohi Morning Chai (5s
9:16)". AAR-19 copies prompts from THAT document. This document is retained as
a QC annex: it is substantively identical (same concept, spec, and safety
frame) and adds four requirements the canonical brief should adopt into the
asset record and preflight:

1. **Anchor provenance (Refpack RC-9):** record the anchor ID and the anchor
   crop's SHA-256 in the asset record so identity continuity is provable.
2. **Publish master resolution:** 720×1280 is the TEST-render resolution only
   (AAR-16 cost band). The publish master must be 1080×1920 (AAR-13 §3);
   re-render or upscale before any publication.
3. **Overlay numeric spec (Refpack Stage A):** the `AI-generated` overlay is
   lower-right, contrast ≥ 4.5 (delivered-asset convention), right/bottom
   margins ≥ 24 px, verified on a 420 px phone-canvas JPEG round-trip,
   continuous across all 5 s.
4. **Per-frame anatomy gate:** hands, fingers, grip, cup, and saucepan are
   checked on sampled frames throughout the clip (pour-hold frames included),
   not only on the first frame — the canonical §12 items 6/11 cover this; this
   annex makes the per-frame cadence explicit.

Everything below is the original annex content, kept for traceability.

---

**Issue:** AAR-17 (child of AAR-16)
**Owner:** Creative Director
**Render owner:** AAR-19 (AI Visual Producer)
**Copy partner:** AAR-18 (Content Strategist — final caption)
**Model:** Seedance 2.5 via Sogni (`videoModel=seedance2-5`)
**Status:** Approved for render — this document is the render contract for AAR-19.

---

## 1. Concept

A 5-second single-shot diary moment: Aarohi makes her morning chai in a bright
home kitchen. She pours from a small steel saucepan into a clay kulhad, steam
rising, takes one unhurried sip, and glances toward the window light with a
faint natural smile. No plot, no dialogue — one grounded, everyday beat that
reads as a real morning. This is the low-risk first render: static camera,
ambient-only audio, one approved wardrobe set, one location.

Why this concept: it is Persona Bible §3 approved example #4 (making chai in a
bright kitchen) and pairs directly with the Caption-First Template's daily
lifestyle example (AAR-15 §"Daily lifestyle / mood moment"). It exercises every
QA lane that matters — identity lock, hair, markers, wardrobe, motion physics,
native audio — without any risky element.

## 2. Format and technical spec

| Parameter | Test render (AAR-19 first pass) | Publish master |
|---|---|---|
| Duration | 5 s (fixed; do not extend) | 5 s |
| Model | Seedance 2.5 (`seedance2-5`) | Seedance 2.5 (`seedance2-5`) |
| Resolution | 720p (720×1280) | 1080×1920 (Reels minimum per AAR-13 §3) |
| Aspect ratio | 9:16 vertical | 9:16 vertical |
| Audio | Native ambient ON, no speech | Native ambient ON, no speech |
| Shots | Exactly 1 continuous shot; no cuts | Same |
| Frame rate | Model default (30 fps preferred) | Same |

The 9:16 vertical aspect is mandatory — this asset is an Instagram Reel.
Render the test at 720p to validate the pipeline at AAR-16's quoted cost band
(~$1.50 published Seedance 2.5 5s/720p). The publish candidate must be re-rendered
or upscaled to 1080×1920 before any publication; 720p is not publishable (AAR-13 §3
resolution gate).

## 3. Camera

- Neutral eye-level, waist-up medium framing, subject centre-left with negative
  space right (leaves room for the disclosure overlay and platform UI).
- Locked-off tripod framing for the full 5 seconds. No pan, no tilt, no zoom,
  no handheld feel, no shake.
- Do not crop at the forehead or the hands — bindi and the pour must stay in
  frame for the entire shot.

## 4. Action (the 5 seconds)

- 0.0–2.0 s: she pours chai from the steel saucepan into the clay kulhad on the
  counter; steam rises visibly.
- 2.0–3.5 s: she lifts the kulhad with both hands and takes one small, calm sip.
- 3.5–5.0 s: she lowers the cup and turns her gaze toward the window light,
  faint natural smile. Hold; no new action begins.
- Hands, fingers, and grip must stay anatomically correct in every frame
  (AAR-13 §3 anatomy gate applies per-frame to video).

## 5. Lighting and colour

- Soft morning daylight from frame left (window), warm but truthful colour.
- Realistic skin texture with visible pores; no beauty-filter smoothing.
- Natural shadow logic; no glow edges, halos, or HDR look.

## 6. Native-audio direction (ambient only)

- Ambient kitchen soundscape: gentle liquid pour, faint cup clink, soft steam,
  distant morning birds or street ambience at low level.
- No speech, no voiceover, no lip-synced vocals, no music. Music, if used at
  all, is a post-publication platform decision (AAR-18/AAR-4) and never a
  generation output.
- Rationale: ambient-only avoids lip-sync drift risk and voice-identity claims
  on a first render; the persona is defined visually, not vocally.

## 7. Wardrobe and identity lock (non-negotiable)

- Wardrobe: soft cotton kurta (warm muted tone) + relaxed trousers — approved
  silhouette #1 from Reference Pack §4. Opaque, secure, non-body-emphasising.
- Identity: the same fictional North Indian woman, 22–26, wheatish skin with
  natural even texture, long open dark hair worn fully down for the entire
  clip, small centred maroon bindi, silver jhumkas.
- Generation must anchor on the approved reference set
  (`AAROHI_REFERENCE_PACK_v2_FACE_BODY_SHEET.png` v2.1 + character sheet v2.1),
  per RC-9: record the anchor ID and the anchor crop's SHA-256 in the asset
  record. The hair-only rule applies: no frame may inherit the character
  sheet's camisole garment (Refpack §3 hair-only rule).

## 8. Final text-to-video prompt (copy exactly)

Positive prompt:

> Realistic editorial diary video, 5 seconds, one continuous locked shot, 9:16
> vertical. A fictional North Indian woman in her mid-twenties, wheatish skin
> with natural texture, long open dark hair worn fully down, a small centred
> maroon bindi, and silver jhumkas, wearing a soft cotton kurta in a warm
> muted tone with relaxed trousers. In a bright home kitchen with soft morning
> daylight from a window at frame left, she pours fresh chai from a small steel
> saucepan into a clay kulhad on the counter, steam rising, then lifts the cup
> with both hands, takes one calm unhurried sip, lowers it and turns her gaze
> toward the window light with a faint natural smile. Neutral eye-level medium
> waist-up framing, camera locked on a tripod with no movement, warm truthful
> colour, realistic skin and fabric texture, natural depth of field, quiet
> domestic ambience with a gentle pour and soft steam, no speech. Everyday,
> grounded, respectful lifestyle editorial. No on-image text of any kind.

Negative prompt / exclusion block (Persona Bible §3 adapted for video):

> Do not change her face, apparent age, complexion, hairline, or facial
> proportions at any point in the clip. No tied hair, braid, ponytail, bun,
> clip-up, or updo; her hair stays long and visibly open in every frame. No
> missing maroon bindi or silver jhumkas. No wardrobe change mid-clip; no
> sheer, tight, low-cut, strapless, wet, lingerie-like, or bodycon clothing.
> No seductive pose or expression, no reclining, no bedroom, bathroom, or bed
> setting, no body-focused crop, no low-angle chest or hip emphasis. No second
> person, no extra hands entering frame, no text, captions, watermarks, or
> logos in frame. No camera shake, no whip pan, no speed ramp. No plastic or
> over-smoothed skin, no warped fingers or duplicated hands, no morphing
> objects, no melting cup or saucepan geometry.

## 9. Disclosure handling (resolves Persona Bible §4 vs AAR-13/AAR-15)

- The generation is text-free. No readable text may be baked into the render
  (AAR-13 §1 — AI typography is an automatic reject).
- The published asset carries the exact string `AI-generated` as a reel-native
  overlay applied in post-production, not as a generation output. The Persona
  Bible §4 disclosure standard is the standing approval of this exact copy
  (hyphenated, never replaced by a brand label) — that is the recorded
  campaign-text exception under AAR-13 §2; no other text is approved.
- Overlay spec (Refpack Stage A conventions): lower-right safe area, high
  contrast (≥ 4.5 delivered-asset convention), right/bottom margins ≥ 24 px,
  readable after a 420 px phone-canvas JPEG round-trip, present continuously
  across the full 5 seconds (single shot ⇒ no undisclosed cutaway is possible,
  but the overlay must never drop out).
- Raw renders without the overlay are internal work files; the overlay-bearing
  file is the only outward-facing deliverable (Refpack §2/Stage C).

## 10. Acceptance criteria (AAR-19 QA gate — all must pass)

Identity and continuity (Refpack Stage B):

- [ ] B1 Face unmistakably matches the approved Aarohi anchor; no drift across all 5 s.
- [ ] B2 Reads as North Indian woman, 22–26, wheatish, naturally textured skin.
- [ ] B3 Hair long, open, down in every frame; never reads as tied.
- [ ] B4 Bindi visible whenever the forehead is in frame (it is, for the full shot).
- [ ] B5 Jhumkas visible whenever ears are visible (natural hair occlusion allowed).
- [ ] B6 Wardrobe is kurta + relaxed trousers (§4 silhouette #1); opaque, secure.
- [ ] B7 Action, pose, setting everyday and non-suggestive; kitchen is non-intimate.

Clean-image gates (AAR-13 §1/§3):

- [ ] No readable text, logo, watermark, or UI chrome baked into any frame.
- [ ] Anatomy per frame: hands, fingers, grip, cup, saucepan plausible throughout;
      no morphing or fused geometry.
- [ ] Lighting consistent across the clip; physics of pour/steam plausible.
- [ ] No artifacts: ghosting, duplicated objects, oversharpening, compression mush.

Disclosure (Persona Bible §4 + Refpack Stage A on the delivered file):

- [ ] Exact string `AI-generated` overlaid, lower-right, high contrast,
      ≥ 24 px margins, survives phone round-trip, visible for all 5 s.

Technical (AAR-16 plan + AAR-13 §3):

- [ ] 5 s duration; 9:16; test at 720×1280; publish master at 1080×1920.
- [ ] Native ambient audio present, no speech artifacts or phantom vocals.
- [ ] Single continuous shot; no cuts, no camera drift.
- [ ] Anchor provenance recorded: anchor ID + anchor crop SHA-256 (RC-9).
- [ ] Model, resolution, duration, workflow ID, and live cost estimate recorded
      in the asset record; cost quoted before submission, `confirm_cost=true`.

Copy handoff (AAR-15 — owned by AAR-18):

- [ ] Caption follows the Caption-First Template with the disclosure line
      "AI-generated visual; caption and storytelling by Aarohi's team."
- [ ] Caption carries all storytelling; nothing except the `AI-generated`
      badge appears on the visual.

Release decision (Refpack §5): any unchecked or uncertain box ⇒ REJECT —
regenerate with a corrected brief; a caption disclaimer is never a remedy.

## 11. Render notes for AAR-19

- Quote the live Sogni estimate for 5 s / 720p before submission and record it
  next to the published Seedance 2.5 figure (~$1.50) for variance tracking.
- Save the MP4 to a durable location immediately on completion; the 24-hour
  URL is not storage.
- If Seedance 2.5 rejects the prompt length, trim §8's negative block first —
  never the identity-lock clauses.
- Report failures as defect + failing criterion (e.g. "B3: hair reads tied at
  t=4.2 s") so this brief can be revised precisely.