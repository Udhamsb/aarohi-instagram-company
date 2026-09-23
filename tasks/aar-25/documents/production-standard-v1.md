**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 12: `**Owner:** Creative Director (AAR-25). **Applies to:** every Aarohi photo and video content asset — stills, ca`
- line 25: `- **Model selection, pricing, and spend** are governed by AAR-27 (currently Runway Dev Models for the video pa`
- line 29: `**Z-0: A delivered image or video frame contains zero visible text. No means no.**`
- line 55: `- **C-5 Video identity.** Identity and markers verified per sampled frame (see §4 sampling). One non-compliant`
- line 66: `- **FR-3 Platform survival:** subject and (after overlay) badge survive the 4:5 profile-grid crop and stay cle`
- line 73: `- **SF-3 Disclosure on outward masters:** exact `AI-generated` overlay present, high contrast, inside the plat`
- line 78: `- **CN-2 Within a video:** identity, wardrobe, and props stable across all sampled frames; no duplicated, vani`
- line 91: `- P0-4 Output spec explicit: exact width×height — never a bare ratio string (platforms ignored `ratio "9:16"` `
- line 92: `- P0-5 Platform spec achievable: stills ≥1080 px short edge (4:5 default 928×1152 or larger); reel publish mas`
- line 98: `- P1-1 Container/dimensions: ffprobe dimensions equal the ordered spec (not the requested one), fps and durati`
- …and 7 further line(s) in this document reference the same superseded formats.

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# Aarohi Visual Production Acceptance Standard v1.0 — Zero Text + Character Consistency

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 14: `- **Disclosure timing (supersedes Persona Bible §3 positive prompt).** Generation prompts must NOT request the on-image `
- line 36: `- **Z-3 The only permitted on-asset text** is (a) the post-production disclosure overlay, exact string `AI-generated` (h`
- line 64: `- **SF-3 Disclosure on outward masters:** exact `AI-generated` overlay present, high contrast, inside the platform safe `

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Owner:** Creative Director (AAR-25). **Applies to:** every Aarohi photo and video content asset — stills, carousel frames, reel frames, covers, exports — from prompt construction through handoff.
**Status:** Locked acceptance standard and handoff gate. The AI Visual Producer runs it as the final pre-handoff self-check; the receiving publish/QA gate refuses any asset without a passing preflight record. Non-negotiable rows must not be reinterpreted.
**Cost boundary:** this standard itself involves no billable generation. Preflight Pass 0 plus the AAR-27 cost gate (live estimate + explicit confirm_cost) must pass before any paid render.
**Scope exemption:** the internal anchor/reference sheets (reference pack v2.1) are tools, not content assets; their burned-in bands are governed by the reference-pack standard (AAR-7), not by §1 here.

## 0. Precedence and consolidation

This standard consolidates the visual rules scattered across AAR-2 (Persona Bible), AAR-7 (reference pack v2.1), AAR-12 (clean-image + caption template), AAR-13 (approval standard), AAR-14 (generation/QC standard), and AAR-15 (caption-first copy). Where an earlier document conflicts with this one, this one governs.

Explicit reconciliations:

- **Disclosure timing (supersedes Persona Bible §3 positive prompt).** Generation prompts must NOT request the on-image disclosure. The render itself is text-free; the exact `AI-generated` overlay is applied in post-production on the raw master (the practice proven on AAR-20). The Persona Bible §4 disclosure requirements remain fully in force — at the overlay/deliverable stage, not the generation stage.
- **Pseudo-text (supersedes the "illegible blur passes" convention).** Glyph-like marks and pseudo-text are defects under §1 and fail the delivered asset, matching the AAR-14 rejection-loop precedent (chalkboard menu) and this issue's explicit "accidental glyphs" prohibition.
- **Model selection, pricing, and spend** are governed by AAR-27 (currently Runway Dev Models for the video path per AAR-21/AAR-22; the OpenRouter image path per AAR-14). This standard is model-agnostic: it measures delivered files, never requested parameters.

## 1. The zero-text rule (absolute, non-negotiable)

**Z-0: A delivered image or video frame contains zero visible text. No means no.**

"Text" means every one of the following, whether intentional, incidental, or accidental:

1. Typography: captions, titles, headings, fake quotes, labels, hashtags, CTAs, subtitles, decorative typography, graffiti.
2. Signage: shop signs, menus, boards, posters, billboards, street furniture.
3. Product and packaging: labels, tags, brand names, instructions, price tags.
4. Screens and UI: phone/app UI, app frames, notifications, speech bubbles, fake chat, TV/laptop screens with content.
5. Logos and brand marks, watermarks, stamps, seals.
6. Apparel and props: text printed on clothing, tote bags, caps, mugs, book spines, newspapers, documents, vehicle markings.
7. Accidental glyphs: pseudo-text, gibberish letterforms, hallucinated alphabets, melted or warped glyphs — even one character, even unreadable. Marks a viewer would read as "writing" fail exactly like legible words.

Operative rules:

- **Z-1 Prompt silence on text.** No generation prompt may request or imply text anywhere in frame: no captions, typography, signage, watermarks, labels, logos, subtitles, or UI. Scene descriptions use "a" not "the" for signage-bearing surfaces, or exclude the surface outright.
- **Z-2 Verbatim negative block in every prompt.** `text, letters, numbers, captions, subtitles, signage, labels, typography; logos, brand marks, watermarks, stamps; UI elements, app frames, phone-screen UI, fake quotes, speech bubbles; irrelevant decorative elements` — plus explicit surface exclusions whenever the scene implies boards, screens, shelves, or packaging (the AAR-14 lesson: an unexcluded chalkboard menu rendered into both variants and failed QC).
- **Z-3 The only permitted on-asset text** is (a) the post-production disclosure overlay, exact string `AI-generated` (hyphenated), applied after Pass 1–2 QC passes on the raw master; and (b) the AAR-13 §2 exception path — board-approved campaign text with the exact copy pre-approved, minimal and legible, always paired with a clean no-text variant. Everything else is an automatic reject.
- **Z-4 Remedy order for text defects:** 1) crop out if composition survives platform specs; 2) blur/clone in post if cropping fails; 3) regenerate only through the consolidated correction brief (§6). Never regenerate a single defect piecemeal while other defects wait.
- **Z-5 Evidence, not intent.** Compliance is verified by measurement on the delivered bytes (automated scan + 4x-zoom visual check per sampled frame, tool and verdict recorded). "The prompt asked for no text" is not evidence.

## 2. Character-consistency requirements (non-negotiable)

- **C-1 Anchor lock.** Every generation of the persona conditions on the approved anchor set (reference pack v2.1 face/body sheet + character sheet, INTERNAL-ONLY — never published). Anchor crop for identity conditioning: face + hair, above shoulders.
- **C-2 Provenance.** Every asset record names the anchor file IDs and the SHA-256 of the anchor crop used (RC-9). A missing provenance entry fails handoff.
- **C-3 Identity lock.** One consistent fictional North Indian woman, age 22–26; wheatish skin with natural texture; long open dark hair — never tied, braided, clipped up, bunned, ponytailed, or in an updo; small centred maroon bindi visible whenever the forehead is in frame; silver jhumkas visible whenever the ears are in frame (natural hair/angle occlusion allowed); natural makeup only.
- **C-4 Hair-only rule.** The character sheet's "Hair Variations — Open Hair" panel is a HAIR-ONLY reference; its camisole garment is unapproved and must never be inherited into any frame.
- **C-5 Video identity.** Identity and markers verified per sampled frame (see §4 sampling). One non-compliant frame fails the asset — the per-frame gate that fixed the AAR-20 wardrobe drift.
- **C-6 No blending.** No second face, no blended identity, no age drift, no complexion shift between assets or frames.
- **C-7 Wardrobe lock.** Only the eight approved silhouettes in `AAROHI_WARDROBE_REFERENCE_v1.png` (§4 list of AAR-7). Any unapproved garment is a reject regardless of frame quality.
- **C-8 Drift handling.** Face drift, hair breach, marker breach, or wardrobe drift = immediate reject. The remedy is a new approved asset, never a caption disclaimer.

## 3. Framing, wardrobe, setting, safety, continuity checks

Each check is pass/fail at full size on every sampled frame.

- **FR-1 Camera:** eye-level or neutral; no voyeuristic angles; no body-focused crop (chest/waist/hips/legs/lips emphasis).
- **FR-2 Composition:** subject placement and framing serve the story; no cut-off limbs, awkward crops, or cluttered edges; negative space usable.
- **FR-3 Platform survival:** subject and (after overlay) badge survive the 4:5 profile-grid crop and stay clear of 9:16 UI reservations.
- **WD-1 Approved list only** (C-7); opaque, secure, non-body-emphasising; chest, midriff, hips, upper thighs covered.
- **WD-2 Exclusions:** no sheer, skin-tight, plunging, strapless, lingerie-like, wet, transparent, or bodycon styling.
- **ST-1 Settings:** plausible public or domestic, non-intimate — bright home corner, balcony, bookshop, café table, market lane, park path, campus-style exterior, work/study desk, home preparation.
- **ST-2 Prohibited settings:** bedroom, bathroom, bed, shower, changing room, poolside, or similarly intimate setting.
- **SF-1 Modesty of pose:** no reclining, arched back, lip-biting, sultry gaze, provocative dancing, or body display.
- **SF-2 Copy safety:** caption, hashtags, and any on-asset overlay carry no sexualised, flirtatious, appearance-led, or engagement-bait language.
- **SF-3 Disclosure on outward masters:** exact `AI-generated` overlay present, high contrast, inside the platform safe area (AAR-11 numbers for 1080×1920 reels: above the y≥1248 caption/audio reservation, clear of the x≥853 action rail below y=1150, inside the 4:5 grid-kept region; stills default lower-right with ≥24 px margins), present on every carousel slide and reel shot — no undisclosed cutaway.
- **SF-4 Internal/outward separation:** anchor sheets and raw renders never go outward-facing; the overlaid master is the only outward deliverable.
- **SF-5 Likeness and IP:** no real-person likeness, no real brand marks or third-party IP glyphs.
- **SF-6 Privacy:** no identifiable bystanders in focus.
- **CN-1 Within a carousel/set:** same person, coherent wardrobe logic, consistent lighting family, setting that reads as one story.
- **CN-2 Within a video:** identity, wardrobe, and props stable across all sampled frames; no duplicated, vanishing, or morphing objects; motion continuous (single continuous shot unless the brief approves cuts); action beats match the brief.
- **CN-3 Across a package:** consistent identity read and grounded diary voice across assets.
- **CN-4 Visual/copy agreement:** the visual supports, never contradicts, the caption.

## 4. Multi-pass preflight (the handoff gate)

Run in order. Any FAIL anywhere = the asset is not accepted; no near-miss passes. One unchecked or uncertain box = not accepted.

**Pass 0 — brief completeness (before any generation call; blocks billable spend)**

- P0-1 Approved brief/concept exists and maps to an AAR-26 prompt-package entry (or documented equivalent).
- P0-2 Prompt carries the Z-2 verbatim negative block and contains zero text-requesting phrases (Z-1).
- P0-3 Anchor named with SHA-256 (C-1/C-2).
- P0-4 Output spec explicit: exact width×height — never a bare ratio string (platforms ignored `ratio "9:16"` on both Sogni models; explicit width/height was honored every time) — plus fps and duration for video.
- P0-5 Platform spec achievable: stills ≥1080 px short edge (4:5 default 928×1152 or larger); reel publish master 1080×1920 planned; audio stream planned for reels.
- P0-6 AAR-27 gate satisfied: approved model path, live cost estimate recorded, explicit confirm_cost — before any billable render.
- P0-7 Correction budget acknowledged: ≤2 correction cycles per asset before escalation (§6).

**Pass 1 — automated QC (runs before any human or vision review)**

- P1-1 Container/dimensions: ffprobe dimensions equal the ordered spec (not the requested one), fps and duration in spec; reels contain a real audio stream (silent MP4 = fail; Instagram treats it as a photo/clip).
- P1-2 Zero-text scan: automated scan on the full still / every sampled video frame; any legible string or glyph-like mark = fail; tool and verdict recorded (Z-5).
- P1-3 Badge gates on overlaid masters: exact-string region match, contrast ≥4.5 on the delivered convention (WCAG 2.1 figure reported alongside), margins ≥24 px, inside the safe area, 30 px guard band clear of other text ink, and a phone round-trip (420 px canvas, JPEG q26) that keeps the badge readable.
- P1-4 Integrity: asset SHA-256 recorded; one file per live name (superseded files renamed or deleted — the AAR-11 collision lesson).

**Pass 2 — visual/vision review (full size, every sampled frame)**

- P2-1 Identity and markers per frame (C-3, C-5).
- P2-2 Wardrobe per frame (C-7, WD-1/WD-2).
- P2-3 Zero-text re-check at 4x zoom on every sampled frame, including accidental glyphs (Z-0).
- P2-4 Anatomy: hands, fingers, limbs, teeth, eyes, reflections plausible; no duplicated or fused features.
- P2-5 Realism: natural skin texture; no plastic/waxy skin, oversharpening halos, compression mush, ghosted edges, or watermark-like smudges.
- P2-6 Lighting: consistent direction, colour temperature, and shadow logic.
- P2-7 Framing, setting, safety rules (§3 FR/ST/SF).
- P2-8 Relevance: matches the approved brief and supports the caption.
- P2-9 Motion continuity for video (CN-2).

**Pass 3 — platform preview and documentation**

- P3-1 Platform preview: 4:5 grid crop keeps subject + badge; 9:16 UI reservations clear; readable on a phone-sized canvas.
- P3-2 Asset record complete: model id/version, exact parameters, anchor IDs + SHA-256, asset SHA-256, prompt + negative block, per-rule QC verdicts, cost record if billed.
- P3-3 Labelling: raw master marked internal; overlaid master marked outward-facing; nothing internal ever published.
- P3-4 Verdict: ACCEPT only when every rule across Passes 0–3 is PASS.

**Video frame sampling:** ≥10 frames evenly spread across the full duration, always including the first and last frame, plus any frame where automated QC flags doubt. Stills: full image plus 4x zoom of every suspect region.

## 5. Objective pass/fail thresholds

| # | Measure | Pass condition | Fail |
|---|---|---|---|
| T-1 | Legible text or glyph-like marks (per frame) | 0 instances | any 1 instance |
| T-2 | Badge contrast | ≥4.5 delivered convention ((Lmax+5)/(Lmin+5)) | <4.5 |
| T-3 | Badge margins | ≥24 px from right/bottom edges; inside platform safe area | any violation |
| T-4 | Badge phone round-trip | readable at 420 px canvas after JPEG q26 | unreadable |
| T-5 | Video identity sampling | 100% of ≥10 sampled frames compliant | any 1 frame out |
| T-6 | Wardrobe | approved-list silhouettes in 100% of sampled frames | any deviation |
| T-7 | Resolution (measured, not requested) | stills ≥1080 px short edge; reel publish master 1080×1920 | under spec |
| T-8 | Reel audio | ≥1 audio stream with real content | silent or absent |
| T-9 | Anatomy/artifacts | 0 visible defects at full size | any defect |
| T-10 | Provenance | anchor + asset SHA-256 in record | missing |
| T-11 | Correction cycles | ≤2 per asset | 3rd failure escalates |

## 6. The single consolidated correction brief (mandatory format)

No piecemeal regeneration. When any preflight pass fails:

1. **Freeze.** No regeneration is submitted until the correction brief below is complete.
2. **Consolidate.** ALL defects from ALL passes go into ONE correction brief:
   - Header: asset name, brief version, anchor IDs + SHA-256, failed workflow id (if any), date.
   - Defect table — one row per defect: `rule ID | finding (what, where, which frame) | class: POST-EDIT or REGEN | exact remedy`.
   - POST-EDIT rows (crop, blur/clone, overlay fix) are batched into a single re-edit session.
   - REGEN rows get the exact prompt revision: the failing constraint front-loaded in BOTH the positive and negative blocks (the AAR-20 rev-2 lesson: wardrobe as "top priority constraint" in both blocks fixed in one render what verbatim rev-1 blocks failed twice).
3. **One cycle.** All REGEN defects ship in one revised prompt and one render call (or one batch); all POST-EDIT defects ship in one re-edit pass.
4. **Full re-preflight** from Pass 1 on the corrected asset — never re-run only the failed rule.
5. **Loop limit.** Maximum 2 correction cycles per asset. A third failing pass escalates to the Creative Director with the full defect history; no further spend without a CD decision (aligned with the AAR-27 cost gate).
6. **Log.** Record rule | finding | remedy | verdict per cycle; rename/delete superseded files so each live filename resolves to exactly one file.

## 7. Handoff record (what the AI Visual Producer delivers)

A handoff is accepted only with all of the following, in one record, no side-channels:

1. The completed preflight record: every rule ID P0–P3 with verdict and measurement.
2. The files: raw internal master + overlaid outward master, unique names, SHA-256 each.
3. The asset record block (P3-2 fields).
4. The correction history: any correction briefs with per-cycle verdicts.

The receiving gate (publish/QA, AAR-27 readiness) rejects any handoff missing an item, naming the rule ID and defect in the rejection feedback.

## 8. Boundaries

- This standard authorizes no billable generation and no publication. Spend requires the AAR-27 gate; publication requires separate authorization (AAR-10).
- If no approved generation path is reachable, the blocker is reported — frames are never fabricated.
- Only the Creative Director (or a specifically authorized approver) may replace anchors or revise this standard; revisions ship as a new version with a change summary.