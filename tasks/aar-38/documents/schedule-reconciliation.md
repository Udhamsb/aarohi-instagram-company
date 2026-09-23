# AAR-38 — live-schedule reconciliation to carousel-only, and the pre-publish QA gate

**Issue:** AAR-38 · **Owner:** Community & Insights Manager · **Run:** `913ff37b-0815-47e2-adde-4989805f6b96`
**Reconciliation committed:** 2026-09-22T14:16Z · **Binding standard:** AAR-34 `daily-format-standard`
**Disclosure standard:** AAR-33 `disclosure-policy` · **Provider:** Zernio MCP (Paperclip tool gateway), account `@aarohi.kapoor.diaries` (`6aab7e688d284ffb210ca690`)

## Outcome in one line

All six remaining Week 1 slots were scheduled in the old formats and none may publish under AAR-34.
**The 2026-09-23 carousel's slides do not exist** (AAR-36 render gate NO-GO, 0 credits — no billable
render submitted), so no slot's media could be replaced. **All six slots were cancelled**, each
verified absent by a fresh provider read-back. Nothing was published. The schedule for
`@aarohi.kapoor.diaries` is now **empty**, and the publish step is **gated on the rendered slides**.

## 1. Live read-back of the schedule, before any mutation

`posts_list_posts {status: scheduled}` returned exactly six posts, all on `aarohi.kapoor.diaries`
(the other connected account, `neuralwire.official`, held none):

| Date (UTC) | Day | Format as scheduled | Media | Provider post id |
|---|---|---|---|---|
| 2026-09-23T14:30:00Z | Wed | reel | `AAR-W1-WED-REEL.mp4` (video) | `6ab21c5bea3a3c8c1e37346b` |
| 2026-09-24T14:30:00Z | Thu | reel | `AAR-W1-THU-REEL.mp4` (video) | `6ab21c60fe66fba341815bf4` |
| 2026-09-25T14:30:00Z | Fri | static 4:5 | `AAR-W1-FRI-STATIC.png` (image) | `6ab21c63a5cf35afa3c9795f` |
| 2026-09-26T14:30:00Z | Sat | reel | `AAR-W1-SAT-REEL.mp4` (video) | `6ab21c678947239137dc5b33` |
| 2026-09-27T14:30:00Z | Sun | reel | `AAR-W1-SUN-REEL.mp4` (video) | `6ab21c6bea3a3c8c1e373723` |
| 2026-09-28T14:30:00Z | Mon | reel | `AAR-W1-MON-REEL.mp4` (video) | `6ab21c708947239137dc5c1a` |

All six carried `platformSpecificData.isAiGenerated: true`, account id
`6aab7e688d284ffb210ca690` passed explicitly, timezone `Asia/Kolkata`, post `status: scheduled`,
platform target `status: pending`, `publishAttempts: 0`.

Tuesday 2026-09-22 was already **published** and is not a slot: post `6ab21c1013e2cd514b3d63d7`,
platform `status: published`, native Instagram media id `18095719958399390`, `publishedAt
2026-09-22T06:12:24.417Z`, five `image` media items. It stands as published (AAR-34 §7 — no
retroactive rewrite).

## 2. Action per slot, with a read-back after every mutation

The only compliant action was **cancellation**: replacing a slot's media requires the approved
daily-format carousel, and that asset set does not exist (§4). Deleting a scheduled post is the
provider's documented cancel path (`DELETE /v1/posts/{postId}` — "Delete a draft or scheduled
post… Published posts cannot be deleted"). All six were within 24h of their slot and none had
passed, so all six were deletable.

| Date | Day | Provider post id | Action | HTTP | Absent on read-back | Scheduled remaining |
|---|---|---|---|---|---|---|
| 2026-09-23 | Wed | `6ab21c5bea3a3c8c1e37346b` | cancelled | 200 | **true** | 5 |
| 2026-09-24 | Thu | `6ab21c60fe66fba341815bf4` | cancelled | 200 | **true** | 4 |
| 2026-09-25 | Fri | `6ab21c63a5cf35afa3c9795f` | cancelled | 200 | **true** | 3 |
| 2026-09-26 | Sat | `6ab21c678947239137dc5b33` | cancelled | 200 | **true** | 2 |
| 2026-09-27 | Sun | `6ab21c6bea3a3c8c1e373723` | cancelled | 200 | **true** | 1 |
| 2026-09-28 | Mon | `6ab21c708947239137dc5c1a` | cancelled | 200 | **true** | 0 |

This provider's error responses are not reliable evidence that nothing happened, so each delete was
followed by a **fresh list read-back** (`aar38_mine/reconcile_ledger.json`) instead of trusting the
2xx. An independent post-pass then confirmed each of the six ids individually returns
`Error: [404] Post not found (code: post_not_found)` (`aar38_mine/verification.json`).

## 3. Final state of the account (read back after the last mutation)

- **Scheduled on `aarohi.kapoor.diaries`: 0.** `posts_list_posts {status: scheduled}` →
  `pagination.total: 0`; nothing is scheduled on any account.
- **Queue slots: none.** `queue_list_queue_slots` → `exists: false`, `nextSlots: []`;
  `queue_preview_queue` → `No queue schedule found for this profile`. No unattended publishing path
  can fire a post.
- **Drafts: 0.** `posts_list_posts {status: draft}` → `total: 0`.
- **Failed retries: none on this account.** **74** failed posts exist (second-run recount;
  the earlier "50" was the list page limit, not the total — see §7), **all on
  `neuralwire.official`**; zero belong to `aarohi.kapoor.diaries`, so nothing can self-retry into
  the Aarohi grid.
- **Published and untouched:** Tuesday 2026-09-22 (`6ab21c1013e2cd514b3d63d7`, native
  `18095719958399390`, published 06:12:24.417Z).
- **Account postable:** `accounts_get_all_accounts_health` → `status: healthy`, `canPost: true`,
  `tokenValid: true`, `needsReconnect: false`. Publishing authority already exists (AAR-10 closed
  `done`); only the assets are missing.

## 4. First daily carousel — publish step is GATED, not done

Nothing was published and nothing was rescheduled, because the slides for 2026-09-23 do not exist.

**What is missing (short list):**

1. **The rendered slides — the only hard blocker.** AAR-36 (AI Visual Producer) closed its
   pre-render gate **NO-GO**: the 5-call `nano_banana_2` contract is exactly 10 Higgsfield credits
   at 2 credits/call and the live balance is **0**. No billable render was submitted, so **zero**
   1080×1350 slides exist. AAR-36 is now `blocked` and carries `render-preflight-contract`.
   Closing it needs a human: fund the wallet, then approve the 10-credit contract with
   `confirm_cost=true`. That is a spend decision, not an agent action.
2. **Cost approval** — the `confirm_cost=true` gate above, per AAR-27/AAR-29/AAR-34 §5.

**What is no longer missing** (it landed during this run):

- **AAR-35 (Creative Director) is `done`** and published the approved brief and gate:
  `daily-brief-2026-09-23` (the verbatim LOCKED OUTFIT STRING, the five scene clauses, the verbatim
  positive and negative prompts, 5 slides, 1080×1350, one lighting family, one framing distance),
  `carousel-approval-criteria` (CAC-1…CAC-31, pass/fail, measured on the delivered bytes) and
  `outfit-rotation-plan`.
- **AAR-37 `rolling-carousel-calendar`** (done) gives the calendar, the date's outfit and the
  first caption, which already carries the mandatory disclosure line.

**Publish resumes when:** the 5 rendered slides exist and the QA below PASSES. Then the first daily
carousel goes out at 20:00 IST / 14:30 UTC on 2026-09-23, or the slot is re-planned with the
Creative Director if the render slips past it. All six 14:30Z slots are free for that.

## 5. Pre-publish QA — what is actually measured, and what is not

Two harnesses, both self-tested below.

### 5.1 `aar38_mine/carousel_qa.py` — the per-post gate

| # | Criterion (AAR-35 ID) | Method | Auto-verdict? |
|---|---|---|---|
| 1 | still-image carousel, count 4–6, default 5 (CAC-1/CAC-2) | file count; any `.mp4` in the set fails outright | yes |
| 2 | every slide 4:5 1080×1350 (CAC-3/CAC-4) | **IHDR read from the file bytes**, not metadata; plus the reduced ratio named on failure | yes |
| 3 | one single outfit across all slides (CAC-5/CAC-6) | visual read vs the AAR-35 locked string; dhash slide-similarity reported as a duplicate signal only | **no — explicit UNVERIFIED** |
| 4 | zero text in frame (CAC-10/CAC-11) | visual read | **no — explicit UNVERIFIED** |
| 5 | no on-image AI-generated mark (CAC-12) | visual read + known-box exact-fill probe with matched controls | **no — explicit UNVERIFIED** |
| 6 | caption disclosure line present (CAC-28) | regex over the caption text | yes |
| 7 | platform AI-content label enabled (CAC-29) | `isAiGenerated` on the built post | yes |
| — | provenance (CAC-26) | sha256 **and** byteSize against an attachment registry | yes |

### 5.2 `aar38_mine/carousel_set_signals.py` — set-level signals (CAC-8/20/21/22)

Colourway drift (region-sampled CIEDE2000 vs slide 1, threshold 12), lighting side
(outer-third luminance), framing scale (centre-column contrast mass, ±10%) and eye-line placement.
Full CIEDE2000 is implemented (Sharma et al.).

**These are signal generators, not verdicts, and on the calibration set they fail as proxies.**
Run against the published Tuesday slides: the eye-line proxy returned band `y=1153` on **5/5**
slides — it latched onto the burned-in caption plate's top edge near the frame bottom, not an eye
line — and the subject-height proxy returned `0.89–1.00` of frame height, i.e. "the subject fills
the frame", which no waist-up framing does. The lighting proxy also split 4 right / 1 left. None of
those readings describes the actual images. **No CAC-8/20/21/22 verdict may be issued from this
script.** It is retained as a documented negative result so the next session does not rebuild it
and trust it.

### 5.3 Self-test evidence — the harness was exercised on real bytes

The published Tuesday assets were downloaded and matched **6/6 byte-identical** to the AAR-3
attachment registry (`calibration_provenance.json`), then used as fixtures:

| Fixture | Result |
|---|---|
| Real 5-slide carousel, valid caption, label on | slide_count **PASS** (5); geometry **PASS**, 5/5 measured `1080x1350` by IHDR; caption+label **PASS**; 0 blocking defects → *INCOMPLETE (visual reads outstanding)* |
| 5 slides, two resized (1080×1920 and 1440×1440) | geometry **FAIL** — named `slide2.png is 1080x1920 (9:16)` and `slide4.png is 1440x1440 (1:1)` |
| 2-slide set | slide_count **FAIL** — "slide count 2 outside 4-6" |
| Caption with no disclosure line | **FAIL**, blocking defect recorded |
| `isAiGenerated: false` | **FAIL**, blocking defect recorded |
| Real AAR-37 caption, `isAiGenerated: true` | **PASS** — both disclosure patterns matched, human-directed clause matched |
| Real AAR-37 caption, `isAiGenerated: false` (negative control) | **FAIL** — label off |

### 5.4 Honest limits of this harness

- **The three visual checks are flagged, not measured.** No auto-PASS exists for outfit
  consistency, text-free frames or the on-image mark: each needs a visual read of every slide (or
  AAR-35's brief) that this harness does not perform. CAC-13…CAC-19, CAC-21…CAC-25 and CAC-27 are
  likewise visual/human, and the AAR-35 gate requires 4x-zoom reads for the text criteria.
- **I disproved my own plate probe.** I first reported a whole-frame exact-RGB(18,18,18) fraction as
  a badge detector, then tested it: the published Tuesday slides read 2.5–6.9% of frame in scatter
  from genuinely black photographic content (row histogram spread over 5–8 of 27 bands, not one
  compact band). It is not a detector and is now labelled as such. The **validated** probe measures
  the known badge rectangle `(700,1080,291×57)` against matched-size control boxes: Tuesday slide 1
  reads plate `0.398` / glyph `0.272` with every control at `0.000`, and the AAR-33-era clean
  expected reading is plate ≈ 0 in the same box.
- **A hand-rolled long-run text detector misfired and is not shipped as a verdict.** It found
  candidate caption plates, but its own matched control boxes returned 0.11–0.60 glyph fraction —
  as "dirty" as the candidates — so it cannot separate a composited plate from photographic
  content. Text-free frames stay a visual read.
- **Fixture caveat, stated so it cannot be mistaken for a template.** The published Tuesday slides
  are **pre-AAR-33 history**: they carry burned-in caption plates ("A realistic active-day reset"
  etc.) and an `AI-generated` badge, which would be a **FAIL** under AAR-33 today. They are used
  only to prove the harness measures real 1080×1350 bytes correctly.
- **Independence.** This is the same agent that will run the pre-publish QA, so this is the producer
  testing its own instrument. That is **not** independent review of the eventual carousel. The
  identity/outfit read (CAC-5/CAC-6/CAC-13) should be certified by a different owner, per the
  AAR-35 gate.

## 6. Why cancellation, not replacement

The issue allows "replace its media with the approved daily-format carousel before its publish
time, **or** cancel the slot". Replacement was impossible: the approved carousel needs 5 rendered
1080×1350 slides in one locked outfit, the render gate is NO-GO at 0 credits, and no billable call
may be made without the human cost approval. Cancelling is the only choice that satisfies the hard
rule — "do not leave a reel or a static scheduled to publish as the day's post" — and it is
reversible: all six 14:30Z slots are now free for a fresh carousel. Every cancellation happened
**before** the first publish time (2026-09-23T14:30Z).

## Evidence files (host path)

- `aar38_mine/reconcile_ledger.json` — pre-state, per-slot delete result, read-back after each
- `aar38_mine/verification.json` — independent post-pass: scheduled total, published Tuesday, 404 per cancelled id
- `aar38_mine/carousel_qa.py` — the per-post QA gate
- `aar38_mine/harness_selftest.json`, `aar38_mine/qa_case_*.json` — self-test evidence
- `aar38_mine/carousel_set_signals.py`, `aar38_mine/cac_signals_tuesday.json` — the set-level proxies and their negative calibration
- `aar38_mine/badge_box.py`, `plate_control.py`, `plate_finder.py` — the probe validation behind §5.4
- `calibration_provenance.json` — 6/6 Tuesday/Friday assets sha256+byteSize matched

## 7. Second-run verification of this artifact (2026-09-22, run `26096d1d-2536-470b-8b5b-e970df2fd997`)

**Independence: not independent.** This is a second run of the *same* agent, not review by a
different owner. It re-measured the artifact from the provider's live records rather than reading
this document's own summary. Every figure below was re-derived from Zernio, and the QA harness was
re-executed on bytes fetched from the board independently of the first run's copies.

| Claim in this document | Second-run result |
|---|---|
| Six slots cancelled, each absent on read-back | **reproduced** — all six ids return `[404] post_not_found` |
| Scheduled on any account: 0 | **reproduced** — `posts-list {status: scheduled}` → "No posts found" |
| Drafts: 0 | **reproduced** — "No posts found with status draft" |
| No queue slots | **reproduced** — `exists: false`, `nextSlots: []` |
| Failed posts: 50, all on the other account, 0 on Aarohi | **corrected — the total is 74.** Attribution reproduced: 74/74 on `neuralwire.official`, **0** on `aarohi.kapoor.diaries`. The conclusion is unchanged; the count was a misread of the `limit=50` page |
| Six old-format slots as listed (5 video + 1 image) | **reproduced** — `mediaItems[0].type` = video ×5, image ×1, with the same filenames |
| Tuesday published, native `18095719958399390`, 5 image slides | **reproduced** |
| Account postable (`canPost`/`tokenValid`/`needsReconnect`) | **reproduced** — healthy, `canPost: true`, `tokenValid: true`, `needsReconnect: false` |
| Attachment `aar38_schedule_reconciliation.json` = 7092 B, sha `d0d2b0…` | **reproduced byte-identical** — raw-byte sha256 and byteSize match the registry |
| Calibration provenance 6/6 (5 Tuesday slides + Friday static) | **reproduced** — re-downloaded from the board; all 6 match on sha256 **and** byteSize |
| Blocker edge AAR-38 → AAR-36, `unblockDescriptor.owner = board` | **reproduced** — `blockedBy` and `diagnostics/blockers` both name AAR-36 (`blocked`); `blockerAttention.state: covered` |
| AAR-35 / AAR-37 `done` with the named documents; AAR-36 unresolved | **reproduced** — `carousel-approval-criteria`, `daily-brief-2026-09-23`, `outfit-rotation-plan`, `rolling-carousel-calendar`, `render-preflight-contract`. AAR-36 read `blocked` at verification time (14:26Z) and has since moved to `in_progress` — still the one unresolved blocker; the blocker edge is what matters, not its transient status |

**The QA harness was re-executed, not re-read.** Fetched the five Tuesday slides from the board's
attachment registry and ran `aar38_mine/carousel_qa.py` on those bytes: slide count **PASS** (5),
geometry **PASS** on all five measured `1080x1350` by IHDR, provenance **5/5 match**, verdict
`INCOMPLETE (visual reads outstanding)`, zero blocking defects. Then re-ran it on fixtures that must
fail, to confirm the gate discriminates rather than always passing: 5 slides at 1080×1920 and
1440×1440 → **FAIL** naming each wrong size; a 2-slide set → **FAIL** ("slide count 2 outside
4-6"); a caption without the disclosure line → **FAIL**. The harness fails bad input and passes good
input, so its PASS readings carry information.

**Not re-measured by this run:** the three visual criteria (outfit consistency, zero text in frame,
no on-image mark) — they remain `UNVERIFIED` for the reasons §5.4 gives, and no carousel slides
exist to measure them on anyway. The `carousel_set_signals.py` proxies stay withdrawn.

**One precision on wording.** The six posts are **hard-deleted** by the provider's documented cancel
path, so none of them appears in `posts-list {status: cancelled}` (that listing holds nine unrelated
older posts, none of ours). "Cancelled" in §2 means "cancelled by deletion, confirmed by 404", not
a status transition to `cancelled` — stated here so a later session reconciling by status alone does
not think the six were never touched.

**Post-verification board note (2026-09-22T14:38Z).** AAR-36 has moved `blocked` → `in_progress` since this verification ran, so the render path is being worked; it remains the single unresolved blocker on AAR-38 and the blocker edge is unchanged (`blockerAttention.state` `covered`). No monitor is armed on AAR-38 by design: `executionPolicy.monitor` and `blocked` are mutually exclusive, and AAR-36's completion fires the `issue_blockers_resolved` wake that resumes this issue automatically. Publishing stays gated until the five 1080×1350 slides exist and the §5 gate passes.
