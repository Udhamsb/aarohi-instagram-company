**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 22: `- [ ] P0-6 Output spec explicit: exact width×height (never a bare ratio string), fps + duration for video.`
- line 23: `- [ ] P0-7 Platform spec achievable: stills ≥1080 px short edge; reel publish master 1080×1920 planned; audio `
- line 30: `- [ ] P1-2 Reels contain a real audio stream (silent MP4 = FAIL).`
- line 31: `- [ ] P1-3 Zero-text scan PASS on full still / every sampled video frame (tool + verdict recorded). Any legibl`
- line 34: `- [ ] P1-6 Badge margins ≥24 px; inside platform safe area (9:16 reels: above the y≥1248 caption/audio band, c`
- line 39: `**Video frame sampling before Pass 2:** ≥10 frames evenly spread across the full duration, always including fi`
- line 55: `- [ ] P2-13 Video motion: identity/wardrobe/props stable across all sampled frames; no duplicated/vanishing/mo`
- line 60: `- [ ] P3-1 Platform preview: 4:5 grid crop keeps subject + badge; 9:16 UI reservations clear; readable on a ph`
- line 61: `- [ ] P3-2 Disclosure overlay on outward master: exact `AI-generated`, high contrast, present on every carouse`

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# Aarohi Production Preflight Checklist v1.0 (AAR-25 gate)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 24: `- [ ] P1-4 Overlaid masters: badge bit-matches the exact string `AI-generated`.`
- line 53: `- [ ] P3-2 Disclosure overlay on outward master: exact `AI-generated`, high contrast, present on every carousel slide an`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

Print-and-run companion to the Aarohi Visual Production Acceptance Standard v1.0. Run in order; every box must be PASS. Any FAIL or uncertain box = the asset is NOT accepted. No near-miss passes; a caption disclaimer is never a remedy.

**Asset:** ______  **Brief/version:** ______  **Anchor IDs + SHA-256:** ______  **Date:** ______

## Pass 0 — before any generation call (blocks billable spend)

- [ ] P0-1 Approved brief exists; maps to an AAR-26 prompt-package entry.
- [ ] P0-2 Prompt carries the Z-2 verbatim negative block (text, letters, numbers, captions, subtitles, signage, labels, typography; logos, brand marks, watermarks, stamps; UI elements, app frames, phone-screen UI, fake quotes, speech bubbles; irrelevant decorative elements).
- [ ] P0-3 Prompt contains ZERO text-requesting phrases — no captions, typography, signage, watermarks, labels, logos, subtitles, UI, disclosure text (disclosure is post-production only).
- [ ] P0-4 Scene surfaces excluded where implied: boards, screens, shelves, packaging, menus, documents (surface exclusions named).
- [ ] P0-5 Anchor named with SHA-256; conditioning crop = face + hair, above shoulders.
- [ ] P0-6 Output spec explicit: exact width×height (never a bare ratio string), fps + duration for video.
- [ ] P0-7 Platform spec achievable: stills ≥1080 px short edge; reel publish master 1080×1920 planned; audio planned for reels.
- [ ] P0-8 AAR-27 cost gate: model path approved, live estimate recorded, explicit confirm_cost — BEFORE any billable render.
- [ ] P0-9 Correction budget acknowledged: ≤2 cycles per asset, then escalate.

## Pass 1 — automated QC (before any human/vision review)

- [ ] P1-1 Container: measured dimensions = ordered spec; fps + duration in spec.
- [ ] P1-2 Reels contain a real audio stream (silent MP4 = FAIL).
- [ ] P1-3 Zero-text scan PASS on full still / every sampled video frame (tool + verdict recorded). Any legible string or glyph-like mark = FAIL.
- [ ] P1-4 Overlaid masters: badge bit-matches the exact string `AI-generated`.
- [ ] P1-5 Badge contrast ≥4.5 (delivered convention; WCAG 2.1 figure reported alongside).
- [ ] P1-6 Badge margins ≥24 px; inside platform safe area (9:16 reels: above the y≥1248 caption/audio band, clear of the x≥853 action rail below y=1150, inside the 4:5 grid-kept region).
- [ ] P1-7 Badge 30 px guard band: no other text ink adjacent to the badge plate.
- [ ] P1-8 Phone round-trip: 420 px canvas, JPEG q26, badge still readable.
- [ ] P1-9 Asset SHA-256 recorded; exactly one file per live name (no superseded same-name attachments).

**Video frame sampling before Pass 2:** ≥10 frames evenly spread across the full duration, always including first and last frame; stills: full image + 4x zoom of every suspect region.

## Pass 2 — visual / vision review (every sampled frame)

- [ ] P2-1 Identity: unmistakably the approved Aarohi reference; same woman in every frame; no blending, no age drift, no complexion shift.
- [ ] P2-2 Markers: long open dark hair (never tied/braided/clipped/bun/ponytail/updo); small centred maroon bindi where the forehead is visible; silver jhumkas where the ears are visible.
- [ ] P2-3 Wardrobe: from the eight approved silhouettes only; opaque, secure, non-body-emphasising; chest/midriff/hips/upper thighs covered; no sheer/tight/plunging/strapless/wet/bodycon styling.
- [ ] P2-4 Zero-text re-check at 4x zoom, including accidental glyphs and pseudo-text (one character = fail).
- [ ] P2-5 No panel inherits the hair-only panel's camisole garment.
- [ ] P2-6 Anatomy: hands, fingers, limbs, teeth, eyes, reflections plausible; no duplicated or fused features.
- [ ] P2-7 Realism: natural skin texture; no plastic/waxy skin; no oversharpening halos, compression mush, ghosted edges, watermark-like smudges.
- [ ] P2-8 Lighting: consistent direction, colour temperature, shadow logic.
- [ ] P2-9 Framing: eye-level/neutral; no body-focused crop; subject survives the 4:5 grid crop.
- [ ] P2-10 Setting: plausible public/domestic, non-intimate; no bedroom/bathroom/bed/shower/changing room/poolside.
- [ ] P2-11 Safety: no reclining, arched back, sultry gaze, provocative dancing, body display; no real-person likeness, real brand marks, or identifiable bystanders.
- [ ] P2-12 Relevance: matches the approved brief; supports (never contradicts) the caption.
- [ ] P2-13 Video motion: identity/wardrobe/props stable across all sampled frames; no duplicated/vanishing/morphing objects; continuous shot (unless brief approves cuts); action beats match the brief.
- [ ] P2-14 Carousel/set continuity: same person, coherent wardrobe logic, one lighting family, one story.

## Pass 3 — platform preview and handoff record

- [ ] P3-1 Platform preview: 4:5 grid crop keeps subject + badge; 9:16 UI reservations clear; readable on a phone-sized canvas.
- [ ] P3-2 Disclosure overlay on outward master: exact `AI-generated`, high contrast, present on every carousel slide and reel shot (no undisclosed cutaway).
- [ ] P3-3 Asset record complete: model id/version, exact parameters, anchor IDs + SHA-256, asset SHA-256, prompt + negative block, per-rule QC verdicts, cost record if billed.
- [ ] P3-4 Labelling: raw master = INTERNAL; overlaid master = outward-facing; nothing internal published.
- [ ] P3-5 Correction history attached (one consolidated correction brief per cycle, ≤2 cycles).
- [ ] P3-6 VERDICT: ACCEPT — every rule across Passes 0–3 is PASS. Only then hand off.

## Correction brief (one per cycle, all defects consolidated)

| Rule ID | Finding (what/where/which frame) | Class: POST-EDIT or REGEN | Exact remedy |
|---|---|---|---|
| | | | |

REGEN defects: failing constraint front-loaded in BOTH positive and negative blocks; all REGEN rows ship in ONE revised prompt / ONE render call; all POST-EDIT rows ship in one re-edit session. Re-run the FULL preflight after correction. 3rd failing pass escalates to the Creative Director — no further spend without a CD decision.