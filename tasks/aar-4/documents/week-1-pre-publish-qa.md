# AAR-4 — Aarohi Week 1 pre-publish QA (seven posts)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 126: `## 5. §4 AI-generated disclosure — **FAIL, and this is the blocking creative defect**`
- line 128: `Exact string check first: the burned-in text is the hyphenated `AI-generated` in all 31 assets,`
- line 160: `"platform crop/compression"; §5 lists "Disclosure breach: AI-generated is missing, obscured,`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Reviewer:** Community & Insights Manager · **Run:** 27fa9973-d50c-455a-9140-54224a31dfba
**Reviewed:** the 43 delivered files re-downloaded from AAR-3 (issue `d1f11deb`)
**Method:** independent re-measurement off the delivered bytes (sha256-verified against the
AAR-3 attachment registry). The producer's own QA harness was not reused.
**Sources of truth:** `AAROHI_PERSONA_BIBLE.md` (attachment `7a69b57b`) §§1, 2, 3, 4, 5, 6.
**Verdict:** **QA COMPLETE — PUBLISH BLOCKED.** No publication was attempted.

---

## 0. Provenance of the reviewed bytes

All 41 of the 43 local review files matched the AAR-3 attachment registry by **sha256 and
byteSize** (41 verified, 0 mismatch) — 31 labelled visuals, 5 reel masters, 3 QA/registry
artefacts, 2 documents. The 2 unmatched files are the local anchor crops the producer bound
to generation calls (`ANCHOR_1FE53BA0…`, `ANCHOR_3678916C…`); their sources are attached to
AAR-3 as `1FE53BA0-…png` (1536×1024) and `3678916C-…png` (1222×1287).

The re-issued §7 reference pack from AAR-7 was re-downloaded and re-hashed: all three files
match the handoff digests (`2b57257e59a0164d`, `23364dba7cb29159`, `f09bcea5ccd12729`). Both
sheets and the wardrobe reference **do carry** a composited near-black plate with white
glyphs (10679 / 10062 / 44687 glyph-on-plate px) — the §7.1 disclosure gap is closed on the
reference side, which the producer could not verify from inside its own run.

---

## 1. Per-post checklist

Legend: **PASS** verified this review · **FAIL** blocking defect · **PASS\*** verified with a
recorded caveat.

| # | Post | §1 face | §1 hair down | §1 bindi | §1 jhumkas | §2 modesty/pose/setting | §4 label | §4 grid-crop survival | §5 form/safety | Audio | Upload readiness |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Mon — 10-min morning movement (reel 20.0 s) | PASS | PASS | PASS | PASS\* | PASS | FAIL | FAIL | PASS | FAIL | BLOCKED |
| 2 | Tue — active-day reset (carousel 4:5 ×5) | PASS | PASS | PASS | PASS\* | PASS | PASS | n/a (4:5) | n/a | n/a | BLOCKED |
| 3 | Wed — desk-to-dinner athleisure (reel 12.0 s) | PASS | PASS | PASS | PASS\* | PASS | FAIL | FAIL | n/a | FAIL | BLOCKED |
| 4 | Thu — beginner lower-body strength (reel 16.0 s) | PASS | PASS | PASS | PASS\* | PASS | FAIL | FAIL | PASS | FAIL | BLOCKED |
| 5 | Fri — Friday self-care (static 4:5) | PASS | PASS | PASS | PASS\* | PASS | PASS | n/a (4:5) | n/a | n/a | BLOCKED |
| 6 | Sat — festive kurta + sneakers (reel 16.0 s) | PASS | PASS | PASS | PASS\* | PASS | FAIL | FAIL | n/a | FAIL | BLOCKED |
| 7 | Sun — desk-stiffness stretch (reel 16.0 s) | PASS | PASS | PASS | PASS\* | PASS | FAIL | FAIL | PASS\* | FAIL | BLOCKED |

"Upload readiness" is BLOCKED for all seven for a task-level reason, not a creative one: there
is no connected Instagram account and no publishing authority (§5 below).

---

## 2. §1 identity — face, hair, bindi, jhumkas

Read at magnification on all 31 delivered visuals (head-crop strips + a 31-cell face grid,
generated from the delivered PNGs; `qa/faces_*.png`, `qa/face_grid.png`).

- **Face / apparent age / complexion — PASS.** One consistent subject across all 31 assets:
  same oval face, eyes, brows, nose, lip shape, jawline and hairline; consistent wheatish
  complexion with natural texture; reads 22–26 throughout. No lookalike substitution and no
  complexion drift between the five reels, the carousel, the static and the five covers.
- **Hair — PASS.** Long, dark, open, centre/soft-side part, visibly **down** in every asset.
  No tied, braided, clipped-up, bun, ponytail or updo frame found. The two frames where a hand
  is in the hair (`SUN_REEL_S1`, `SUN_REEL_S3`) still show it loose and open, which §1 allows.
- **Bindi — PASS.** A small centred maroon bindi is clearly visible in every asset where the
  forehead is in frame, and it is a small dot, not a fashion-sized graphic. Magnified read
  confirmed on the Mon/Wed/Thu/Sat/Sun/Tue/Fri/cover strips.
- **Jhumkas — PASS\*.** Silver earrings are visible in **both** ears in every asset with a
  frontal read (20 shot frames + carousel + static + covers). In **five** frames — `MON_REEL_S3`,
  `WED_REEL_S1`, `SAT_REEL_S1`, `SAT_REEL_S3`, `SAT_REEL_S4` — the subject is turned to a strong
  three-quarter or near-profile and the far-side earring is hidden by hair or out of frame.
  §1 permits "natural occlusion by hair or angle", so this passes on the bible's own wording.
  **Caveat recorded, not blocking:** at native resolution the earring form reads as a
  **dangling silver dangle/hook** — a bell-shaped jhumka with the characteristic flared rim is
  only clearly legible at the smaller render sizes. It is a silver, dangly, traditional-style
  earring in every frame, which satisfies the marker lock; if the board wants the *jhumka
  silhouette specifically* unmistakable at thumbnail size, that is an art-direction call for the
  Creative Director, not a blocker. Recommend a one-line wardrobe note in the reference pack.

## 3. §2 non-sexualised styling, pose, setting and copy

- **Wardrobe — PASS.** Every frame is opaque and secures chest, midriff, hips and upper thighs:
  Mon (long-sleeve tee + straight track pants), Tue (opaque kurta/printed sets, cardigan),
  Wed (long cardigan over opaque crew tee, straight trousers), Thu (tee + track pants),
  Fri (kurta + cardigan), Sat (straight-cut kurta with opaque trousers, secure drape),
  Sun (long-sleeve top + trousers). No sheer, tight, plunging, strapless, wet, lingerie-like or
  bodycon styling found in any of the 31 frames.
- **Pose and framing — PASS.** Eye-level or neutral camera; standing, seated, walking, lacing a
  shoe, stretching. No reclining, arched-back, lip-bite, sultry gaze, provocative dance or
  body-display. No body-focused crop and no low-angle chest/hip emphasis. The Wednesday
  "desk-to-dinner" reel is a layering transition, **not** a body reveal, and there is no
  changing-room scene.
- **Setting — PASS.** Living-room corner, kitchen counter, study desk, park path, home hallway,
  market lane, café/bookshop exterior, sunlit window. No bedroom, bathroom, bed, shower,
  changing-room or poolside setting anywhere. All public or domestic and non-intimate.
- **Copy — PASS.** Captions, on-image text, CTAs and hashtags are warm Hinglish, ordinary and
  non-flirtatious, with no appearance-led bait: e.g. Mon "Save karo for tomorrow morning, aur
  comment karo: movement ya chai pehle?", Sat "team sneakers ho ya juttis?", Fri "chai-loving
  dost ko bhejo". No double entendre, no romantic-availability cue, no thirst-trap language.

## 4. §5 beginner exercise safety (Mon / Thu / Sun only)

Read off the actual delivered frames, not the shot list.

- **Mon — 10-minute morning movement: PASS.** `MON_REEL_S2` is the full-body supported squat the
  producer regenerated after rejecting the first crop; feet are flat and roughly hip-width,
  knees track in line with the toes, chest lifted, neutral spine, controlled beginner depth,
  hips/knees/feet all inside the frame. `MON_REEL_S3` wall push-up keeps a straight
  head-to-heel line. `MON_REEL_S4` march stays upright with a modest knee lift. `MON_REEL_S5`
  is a calm over-arch reach with no forced extension. Pace and range read beginner.
- **Thu — beginner lower-body strength: PASS.** `THU_REEL_S2` sit-to-stand with a stable chair
  behind, feet flat, chest lifted, weight through mid-foot, controlled rise.
  `THU_REEL_S3` supported lunge with the front knee stacked over the ankle, short safe range,
  upright torso, hand support at the hip. `THU_REEL_S4` carries the explicit stop cue
  ("Sharp pain? Stop."). No pain-normalising frame.
- **Sun — desk-stiffness stretch: PASS\*.**
  - `SUN_REEL_S1` neck side-stretch: gentle range, no hyperextension, hand lightly on the head
    rather than pulling — **but the caption for this shot is "Desk-stiff? 3 gentle moves." while
    the following two shots are labelled "1. 5 slow shoulder rolls" and "3. Easy chest opener":
    the numbering skips 2.** The movement shown in `SUN_REEL_S2` (seated chair side-bend) is
    the missing step 2. The movement itself is safe and the torso stays upright; the defect is
    sequencing in on-screen copy, which will read as a mistake to a viewer. Recorded as a
    **medium** copy defect, not a safety blocker. It should be a one-frame text fix.
  - `SUN_REEL_S3` chest opener: loosened into a straight, un-fitted tunic with no forced arch.
    The producer's §2 rejection and regeneration of this frame is confirmed as fixed.
  - `SUN_REEL_S4` carries the stop cue ("No force. If it hurts, stop.").
- **Tuesday and Friday carry no exercise** — §5 is not applicable. `AAR-W1-TUE-CAR-S4` shows
  food preparation (fruit and nuts into a lunch box); no calorie, weight or diet claim appears
  in any caption of the seven posts.

## 5. §4 AI-generated disclosure — **FAIL, and this is the blocking creative defect**

Exact string check first: the burned-in text is the hyphenated `AI-generated` in all 31 assets,
white on a near-black plate, with glyph coverage 13.9–15.8 % of the plate box — the string and
its AA-level in-frame contrast are correct (measured 18.73:1 for every asset; 21.0:1 after a
420 px downscale + JPEG q26 round-trip; the producer's reported 5.04–5.33:1 is a more
conservative metric on the same glyphs, and it also clears AA).

The failure is **placement**, and it is measured, not asserted:

| Measurement | Value | Consequence |
|---|---|---|
| Badge box on all 25 9:16 assets | `x=733, y=1753, 291×57` | fixed, uniform |
| Distance from bottom edge | **110 px** | — |
| Instagram Reels UI reservation, bottom | **672 px** (y ≥ 1248) | badge is **100 % inside** the caption/audio band on all 25 assets |
| Instagram action rail reservation | x ≥ 853 below y ≥ 1150 | badge right edge reaches **x = 1024**; the box overlaps the reserved rail region |
| 4:5 profile-grid centre crop | trims y ≥ 1635 | badge is **100 % inside the trimmed band** on all 25 assets |

Meta publishes the Reels safe-zone figures as top 270 / bottom 672 / sides 64 with the
bottom-right action rail stepped out to 227 px from the right starting at y = 1150; on a
1080×1920 cover the main profile grid centre-crops to 4:5, deleting the top and bottom ~285 px.

Concretely, for these deliverables:

- In the **Reels player**, the badge sits exactly where Instagram draws the caption, username,
  audio attribution and the like/comment/share rail. The other burned-in copy is in the same
  band; the badge is the **right-most and lowest** element, so it is the first thing covered.
- In the **main profile grid**, every reel cover is cropped to 4:5 and the badge — with the
  whole lower third of the cover — is **not displayed at all**.
- The five reel **shot frames** repeat the same placement, so the defect propagates to every
  frame of every reel (confirmed by decoding frames back out of the encoded MP4s: 6 frames per
  reel, badge present and unclipped in the file, at y=1753–1810 in all of them).

Bible §4 requires the disclosure to be "away from UI overlays, crop edges" and to survive
"platform crop/compression"; §5 lists "Disclosure breach: AI-generated is missing, obscured,
cropped…" as a reject-and-regenerate condition. **§4 therefore cannot be signed off.**

Recommended fix (cheap, no regeneration): keep the plate and type, move it up and left of both
bands. Working target from the delivered geometry: the badge must sit fully above y = 1248 and
fully inside x ≤ 853 → a box such as `x=700, y=1210, 291×57` clears the caption band, the
action rail and the 4:5 trim on all 25 assets while staying bottom-right in the safe area.

**Secondary §4 observation (Mon and Sun covers).** On `AAR-W1-MON-REEL-COVER` and
`AAR-W1-SUN-REEL-COVER` the headline block extends past the 4:5 grid-trim line (glyph pixels
reach y = 1919 / 1910), so the bottom of the headline is deleted in grid view as well. The
Wed/Thu/Sat covers stop at y = 1877, which is still below the trim line. The four cover
rejections and rebuilds the producer recorded (headline over the face, badge crop in the
Ken-Burns build) are confirmed fixed, but the placement target itself was never brought inside
the published safe zone.

## 6. Audio and reel-native upload readiness

- **Reels are silent — they will not upload as Reels.** All five masters contain exactly one
  stream, `h264` video, 30 fps, yuv420p, High/4.0, no audio stream at all (`ffprobe`: Mon 600
  frames/20.0 s, Wed 360/12.0 s, Thu/Sat/Sun 480/16.0 s). Instagram accepts a video-only asset,
  but a 9:16 MP4 with no audio track is treated as a **photo/clip upload, not a Reel** — the
  Reel-audio pipeline and the Reels tab do not apply. The package specifies a Hinglish
  voiceover for each reel ("Aaj motivation low hai? Koi drama nahi…") and no audio exists to
  carry it.
- **Rights-safe audio: PASS by construction.** Because the masters carry no audio, no music or
  voice track is present, so there is nothing to clear. I found no licensed or unattributed
  audio in the delivered bytes. If a track is added later it must be re-cleared (Instagram
  business accounts are restricted to the licensed music catalogue) — that review has not been
  done and would need a real audio file.
- **Account-native upload readiness — BLOCKED.** Container/metadata is otherwise fine:
  moov atom before mdat (`ftyp, moov, free, mdat`) on all five, so progressive/faststart upload
  works; 1080×1920 9:16 H.264 MP4 and 1080×1350 4:5 PNG match Instagram's documented formats;
  file sizes 4.6–8.1 MB are well inside limits. The gap is not the container.

## 7. Superseded attachments still sit under the live filenames (blocking, operational)

AAR-3 holds 65 attachments. The 18:47 pre-correction build is still attached **under the same
filenames as the 19:26 deliverables**, so a publisher picking by name can pick the wrong file:

| Filename | superseded (18:47) | delivered (19:26) |
|---|---|---|
| `AAR-W1-FRI-STATIC.png` | `5070a362` 269,949 B | `47ae8a91` 1,775,277 B |
| `AAR-W1-TUE-CAR-S1…S5.png` (×5) | `905b75d6`, `6ab7d6c3`, `4dc65eda`, `9dca258b`, `eb1720e6` (~250–274 kB) | `4661328c`, `2ac2580d`, `f9a95638`, `713e3ae4`, `12a3ae71` (1.9–2.6 MB) |
| `AAR-W1-MON/WED/THU/SAT/SUN-REEL.png` | `e25afbe9`, `a679eb53`, `60aa9b36`, `40239f8d`, `91a197c8` | (superseded single-frame masters; the live reels are the `.mp4` files) |

`AAR-W1-MON/WED/THU/SAT/SUN-REEL.png` are v2 single-frame "reel" masters that no longer
correspond to the delivered reels; nothing references them. `reel_registry.json` and
`AAR-W1-FRI-STATIC.png`/`AAR-W1-TUE-CAR-S*` each exist twice.

The producer's v2→v3 correction was handled correctly on the *covers* (the defective v1 covers
were deleted from the issue), but not on the statics, carousel slides or old reel PNGs.
**Fix before publish:** delete the 18:47 superseded attachments, or have the publisher use the
attachment IDs recorded in `qa/aar4_checklist.json` rather than filenames.

## 8. Hinglish caption / CTA / hashtag lane

Checked the seven captions, CTAs and hashtag sets as delivered in §4 of the production package.

- **Language and CTA — PASS.** Natural, warm Hinglish; every post has a distinct CTA
  (save / comment / swipe / send-to-a-friend) with no repetition across the week. Voiceover
  scripts read as spoken Hinglish, not translated English.
- **Hashtags — PASS with a note.** Five per post, category-appropriate, no banned or
  appearance-led tags. `#AarohiDiaries` is the consistent brand tag on all seven.
  `#HomeWorkoutIndia` and `#IndianWellness` are broad-but-relevant; no spam-stacking.
- **Mix — PASS.** fitness Mon/Thu/Sun = 3, lifestyle Tue/Fri = 2, fashion Wed/Sat = 2, against
  the brief's 40/35/25 target. Five reels + one 5-slide carousel + one static.
- **Sequencing — one defect** (Sun on-screen numbering skips 2 of 3; see §4 above).

---

## 9. Disposition

**QA: complete and evidence-backed for all seven posts.** Identity, modesty, safety, copy and
the disclosure *string* all pass with the caveats recorded above. **Publication: not attempted
and not authorised.**

Blockers, in priority order:

1. **No connected Instagram account and no publishing authority** — first-class blocker raised
   as **AAR-10**. Verified this run: the company's 7 tool connections contain no Instagram /
   Meta / Facebook / social-publishing connection; the 46-app company gallery contains no such
   app; the live Zapier connection exposes 17 MCP tools but has no Instagram account
   authenticated behind it, so no publish action can be enabled.
2. **§4 disclosure placement** — blocking creative re-edit (§5 above).
3. **Silent reel masters** — blocking re-export or an explicit accept-audio-post decision (§6).
4. **Superseded attachments under live filenames** — blocking operational cleanup (§7).

Evidence: `qa/aar4_checklist.json`, `qa/independent_qa.json`, `qa/badge_uizone.json`,
`qa/label_survival.json`, `qa/uizone_measure.json`, `qa/face_grid.png`, `qa/faces_*.png`,
`qa/safezone_overlay.png`, `qa/superseded_compare.png`, plus the review scripts
(`qa_badge.py`, `faces.py`, `badge_uizone.py`, `label_survival.py`, `safezone.py`,
`superseded_check.py`, `refpack_check.py`, `verify_hashes.py`, `atoms.py`).
