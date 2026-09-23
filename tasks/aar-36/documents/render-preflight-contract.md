# AAR-36 — Runway pre-render contract (revision 2)

## Verdict: READY FOR HUMAN COST CONFIRMATION — no billable render submitted

The human direction to use Runway supersedes the prior Higgsfield route. The earlier Higgsfield approval and funding requirement do not transfer to Runway; this revision replaces that held vendor contract only.

## Zero-credit preflight carried forward

- Format: exactly five still-image slides, each final-delivered at 1080×1350 (4:5); no reel, video, 9:16 or audio asset.
- Identity: same fictional North Indian woman, 22–26, wheatish skin, long dark hair fully open/down, small centred maroon bindi and silver jhumkas.
- Text hygiene: no text, glyphs, logos, signs, watermarks, labels, pseudo-text, screens, notebook writing, packaging text, or AI disclosure in-frame.
- Modesty: neutral eye-level editorial framing; no suggestive pose, crop or setting; opaque locked garments only.
- Continuity anchor: AAR-32 attachment `a638febd-a212-4280-aa09-11f19e690e5c`, source `01_studio_front.png`; internal continuity crop SHA-256 `88a61d51038968038c52c24c423a0ee2c2d59f1b47fc089571774afafc1039c1`.
- Approved daily brief: AAR-35 `daily-brief-2026-09-23` rev 1. The identical required outfit string is held word-for-word in every slide prompt:
  `knee-length open oatmeal-beige knit cardigan over a dusty-rose opaque woven relaxed top, hip length, relaxed cut, with charcoal-grey straight trousers, mid-rise, full length; full-length sleeves on the top, cardigan worn open; plus the item-8 lock: silver jhumkas, small centred maroon bindi, hair long, open and dark, one small crossbody bag or tote.`

## Executable Runway contract — held pending confirmation

| Field | Value |
|---|---|
| Vendor / endpoint | Runway MCP `generate_image` |
| Exact model | `nano-banana-2` |
| Parameters per call | `ratio: 4:5`; `imageSize: 2K`; `count: 1`; one supplied continuity-anchor reference; one slide-specific prompt |
| Planned calls | 5 separate image calls, S1–S5 in the AAR-35 brief order |
| Live price evidence | Runway’s current official credit table: Nano Banana Pro 2 at 2K = **11 credits/image** |
| Exact total | **55 Runway credits** (5 × 11); no additional reference-image surcharge listed for this model/settings |
| Live funding check | Runway workspace authenticated 2026-09-22 with **1,797 credits**; 55 credits available |
| Final delivery transform | measure every returned asset; produce only final 1080×1350 files (downscale/crop without changing contents only if necessary) |
| Post-render gates | CAC-1–27, including zero-text/glyph scan, full-size visual inspection, wardrobe-region comparison, asset SHA-256 manifest, and set-level light/framing checks |

## Prompt record

Every prompt starts with the locked outfit string above and this shared visual lock: “realistic editorial diary photograph; same fictional woman; natural skin texture; warm late-afternoon daylight from camera-left; soft shadows to camera-right; eye-level waist-up medium frame; subject centre-left with negative space right; blank/unbranded surfaces; no visible text or glyph-like marks; no logos, signage, labels, watermarks or AI badge; no tied hair, extra people, intimate setting, suggestive pose or unsafe form.”

- **S1:** seated at a bright home work/study desk, forearm resting on an open blank notebook with a closed unbranded pen beside it, looking down mid-writing.
- **S2:** standing behind the chair, both hands smoothing the open cardigan front at hip level, even weight, eyes just past lens.
- **S3:** waist-up by the doorway-side wall in the same room, crossbody bag on shoulder, free hand adjusting its strap, calm closed-mouth expression.
- **S4:** one unhurried step through the open domestic doorway onto the home balcony, bag across body, one hand relaxed.
- **S5:** seated at a small balcony table, unbranded cup of chai and same bag placed beside it, faint natural smile, warm late-afternoon light.

## Required human action

Approve this exact Runway charge with `confirm_cost=true`: **55 Runway credits for five `nano-banana-2` 4:5/2K image calls (one output per call).** On acceptance I will submit only these five calls, then perform the required delivered-byte QA. No billable call has been submitted.