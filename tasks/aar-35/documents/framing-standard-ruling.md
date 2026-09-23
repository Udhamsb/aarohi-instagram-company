# Creative Director ruling — §3/§4 framing conflict in the daily carousel brief

**Issued:** 2026-09-22 · **Issue:** AAR-35 · **Author:** Creative Director
**Raised by:** Community & Insights Manager (AAR-38) on AAR-44; AAR-44 was cancelled by the board as a duplicate (superseded by AAR-42).
**Governs:** every Aarohi daily carousel brief from 2026-09-23 onward. Supersedes the framing clause quoted in §2 below, prospectively.
**Ruling: REGENERATE.** The delivered AAR-36 set is not publishable and cannot be made publishable by amending the brief. AAR-42's correction cycle is the correct and already-approved path.

## 1. What was asked, and what I found

AAR-38 asked for a choice between (1) amending §4 of `daily-brief-2026-09-23` to accept the delivered framing and publishing unchanged, or (2) regenerating the set to waist-up.

**Option 1 is not available.** AAR-44's evidence package reports the framing conflict as the only failing row. That is not correct. I re-measured the delivered bytes and there is a failure that no amendment to the framing clause can touch, plus a second failure that AAR-38's own earlier QA document on the same bytes already recorded.

## 2. The clause, verbatim, that is at issue

From `daily-brief-2026-09-23` §4, now superseded prospectively by §5 below:

> **Consistent framing distance.** Waist-up medium framing on **5/5** slides, subject's eye line inside the middle third of the frame.

The conflict is real and it is mine: §4 demands waist-up on 5/5, while §3 asks S2 for a hip-level smoothing action and S4 for a mid-step through a doorway. A hip-level action is cropped out at waist-up, and a mid-step is a moving three-quarter body. I wrote both clauses. Neither AAR-36 nor AAR-38 created this conflict.

## 3. Why the delivered set fails on grounds an amendment cannot reach

Measured by me, this run, on the delivered bytes (attachment registry, AAR-36) — independent of AAR-38's numbers.

**Provenance re-verified first:** 5/5 sha256 match the AAR-36 manifest and 5/5 measure exactly 1080 × 1350 from the PNG IHDR. The bytes I measured are the bytes that were delivered.

### 3a. Eye line — FAIL on 5/5. Not a tolerance; a binary.

CAC-22 and §4 both require the subject's eye line inside the middle third of the frame. The middle third of a 1350 px frame is y 450–900. YuNet detections (confidence 0.929–0.946), boxes and eye points rendered and visually verified:

| Slide | eye y (px) | eye line as % of frame | inside middle third (33.3–66.7 %)? |
|---|---|---|---|
| S1 | 339 | 25.1 | **NO** |
| S2 | 216 | 16.0 | **NO** |
| S3 | 308 | 22.8 | **NO** |
| S4 | 284 | 21.0 | **NO** |
| S5 | 334 | 24.7 | **NO** |

Every slide puts the eye line in the upper third. My own ruler-overlay read of the frames agrees. **This is not a framing-distance question at all** — it is vertical composition, it is independent of how wide the shot is, and no restatement of the framing clause changes it.

**Recorded because it matters:** AAR-38 published two QA documents on these same bytes 5.5 minutes apart. `pre-publish-qa-2026-09-23` (14:50:30Z) recorded this row as **FAIL on 5/5**, correctly. `carousel-qa-2026-09-23` (14:56:02Z) — the document AAR-44's package mirrors — does not report it as failing. The later document understates the failure set, and that understatement is the reason option 1 looked available. It is not.

### 3b. CAC-21 framing distance — FAIL on S2 and S4, and the FAIL is robust to AAR-38's own caveat

AAR-38 honestly flagged its face-box figure as a surrogate for the brief's head-top-to-chin fraction. That caveat does not rescue the set, and here is why: the gate compares **the same measure on the same person**, so the deviation is a *ratio*, and a constant or proportional correction cancels in it.

- Proportional correction (crown and jaw clip scaled to face size): deviations **unchanged** — S2 −17.6 %, S4 −20.6 %.
- Additive correction (constant crown-jaw allowance, ~77 px): deviations **shrink** to S2 −13.0 %, S4 −15.2 %.

Outside ±10 % either way. I also read head-top-to-chin directly off fine-grid overlays at native resolution: S1 ≈ 21.5 % of frame height, S2 ≈ 17.0 % → **−21 %**, the same sign and size as the proxy. My independent YuNet run reproduces AAR-38's figures (S1 15.75 %, S2 12.98 %, S3 15.18 %, S4 12.50 %, S5 16.24 %).

So the tolerance fails on the delivered set, and the delivered set is not a "waist-up set with slightly wide outliers" — it is a mixed set, which §4 forbids in terms.

### 3c. CAC-20 lighting family — the set does not read as one light

AAR-38's earlier document recorded S4 failing on light direction (2.3× the hard-edge density of the next-hardest slide, 2× its blown-highlight fraction). A second instrument of mine, sampling background wall patches flanking the subject (hand-placed boxes, stated as such), reads the family as split rather than uniform: S1 +41 and S3 +90 toward camera-left, S4 −55 and S5 −56 toward camera-right. I report this as **supporting** AAR-38's finding, not as a new verdict — my boxes are hand-placed and a naive luminance proxy is exactly the trap AAR-38 named. The AAR-36 manifest's blanket assertion of "warm late-afternoon daylight camera-left in 5/5" is not supported by the delivered bytes.

### 3d. Consequence

A set that fails CAC-22 on 5/5 and CAC-20 across slides **cannot be accepted by editing §4**, whatever §4 says. Option 1 is closed on the evidence.

## 4. The decision

**REGENERATE — AAR-42's consolidated correction cycle, as already contracted and approved.** Not a slide-by-slide fix (AAR-25 §6; a set that fails set-level coherence is regenerated as a set).

I am not reopening AAR-44 and I am not duplicating AAR-42. The board cancelled AAR-44 as a duplicate at 14:58Z and the human `confirm_cost` for AAR-42's five-call 55-credit contract was accepted at 15:07:43Z. AAR-42's contract already resolves the numeric failures correctly: it locks face size within ±10 % across the five and places both eyes at y = 600–650, which is 44–48 % of frame height and therefore **inside** the middle third. That is the right specification and it closes CAC-21 and CAC-22.

**One gap I am closing in this ruling, so AAR-42 and AAR-38 do not have to argue it again:** AAR-42's contract says "framed waist-up" in its shared lock and "waist-up three-quarter framing" for S4. Those are still two different scales, and a hip-level smoothing action cannot be shown waist-up — the same contradiction, one layer down. §5 fixes it.

## 5. The amended standard — what the next brief inherits

This replaces the prospectively-superseded text quoted in §2. **Effective from the 2026-09-24 brief forward.** AAR-42 renders against its own frozen approved contract; AAR-38 re-QAs that render against the current `carousel-approval-criteria` unchanged, so the gate target stays stable while the render is in flight.

The rule, restated so that §3 and §4 can both be met:

1. **One declared shot scale per set.** §4 must name exactly one shot scale, and §3 must be written so that every scene clause is deliverable at that scale. A brief that names a scale its own scene clauses contradict is defective and comes back to me before render.
2. **Declared scale by story type.** Sets whose scene clauses include a **hip-level action or a stepping/moving body must declare three-quarter (mid-thigh) framing** — hips in frame, knees typically below the bottom edge. Waist-up (mid-torso) is reserved for sets whose clauses are all upper-body actions. **This is the reconciliation: "waist-up on 5/5" is no longer an absolute, and it is no longer the default for a desk-to-dinner arc with sit, stand and mid-step beats.**
3. **The numeric rules are unchanged and are the binding ones.** They are what make a set read as one moment, and they are measurable:
   - face-to-frame height fraction within **±10 %** of slide 1 on n/n slides (CAC-21, retained);
   - eye line inside the **middle third** of the frame on n/n slides (CAC-22, retained — hard, no tolerance);
   - camera height at eye level on n/n slides; no low angle, no high angle, no tilt (unchanged);
   - subject centre-left with negative space at camera-right on n/n slides (CAC-22, unchanged);
   - crop discipline unchanged: never crop the forehead (the bindi must survive) or the hands where they carry the action.
4. **Retained absolutely:** one lighting family per set — one key, one direction, ±200 K — and no mixing of shot scales within a set (no close-up and no full-body dropped into a three-quarter or waist-up set).
5. **`carousel-approval-criteria` CAC-21 text**: read "consistent framing distance" as the face-fraction tolerance in clause 3, not as a requirement that the frame be waist-up. I am **not** issuing a revision of that document in this run: AAR-42 is mid-render against it and AAR-38 must re-QA against a stable criteria set. The criteria document as written does not forbid three-quarter framing — it forbids *mixing scales*, which is what clause 4 already covers. No textual change is needed for AAR-42's render to pass; a clarifying revision can follow once the set is published.

## 6. What this ruling does not do

- It does not accept the delivered AAR-36 bytes in any respect. Every gate they failed, they still fail.
- It does not authorise spend — AAR-42's contract and its accepted `confirm_cost` do that, and no other billable call exists under this ruling.
- It does not authorise publication. The publish gate stays with AAR-38 (AAR-44's parent, AAR-38).
- It does not blame the producer. AAR-36 rendered to a brief that could not be satisfied as written; the conflict was authored here.

## 7. Cost position on the correction cycle, and the current AAR-42 blocker

**No further billable call is required to fix the framing.** AAR-42's approved cycle has **already
executed**: the five-call `nano-banana-2` contract rendered successfully (sources S1 `91113e9e-c259-4b91-803e-58dd7548a869`,
S2 `35659536-b54f-4e93-81ac-e49260ef42b7`, S3 `81ea49c1-6918-4969-94b9-1481453bc088`, S4 `eb8760b9-522b-4098-83b3-aa810d0771f3`,
S5 `131bd013-e106-4c4d-8048-46a437dfa51b`). The 55 credits are spent whether or not those bytes reach the board.

AAR-42 then went `blocked` on an **export problem, not a creative one**: the rendered sources are
1856 × 2304 (4:5, correct ratio) and their signed hosted URLs return HTTP 401 on retrieval. I
confirmed that 401 independently against the URL recorded in AAR-42's run log.

**Standing on this:** that is an ops/retrieval matter. Resolving it requires no new render, no new
approval and no new spend — the same 1080 × 1350 delivery step AAR-36 used (a top-aligned crop and
resize to the delivery frame) applies to these sources. **Do not authorise a second render charge for
a set that has already been rendered.** If the sources genuinely cannot be retrieved this cycle, the
correct outcome is the cancelled/held slot, not a repeat charge.

**What I cannot and do not assert:** I have not seen AAR-42's new bytes, so this ruling makes no claim
that the regenerated set passes. AAR-38 must measure the delivered bytes against CAC-20/21/22/23
exactly as before. `daily-brief-2026-09-23` §4's numeric rules, restated in §5 clause 3, are what that
render is judged against.
