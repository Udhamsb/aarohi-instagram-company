# Aarohi daily carousel — approval criteria for the carousel-only daily format (v1.0)

**Issued:** 2026-09-22 · **Issue:** AAR-35 · **Author:** Creative Director
**Authority:** AAR-34 document `daily-format-standard` (binding, company-wide) · AAR-33 document `disclosure-policy` (binding) · AAR-25 `production-standard-v1` + `preflight-checklist-v1` · AAR-7 §4 / `AAROHI_WARDROBE_REFERENCE_v1.png` · AAR-13 `visual-approval-standard`
**Applies to:** every Aarohi daily post from 2026-09-23 onward — the still-image carousel set, its prompt record, and its publish gate.
**Status:** Locked approval standard for the daily format. This document is the acceptance gate the producer's deliverable is judged against; it reuses the AAR-25 rule IDs rather than inventing a parallel vocabulary.

## How this gate is run

Every row below is **pass/fail and measured on the delivered bytes**. One FAIL anywhere = the set is **NOT accepted**. One unchecked or uncertain row = **NOT accepted**. "The prompt asked for it" is not evidence (AAR-25 Z-5). A caption disclaimer is never a remedy for a frame defect.

Measurement tools/commands are named per row so the verdict is reproducible rather than asserted.

---

## Gate 0 — format gates (checked before any aesthetic judgement)

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-1** | The day's deliverable is a still-image carousel | Count of delivered slide files in the set, and the format of each file | Still-image set of exactly the briefed slide count, `4 ≤ n ≤ 6` (default 5) | Any reel, video, video master or single static delivered as the day's post — the daily slot fails outright |
| **CAC-2** | Slide count matches the brief | Count of delivered files vs the count named in the approved brief | `n` equals the briefed count, and `4 ≤ n ≤ 6` | `n` ≠ briefed, or `n < 4`, or `n > 6` |
| **CAC-3** | Every slide is 1080 × 1350 px | `PIL Image.open(f).size` on each delivered file (never the requested parameters) | 5/5 (or n/n) measure exactly `(1080, 1350)` | Any slide measures anything else |
| **CAC-4** | Every slide is exactly 4:5 portrait | `width / height` per slide | Ratio = 0.8000 on n/n slides | Any slide in any other ratio (including 9:16 or square) |

---

## Gate 1 — one outfit across the whole set

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-5** | Exactly one outfit for the whole carousel | Garment-class review at full size on every slide: the cardigan/outer layer, the base top and the trousers are present in **100%** of slides | The same garment set appears on n/n slides, no slide adds, removes, or swaps a layer | Any slide carries a garment, layer or outfit that another slide does not |
| **CAC-6** | The outfit is the one the rotation plan locked for that date | The briefed verbatim outfit string for that date vs the visible garments | The visible garments match the locked string for the date in n/n slides | The outfit belongs to another day's silhouette, or is outside the locked string |
| **CAC-7** | The outfit string is held verbatim in every prompt | Substring match of the exact locked string against each slide prompt in the render record | n/n prompts contain the string word-for-word | Any prompt missing the string, or carrying a reworded/abbreviated version |
| **CAC-8** | No colourway drift across slides | Sampled garment patch from each of the three fixed garment regions per slide; mean ΔE00 against slide 1 | Mean ΔE00 ≤ 12 for each region, and no perceptible hue shift | Any region > 12, or any hue shift a human would name as a different garment colour |
| **CAC-9** | Only approved silhouettes are worn | Each visible garment mapped to an AAR-7 §4 item (1–7) plus the item-8 accessory lock | Every visible garment maps to an approved item, and to the item the rotation plan assigned that date | Any garment outside the list = **modesty breach, REJECT — regenerate** (AAR-7 §4, AAR-25 C-7/WD-1) |

*CAC-8 note:* a layer change is a FAIL regardless of ΔE — the colour measure exists to catch drift, not to license variation.

---

## Gate 2 — zero text and no on-image disclosure mark

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-10** | Zero visible text in frame | Automated zero-text scan on each full slide **plus** 4x-zoom visual re-check of every slide; tool and verdict recorded (AAR-25 P1-2 / P2-4 / Z-5) | 0 legible strings and 0 glyph-like marks across n/n slides | Any 1 instance — typography, signage, labels, packaging, screens/UI, logos, watermarks, apparel or prop text, pseudo-text, gibberish letterforms, melted glyphs. One character = FAIL (Z-0) |
| **CAC-11** | Named scene exclusions actually absent | Per-slide check of the surfaces the brief excluded | No shop signs, price/menu boards, chalkboards, posters or banners; no readable labels or price tags; no book cover or spine text; no printed/embroidered text on clothing, bags or props; no document or notebook page with legible writing; no screen or app UI with content; no brand marks on props | Any excluded surface renders with text or glyph-like marks |
| **CAC-12** | No on-image AI-generated disclosure mark | Exact-string region scan for `AI-generated` / `AI generated` plus 4x-zoom visual check on n/n slides | Zero on-image badges, overlays, plates, stamps or disclosure glyphs | Any on-image AI-generated mark or disclosure text = **FAIL** (AAR-33 §1/§4). Presence is a defect, not a requirement |

---

## Gate 3 — locked identity and modesty

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-13** | Identity lock held on every slide | Full-size comparison of each slide face against the approved anchor crop (reference pack v2.1) | n/n slides read as the same fictional North Indian woman, 22–26, wheatish skin with natural texture; no second face, no blending, no age drift, no complexion shift | Any slide with face drift, blended identity, age or complexion shift (AAR-25 C-3/C-6, AAR-7 RC-1/RC-2) |
| **CAC-14** | Hair fully open and down | Full-size check per slide | Long dark hair visibly open and down in n/n slides | Tied, braided, clipped, bunned, ponytail, updo, or hair that does not visibly read as long and open |
| **CAC-15** | Identity markers present where their area is in frame | Full-size check per slide | Small centred maroon bindi visible wherever the forehead is in frame; silver jhumkas visible wherever the ears are in frame (natural hair/angle occlusion allowed) | Either marker absent when its area is visible |
| **CAC-16** | Modesty cover held | Full-size check per slide (AAR-25 WD-1/WD-2, Persona Bible §2) | Chest, midriff, hips and upper thighs covered in n/n slides; fabric opaque and secure | Any exposure; any sheer, skin-tight, plunging, strapless, lingerie-like, wet, transparent or bodycon styling |
| **CAC-17** | Pose, angle and setting are non-suggestive | Full-size check per slide (AAR-25 FR-1/ST-1/ST-2/SF-1) | Eye-level or neutral; plausible public or domestic setting; natural everyday posture | Any reclining, arched back, lip-biting, sultry gaze, body display, body-focused crop, or intimate setting (bedroom, bathroom, bed, shower, changing room, poolside) |
| **CAC-18** | No hair-only-panel garment inherited | Full-size check per slide | No camisole or thin strap garment anywhere in the set | Any slide shows the character sheet's camisole garment (AAR-25 C-4, AAR-7 §3, wardrobe sheet usage rule 4) |
| **CAC-19** | No unapproved or third-party content | Full-size check per slide | No real-person likeness, no real brand marks or third-party IP glyphs, no identifiable bystander in focus | Any of the above |

---

## Gate 4 — set-level coherence (the carousel reads as one moment)

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-20** | One lighting family | Dominant light direction per slide (from the shadow side) + colour-temperature estimate per slide, compared against slide 1 | One light direction in n/n slides (all shadows fall the same way) and colour temperature within **±200 K** of slide 1; no slide lit by a visibly different source (on-camera flash, direct lamp, overhead downlight, night interior) | Any slide lit from a different side, at a different temperature beyond ±200 K, or by a different class of source |
| **CAC-21** | Consistent framing distance | Face-to-frame height fraction per slide (top of head to chin, as a fraction of frame height), compared against slide 1 | Within **±10%** of the slide-1 fraction on n/n slides; same subject size, same camera distance | Any slide materially closer or further away, or a different shot scale (full-body/close-up mixed into a waist-up set) |
| **CAC-22** | Consistent camera height and placement | Eye-line position in frame + subject horizontal placement per slide | Subject's eye line inside the middle third of the frame and subject placed centre-left with negative space at camera-right in n/n slides | Any slide with a low/high angle, or subject placement that breaks the set's composition |
| **CAC-23** | One story, in order | Each delivered slide's scene vs its briefed scene clause | Slide *k* shows scene *k* for all k, and the sequence reads as one continuous day in one outfit | Any slide whose scene does not match its clause, or an order that breaks the story |
| **CAC-24** | Visual/copy agreement | Slide contents vs the caption set (AAR-37) | Every caption line is traceable to something actually visible in the slides; the visual never contradicts the caption | Any caption line about a garment, setting or activity that is not in the slides (AAR-25 CN-4) |
| **CAC-25** | Anatomy, realism and artifacts | Full-size review of n/n slides (AAR-25 P2-4/P2-5/P2-6) | 0 visible defects: plausible hands/fingers/limbs/teeth/eyes/reflections; natural skin texture; no plasticky or waxy skin; no oversharpening halos, compression mush, ghosted edges or watermark-like smudges | Any visible defect |
| **CAC-26** | Provenance recorded per slide | Render record fields | Every slide names its anchor id, the anchor crop's SHA-256 and its own asset SHA-256, with one file per live filename | Any missing field, or a superseded file sharing a live name (AAR-25 P1-9/P3-3, AAR-7 RC-9) |
| **CAC-27** | Correction budget respected | Cycle count in the correction history | ≤ 2 correction cycles for the set, each one consolidated brief, full preflight re-run after correction | A 3rd failing pass — escalate to the Creative Director before any further spend (AAR-25 §6, AAR-27 gate) |

---

## Gate 5 — publish-time gates (outside the frame, still mandatory)

| ID | Criterion | Measurement | PASS | FAIL |
|---|---|---|---|---|
| **CAC-28** | Caption carries the disclosure line | Caption text as published | Caption contains the plain-language note that the visual is AI-generated and that caption/storytelling is human-directed (AAR-15 §5) | Caption disclosure missing |
| **CAC-29** | Platform AI-content label enabled | Publish payload + account state read back from the provider | Instagram `isAiGenerated: true` set on the post **and** the profile-level "AI-generated profile" label enabled | Either missing — this, not an on-image badge, is the disclosure breach standard now |
| **CAC-30** | Only approved slides shipped | Published media list vs the approved manifest | Published set = the approved slides, in the approved order, none added or dropped | Any undisclosed extra or substituted slide ("no undisclosed cutaway" carried over from AAR-25 B10) |
| **CAC-31** | Billable-render gate honoured | Render record + cost record | Recorded render contract, live estimate and explicit human `confirm_cost` precede every billable call | Any billable call made without the recorded approval |

---

## Escalation

- Frame defect → the producer's consolidated correction brief (AAR-25 §6), one cycle, full preflight re-run.
- Unapproved garment → **modesty breach, regenerate** — never a caption fix.
- On-image disclosure mark → re-edit to a clean frame before handoff or publish.
- A third failing pass, or a spend decision, escalates to the Creative Director; only the Creative Director revises this standard, and a revision ships as a new version with a change summary.
