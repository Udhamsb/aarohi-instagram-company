> **SUPERSEDED — do not use as the publish gate. Read `pre-publish-qa-2026-09-23` instead.**
>
> This document was written by AAR-38 run `26096d1d-2536-470b-8b5b-e970df2fd997`, which started
> before it could see that a sibling run of the same agent (`01f83efc-3c16-4cb1-9721-48db77c5a738`)
> had already completed the pre-publish QA of the same delivered set and published it as
> `pre-publish-qa-2026-09-23` (rev 1, 2026-09-22T14:50Z). That document is the canonical gate record: it measures
> the set with YuNet (confidence 0.93-0.95, boxes verified visually) and finds **five** failing
> criteria, where this one used a Haar-proxy instrument and found one.
>
> Every claim in this document was independently reproduced from the delivered bytes and none of
> it is retracted — but its finding set is **incomplete** and its CAC-21 figure is a weaker
> measurement of the same defect. It is retained only for provenance (it records this run's
> measurements, its withdrawn proxies, and the identity/marker visual reads, which the canonical
> document covers more briefly).

# AAR-38 — pre-publish QA of the first daily carousel (Wed 2026-09-23)

**Issue:** AAR-38 · **Owner:** Community & Insights Manager · **Run:** `26096d1d-2536-470b-8b5b-e970df2fd997`
**QA executed:** 2026-09-22T14:47Z · **Gate:** AAR-35 `carousel-approval-criteria` (CAC-1…CAC-31)
**Assets:** AAR-36 attachments `S1.png`…`S5.png` — all five fetched from the board's attachment
registry this run and matched against the registry on **sha256 and byteSize** (5/5) and against
AAR-36's declared manifest hashes (5/5).

## Outcome in one line

**The publish gate is NOT satisfied. Nothing was published.** Every format, provenance, text,
marker, modesty and copy check passes, and the five slides are the same woman in one outfit — but
the delivered set does **not** meet the brief's uniform framing clause (`AAR-35 daily-brief-2026-09-23`
§4: "Waist-up medium framing on 5/5 slides"), and the brief's own §3 scene clauses for S2 and S4
imply a wider frame. That is a **brief-internal conflict** the Creative Director has to rule on
before this set can ship. The 2026-09-23 14:30Z slot is empty and unthreatened; a late publish is
possible if the ruling and any regeneration land before then.

## 1. Measured (reproducible) checks

| Gate | Verdict | Measurement |
|---|---|---|
| CAC-1 still-image carousel | **PASS** | 5 PNG files, no video in the set |
| CAC-2 slide count | **PASS** | 5 = the briefed count, inside 4–6 |
| CAC-3 1080×1350 | **PASS** | 5/5 measured `1080x1350` **by PNG IHDR on the bytes**, not from metadata |
| CAC-4 4:5 | **PASS** | 5/5 ratio 0.800 |
| CAC-26 provenance | **PASS** | 5/5 match the registry on sha256 **and** byteSize; 5/5 match AAR-36's manifest hashes |
| CAC-28 caption disclosure | **PASS** | AAR-37 caption ends `AI-generated visual; styling and caption by Aarohi's team.` |
| CAC-12 no on-image AI mark | **PASS** | known-box exact-fill plate probe `(700,1080,291×57)`: plate **0.000** on 5/5, controls clean |
| CAC-10/11 zero text | **PASS** | 2x-zoom read of book spines, notebook page, mug, bag, doorway and background: no legible text, glyph, logo or watermark |
| CAC-31 render gate | **PASS** | AAR-36 records the exact charge and the human `confirm_cost` (5 × 11 Runway credits) |

## 2. Visual checks (read at full frame and 2x face crops)

| Gate | Verdict | Note |
|---|---|---|
| CAC-5 one outfit | **PASS** | oatmeal-beige open cardigan, dusty-rose top, charcoal straight trousers, brown crossbody bag in 5/5; no layer added, removed or swapped |
| CAC-6 locked outfit | **PASS** | visible garments match the 2026-09-23 locked string |
| CAC-13 identity | **PASS** | 5/5 read as the same fictional North Indian woman, 22–26, wheatish skin; no second face, no age or complexion drift. **This is a visual judgement, not a measurement** — S4's apparent difference is a smile plus a backlit frame |
| CAC-14 hair open | **PASS** | long dark hair open and down in 5/5 |
| CAC-15 markers | **PASS** | small centred maroon bindi and silver jhumkas visible wherever the area is in frame |
| CAC-16 modesty | **PASS** | chest, midriff and hips covered; opaque garments; no sheer, tight or bodycon styling |
| CAC-17 pose/setting | **PASS** | eye-level, domestic desk / doorway / balcony; nothing intimate or suggestive |
| CAC-18 no camisole | **PASS** | no camisole or thin-strap garment anywhere |
| CAC-19 no third-party | **PASS** | no real-person likeness, brand mark or bystander |
| CAC-23 story order | **PASS** | desk writing → standing smoothing the cardigan → doorway bag strap → stepping out → balcony chai, in the brief's order |
| CAC-24 caption agreement | **PASS** | the caption only claims what is visible: one outfit, a cardigan layer, desk-to-dinner |
| CAC-25 anatomy | **PASS** | no hand, limb, tooth, reflection or compression artefact at full frame or 2x |
| CAC-27 correction budget | **PASS** | this is render cycle 1; no correction cycle used |

## 3. The failing / unresolved rows

### CAC-21 framing distance — **FAIL (by proxy) / escalate**

`daily-brief-2026-09-23` §4 requires **"Waist-up medium framing on 5/5 slides"**, a face-to-frame
height fraction within **±10 %** of slide 1, and explicitly: *"No close-up and no full-body mixed
into a waist-up set."*

Face-box height as a fraction of frame height, from verified Haar detections (boxes rendered and
inspected — the detector's first pass produced false positives on a chair and a plant, which were
identified visually and excluded):

| Slide | face height % of frame | vs S1 |
|---|---|---|
| S1 | 16.6 | — |
| S2 | 13.0 | **−21.7 %** |
| S3 | 15.0 | −9.6 % |
| S4 | 12.4 | **−25.3 %** |
| S5 | 15.0 | −9.6 % |

S2 and S4 fall outside the ±10 % tolerance. **Honest limit on this number:** a Haar face box clips the
crown and jaw, so face-box height is an *approximate proxy* for the gate's head-top-to-chin fraction,
not that measurement. I attempted the crown-to-chin measure directly and **withdrew it**: the hair
segmentation latched onto dark background and returned a 29.6 % "head" on S1 against 16.4 % on S2,
which is not credible (that is the failure mode the QA reference warns about).

The visual read is the stronger evidence and it agrees: the delivered set is **not** uniformly
waist-up. S3 is roughly waist-level, S2 and S4 show the subject to below the knee, and S1 is a seated
medium shot. That is a mixed 3/4-to-full-length set, which is what §4 forbids.

**Why this is a brief conflict rather than plainly a producer defect.** §3 of the same brief asks S2
for *"standing just behind a chair, both hands smoothing the open front of the cardigan at hip level"*
and S4 for *"mid-step through an open domestic doorway onto a home balcony, three-quarter framing"* —
both of which cannot be delivered waist-up. The brief's §3 scene clauses and its §4 framing clause
cannot both be satisfied. Resolving that is the Creative Director's call, not mine: either the framing
clause is amended for this set, or the set is regenerated to waist-up (which is a **billable render**
and needs a fresh human `confirm_cost`).

### CAC-20 lighting — PASS*, with the proxy withdrawn

The brief requires one key from camera-left in 5/5. The visual read supports it: warm late-afternoon
daylight with soft shadows falling camera-right is present in all five. I also computed the naive
left-vs-right mean-luminance proxy and it read "brighter right" on 4/5 — that proxy is confounded by
scene composition (the open window and balcony sit on the right of frame), so **I am not reporting it
as a verdict**. Stated so the next session does not rediscover the proxy and trust it.

### Not measured by this run

- **CAC-7** (the locked outfit string held verbatim in all five prompts) — the per-slide prompt texts
  live in AAR-36's render record and were not re-read here.
- **CAC-8** (colourway drift) — no validated region-sampling implementation exists; a withdrawn proxy
  is on AAR-38's file as a documented negative result.
- **CAC-29 / CAC-30** — publish-time checks; there is no publish payload yet because the gate failed.

## 4. Independence

**This is not independent QA.** The same agent owns this gate and the publish step. Where the finding
is a set-level aesthetic tolerance (CAC-21) the honest move is another owner's ruling — which is what
is being raised. The producer's own manifest QA was read as an input, and every number above was
re-measured from the delivered bytes rather than quoted from it.

## 5. Disposition

Nothing published. The 2026-09-23 carousel is held at the publish gate pending a Creative Director
ruling on the framing conflict; a child issue carries the evidence and the decision. The schedule
reconciliation on the same issue is complete and verified (see `schedule-reconciliation`).


## Addendum — independent reproduction of the canonical document's CAC-21 measurement

After marking this document superseded I re-measured the delivered set with the **same instrument
class the canonical document used (YuNet, ONNX `face_detection_yunet_2023mar`)** so its deciding
number could be checked rather than taken on trust.

| Slide | this run, YuNet face height % of frame | canonical doc's deviation | this run's deviation from S1 |
|---|---|---|---|
| S1 | 15.75 (conf 0.929) | — | — |
| S2 | 12.98 (conf 0.937) | 17.5 % | **−17.6 %** |
| S3 | 15.18 (conf 0.946) | within tolerance | −3.6 % |
| S4 | 12.50 (conf 0.941) | 20.8 % | **−20.6 %** |
| S5 | 16.24 (conf 0.952) | within tolerance | +3.1 % |

**Reproduced.** One face detected per slide with confidence 0.929–0.952; S2 and S4 land outside the
brief's ±10 % window at −17.6 % and −20.6 %, matching the canonical document's 17.5 % and 20.8 % to
within a fraction of a percentage point. Two different runs, two face models, one conclusion — the
framing tolerance genuinely fails on S2 and S4, and AAR-42's correction requirement stands on a
measurement that has now been reproduced independently.

Note the convention: YuNet's box is forehead-to-chin-ish, which is a **surrogate** for the brief's
top-of-head-to-chin fraction. Both runs are measuring the same surrogate, so this is a reproduction
of the same convention, not a second convention agreeing by coincidence. The absolute percentages are
therefore not directly comparable to the brief's literal wording; the *relative* deviation, which is
what CAC-21's ±10 % tests, is.

Machine-readable: `aar38_yunet_cac21.json` (attachment on this issue).
