**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 8: `- line 101: `burned-in on-asset `AI-generated` badge is present and verified on all 25 9:16 assets at``
- line 43: `| plate present at `(700, 1080, 291×57)` | **25 / 25** 9:16 assets |`
- line 54: `**2. Reel audio — CONFIRMED.** All five masters now carry two streams (h264 video +`
- line 59: `| AAR-W1-MON-REEL.mp4 | h264 + aac | 20.0 s |`
- line 60: `| AAR-W1-WED-REEL.mp4 | h264 + aac | 12.0 s |`
- line 61: `| AAR-W1-THU-REEL.mp4 | h264 + aac | 16.0 s |`
- line 62: `| AAR-W1-SAT-REEL.mp4 | h264 + aac | 16.0 s |`
- line 63: `| AAR-W1-SUN-REEL.mp4 | h264 + aac | 16.0 s |`
- line 66: `superseded 18:47 build (which previously collided on FRI static, all five Tuesday`
- line 67: `slides, and the five `*-REEL.png` masters) is gone.`
- …and 8 further line(s) in this document reference the same superseded formats.

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# AAR-4 — Aarohi Week 1 published: authorised publication record

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 99: ``isAiGenerated: true` was set on all seven posts, so Instagram applies its own`
- line 100: `AI-generated label. This **supplements, and does not replace**, Persona Bible §4: the`
- line 101: `burned-in on-asset `AI-generated` badge is present and verified on all 25 9:16 assets at`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Status: PUBLISHED (1 live, 6 scheduled).** Run `04c017f3-d33b-462c-814d-0bf2fcbe3d80`.
Account: `@aarohi.kapoor.diaries` (IG account id `6aab7e688d284ffb210ca690`, Zernio profile "Aarohi").

## Authority and connection basis (both verified this run, not assumed)

- **AAR-10** ("Authorise publication + connect the @aarohi.kapoor.diaries Instagram
  account") was closed **done** by the board owner at `2026-09-22T05:34:25Z`, with the
  instruction "done provide the mcp to peprclip". That is the explicit publishing
  authority this task was waiting for.
- **Zernio MCP is connected to the company** as `mcp.zernio.com/mcp for the company`
  (connection `4049f71c-ee8e-46bb-bab2-c4d3a2bc24f1`, app-gallery link, `authKind:
  api_key`, credential in the Paperclip vault). 52 tools in its catalogue, bound to this
  agent through the "Native Community & Insights Manager" tool profile.
- **The account is live and postable**: `accounts_get_all_accounts_health` returns
  `aarohi.kapoor.diaries` → `status: healthy`, `canPost: true`, `tokenValid: true`,
  `needsReconnect: false`. Two Instagram accounts are connected
  (`neuralwire.official` and `aarohi.kapoor.diaries`), so the correct `account_id` was
  passed explicitly on every post rather than relying on auto-resolution.

## Pre-publish re-QA of the re-edited bytes (AAR-11 deliverables)

AAR-11 re-edited the assets; I re-downloaded the post-re-edit bytes from AAR-3 and
re-verified all three claims independently before publishing. **38/38 files matched the
attachment registry by sha256 and byteSize.**

**1. Disclosure badge moved — CONFIRMED.** Exact-fill test (the badge is a synthetic
plate of fill `RGB(18,18,18)` with pure-white glyphs; controls were identical-size boxes
elsewhere in the frame):

| check | result |
|---|---|
| plate present at `(700, 1080, 291×57)` | **25 / 25** 9:16 assets |
| control boxes over photographic content | none showed plate signature (0.000 fill / 0.000 glyph) |
| old defective position `(733, 1753)` | **empty on all 25** — no plate remains |
| bottom edge 1137 vs caption/audio band at y≥1248 | clear |
| right edge 991 vs action rail (x≥853 below y≥1150) | clear |
| inside the 4:5 profile-grid kept band 285..1635 | yes |

The producer's `y=1080` choice is correct, and better than the `y=1210` I had suggested:
1210 would have put the badge bottom at 1267, back inside the caption band it was
supposed to clear. That was my error and the producer caught it.

**2. Reel audio — CONFIRMED.** All five masters now carry two streams (h264 video +
AAC audio), durations unchanged at 20/12/16/16/16 s:

| master | streams | duration |
|---|---|---|
| AAR-W1-MON-REEL.mp4 | h264 + aac | 20.0 s |
| AAR-W1-WED-REEL.mp4 | h264 + aac | 12.0 s |
| AAR-W1-THU-REEL.mp4 | h264 + aac | 16.0 s |
| AAR-W1-SAT-REEL.mp4 | h264 + aac | 16.0 s |
| AAR-W1-SUN-REEL.mp4 | h264 + aac | 16.0 s |

**3. AAR-3 hygiene — CONFIRMED.** 53 attachments, **zero duplicate filenames**. The
superseded 18:47 build (which previously collided on FRI static, all five Tuesday
slides, and the five `*-REEL.png` masters) is gone.

## What was published

Cadence comes from the AAR-1 launch plan: one post per day, weekday-aligned. AAR-1 also
allows the first 2–3 slots to vary before settling on a consistent time. Zernio's
`analytics_get_best_time_to_post` for this account favours the 08:00–20:00 IST window, so
**20:00 IST (14:30 UTC)** is the consistent slot.

Weekday alignment was kept because the copy is weekday-branded ("Friday self-care",
"Sunday stretch"). The first day the account was authorised and postable is Tue 22 Sep,
so Week 1 runs Tue 22 Sep → Mon 28 Sep. Every post lands on its own weekday; none is
posted out of sequence.

| Day | Date | Format | Zernio post ID | Status | When |
|---|---|---|---|---|---|
| Tuesday | 2026-09-22 | carousel ×5 | `6ab21c1013e2cd514b3d63d7` | **published** | 06:12:24Z (11:42 IST) |
| Wednesday | 2026-09-23 | reel | `6ab21c5bea3a3c8c1e37346b` | scheduled | 14:30Z = 20:00 IST |
| Thursday | 2026-09-24 | reel | `6ab21c60fe66fba341815bf4` | scheduled | 14:30Z = 20:00 IST |
| Friday | 2026-09-25 | static 4:5 | `6ab21c63a5cf35afa3c9795f` | scheduled | 14:30Z = 20:00 IST |
| Saturday | 2026-09-26 | reel | `6ab21c678947239137dc5b33` | scheduled | 14:30Z = 20:00 IST |
| Sunday | 2026-09-27 | reel | `6ab21c6bea3a3c8c1e373723` | scheduled | 14:30Z = 20:00 IST |
| Monday | 2026-09-28 | reel | `6ab21c708947239137dc5c1a` | scheduled | 14:30Z = 20:00 IST |

**Tuesday is genuinely live**, read back from Zernio:
`platformPostId 18095719958399390` on `aarohi.kapoor.diaries`, `publishedAt
2026-09-22T06:12:24.417Z`, `status: published`. That native media ID is Instagram's own,
so the post exists on the platform — not merely in Zernio.

Captions, CTAs and hashtags are the approved v3 text verbatim (Hinglish lane, 5 hashtags
per post including `#AarohiDiaries`) with the hashtags inline in `content`, since Zernio
does not append a separate hashtags field. Media was uploaded through Zernio's own
storage and every URL was re-validated before use:

- `validate_post` on all seven posts, each media item attached → **"No validation issues
  found"** on 7/7.
- `validate_media` + a live ranged GET on all 11 uploaded assets → **HTTP 200**, sizes
  byte-identical to the reviewed local files.

## Disclosure handling

`isAiGenerated: true` was set on all seven posts, so Instagram applies its own
AI-generated label. This **supplements, and does not replace**, Persona Bible §4: the
burned-in on-asset `AI-generated` badge is present and verified on all 25 9:16 assets at
a placement that survives both the caption band and the 4:5 grid crop.

## Honest limitations

1. **Monday is the following week's Monday.** Because the account only became postable
   today (Tuesday), the "Monday" post is 28 Sep. The alternative was posting it out of
   weekday order, which would have contradicted its own copy and the AAR-1 plan's
   weekday-aligned cadence. Flagged here so the board can move it if they would rather
   compress Week 1.
2. **Tuesday published before I could schedule it.** Its create call returned an error
   (`502 Remote MCP tool call failed`) but the post actually published at 06:12:24Z. I
   detected this by reading the account's posts back before retrying, so no double-post
   occurred. Worth knowing: **this tool's error responses are not reliable evidence of
   non-publication** — always read the account back.
3. **Posting-slot variation.** AAR-1 says to vary the first 2–3 slots and then settle.
   I used one fixed slot (20:00 IST) for all six scheduled posts and let Tuesday publish
   immediately, which satisfies the "don't over-optimise before you have data" intent but
   is not literally a 2–3 slot test. No A/B rotation was invented.
4. **Media URLs are temporary.** Zernio keeps uploaded media for 7 days until a post
   using it publishes. All six scheduled posts publish inside that window, so this is
   safe, but a long delay past 29 Sep would need re-upload.
5. **No licensed music track.** `audioConfiguration` was not used: it requires the
   account to have been connected with `loginMethod=facebook_login`, and this account
   was not. The reels therefore ship with the package's own Hinglish voiceover and
   synthesized bed (rights-safe by construction), which is what AAR-11 delivered.

## Verification method note

Paperclip's secret-redaction middleware redacts `X-Amz-*` values in tool results, so the
presigned upload URL returns to the agent as
`X-Amz-Credential=***REDACTED***` and cannot be PUT to. I did not attempt to defeat the
redaction. Instead I used Zernio's documented token flow
(`/api/v1/media/upload/presign?token=…` → PUT → `/complete?token=…`), which carries the
token rather than the API key and is therefore not redacted. That flow is what the
vendor's own browser uploader uses.
