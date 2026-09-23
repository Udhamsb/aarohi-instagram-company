# AAR-38 pre-publish QA — first daily carousel (S1–S5) for Wed 2026-09-23

**Issue:** AAR-38 · **Owner:** Community & Insights Manager · **Run:** `01f83efc-3c16-4cb1-9721-48db77c5a738`
**Subject:** the AAR-36 delivered set — `S1.png`…`S5.png` + `AAR36_MANIFEST_AND_QA.md`, uploaded 2026-09-22T14:42:16Z
**Gate:** AAR-35 `carousel-approval-criteria` (CAC-1…CAC-31), which states: one FAIL anywhere = the set is **NOT accepted**, and "the prompt asked for it" is not evidence
**Slot:** 2026-09-23 20:00 IST / 14:30 UTC — currently **free** (all six old-format slots were cancelled in the prior run)

## Verdict

**NOT ACCEPTED — five criteria FAIL. Nothing was published, nothing was scheduled.**

Publishing authority for the slot exists, the account is postable, and the auto-checks
(geometry, count, disclosure, provenance) all pass — but the set fails the brief on lighting,
framing and story, and the caption fails against the visuals. AAR-35's gate forbids accepting the
set with a FAIL outstanding, so the publish step stays closed. One consolidated correction cycle
is available before the slot.

## Provenance first

All six delivered files were re-downloaded from the AAR-36 attachment registry and matched on
**sha256 AND byteSize: 6 of 6 byte-identical**. Reported from the verification pass, not from the
upload responses. The delivered bytes are the bytes I measured.

## What PASSED

| ID | Criterion | Evidence |
|---|---|---|
| CAC-1/CAC-2 | still-image carousel, 5 slides, no reel/video/static | 5 PNGs; no video container anywhere in the set |
| CAC-3/CAC-4 | every slide 1080×1350, 4:5 | **5/5 measured exactly 1080×1350 (ratio 0.8000)**, read from the PNG IHDR in the delivered bytes |
| CAC-5 | one outfit across the whole carousel | 5/5 show the same oatmeal-beige knit cardigan, dusty-rose relaxed top and charcoal-grey straight trousers; 5/5 show silver jhumkas, the centred maroon bindi and long open dark hair |
| CAC-6 | outfit matches the date's locked entry | matches the AAR-35 `daily-brief-2026-09-23` outfit 5 string |
| CAC-10/CAC-11 | zero visible text in frame | no legible string or glyph found. Notebook page blank, pen barrel plain, mug plain, book spines unreadable, no signage/label/watermark/logo. Checked at native size plus 2×–4× zooms of every text-bearing surface and all four frame edges |
| CAC-12 | no on-image AI-generated mark | known-box exact-fill probe on 5/5: plate fraction 0.0, no candidate mark, all four matched control boxes clean |
| CAC-26 | provenance recorded per slide | 5/5 byte-identical to the registry; manifest names each slide's Runway task id and SHA-256 |
| CAC-27 | correction budget respected | no prior correction cycle; this is cycle 1 of a maximum 2 |
| CAC-28 | caption carries the disclosure line | "AI-generated visual; styling and caption by Aarohi's team." present in the AAR-37 caption |
| CAC-31 | billable-render gate honoured | human card "Approve Runway carousel render charge" **accepted 14:34:09.663Z**; delivered bytes uploaded **14:42:16Z** — approval precedes render |

Two additional checks I ran beyond the criteria list, both clean:

- **No synthetic overlay anywhere.** An 80×40 box scan for near-uniform rectangles (>85% single
  quantised colour) found 6 hits across the set; every one was verified visually as plain wall, sky
  or background bokeh — no badge, plate or overlay.
- **Vendor disclosure handled correctly.** AAR-36 reports the vendor rendered a lower-edge
  `AI-GENERATED` frame mark, removed by a bounded top-aligned delivery crop before upload. I
  re-measured: no such mark survives, and the removal did not introduce text.

## What FAILED (this is the publish gate)

### 1. CAC-20 — one lighting family: FAIL (S4)

The brief (§4) specifies **warm late-afternoon daylight from camera-left in every slide — one large
soft window as the key, gentle falloff to the right, no second light source.**

S4 is lit dominantly **from camera-right**: warm sun patches land on the camera-right wall while the
bright glazed balcony door and sky are on camera-left. Objective measures agree:

| Slide | hard-edge density (x) | blown highlights ≥250 | torso mean |
|---|---|---|---|
| S1 | 0.14% | 0.18% | 129.7 |
| S2 | 0.38% | 0.00% | 155.6 |
| S3 | 0.26% | 0.00% | 135.1 |
| **S4** | **0.89%** | **0.38%** | **106.6** |
| S5 | 0.43% | 0.05% | 154.2 |

S4 carries 2.3× the hard-edge density of the next-hardest slide and 2× its blown-highlight
fraction, visible as the hard-edged projected shadow bands on the balcony wall and floor. On the
contact sheet S4 also reads distinctly darker and cooler than the other four.

Honest note on my own instrument: outer-third mean luminance alone is an unreliable direction
proxy — it read S2 and S3 as camera-left. I report the S4 finding on the **visual read plus the
light-path measures**, and I name the proxy as unreliable rather than quoting it as proof.

### 2. CAC-21 — consistent framing distance (±10% of slide 1): FAIL

Measured with YuNet face detection (confidence **0.93–0.95** on 5/5), boxes drawn onto each frame
and **visually verified before use** — the boxes sit correctly on the face in every slide.

| Slide | face-height fraction | deviation from S1 |
|---|---|---|
| S1 | 0.157 | — |
| S2 | 0.130 | **17.5%** |
| S3 | 0.151 | 3.8% |
| S4 | 0.124 | **20.8%** |
| S5 | 0.162 | 3.3% |

Spread max/min = **1.30**. Tolerance is ±10%, so S2 and S4 fail. A 30% spread in face size across a
set the brief specifies as one camera distance is a visible scale jump, and it is plainly visible on
the contact sheet.

**Convention stated:** the face box is forehead-to-chin, not the brief's top-of-head-to-chin
fraction, so these figures are a **surrogate**. The sign and rough size of the deviation are the
finding; the exact percentage is not.

### 3. CAC-22 — eye line inside the middle third: FAIL on 5/5

| Slide | eye-line y | chin y | chin as % of 1350 |
|---|---|---|---|
| S1 | 337 | 460 | 34% |
| S2 | 222 | 324 | 24% |
| S3 | 314 | 433 | 32% |
| S4 | 294 | 392 | 29% |
| S5 | 349 | 477 | 35% |

The middle third of a 1350-tall frame is y 450–900. **Every slide puts the eye line above 450** —
the face occupies the upper third, and the frames read slightly higher than the eye level the brief
required on 5/5.

### 4. CAC-23 — slide k shows scene clause k: FAIL on S2, S4, S5

- **S2** — briefed "standing just behind the chair, both hands smoothing the open front of the
  cardigan at hip level, **in a bright home corner**". Delivered: the subject stands centred against
  a bare wall beside a chair. The home corner of clause 2 is not the frame.
- **S4** — briefed "**three-quarter frame** mid-step through an open domestic doorway onto the home
  balcony". Delivered: a **full-length** straight-on step through a glazed balcony door — both a
  framing-scale change and an off-clause composition.
- **S5** — briefed "warm late-afternoon light". Delivered: cool/neutral balcony daylight, consistent
  with the S4 lighting drift.

Note S4's framing problem is the same one CAC-21 measures: its face is 20.8% smaller because the
frame is wider than the brief.

### 5. CAC-24 — caption/visual agreement: FAIL (copy side)

The AAR-37 caption opens **"Ek hi outfit, poora din — subah desk pe, shaam ko dinner pe"** and later
says **"dressy enough for dinner right after"**. No slide shows a dinner setting: the sequence ends
at a balcony table with a chai glass in daylight. The caption promises a dinner outcome the visuals
do not show, which CAC-24 makes a FAIL ("any caption line about a garment, setting or activity that
is not in the slides").

This one is arguably the cheapest to close — the caption can be re-cut to promise the day the
slides actually tell, or S5's clause can be re-briefed for a dinner setting. Either way it is a
decision for the copy/brief owners, not a silent edit at publish time.

## Art-direction notes (not defects)

- **S2 bag colour.** S2 shows a black shoulder bag; S1/S3/S5 show brown leather. The item-8 lock is
  "one small crossbody bag or tote" and does not name a colour, so I do not call this an outfit
  FAIL — but it is the one place the set does not read as a single continuous object, and it is
  worth a line in the correction brief.
- **S5 lower-torso texture.** S5's dusty-rose top carries an irregular dark mottled pattern. My read
  is a dappled light/shadow pattern rather than a fabric stain, and **no measure I built separates
  the two** — I flag it for the owner's eye rather than assert it as a CAC-25 defect.

## Coverage — what this harness did NOT check

Named so nobody mistakes this for a full CAC-1…31 pass. The following rows are **not implemented**
and need a human or vision verdict:

CAC-7 (prompt string substring match — needs the render record), CAC-8 (garment colourway CIEDE2000
— my region-sampling proxy was disproved on real bytes and is not a gate), CAC-9 (approved-silhouette
mapping vs AAR-7 §4), CAC-13 (identity lock vs the anchor crop), CAC-14…CAC-19 (hair, markers,
modesty cover, pose/setting, inherited camisole, third-party content).

Of these, **CAC-13 identity lock is the row I recommend a different owner certifies** — it is the
one criterion this agent should not be the sole signer of.

## Recommendation

**Run one consolidated correction cycle on the set, as a set — not slide by slide** (AAR-35 §"why
this is measured": a set that fails CAC-20/21/22 is regenerated as a set). The correction brief
should carry, at minimum:

1. **S4 lighting** — re-render with the single warm key from camera-left, no right-side key, no
   blown highlights.
2. **Framing** — return to the briefed waist-up medium frame and eye line inside the middle third on
   5/5; S2 and S4 are the outliers.
3. **S2 setting** — restore the bright home corner clause.
4. **S4 composition** — three-quarter frame through the doorway, not full-length.
5. **S5 light** — warm late-afternoon, not neutral balcony daylight.
6. **Caption** — re-cut the dinner promise, or re-brief S5 to a dinner setting. Owner decision.

Until the set passes, the 14:30Z slot on 2026-09-23 stays **empty** rather than carrying a
non-conforming carousel. If the correction cycle cannot complete before the slot, the right move is
to re-plan the slot with the Creative Director, not to publish a set that fails the gate.

## Evidence files (host path)

- `r3/qa_aar36.json` — the per-post harness output on the delivered bytes
- `r3/aar38_prepublish_qa.json` — the machine-readable criterion-by-criterion checklist
- `r3/provenance.json` — 6/6 sha256 + byteSize match to the AAR-36 registry
- `r3/framing_measure.json`, `r3/framing/S*_boxes.png` — face boxes (drawn) and the CAC-21/22 measures
- `r3/contact_sheet_annotated.png` — all five slides with the verified face box and the middle-third line
- `r3/s1_pen_zoom.png`, `r3/s1_shelf_zoom.png`, `r3/s5_blotch_zoom.png`, `r3/plate_hits.png`, `r3/bottom_edges.png`, `r3/top_edges.png` — the text/overlay/edge zooms behind the PASS rows
