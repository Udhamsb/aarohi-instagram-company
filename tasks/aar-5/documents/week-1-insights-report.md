**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 49: `| Wed | 2026-09-23 | reel | `6ab21c5bea3a3c8c1e37346b` | scheduled | 14:30 |`
- line 50: `| Thu | 2026-09-24 | reel | `6ab21c60fe66fba341815bf4` | scheduled | 14:30 |`
- line 51: `| Fri | 2026-09-25 | static 4:5 | `6ab21c63a5cf35afa3c9795f` | scheduled | 14:30 |`
- line 52: `| Sat | 2026-09-26 | reel | `6ab21c678947239137dc5b33` | scheduled | 14:30 |`
- line 53: `| Sun | 2026-09-27 | reel | `6ab21c6bea3a3c8c1e373723` | scheduled | 14:30 |`
- line 54: `| Mon | 2026-09-28 | reel | `6ab21c708947239137dc5c1a` | scheduled | 14:30 |`
- line 68: `| 2026-09-17 08:14 | static | 18 | 26 | 5 | 0 | 0 | 0 | 19.23 | — | — |`
- line 69: `| 2026-09-17 09:31 | **reel** | 124 | 137 | 4 | 0 | 0 | 0 | 2.92 | 23.3 | 90.2 |`
- line 70: `| 2026-09-18 09:33 | static | 23 | 43 | 5 | 0 | 0 | 0 | 11.63 | — | — |`
- line 71: `| 2026-09-18 09:38 | **reel** | 137 | 159 | 4 | 2 | 0 | 0 | 3.77 | 32.9 | 65.0 |`
- …and 25 further line(s) in this document reference the same superseded formats.

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# AAR-5 — Aarohi Week 1 insights and Week 2 series recommendation

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 241: `these standards, and carry a baked-in AI-generated disclosure badge per the AAR-4 record.`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Verdict: PARTIAL. The 24-hour Week 1 metrics this task requires do not exist yet.**
Run `aa8c445e-081f-4f15-9992-6fcc93e85847`, 2026-09-22.

The honest summary: Week 1 is not finished publishing. At measurement time exactly **one of
seven** Week 1 posts was live, and it had been live for **13 minutes**. Six posts are still
scheduled. I did not substitute the account's older posts for Week 1 data, and I did not
compute the requested metrics over a window that does not exist.

What I did produce: the full measurement apparatus, a settled-metrics read of the account,
every data gap stated with its evidence, and two candidate Week 2 series labelled
**PROVISIONAL** because neither saves nor completion — the two measures the objective names —
could be sourced.

---

## 1. Source and measurement window (as required)

| | |
|---|---|
| Source | Paperclip tool gateway → **Zernio MCP** → Instagram Graph insights API |
| Connection | `mcp.zernio.com/mcp for the company`, id `4049f71c-ee8e-46bb-bab2-c4d3a2bc24f1`, `authKind: api_key` |
| Account | `@aarohi.kapoor.diaries` (Zernio account `6aab7e688d284ffb210ca690`, profile "Aarohi" `6aab7b2a184320f175383344`) |
| Access confirmed | `hasAnalyticsAccess: true`; health reports `canPost: true`, `canFetchAnalytics: true`, `analyticsSupported: true`, scope `instagram_business_manage_insights` **granted** |
| Read at | **2026-09-22T06:24:15Z** (feed `lastSync`), per-post metrics stamped `2026-09-22 05:57:10` |
| Forced re-sync | `analytics_sync_external_posts` called twice (06:24Z, 06:26Z) |
| Window requested | 24 hours after each Week 1 post goes live |
| Window status | **NOT REACHED** |

Tools called: `accounts_list`, `accounts_get_account_health`, `accounts_get_follower_stats`,
`posts_list`, `posts_get`, `analytics_get_analytics`, `analytics_get_post_timeline`,
`analytics_sync_external_posts`, `analytics_get_daily_metrics`,
`analytics_get_best_time_to_post`, `comments_list_inbox_comments`,
`comments_get_inbox_post_comments`, `docs_search`.

## 2. Why the window is empty — Week 1 publish state

| Day | Date | Format | Zernio ID | Status | Publishes (UTC) |
|---|---|---|---|---|---|
| Tue | 2026-09-22 | carousel ×5 | `6ab21c1013e2cd514b3d63d7` | **published** | 06:11:25 |
| Wed | 2026-09-23 | reel | `6ab21c5bea3a3c8c1e37346b` | scheduled | 14:30 |
| Thu | 2026-09-24 | reel | `6ab21c60fe66fba341815bf4` | scheduled | 14:30 |
| Fri | 2026-09-25 | static 4:5 | `6ab21c63a5cf35afa3c9795f` | scheduled | 14:30 |
| Sat | 2026-09-26 | reel | `6ab21c678947239137dc5b33` | scheduled | 14:30 |
| Sun | 2026-09-27 | reel | `6ab21c6bea3a3c8c1e373723` | scheduled | 14:30 |
| Mon | 2026-09-28 | reel | `6ab21c708947239137dc5c1a` | scheduled | 14:30 |

The single live post's own 24-hour window closes **2026-09-23T06:11:25Z**. The last Week 1
window closes **2026-09-29T14:30:00Z**. That is the earliest date a complete Week 1 report is
possible.

## 3. What the reach / completion / saves / shares / follows read actually says

I measured the account's **six pre-existing external posts** (imported from Instagram,
published 2026-09-17 → 2026-09-20). These are **not Week 1 calendar posts** and are labelled as
such; they are the only posts on this account old enough to carry settled metrics.

| Published (UTC) | Format | Reach | Impr. | Likes | Comments | Saves | Shares | ER % | Watch % of dur | Skip % |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-09-17 08:14 | static | 18 | 26 | 5 | 0 | 0 | 0 | 19.23 | — | — |
| 2026-09-17 09:31 | **reel** | 124 | 137 | 4 | 0 | 0 | 0 | 2.92 | 23.3 | 90.2 |
| 2026-09-18 09:33 | static | 23 | 43 | 5 | 0 | 0 | 0 | 11.63 | — | — |
| 2026-09-18 09:38 | **reel** | 137 | 159 | 4 | 2 | 0 | 0 | 3.77 | 32.9 | 65.0 |
| 2026-09-18 20:53 | static | 26 | 34 | 5 | 0 | 0 | 0 | 14.71 | — | — |
| 2026-09-20 12:17 | static | 5 | 10 | 2 | 0 | 0 | 0 | 20.00 | — | — |

**Reach:** 333 total across 409 impressions. Reels averaged **130.5** reach per post against
**18.0** for static/carousel — a **7.25×** difference. The two highest-reach posts on the
account are both reels.

**But reach is not the whole story, and this is where the objective's warning about vanity
metrics bites.** Likes per reach run **3.07%** on reels versus **23.61%** on static/carousel,
and mean engagement rate is **3.34%** against **16.39%**. The reach advantage is real; the depth
is not.

**Reel completion:** the `completionRate` field is **0 on every post**, including reels that do
carry watch data. It is not populated on this connection's Instagram path. I used the surrogate
the API does give: average watch time as a percentage of reported duration, plus skip rate.
Both reels are ~10 s; average watch was **3.285 s (32.9%)** and **2.327 s (23.3%)**, with
`reelsSkipRate` **65%** and **90.2%**. Total watch time on one was 502,678 ms. So: wide reach,
shallow viewing.

**Saves:** **0** on every post in every window. **Shares:** **0** on every post in every window.
Neither can be ranked. This matters — see §4.

**Follows:** per-post follows are **unusable** — `null` on both reels (Meta does not expose that
metric for Reels; Zernio's docs say so explicitly) and `0` on the statics. Only the account-level
daily series is available:

| Date | 09-17 | 09-18 | 09-19 | 09-20 | 09-21 | 09-22 |
|---|---|---|---|---|---|---|
| Followers | 0 | 0 | 7 | 15 | 19 | **22** |

22 followers, +22 across the window, measured 2026-09-22T06:00:55Z. The gain lands on 09-19 and
09-20, before any Week 1 post existed.

**Comment themes:** the entire account holds **2 comments** — one audience comment
(`aidosthindi`: *"I love goolgapa"*, on the pre-existing pani puri reel, i.e. **positive**) and
one owner reply. Six of seven inbox rows have `commentCount 0`, and the live Week 1 post has
**zero**. One audience comment is not a theme set. I am reporting a **positive** signal of n=1
and **no negative themes observed** rather than manufacturing theme categories.

## 4. Data gaps (disclosed, with evidence)

1. **No 24-hour metrics for any Week 1 post** — 6 of 7 still scheduled; the live one was 13 minutes old. Evidence: `analytics_get_analytics` returns 6 posts, all `isExternal: true`, none a Week 1 id; `posts_list status=scheduled` returns the 6 remaining Week 1 ids.

2. **The live Week 1 post has no analytics row at all.** Not staleness — the feed `lastSync` (06:24:15Z) is *newer* than the post's platform `createdTime` (06:12:19Z), and a forced sync did not add it. `analytics_get_post_timeline` returns `null` by its Zernio id; by the id the sync tool returned (`6ab21f0f784f8eebd68a33eb`) it returned `null` on the final read; by platform post id `18095719958399390` it returned a single 2026-09-22 row of all zeros.

3. **`completionRate` is unusable** — 0 everywhere while watch-time fields are non-zero. The field and the surrogate disagree; I report the surrogate. This is the single biggest gap against the objective, which names completion as a selection criterion.

4. **Saves = 0 everywhere**, and **shares = 0 everywhere**. Zernio's own docs: *"Counts below 5 may be returned as 0 due to Meta's privacy floor on small audiences."* At 22 followers I cannot separate "nobody saved it" from "below the floor". Saves-based series selection is therefore **untestable at this volume** — not merely pending.

5. **Per-post follows unusable** — `null` on Reels by Meta's design.

6. **No Week 1 reel completion evidence** — all five Week 1 reels are unpublished.

7. **Comment themes uncompilable** — 2 comments total, 1 audience-authored.

8. **Best-time-to-post too thin** — 5 slots, each computed from 1–2 posts; top slot is Thursday 09:00 at avg engagement 5.5 over 2 posts. I did not act on it.

9. **The measured population is not the Week 1 population** — the six posts above predate the calendar and were published by hand, so format/CTA conclusions carry pre-launch conditions.

## 5. Week 2 series recommendations — two, labelled PROVISIONAL

The objective asks for two series selected on **saves and completion**. Neither is available.
Rather than invent numbers, I based both on the only settled evidence on this account — reach and
depth engagement by format — and marked what would falsify each. Both must be re-scored against
saves and completion at the re-wake in §6.

**Series 1 — Episodic street-food / daily-life Reels, one numbered episode per slot.**
*Basis: reach (PROVISIONAL).* Reels averaged 130.5 reach per post vs 18.0 for static/carousel —
7.25×. Both highest-reach posts are reels, both use a street-food hook (`pani puri`) and a
two-option question CTA.
*Caveats:* reels convert depth at 3.07% likes-per-reach vs 23.61%; average watch was only 32.9%
and 23.3% of a 10 s duration with skip rates of 65% and 90.2%; saves and completion are both 0,
so the objective's own test cannot confirm this series; n=2.
*Falsified if:* Week 1 reels land at or below static reach per post, or the Week 1 carousel
records more saves than the reels.

**Series 2 — Save-oriented utility carousels, one checklist/routine you can swipe-and-save per slot.**
*Basis: depth engagement by format + the Week 1 Tuesday design (PROVISIONAL).* Static/carousel
ran 23.61% likes-per-reach vs 3.07% for reels, and a higher mean engagement rate (16.39% vs
3.34%). Week 1's only carousel is the Tuesday post, built for exactly this
(*"Swipe, save, aur apna one non-negotiable reset comment karo"*). Every measured post already
asks a two-option question CTA and **none has a save CTA** — so save-oriented design is untested
here, not disproven.
*Caveats:* saves are 0 everywhere and Meta's privacy floor hides sub-5 counts, so this is a
hypothesis about depth, not a measured result; n=4 statics, none a checklist carousel.
*Falsified if:* the Week 1 Tuesday carousel records saves=0 after its 24h window while reels
record non-zero saves.

## 6. How this gets closed

The task cannot be completed by re-reading sooner — the metrics do not exist until the posts are
live and measured. So the issue is parked on a real, dated monitor rather than closed:

- **Earliest (Tuesday only, 24h):** 2026-09-23T06:11:25Z
- **Complete Week 1 (all windows closed):** **2026-09-29T14:30:00Z**
- **Recommended re-check:** 2026-09-29T15:00:00Z

At that re-check: force a `analytics_sync_external_posts` refresh, then re-score **saves per
post**, **completion proxy (avg watch % + `reelsSkipRate`) per reel**, **shares per post**,
**reach per post by format**, the **account follower delta** across the Week 1 window, and
**comment themes** once volume exists. Decision rule: keep the series that wins on
saves-per-reach and watch%; drop or reshape the other.

Note the standing constraint: if saves and shares remain 0 on all seven Week 1 posts after their
windows close, that is itself a finding — the objective's saves-and-completion selection rule is
not measurable on this account at 22 followers, and the recommendation basis should be changed
deliberately rather than worked around.

**Machine-readable companion:** `aar5-week1-measurement.json` attachment carries every post row,
the aggregates, all nine gaps with evidence, and both recommendations with their falsifiers, so a
later session can re-check without re-running this analysis.


---

# Pass 2 — monitor checkpoint, 2026-09-22T07:05Z (run 0162075c)

The pass-1 monitor fired 29 minutes after it was set, so this run re-measured. **Nothing
material changed, and the report above stands unaltered.**

## 2.1 What changed between passes

Between the pass-1 read (feed `lastSync` 06:24:15Z) and the pass-2 read (07:01:56Z):

| Check | Pass 1 | Pass 2 |
|---|---|---|
| Metric fields changed | — | **0** |
| Week 1 posts live | 1 | 1 |
| Week 1 posts scheduled | 6 | 6 |
| Week 1 posts with a metric row | 0 | 0 |
| Saves / shares / completionRate | 0 | 0 on every post |
| Followers | 22 | 22 (series unchanged) |
| Account comments | 2 (1 audience) | 2 (1 audience) |
| Account health / analytics access | healthy / true | healthy / true |

The live Tuesday post is now 50 minutes old, still absent from the analytics feed, and its
timeline reads a single 2026-09-22 row of all zeros. The six pre-existing posts' metric
values are byte-identical to pass 1. **The nine data gaps in §4 are unchanged, and the two
PROVISIONAL series in §5 are unchanged.**

## 2.2 A durable-progress defect found and fixed

The pass-1 monitor was set for 2026-09-29T15:00Z and was **consumed at 06:59:46Z**, 29
minutes later. The activity log (`issue.monitor_triggered`) shows `actorType: user`,
`actorId WQDCSqxCyGwdDVj9d5IDBZRvJFm99UYI`, **`source: manual`** — a human ran *check now*.
The schedule did not misfire.

The harmful part is the side effect: **a manual monitor check consumes the pending
schedule.** Immediately after it, `monitorNextCheckAt` and `executionPolicy` were both
`null`. Left unnoticed, the 2026-09-29 full-report wake would never have fired and this
issue would have sat `in_progress` indefinitely — the exact failure my pass-1 disposition
was intended to prevent.

Fixed in this run: the monitor is re-armed and verified (`monitorNextCheckAt`
2026-09-23T07:00:00Z, read back from the issue). **Rule for future passes: after any
monitor wake, read `monitorNextCheckAt` back and re-arm if it is null.** The next pass
must itself leave a dated schedule behind.

## 2.3 New creative standards adopted while this issue was parked

Four issues closed on the board between 06:46Z and 06:57Z, after Week 1 published:

- **AAR-12** (done 06:46Z) — *Clean-Image + Caption Template*. Images are text-free by
  default; AI-style headings, fake quotes, labels, watermarks, captions, CTAs and hashtags
  baked into the visual are rejects.
- **AAR-13** (done 06:52Z) — visual approval standard applying the above.
- **AAR-15** (done 06:53Z) — caption-first copy template: hook, context, value/feeling, one
  CTA, disclosure, 3–6 specific hashtags; wording must be traceable to what is in the image.
- **AAR-14** (done 06:57Z) — clean-image generation and QC standard.

This binds the §5 recommendations in one specific way: **any on-image save-nudge or on-image
CTA is now non-compliant**, so the save-oriented carousel series must carry its save ask in
the caption only. Both series are restated in caption-first terms in the machine-readable
companion.

It also constrains what Week 1 can teach: the Week 1 assets went live at 06:11Z, *before*
these standards, and carry a baked-in AI-generated disclosure badge per the AAR-4 record.
**Week 1 visuals must not be treated as exemplars of the new clean-image standard**, and any
Week 2 asset built to imitate them would now fail AAR-13.

## 2.4 How this still closes

- **Checkpoint 1 — 2026-09-23T07:00Z.** Tuesday's 24h window closed at 06:11Z. This pass
  tests the single biggest unknown: whether saves, shares and watch-time populate for a
  Week 1 post at all. It is deliberately not the report run.
- **Full report — 2026-09-29T15:00Z.** All seven Week 1 posts closed 24h (the last publishes
  2026-09-28T14:30Z). This is when §5's PROVISIONAL series get re-scored on saves and
  completion as the objective requires.

Standing constraint, restated because it is the likeliest way this task fails quietly: if
saves and shares are still 0 across all seven Week 1 posts after their windows close, the
objective's saves-and-completion selection rule is not measurable on a 22-follower account,
and the recommendation basis must be changed deliberately — with the reason recorded — rather
than worked around.
