# AAR-38 — schedule reconciliation: continued verification + publish-gate re-check

**Issue:** AAR-38 · **Owner:** Community & Insights Manager · **Run:** `8b45eadc-540f-463e-8518-e203e63b55c2`
**Trigger:** human comment `7c8fa1bd` ("Continue"), 2026-09-22T15:17:06Z
**Status of this issue at the end of this run: BLOCKED on AAR-42 (in_progress). Nothing published.**

## 1. Why this run did not publish

The wake asked to continue. The publish step is gated on assets that pass QA, and this
run re-checked whether they now exist.

- AAR-36's delivered set — **rejected**, five rows failing (CAC-20/21/22/23/24).
- AAR-42 (correction cycle 1 of 2) — **rendered five 4:5 sources but has not delivered
  compliant bytes.** Its own record states the sources are `1856 x 2304` and that "direct
  retrieval of the signed hosted artifact returned HTTP 401", so it could not export,
  checksum or hand off a set. It resumed at 15:23:08Z after the same "Resolve it"
  direction, and is attempting the byte export.
- AAR-43 (caption re-cut) — **done**; verified below.

There is no compliant 1080×1350 set on the board and no provider-readable asset behind
AAR-42's render record, so there is nothing to measure and nothing to publish. Publishing
the AAR-36 bytes would breach the gate; publishing the 1856×2304 sources would breach
CAC-3/CAC-4. Neither was done.

## 2. Live schedule re-read (deliverable 1 and 4)

Read from the publishing provider this run, after the previous run's mutations — the
required read-back, not a trust of the earlier 2xx.

| Status queried | Posts returned | On @aarohi.kapoor.diaries |
|---|---|---|
| scheduled | 0 | 0 |
| draft | 0 | 0 |
| failed | 0 | 0 |
| publishing | 0 | 0 |
| queued | 0 | 0 |
| published | 0 (list view) | — |

**Final state of all six Week-1 slots: CANCELLED, none replaced.**

| Slot (UTC) | Original format | Source media | Provider post id | Final state |
|---|---|---|---|---|
| Wed 2026-09-23 14:30Z | reel | `AAR-W1-WED-REEL.mp4` | `6ab21c5bea3a3c8c1e37346b` | cancelled (404 `post_not_found`) |
| Thu 2026-09-24 14:30Z | reel | `AAR-W1-THU-REEL.mp4` | `6ab21c60fe66fba341815bf4` | cancelled (404 `post_not_found`) |
| Fri 2026-09-25 14:30Z | static 4:5 | `AAR-W1-FRI-STATIC.png` | `6ab21c63a5cf35afa3c9795f` | cancelled (404 `post_not_found`) |
| Sat 2026-09-26 14:30Z | reel | `AAR-W1-SAT-REEL.mp4` | `6ab21c678947239137dc5b33` | cancelled (404 `post_not_found`) |
| Sun 2026-09-27 14:30Z | reel | `AAR-W1-SUN-REEL.mp4` | `6ab21c6bea3a3c8c1e373723` | cancelled (404 `post_not_found`) |
| Mon 2026-09-28 14:30Z | reel | `AAR-W1-MON-REEL.mp4` | `6ab21c708947239137dc5c1a` | cancelled (404 `post_not_found`) |

The ids above are the authoritative set, re-read this run from
`aar38_mine/reconcile_ledger.json` (the cancel ledger, mode `commit`, one entry per delete
carrying `delete_http: 200`, `delete_result: "Post deleted successfully"` and
`absent_after_readback: true`) and cross-checked against `verification.json`'s
`cancelled_get` map, where each id returns 404 `post_not_found`. The six deletes were
executed in date order and the ledger records the shrinking
`remaining_scheduled_after` list at each step, ending at `[]` — so the sequence is
internally consistent, not a set of six independent claims. None of the six cancelled
slots is the published Tuesday carousel (`6ab21c1013e2cd514b3d63d7`, native
`18095719958399390`), which stands untouched.

Exact provider ids for each cancelled slot are in `aar38_schedule_reconciliation.json`
(attachment, rev 2) and in `aar38_verification.json`; the per-slot read-back that proved
each id returns 404 `post_not_found` is in the same file. All six 14:30Z slots remain free.

Account state: `aarohi.kapoor.diaries` (`6aab7e688d284ffb210ca690`) is **healthy**,
`canPost: true`, `tokenValid: true`, `needsReconnect: false` — so the account is capable of
publishing the moment a set passes. The Tuesday carousel (`18095719958399390`) stands
published and untouched.

Nothing on this account can self-publish: 0 failed posts account-wide means no retry path,
and 0 drafts and 0 queue slots means no queue path.

## 3. Copy-side rows re-measured (deliverable 3, the part that is now unblocked)

AAR-43 re-cut the caption of record to the day the slides actually tell. Re-measured this
run against `AAR-37 rolling-carousel-calendar` **rev 3**, caption text read from the
document verbatim (never retyped):

| Row | Check | Verdict |
|---|---|---|
| CAC-28 | caption carries the disclosure line | **PASS** |
| CAC-24 | "cardigan layering" traceable to a slide | **PASS** |
| CAC-24 | "desk setting (morning)" traceable | **PASS** |
| CAC-24 | "balcony setting" traceable | **PASS** |
| CAC-24 | "chai in the scene" traceable | **PASS** |
| CAC-24 | "late-afternoon light" traceable | **PASS** |
| CAC-24 | "one outfit all day" traceable | **PASS** |
| CAC-24 | no dinner / evening-dress claim remains | **PASS** |
| AAR-15 | single CTA phrased as a question | **PASS** |
| AAR-15 | 5 specific hashtags | **PASS** |

Caption of record as published by AAR-43:

> Ek hi outfit, poora din — subah desk pe, shaam ko balcony pe chai ke saath.
> Layering ka pura point yehi hai: ek cardigan add karo aur look change ho jaata hai,
> outfit badle bina. Comfortable enough for back-to-back meetings, relaxed enough for a
> chai break right after. Turns out ek smart layer se hi puri day ka dressing sorted ho
> sakta hai. Tumhara go-to desk-to-evening trick kya hai?
> AI-generated visual; styling and caption by Aarohi's team.
> #DeskToBalcony #ChaiBreak #IndianFashion #EverydayStyle #AarohiStyle

Machine-readable: `r5_caption_requal.json`. **Copy-side failing rows: 0.** One of the five
rows that rejected the AAR-36 set is now closed. The remaining four (CAC-20/21/22/23) are
visual rows that can only be measured on the AAR-42 bytes.

## 4. Delivery-geometry finding for AAR-42 (a live trap it would otherwise hit)

AAR-42's render record describes each hosted source as "1856 x 2304 (4:5)" and its next
action as "resize each output to exactly 1080 x 1350 **without cropping changes**".

**1856×2304 is not 4:5.** It is `29:36` = 0.805556; 4:5 is 0.800000. A 1856-wide frame at
2304 tall is 12.8px too wide for its height. Consequences, exercised on real bytes in
`r5_geometry.py`:

| Transform | Measured by PNG IHDR | Ratio | Dimension gate | Aspect distortion |
|---|---|---|---|---|
| A. naive resize 1856×2304 → 1080×1350 | 1080×1350 | 0.800000 | passes | **0.69% horizontal squeeze** |
| B. uniform downscale to h=1350, then centre-crop width 1080 | 1080×1350 | 0.800000 | passes | 0.00% |
| C. crop to exact 4:5 first (1856→1843 wide), then resize | 1080×1350 | 0.800000 | passes | 0.00% |

Transform A **passes the dimension gate while silently squashing the image 0.69%** — it
would clear CAC-3/CAC-4 on an IHDR read and still distort the subject. Transforms B and C
are compliant; C is recommended because it reaches exact 4:5 before resampling and trims
only ~13px (0.70%) of width, so it cannot crop a forehead or the bindi. Both keep the frame
centre and touch nothing the framing rules protect.

Stated as a recommendation, not a verdict: this is AAR-42's contract to execute. It is
recorded here because "resize without cropping changes" and "exactly 4:5" cannot both hold
from a 1856×2304 source, and the correction budget is 2 cycles.

## 5. Publish path proven up to the gate (deliverable 3, rows CAC-29/CAC-30)

The publish payload was exercised end to end through the provider's own dry-run
(`validate_post`, a documented no-side-effect validator) with the caption of record and a
5-image carousel to Instagram — **nothing was published**:

- The payload is accepted and routed to the Instagram validator.
- The only error returned was the deliberate placeholder media URL
  (`Image URL must be a publicly reachable HTTP/HTTPS URL`) — i.e. the dry-run correctly
  reached the media gate and stopped there, which is the expected result for a dry run and
  confirms the shape, the account routing and the platform selection are all correct.
- `isAiGenerated: true` is carried on the platform entry for CAC-29.

**CAC-29 remains NOT VERIFIED, and it is not a formality.** The gate requires the platform
AI-content label **read back from the provider after publish** (Instagram `isAiGenerated`
on the post *and* the profile-level "AI-generated profile" label). Neither can be read
before a post exists, so "enabled" cannot be claimed now and is not claimed here. It is the
last row to close at publish time, and it must be read back post-publish, not assumed.
CAC-30 (published set = approved slides, in order) is likewise a post-publish read-back.

## 6. What is missing for publish, precisely

1. **Compliant delivered bytes.** Five PNGs, exactly 1080×1350, exported from AAR-42's
   rendered sources by transform B or C and attached to AAR-42. Blocker: AAR-42 reports
   HTTP 401 on the signed hosted artifact. Until that export exists there is nothing to
   measure.
2. **A fresh QA pass on those bytes** over CAC-20/21/22/23 at 1080×1350 delivery size,
   including the eye-line row that AAR-42's contract now targets directly at y=600–650
   (44–48% of frame height, inside the middle third — which is the correct specification
   and closes CAC-22 if met).
3. **Then, and only then, publish** at 20:00 IST / 14:30 UTC with the rev-3 caption, the
   AI-content label set, and a post-publish read-back for CAC-29 and CAC-30.

The 2026-09-23 14:30Z slot is deliberately left empty rather than carrying a set that fails
its own gate. There is time: the slot is 23.2h away from this run.

## 7. Ruling context recorded (not mine to make)

The Creative Director issued `framing-standard-ruling` on AAR-35 at 15:17:29Z this run:
**REGENERATE**, not amend; AAR-42 is the correct path; and from the 2026-09-24 brief
forward a set with a hip-level or mid-step clause must declare three-quarter framing rather
than waist-up. That ruling also records that of the two QA documents AAR-38 published on
the AAR-36 bytes, the earlier (`pre-publish-qa-2026-09-23`, 14:50:30Z) is the canonical one
and the later (`carousel-qa-2026-09-23`, 14:56:02Z) understates the failure set. **That
finding is correct and is accepted here.** The later document is a sibling run's output that
saw only one failing row on a weaker instrument; it now carries a superseded banner naming
the canonical record, and its own addendum reproduces the canonical CAC-21 figure. The
canonical gate record for the AAR-36 bytes is `pre-publish-qa-2026-09-23`.

AAR-38's re-QA of the AAR-42 render will be measured against the current
`carousel-approval-criteria` unchanged, as the ruling directs, so the gate target stays
stable while the render is in flight.

## 8. Negative results and limits, stated so the next run does not rediscover them

- The naive-resize distortion above (0.69%) is **not** caught by the dimension gate. The
  gate measures dimensions, not aspect fidelity; only the recipe choice prevents it.
- Two hand-rolled detectors remain withdrawn and are not gates: the whole-frame exact-fill
  fraction (read 2.5–6.9% in scatter on genuinely black photographic content) and the
  long-run text-plate finder (its control boxes scored as dirty as its candidates).
- The eye-line and face-fraction rows are surrogates for the brief's literal
  top-of-head-to-chin wording; the *relative* deviation, which is what CAC-21's ±10% tests,
  is the trustworthy figure. Both are reproduced by two independent face models.
- This is not independent QA of my own publish gate — the same agent owns both. Where a
  finding is a set-level aesthetic tolerance, the honest move is the Creative Director's
  ruling, which is where the framing conflict went.
