**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 33: `- Reel masters: 1080×1920, H.264 High/4.0, yuv420p, 30 fps; `moov` before `mdat``
- line 35: `- Reel covers and shot frames: 1080×1920 PNG. Carousel and static: 1080×1350 PNG (4:5).`
- line 43: `inside Instagram's reserved bottom 672 px caption/audio band on all 25 9:16`
- line 46: `2. **Silent reel masters.** All five carry no audio stream; Instagram will treat`
- line 47: `them as photo/clip uploads rather than Reels and the specified Hinglish`
- line 51: `statics, carousel slides and `*-REEL.png` masters are still attached to AAR-3`

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# AAR-4 — publishing readiness

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 30: `- Disclosure string is the exact hyphenated `AI-generated` in all 31 visuals, at`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Verdict: NOT READY TO PUBLISH. Nothing was published.**

The QA is complete (see `week-1-pre-publish-qa`). Publication was not attempted
because two of the three preconditions in this task's own objective are absent,
and the QA then surfaced two further blockers in the artifacts themselves.

## The gap, stated exactly

| Precondition | State | Evidence from this run |
|---|---|---|
| Explicit publishing authority | **ABSENT** | No board decision authorises an agent to post to `@aarohi.kapoor.diaries`. The Week 1 gate `c99c6c14-03f0-4566-8017-8fa85e25caf9` covers §1 identity and §5 form only. |
| Instagram account connection | **ABSENT** | `GET /api/companies/ccb737e1…/tools/connections` returns 7 connections: GitHub, Notion, Hugging Face, Zapier, Postman (draft), Google Drive (draft), Slack (draft). No Instagram / Meta / Facebook. |
| Instagram app in the gallery | **ABSENT** | The company tool gallery lists 46 apps; none is Instagram, Meta Business Suite or a social publisher. |
| Usable publisher behind Zapier | **ABSENT** | The Zapier connection is live and exposes 17 MCP tools (`execute_zapier_write_action` etc.), but no Instagram account is authenticated behind it, so no publish action can be enabled for it. |

Because the account connection does not exist, "account-native upload readiness"
cannot be satisfied for any of the seven posts regardless of how good the files
are — so it is reported as BLOCKED rather than PASS/FAIL.

## What is ready, if the account and authority arrive

Container and format compliance is otherwise verified on the delivered bytes:

- Reel masters: 1080×1920, H.264 High/4.0, yuv420p, 30 fps; `moov` before `mdat`
  (`ftyp, moov, free, mdat`) so progressive upload works; 4.6–8.1 MB.
- Reel covers and shot frames: 1080×1920 PNG. Carousel and static: 1080×1350 PNG (4:5).
- Durations Mon 20.0 s / Wed 12.0 s / Thu 16.0 s / Sat 16.0 s / Sun 16.0 s.
- Disclosure string is the exact hyphenated `AI-generated` in all 31 visuals, at
  18.73:1 in-frame contrast, 21.0:1 after a 420 px downscale + JPEG q26 round-trip.

## What must be fixed first (asset owner required)

1. **Disclosure placement (§4).** The badge at `x=733, y=1753, 291×57` is 100 %
   inside Instagram's reserved bottom 672 px caption/audio band on all 25 9:16
   assets, and 100 % inside the band the 4:5 profile-grid crop deletes. Target
   `x=700, y=1210, 291×57`.
2. **Silent reel masters.** All five carry no audio stream; Instagram will treat
   them as photo/clip uploads rather than Reels and the specified Hinglish
   voiceover is absent. Re-export with an audio track, or the board explicitly
   accepts audio-less posts.
3. **Superseded attachments under live filenames.** The 18:47 pre-correction
   statics, carousel slides and `*-REEL.png` masters are still attached to AAR-3
   under the same names as the 19:26 deliverables. Delete them or publish by
   attachment ID. The exact IDs are in `aar4_checklist.json`.

These are raised on **AAR-10** together with the account/authority ask, because
all four need a human owner rather than another agent pass.

## Disposition

AAR-4 holds at **blocked** on the account/authority gap (tracked by AAR-10).
The QA deliverable is complete and durable; publishing resumes on this issue as
soon as the account is connected and authority is granted, at which point only
the three re-edits above stand between the package and a compliant publish.
