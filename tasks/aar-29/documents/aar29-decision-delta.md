**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 50: `| Path | Video | +anchor 20 | Unit | vs $0.80 |`

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# AAR-29 ruling — exact rule/token delta, verbatim blocks

Creative Director, owner of AAR-25. Companion to the AAR-29 ruling comment. All figures measured from the published bytes and from Runway's `openapi.json` / `api.md` (fetched 2026-09-22). Zero spend, zero credentials.

## 0. Where the standard stands

- **AAR-25 §1 Z-2 verbatim block: 215 characters.** Unchanged by this ruling. No Z-2 token is removed, added or reworded.
- **AAR-26's negative blocks are over the 1,000-char `negativePrompt` cap because they are verbose prose, not because Z-2 is too large.** The 215-char mandatory block consumes 21% of a 1,000-char cap.
- The 11:45 revision to AAR-26 is acknowledged and credited: the verbatim Z-2 block is now present in all three negatives, and the AAR-7 §4 silhouette #2 citation is now explicit.

## 1. Current measured state (AAR-26 `script-prompt-package`, updated 11:45:28Z)

| Concept | `promptText`: positive + audio | vs 1000 | `negativePrompt` | vs 1000 |
|---|---|---|---|---|
| C1 Chai Stall Ep.01 | 779 + 191 = 971 | fits | 1,392 | over 392 |
| C2 wind-down | 676 + 121 = 798 | fits | 1,246 | over 246 |
| C3 Chai Stall Ep.02 | 896 + 179 = 1,076 | **over 76** | 1,383 | over 383 |

## 2. Delta 1 — compact negative blocks (owner: AAR-26; removes no Z-2 token)

### C1 Chai Stall Ep.01 — 852 chars (from 1,392)

No visible text of any kind anywhere in the frame: text, letters, numbers, captions, subtitles, signage, labels, typography; logos, brand marks, watermarks, stamps; UI elements, app frames, phone-screen UI, fake quotes, speech bubbles; irrelevant decorative elements no shop signs, no menu or price boards, no chalkboards, no readable labels, no price tags. WARDROBE IS TOP PRIORITY: stitched two-piece salwar-kameez — loose straight-cut kurta, full sleeves, visible cuffs and straight hem, matching salwar, separate dupatta pinned over one shoulder. No sari, no saree, no pallu, no drape, no wrapped or flowing unstructured fabric. Hair fully open and down — no tie, braid, bun, clip or updo. Keep the centred maroon bindi and silver jhumkas. No face, age or complexion change. No sheer, tight, low-cut or bodycon clothing. No extra identified people.

### C3 Chai Stall Ep.02 — 852 chars (identical to C1)

Same block as C1.

### C2 wind-down — 555 chars (from 1,246)

No visible text of any kind anywhere in the frame: text, letters, numbers, captions, subtitles, signage, labels, typography; logos, brand marks, watermarks, stamps; UI elements, app frames, phone-screen UI, fake quotes, speech bubbles; irrelevant decorative elements no book or journal page text, no phone-screen content, no readable labels. No face, age or complexion change. Hair fully open and down — no tie, braid, bun, clip or updo. Keep the centred maroon bindi and silver jhumkas. No reclining or under-covers framing, no sheer or bodycon clothing.

## 3. Delta 2 — C3 `promptText` only (−115 chars)

Replace the identity parenthetical:

- OLD (195): `(wheatish skin, long open dark hair, small centred maroon bindi, silver jhumkas, stitched two-piece salwar-kameez with visible sleeve cuffs and straight hem plus a separate over-shoulder dupatta)`
- NEW (80): `(wheatish skin, long open dark hair, small centred maroon bindi, silver jhumkas)`

896 → 781; 781 + 179 = **961**. Fits.

## 4. Delta 3 — wardrobe vocabulary (2 tokens, C1 + C3)

`a soft cotton dupatta draped symmetrically over one shoulder` (60) → `a soft cotton dupatta pinned over one shoulder` (46).

"drape" is silhouette #3 (sari) vocabulary; the package cites #2, whose rule text is "Dupatta optional, and pinned when worn; no pallu". Prevents the AAR-19/AAR-20 unpinned-drape drift read.

## 5. Cost table

| Path | Video | +anchor 20 | Unit | vs $0.80 |
|---|---|---|---|---|
| veo3.1_fast 8 s audio | 120 | 20 | 140 cr = $1.40 | 1.75x |
| veo3.1_fast 6 s audio | 90 | 20 | 110 cr = $1.10 | 1.375x |
| seedance2_5 6 s @720p | 180 | 20 | 200 cr = $2.00 | 2.50x |
| seedance2_5 5 s @720p | 150 | 20 | 170 cr = $1.70 | 2.125x |
| gen4.5 5 s | 60 | 20 | 80 cr = $0.80 | not executable |

## 6. Verified vendor fields (Runway openapi.json, 2026-09-22)

| model | i2v `promptText` cap | `negativePrompt` | `audio` | native portrait |
|---|---|---|---|---|
| gen4.5 | 1000 | **absent** | **absent** | 720:1280 only |
| veo3.1 | 1000 | 1000 | present | 720:1280, 1080:1920 |
| veo3.1_fast | 1000 | 1000 | present | 720:1280, 1080:1920 |
| seedance2_5 | 15000 | absent | present | up to 1080:1920 |
| seedance2_mini / _fast / seedance2 | 3500 | absent | present | 720:1280 |

Pricing (Runway credits, $0.01/credit): gen4.5 12/s · veo3.1_fast 15/s audio (10 no-audio) · veo3.1 40/s audio (20 no-audio) · seedance2_mini 16/s (80 min) · seedance2_fast 29/s · seedance2 36/s · seedance2_5 30/s @720p, 68/s @1080p (80 min).

## 7. Fallback trigger

If the first `veo3.1_fast` unit fails AAR-25 §4's ≥10-frame wardrobe/identity gate, switch to `seedance2_5` with the identical Delta-1 compact blocks and C1/C3 at 6 s (200 cr = $2.00). The 2.25–2.5x is justified only with that evidence.

> **AAR-33 hard rule (2026-09-22) — no AI-generated text in the image, ever.** The on-image `AI-generated` disclosure is retired company-wide: never requested, rendered, burned in or QC-gated. Frames stay text-free. Disclosure lives outside the frame only — the caption note plus the platform AI-content label, both mandatory. Source of truth: AAR-33 document `disclosure-policy`.
