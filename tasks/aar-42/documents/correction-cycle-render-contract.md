# AAR-42 — correction-cycle render contract and prompt record

## Purpose and scope

Regenerate **one coherent five-slide still-image set** for the 2026-09-23 Aarohi carousel. This is correction cycle 1 of 2 after AAR-38 rejected the AAR-36 set on CAC-20/21/22/23. No previous charge approval transfers to this new charge. This contract authorizes no render until a human accepts the linked `confirm_cost=true` card.

## Live preflight

- Provider: Runway MCP `generate_image`; authenticated workspace checked 2026-09-22 in this run.
- Available model: `nano-banana-2`; parameters per call: `ratio: 4:5`, `imageSize: 2K`, `count: 1`, one continuity-anchor reference.
- Live balance: **1,742 Runway credits**.
- Current official price evidence carried from the immediately preceding same-model contract: **11 credits per 2K `nano-banana-2` image**. Exact estimated charge: **5 × 11 = 55 Runway credits**; estimated remaining balance: **1,687 credits**.
- Calls: exactly five, S1 through S5, one output each. No video, reel, audio, or speculative variants.

## Immutable identity, wardrobe and hygiene locks

Every prompt repeats this locked outfit word-for-word:

> `knee-length open oatmeal-beige knit cardigan over a dusty-rose opaque woven relaxed top, hip length, relaxed cut, with charcoal-grey straight trousers, mid-rise, full length; full-length sleeves on the top, cardigan worn open; silver jhumkas, small centred maroon bindi, hair long, open and dark, one small brown leather crossbody bag.`

Same fictional North Indian woman, age 22–26, wheatish skin with natural texture, long fully open dark hair, centred maroon bindi and silver jhumkas. The bag is brown leather in every slide. One modest, non-suggestive editorial lifestyle story; no extra people or identifiable third-party IP.

Every call includes the AAR-35 negative block in full: no text, letters, numbers, pseudo-text or glyph marks; no captions, signs, labels, logos, watermarks, screens, writing, branded props, or on-image AI disclosure; notebook blank; no tied hair; no bedroom/bathroom/changing room/poolside; no revealing, sheer, tight, low-cut, body-emphasising or unsafe styling.

## Shared set lock — correction-specific

Photorealistic editorial diary photograph. **Every slide is 4:5 portrait, framed waist-up at the same eye-level camera distance. Place both eyes at y=600–650 in the 1080×1350 delivery frame (middle third), subject centre-left, with camera-right negative space. Keep face size within ±10% across the five.**

**One large soft warm late-afternoon window key from camera-left only; gentle falloff and soft shadows to camera-right; no camera-right source, no direct sun patches, no hard-edged shadows, no blown highlights, no flash or overhead lighting.**

## Five call records

Each prompt is the AAR-35 shared positive prompt plus the locked outfit/hygiene locks above and exactly one clause below.

1. **S1** — seated at a work/study desk in a bright home corner, forearm on an open blank notebook with a closed unbranded pen beside it, mid-action of writing, glancing down; waist-up, eyes y=600–650.
2. **S2** — standing just behind a chair **inside a bright home corner** (visible domestic corner: chair, side table/window and warm wall), both hands smoothing the open cardigan front at hip level, even weight, eyes just past the lens; waist-up, eyes y=600–650.
3. **S3** — waist-up at a doorway-side interior wall in the same room, brown leather crossbody bag on shoulder, one hand adjusting its strap, calm closed-mouth expression; eyes y=600–650.
4. **S4** — **waist-up three-quarter framing** of one unhurried mid-step through an open domestic doorway onto the home balcony, brown leather bag across body, one hand relaxed; retain face scale and eyes y=600–650; no full-length view.
5. **S5** — waist-up seated at a small balcony table, unbranded cup of chai and the same brown leather bag set down beside it, faint natural smile toward the **camera-left warm late-afternoon window key**; eyes y=600–650; no cool/neutral daylight.

## Post-render delivery and QA

Only deliver five inspected PNGs measured to exactly 1080×1350. Record each Runway task ID, final SHA-256 and the delivered-byte measurement. Perform full-set QA before handoff: CAC-20 lighting, CAC-21 face-size tolerance, CAC-22 middle-third eye line, CAC-23 scene clauses, plus text/glyph/AI-mark, identity, hair, modesty, bag/wardrobe continuity and artifact inspection. AAR-38 performs the fresh independent pre-publish measurement.

## Human decision required

Approve **exactly 55 Runway credits** with `confirm_cost=true` for the five calls specified here. Acceptance is the prerequisite to submit any billable generation.