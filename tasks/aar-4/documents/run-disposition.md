# AAR-4 — run disposition (run 27fa9973)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Author:** Community & Insights Manager · **Date:** 2026-09-22
**Status:** QA complete · **publish blocked** · nothing published

This document is the run's final disposition record for AAR-4. The agent's
board-session credential is board-scoped, so the run could not post a comment
authored as the agent (`POST /api/issues/{id}/comments` with `authorType: agent`
returns 422 "Comment author type must match authenticated actor"); the record is
left here and on the issue's other surfaces instead.

## Durable results of this run

| Artefact | Location | Verified |
|---|---|---|
| Seven-post pre-publish QA checklist (criterion by criterion, with measurements) | document `week-1-pre-publish-qa` on this issue | re-read: revision 1, 17,288 chars |
| Publishing-readiness gap analysis | document `publishing-readiness` on this issue | re-read: revision 1, 3,454 chars |
| Machine-readable checklist | attachment `aar4_week1_qa_checklist.json` (`955f2855`) | re-downloaded, sha256 + byteSize match |
| Publisher ask (account + authority) | **AAR-10** `7cba61e5-71d5-4b06-80bb-c6939f1f206c`, parent = this issue, assignee = board owner, priority high | read back |
| First-class blocker edge | AAR-4 `blockedByIssueIds = [AAR-10]`; `diagnostics/blockers` → "AAR-4 is blocked by AAR-10" | read back |
| Issue status | **blocked** (`blockedTransitionAt` 2026-09-22T02:46:15Z), blockerAttention `covered / active_child` | read back |

QA evidence lives in the QA workspace under
`cache/scratch/qa/` (`aar4_checklist.json`, `independent_qa.json`,
`badge_uizone.json`, `label_survival.json`, `uizone_measure.json`,
`face_grid.png`, `faces_*.png`, `safezone_overlay.png`,
`superseded_compare.png`) with the review scripts alongside it
(`qa_badge.py`, `faces.py`, `badge_uizone.py`, `label_survival.py`,
`safezone.py`, `superseded_check.py`, `refpack_check.py`, `verify_hashes.py`,
`atoms.py`, `make_checklist.py`).

## Result in one paragraph

All seven Week 1 posts pass §1 identity (one consistent face and age across all
31 visuals, hair worn fully down in every frame, small centred maroon bindi
wherever the forehead is in frame, silver earrings visible on every frontal
frame), §2 modesty/pose/setting/copy, §5 beginner-exercise safety on the three
fitness posts, the Hinglish caption/CTA/hashtag lane, and the §4 disclosure
*string* at measured 18.73:1 in-frame contrast (21.0:1 after a 420 px downscale
+ JPEG q26 round-trip). Publication is blocked by four findings: no Instagram
account connection and no publishing authority (AAR-10); the §4 badge sits 100 %
inside Instagram's reserved bottom-672 px caption/audio band on all 25 9:16
assets and 100 % inside the band the 4:5 profile-grid crop deletes — with a
no-regeneration fix at `x=700, y=1210, 291×57`; all five reel masters are
video-only so Instagram would treat them as non-Reel uploads; and the superseded
18:47 build is still attached to AAR-3 under the same filenames as the 19:26
deliverables.

## What resumes on this issue

Publishing resumes on AAR-4 the moment AAR-10 is resolved (account connected and
authority granted). At that point the three re-edits above are the only work
between this package and a compliant publish, and the QA itself does not need
re-running — only the §4 badge geometry needs re-measuring after the move.
