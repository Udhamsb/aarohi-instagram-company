**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 24: `**Parent:** AAR-23 Photo Videos generation · **Consumers:** AAR-25 (production standard), AAR-26 (script/promp`
- line 60: `| E1 | Meta/IPSOS India Reels study, June 2026 (about.fb.com India newsroom; reported by Mint, NewsBytes, Dail`
- line 61: `| E2 | Metricool 2026 Instagram Study, June 2026 | 24.3M posts, 375K accounts. Reels >4× the interactions of s`
- line 62: `| E3 | Socialinsider 2026 Instagram benchmarks | 35M posts. Median engagement rate — carousels 0.55%, Reels 0.`
- line 63: `| E4 | 2026 algorithm analyses (Mosseri statements, Jan 2026 + several independent 2026 reviews) | Rank order `
- line 64: `| E5 | Instagram, Sept 2026 — "AI-generated profile" label (official blog; Android Headlines, Storyboard18, bu`
- line 69: `| E10 | Zernio/Late API documentation, read live this run | `igReelsAvgWatchTime` and `igReelsVideoViewTotalTi`
- line 78: `The account's **only audience-authored comment ever** is *"I love goolgapa 😍"* from `aidosthindi` on the pani-`
- line 84: `### S3 — Discovery scroller (non-follower, Reels feed) · **FACT-supported**`
- line 85: `Reels reach is **7.25×** carousel/static reach on this account (§3). Reach is the only demand signal this acco`
- …and 38 further line(s) in this document reference the same superseded formats.

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# AAR-24 — Audience demand brief: what the Aarohi audience currently wants to watch

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 48: `| E5 | Instagram, Sept 2026 — "AI-generated profile" label (official blog; Android Headlines, Storyboard18, buzzinconten`
- line 156: `4. **An undisclosed AI persona.** The account must carry Instagram's **"AI-generated profile"** label and caption-level `
- line 211: `- **Disclosure in every caption**: plain-language note that the visual is AI-generated and that caption/storytelling is `
- line 227: `- **AAR-25 *Visual Production Acceptance Standard v1.0*, rule Z-3:** the only permitted on-asset text is (a) **the post-`
- line 229: `- **Persona Bible §4 remains binding**: every visual asset must visibly state `AI-generated` on the asset itself; captio`
- line 231: `So there is **no conflict**: the on-asset `AI-generated` overlay is *permitted* by Z-3 and *required* by §4, and the two`
- line 233: `Two further corrections to the earlier text: AAR-25's wording did **not** ban the marker — its rule Z-3 names it as the `
- line 235: `**Consumers were not misled.** AAR-26's script/prompt package independently states the same rule ("`AI-generated` disclo`
- line 239: `2. **Profile label verification.** No connector tool exposes the profile-level AI label. Somebody with account access sh`
- line 281: ``AI-generated` overlay, applied in post-production. Caption-only disclosure is **not** compliant and is no longer`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Run:** f3688904-d4ac-4499-a46e-9e6f1c319385 · **Read window:** 2026-09-22T10:40Z → 10:47Z
**Revision 2** (independent verification pass, run 6ea17feb-ba9e-4f02-b49a-1393941265fe):
all measured numbers re-derived from the raw gateway captures and confirmed; four textual
defects corrected — see §10 *Verification and corrections*. No metric changed.
**Account:** `@aarohi.kapoor.diaries` (Zernio social account `6aab7e688d284ffb210ca690`)
**Parent:** AAR-23 Photo Videos generation · **Consumers:** AAR-25 (production standard), AAR-26 (script/prompt package), AAR-27 (readiness gate)

## 0. Headline, stated honestly

**First-party audience validation is not possible at this account's current size, and this brief says so instead of dressing inference up as measurement.** Three hard gates were hit, each verified this run:

1. **Demographics are blocked.** `analytics_get_instagram_demographics` returns `age: [], country: [], gender: []` for both `follower_demographics` and `engaged_audience_demographics`. The tool's own response note: *"Requires 100+ followers."* The account has **22**. No age/gender/city segment on this account can be evidenced today.
2. **Saves and shares are unmeasurable, not zero.** `saves = 0` and `shares = 0` on all six settled posts, and the vendor's own documentation states *"Counts below 5 may be returned as 0 due to Meta's privacy floor on small audiences."* Third-party 2026 benchmarks put **average saves per post at 1 for accounts of 1–5K followers**. Saves cannot be a selection metric here.
3. **Week 1 has produced no measurable post.** The only published Week 1 post (Tuesday carousel `6ab21c1013e2cd514b3d63d7`, live 06:11Z) still has **no analytics row** at 10:47Z, and `analytics_get_post_timeline` returns a single 2026-09-22 row of all zeros. Six of seven Week 1 posts are still scheduled.

So this brief is built from (a) the six settled pre-launch posts that are the only measurable content on the account, (b) **India category-demand evidence** from named studies, and (c) clearly-labelled hypotheses. Every theme carries an evidence label. Nothing here is presented as an audience-validated result that is not one.

---

## 1. Sources and how to read the labels

| Label | Meaning |
|---|---|
| **FACT (first-party)** | Measured this run from the account's own Instagram Graph data via the Paperclip tool gateway → Zernio MCP. Numbers are reproducible from `final_snapshot.json` / `analytics_full.json`. |
| **EVIDENCE (third-party)** | Named external study or platform documentation, cited with its own sample size. Not this account's audience. |
| **HYPOTHESIS** | Inference from the two above. Carries an explicit falsifier. |

### First-party source record

| | |
|---|---|
| Surface | Paperclip tool gateway → Zernio MCP connection `4049f71c-ee8e-46bb-bab2-c4d3a2bc24f1` (`mcp.zernio.com/mcp`) |
| Access | `hasAnalyticsAccess` true; `instagram_business_manage_insights` **granted**; account status `healthy`; token valid to 2026-11-16 |
| Feed `lastSync` | **2026-09-22T10:47:10.117Z**, forced re-sync to `dataStaleness.staleAccountCount: 0` |
| Per-post metric stamp | `2026-09-22 09:05:55` |
| Tools called | `accounts-get-account-health`, `accounts-get-follower-stats`, `accounts-list`, `analytics-get-analytics`, `analytics-get-post-timeline`, `analytics-get-daily-metrics`, `analytics-get-best-time-to-post`, `posts-list`, `posts-get`, `comments-list-inbox-comments`, `comments-get-inbox-post-comments`, `analytics_sync_external_posts`, `analytics_get_instagram_demographics`, `analytics_get_instagram_account_insights`, `analytics_get_content_decay`, `search-tools`, `docs-search` |

### Third-party sources cited

| # | Source | What it is |
|---|---|---|
| E1 | Meta/IPSOS India Reels study, June 2026 (about.fb.com India newsroom; reported by Mint, NewsBytes, Dailyhunt) | 4,000+ respondents, 23 cities + rural India. Category engagement: Beauty & makeup 52%, Fashion & trends 52%, Lifestyle 42%, Fitness & Wellness 42%, Comedy 39%, Sports 38%, Travel 37%. 89% of Gen Z use Reels daily; 85% of women; 97% watch video on Meta platforms daily; urban 98% / rural 94%; Reels ≈60% higher creator engagement than other short-form platforms. |
| E2 | Metricool 2026 Instagram Study, June 2026 | 24.3M posts, 375K accounts. Reels >4× the interactions of single images; average Reel watch time **8.5s**, double YoY; carousels **9× more saves** than single images. |
| E3 | Socialinsider 2026 Instagram benchmarks | 35M posts. Median engagement rate — carousels 0.55%, Reels 0.52%, images 0.37%. **Average saves per post for 1–5K-follower accounts: 1 (reels), 1 (carousels), 1 (images).** |
| E4 | 2026 algorithm analyses (Mosseri statements, Jan 2026 + several independent 2026 reviews) | Rank order is watch time → sends/DM shares → likes per reach. Saves ≈3× likes; sends ≈5× likes. Reels reach rate ≈33% vs carousels ≈22%. |
| E5 | Instagram, Sept 2026 — "AI-generated profile" label (official blog; Android Headlines, Storyboard18, buzzincontent) | Undisclosed profiles featuring an AI-generated person become **ineligible for recommendations** (Reels/Explore). Disclosed profiles are **not** penalised for disclosing. Replaces the "AI creator" tag. |
| E6 | MeitY, IT (Intermediary Guidelines…) Amendment Rules, 2026 — notified 10 Feb 2026 | "Synthetically generated information" must be clearly and prominently labelled, with permanent metadata/provenance; labels may not be removed. |
| E7 | ASCI influencer guidelines (India, via press coverage) | Virtual influencers must disclose prominently that consumers are not interacting with a real human. |
| E8 | Meta/Ormax "Micro dramas: The India story", Feb 2026 (via IndianTelevision, ET) | 2,000 CAPI + 50 depth interviews, 14 states. 89% discovered the format through social feeds; 90% watch alone; top genres romance 72%, family drama 64%, comedy 63%; three audience segments (39% incidental, 43% intent-building, 18% high-intent). |
| E9 | AI-disclosure/trust studies on Indian users (2026, Jain University papers; Prestige coverage) | Indian Gen Z show a **"trust-action gap"**: human influencers outperform AI personas on trust and purchase intent; explicit disclosure lowers perceived authenticity. n=332 Indian Instagram users in one study. |
| E10 | Zernio/Late API documentation, read live this run | `igReelsAvgWatchTime` and `igReelsVideoViewTotalTime` are in **milliseconds**; `completionRate` documented 0–1; per-post `follows` is `null` on Reels by Meta's design; privacy floor on counts <5. |

---

## 2. Audience segments — what can and cannot be claimed

**No demographic segment can be evidenced for this account today** (gate 1 above). What follows are **behavioural** segments inferred from the only observed interaction, plus India-level category evidence. Two are HYPOTHESIS with partial FACT support; two are pure HYPOTHESIS.

### S1 — Hinglish relatable-diary viewer · **FACT-supported (n=1 interaction)**
The account's **only audience-authored comment ever** is *"I love goolgapa 😍"* from `aidosthindi` on the pani-puri reel (2026-09-18T19:59Z), followed by an owner reply. Account-wide there are **2 comments total**; **6 of 7** inbox rows read `commentCount: 0`; the live Week 1 post has none. The one audience comment landed on vernacular food content. That is a signal of n=1 — real, and small.
**Corroborating third-party:** E1 puts vernacular/relatable lifestyle content at 42% engagement in India.

### S2 — Save-oriented utility seeker · **HYPOTHESIS**
Routine/reset/how-to demand (E1 fitness & wellness 42%; E3 carousel save advantage). **Not evidenced on this account**: saves are floored (gate 2), so nothing here can be tested at 22 followers with the current metric set.

### S3 — Discovery scroller (non-follower, Reels feed) · **FACT-supported**
Reels reach is **7.25×** carousel/static reach on this account (§3). Reach is the only demand signal this account currently produces in volume.

### S4 — Festival/occasion styler · **HYPOTHESIS**
E1 fashion & trends 52%; festive windows are reported as reach multipliers. Not yet observed on this account.

**Segment conclusion:** design for S1 + S3 (relatable vernacular Reels that reach strangers), keep S2 alive as a *format* experiment rather than a *selection* claim, and treat S4 as a dated seasonal bet. Explicitly **do not** build a targeting strategy on demographics — the data does not exist below 100 followers.

---

## 3. What the account's own numbers say (FACTs)

### 3.1 Population measured
The analytics feed holds **6 posts, all `isExternal: true`** — imported pre-launch posts published 2026-09-17 → 2026-09-20, i.e. **before** the Week 1 calendar. Two are video/Reels (10s each), four are carousel/static. **No Week 1 calendar post has a metric row.** These six are the only settled evidence on the account and are labelled as pre-launch throughout.

### 3.2 Format: reach and depth invert

| Format | n | Avg reach | Likes / reach | Mean engagement rate |
|---|---|---|---|---|
| Reel (video) | 2 | **130.5** | 3.07% | 3.34% |
| Carousel / static | 4 | **18.0** | **23.61%** | **16.39%** |

Reels reach **7.25×** further per post (FACT). Depth runs the other way: static/carousel convert likes per reach **7.7×** better. Total across the six: **333 reach, 409 impressions, 25 likes, 2 comments**.
**EVIDENCE (E2/E3/E4)** agrees on the direction: Reels win discovery, carousels win saves and depth.
**On the ER column:** the vendor `engagementRate` reproduces exactly as `(likes + comments) / impressions × 100` on all six posts, so it is an impressions-denominated rate, not a per-reach one. The two denominations disagree on this data because impressions exceed reach on every post (409 vs 333 total). Where this brief ranks posts by ER it is ranking by that metric; the likes-per-reach column is pooled `sum(likes)/sum(reach)` per format.

### 3.3 Watch behaviour: wide reach, shallow viewing

| Post | Duration | Avg watch | % of duration | Skip rate | `completionRate` field |
|---|---|---|---|---|---|
| pani puri ep 1 (`6aad066b…`) | 10s | 3,277 ms | **32.8%** | 65.0% | 0 (unpopulated) |
| pani puri evening (`6aabb366…`) | 10s | 2,314 ms | **23.1%** | 90.2% | 0 (unpopulated) |

`completionRate` is **0 on every post including Reels that carry watch data** — the field is not populated on this connection. The percentage above is a **derived surrogate** (avg watch ÷ reported duration), named as such (FACT with surrogate caveat; units confirmed ms by E10).
**EVIDENCE:** E2's 8.5s average Reel watch time in 2026 is consistent — an 8–12s target is the honest planning assumption, and **Week 1's 16–20s Reels are a risk on this evidence.**

### 3.4 Saves, shares, follows

- **Saves 0 and shares 0 on all six posts** — and per E10/E3 this is the privacy floor plus a 1-save-per-post benchmark for 1–5K accounts, not evidence of audience refusal. **"No saves" is an unmeasurable claim, not a zero.**
- **Per-post `follows` is unusable**: `null` on both Reels (Meta does not expose it for Reels), `0` on statics. Account-level series only: **22 followers**, 0 → 22 across 09-17…09-22, with the gain on **09-19 and 09-20 — before any Week 1 post existed.** The current following therefore does not contain Week 1's effect, and Week 1 has not yet been tested on a following.

### 3.5 Two findings that change how we measure

- **Content decay (account-scoped, n=6):** 0–6h **8.3%** of final, 6–12h 33.3%, 12–24h 60.6%, 1–2d 86.4%, 2–7d 100%. **Reading a post at 24 hours captures roughly 61% of its eventual engagement** — and the first six hours deliver under a tenth. Implication: judge on 48–72h, and do not optimise for the first-hour spike.
- **"Best time to post" is not actionable:** every slot is computed from **1–2 posts** (top slot Thursday 09:00, avg 5.5 from 2 posts). No slot has ≥3 posts. I did not act on it and recommend nobody does yet.
- **Account insights 30-day (account-scoped):** reach 246, views 406, accounts engaged **9**, total interactions 28. At this volume, single-post differences are inside noise.

---

## 4. Validated themes and hooks (8)

Ranked by strength of available evidence. **"Validated" here means the strongest evidence available on this account — for T1–T3 that is first-party observation; for T4–T8 it is India category evidence plus hypothesis.**

| # | Theme / hook | Evidence | Strength |
|---|---|---|---|
| **T1** | **Street-food diary, numbered episode** — "pani puri diaries, ep 1". Hook: a counting/overshoot gag (*"20 pieces. actual: lost count after the fourth"*) or an episode number. CTA: one two-option question. | **FACT:** both highest-reach posts on the account are street-food / pani-puri content (137 and 124 vs 18.0 carousel-static avg); **one** of them is explicitly numbered ("pani puri diaries, ep 1"), the other is the same series unnumbered — the numbering convention itself is unproven here. The account's **only audience comment** is on one of them. | Highest first-party support (n=2 posts, n=1 comment) |
| **T2** | **6:30 am chai / quiet-morning ritual** — "chai, plants, aur thodi si dhoop… the quiet little chapter nobody sees". | **FACT:** 19.23% ER, 5 likes on 18 reach — **second-highest** of the six measured posts, not the highest (the maximum is 20.0% on the 2026-09-20 bookshop post, §3.2). **EVIDENCE E1:** lifestyle 42%. | Strong first-party depth signal |
| **T3** | **Chai + bookshop / slow-city weekend** — "stumbled into a bookshop… koi deadline nahi"; golden-hour terrace. | **FACT:** 20.0% and 14.71% ER. Taken with T2, **chai / quiet-life content holds the top three ER positions on the account** (20.0% bookshop, 19.23% 6:30 chai, 14.71% golden-hour terrace). | Moderate first-party |
| **T4** | **"Realistic reset" saveable carousel** — 5 slides, one non-negotiable reset each, save ask **in the caption only**. | **EVIDENCE E1** lifestyle 42%; **E2/E3/E4** carousels win saves/depth; **FACT** carousel ER 4.9× Reel ER here. First-party save data unavailable. | Category-backed, on-account untested |
| **T5** | **10-minute no-equipment micro-movement** and **desk-stiffness break** — gentle, beginner, chair-supported. | **EVIDENCE E1** fitness & wellness 42%. **FACT** the plan's own Week 1 fitness Reels are unmeasured. | Category-backed, untested |
| **T6** | **Modest desk-to-dinner / festive kurta + sneakers styling** — practical layering, not a reveal. | **EVIDENCE E1** fashion & trends 52% (joint-highest category) + festive window claim. | Category-backed, untested |
| **T7** | **Numbered episodic series with a recurring title** so viewers can follow an arc, not a one-off. | **EVIDENCE E8:** 89% of Indian viewers discovered micro-drama through social feeds; episodic habit is demonstrated at scale in India. | Strong category evidence, untested here |
| **T8** | **Hinglish two-option question CTA** as the repeatable engagement mechanic. | **FACT:** 6 of 6 measured posts close on a Hinglish option-choice question, but only **4 of 6 offer two options** — the other two offer three (rooftop/terrace/old-city; pani-puri/vada-pav/samosa). Revision 1 said "5 of 6 use a two-option question", which was also wrong. The account's single audience comment sits on one of them — **but total comments across the account are 2.** The honest read: it is *the only CTA form this account has ever used*, not *the form proven to work*. | Observed pattern, effect unproven |

**Hook mechanics that the evidence supports:** a specific number in the first line (T1, T5); a two-option question, exactly one per caption (T8); vernacular first-person narration throughout (E1, E8); the hook must be legible in the caption's first ~150 characters because captions are search-indexed.

---

## 5. Format preferences

| Decision | Recommendation | Basis |
|---|---|---|
| Primary discovery format | **Reels** | **FACT** 7.25× reach per post vs carousel/static; E2 Reels >4× single-image interactions; E4 Reels reach rate ≈33% |
| Depth / save format | **Carousels (4–6 slides)** | **FACT** 16.39% vs 3.34% mean ER; E2 carousels 9× saves of single images; E3 carousel save rate ≈3× Reels |
| Duration | **8–12s for Reels** (Week 1's 16–20s is a risk) | **FACT** 32.8%/23.1% of a 10s Reel watched, 65%/90.2% skip; **E2** 8.5s average Reel watch in 2026 |
| Static single image | **Filler only** | **E3** lowest ER of all formats (0.37%); **FACT** static reach 18.0 avg here |
| Cadence | **3–4 Reels + 1 saveable carousel per week** | E2/E3 consensus; **FACT** the account's best-time data is too thin to set times |
| Timing | **Do not tune publish time yet** | **FACT** no slot has ≥3 posts of support |
| Measurement window | **Judge at 48–72h, not 24h** | **FACT** decay curve: 61% of final engagement by 24h, 86% by 1–2d |
| Aspect | 9:16 Reels, 4:5 carousels, consistent with Week 1 | Continuity with the published package |

---

## 6. Do-not-create list

1. **Any text baked into a visual.** No captions, headlines, CTAs, hashtags, fake quotes, labels, signage with legible words, watermarks, logos, UI, or AI-style typography. (AAR-12 / AAR-13 / AAR-14 / AAR-15; owner directive on AAR-23: *"no text should be on the video or photo, no means no text"*.)
2. **Anything sexualised or modesty-breaching.** No sheer/tight/low-cut/wet/bodycon styling, no provocative pose or dance, no bedroom/bath/pool setting, no body-focused crop or low angle; no appearance-led or engagement-bait copy. (Persona Bible §2, non-negotiable.)
3. **Any identity-breaching frame.** No face drift, no age/complexion change, no tied/braided/up hair, no missing bindi when the forehead is visible, no missing jhumkas when ears are visible. (Persona Bible §1, §5.)
4. **An undisclosed AI persona.** The account must carry Instagram's **"AI-generated profile"** label and caption-level disclosure. Per E5, an undisclosed AI-human profile becomes **ineligible for Reels/Explore recommendations** — it loses exactly the discovery surface Reels demand depends on. Disclosing carries no reach penalty. Also required by E6 (MeitY labelling + provenance) and E7 (ASCI).
5. **Fabricated authority or health claims.** No diagnoses, no results promises, no "doctor says", no invented credentials, no fake quotes. India has a documented wave of synthetic "wellness/doctor" accounts; this account is a disclosed fictional persona and must never borrow clinical authority. (E9, E5.)
6. **A saves-based success test or saves-flavoured claims.** Saves are floored below 5 (E10) and average 1/post at 1–5K followers (E3). Any planned series whose pass/fail criterion is saves is **untestable at 22 followers**.
7. **Demographic targeting claims.** No age/gender/city segment may be asserted; the connector refuses demographics below 100 followers (verified this run).
8. **Long Reels as a discovery play.** Nothing over ~30s until watch data on this account exists; the only two measured Reels did not hold a 10s duration.
9. **Any billable generation before AAR-27's `confirm_cost`.** No assets were generated during this research.

---

## 7. Ranked recommendations for the next content package

Each carries a falsifier, per the objective's requirement to separate facts from hypotheses.

**R1 — Street-food diary, episodic, 8–12s Reel. (PROVISIONAL — strongest first-party support)**
Publish a numbered street-food episode with one counting/overshoot hook and one two-option question in the caption. Text-free frames, lo-fi handheld look, real market lane, face anchor per Persona Bible.
*Basis:* the two highest-reach posts on the account (137, 124 vs 18.0 static average) plus its only audience comment.
*Falsified if:* a Week 2 street-food Reel with settled metrics lands at or below the account's carousel reach per post, **or** it records a lower watch-percentage than the 32.8% first-party best.

**R2 — "Realistic reset" saveable carousel, 5 slides, save ask in the caption. (PROVISIONAL)**
*Basis:* carousel ER here is 4.9× Reel ER; E2/E3 give carousels the save/depth advantage; E1 gives lifestyle 42%.
*Falsified if:* after 72h a Week 2 carousel records fewer likes-per-reach than the Week 2 Reels. **Do not use saves as the test** — at this size it cannot resolve.

**R3 — 10-minute micro-movement and desk-stiffness Reels, ≤12s cut, no equipment. (PROVISIONAL)**
*Basis:* E1 fitness & wellness 42%; Week 1 already ships this pillar.
*Falsified if:* a ≤12s fitness Reel's derived watch-percentage does not exceed the 32.8% first-party best — in which case the pillar is the problem, not the length.

**R4 — Modest occasion styling Reel, timed to the next festive window. (PROVISIONAL, seasonal)**
*Basis:* E1 fashion & trends 52% (joint-highest) and the reported festive reach multiplier.
*Falsified if:* reach lands below the account's own Reel median in a non-festive comparison week.

**R5 — Chai / quiet-morning carousel or static, low production cost. (PROVISIONAL, depth play)**
*Basis:* chai / quiet-morning content holds the 19.23% ER post and shares the top three ER positions with the 20.0% and 14.71% posts (§4, §3.2).
*Falsified if:* it fails to beat the account's static reach average (18.0) by a margin larger than noise.

**Package shape recommended:** 3 Reels (one R1 street-food, one R3 movement, one R4 styling) + 1 R2 carousel + 1 R5 still, per week — matching §5's cadence, with **every Reel ≤12s** and **every caption carrying exactly one CTA**.

### The selection metric the objective names is unavailable — recorded, not worked around
The AAR-23 line asks for content chosen on what the audience wants; the sibling measurement task (AAR-5) named **saves and completion** as the selection metrics. Both are unusable here: saves are privacy-floored and completion is an unpopulated field (§3.3–3.4). The recommendations above therefore stand on **reach and derived watch-percentage**, labelled PROVISIONAL, with the re-score plan below — not on a metric quietly swapped in without saying so.

### Re-score plan
1. **2026-09-23T07:00Z** (AAR-5 checkpoint 1): read the first Week 1 post's settled metrics. This answers the single biggest unknown — whether saves, shares and watch time populate for a Week 1 post at all.
2. **2026-09-29T15:00Z** (AAR-5 full report): all seven Week 1 posts closed at 48–72h. Re-score R1–R5 on reach, derived watch%, and likes-per-reach; if saves remain 0 across all seven, record that the saves rule is unmeasurable at this size and change the basis deliberately.
3. **AAR-5 pass 2 already re-armed that monitor after a manual check consumed it** — the schedule is verified in place (`monitorNextCheckAt 2026-09-23T07:00:00Z`).

---

## 8. Implications for scripts and visual prompts

### Scripts
- **Length: 8–12s spoken, 1 idea.** Hook in the first 2 seconds — a specific number (T1, T5) or a two-option question (T8). Nothing that needs longer than ~25 Hinglish words.
- **First person, present tense, Hinglish.** *"Aaj ka small reset: chai, sunlight, aur 10 quiet minutes."* No ad voice, no slogans.
- **Exactly one CTA per caption, phrased as a genuine question or a simple action.** The save ask belongs in the caption and must never appear on screen.
- **No on-screen text of any kind.** The story lives in the caption (AAR-15 caption-first template: hook → context → value/feeling → one CTA → disclosure → 3–6 specific hashtags).
- **Every caption line traceable to something actually in the frame** (AAR-15). No invented events, no fake quotes.
- **Health content:** non-diagnostic, no results promise, an explicit "stop if sharp pain" cue, support/chair cues retained.
- **Disclosure in every caption**: plain-language note that the visual is AI-generated and that caption/storytelling is human-directed.

### Visual prompts
- **Text-free by default.** The negative prompt must explicitly ban: any letters, glyphs, pseudo-text, fake typography, signage with legible words, shop boards with readable text, posters, labels, logos, brand marks, watermarks, subtitles, UI chrome, or captions.
- **Keep the identity lock blocks** from AAR-3 / Persona Bible §1 and §3 unchanged — same face anchor, wheatish naturally textured skin, long open dark hair, small centred maroon bindi when the forehead is visible, silver jhumkas when ears are visible, modest opaque wardrobe, neutral eye-level framing.
- **Lo-fi over glossy for R1 and R5:** handheld framing, real market lane or a real kitchen counter, mixed available light. The reach evidence here comes from ordinary observed moments, and E9 warns that polish reads as advertising.
- **For R2/R5 carousels:** one idea per slide, 4–6 slides, no slide is exempt from the clean-image rule, and the save nudge lives only in the caption.
- **Food/street prompts (R1):** hands and food in frame, plausible portions, no legible price boards or menu text, no brand packaging.
- **Composition for Reels:** the first frame must carry the hook without any text to lean on — the subject's action and the setting do the work.

### Disclosure standard — resolved, and the earlier "conflict" flag withdrawn

**This paragraph previously reported a conflict between AAR-25's zero-text rule and Persona Bible §4, and recommended satisfying disclosure by caption only. That was wrong on the standards and is withdrawn.**

What is actually in force, read verbatim from the published documents:

- **AAR-25 *Visual Production Acceptance Standard v1.0*, rule Z-3:** the only permitted on-asset text is (a) **the post-production disclosure overlay, exact string `AI-generated`, applied after Pass 1–2 QC on the raw master**. Its disclosure-timing rule is explicit: generation prompts must not request the marker, the render is text-free, and the overlay is applied in **post-production on the raw master**. It states in terms that *"the Persona Bible §4 disclosure requirements remain fully in force — at the overlay/deliverable stage, not the generation stage."*
- **Rule SF-3** already carries the safe-area geometry: overlay present, high contrast, inside the platform safe area, on every carousel slide and reel shot, no undisclosed cutaway.
- **Persona Bible §4 remains binding**: every visual asset must visibly state `AI-generated` on the asset itself; caption-only disclosure is insufficient.

So there is **no conflict**: the on-asset `AI-generated` overlay is *permitted* by Z-3 and *required* by §4, and the two documents agree on where it belongs (post-production, after QC, inside the safe area). Caption-only disclosure would violate the locked standard and must not be used as the sole disclosure.

Two further corrections to the earlier text: AAR-25's wording did **not** ban the marker — its rule Z-3 names it as the express exemption; and the referenced **AAR-11 safe-area defect is fixed** — AAR-11 closed `done` with the badge moved off the caption/audio reservation and the grid-crop band (old `x=733, y=1753` → new `x=700, y=1080, 291×57`, re-measured on all 25 assets). The standing rule for Week 2 is therefore: generate text-free, then apply the exact `AI-generated` overlay in post-production inside the safe area on every asset. Do **not** copy Week 1's original badge geometry, which AAR-11 superseded.

**Consumers were not misled.** AAR-26's script/prompt package independently states the same rule ("`AI-generated` disclosure NOT requested in the generation prompt; flagged for post-generation platform-native overlay on every slide and the teaser clip"), and AAR-25 Z-3/SF-3 carry it. The stale text lived only in this document.

### Two gaps worth closing next, both cheap
1. **Per-post sends/DM shares.** E4 ranks sends as the strongest 2026 signal, and the connector exposes **no per-post sends field** (checked: the analytics row carries impressions, reach, likes, comments, shares, saves, reposts, views, watch time, skip rate — no sends). At 22 followers, sends would be the honest substitute for saves, which are floored. Worth requesting from the connection vendor.
2. **Profile label verification.** No connector tool exposes the profile-level AI label. Somebody with account access should confirm the "AI-generated profile" tag is on, given E5's recommendation-eligibility consequence.

---

## 9. Machine-readable companion

**Use `aar24_demand_brief_rev2.json` (attachment `17415a9a-e313-4686-b0f4-7c817c501e50`, 28,291 bytes, sha256 `f6348d6dc240274a…`).** It carves every measured row, the aggregates, the decay curve, the demographic refusal with its verbatim note, the full source list with samples, all 8 themes with evidence labels, the do-not-create list, and R1–R5 with their falsifiers — so a later session can re-score without re-running this analysis.

`aar24_demand_brief.json` (attachment `3b850cf4-b78b-4192-a536-1c067967ed2c`) is **superseded** by the rev-2 companion. It is retained only because it was the delivered bytes of revision 1; it still contains the withdrawn `standardConflict` field and the pre-correction T2/T3/T8/T1 evidence labels. **Read rev 2, not it.**

**Nothing was generated or published in this run.** No image or video asset was produced, no generation service or billable model was invoked, and no post was created, edited or scheduled.

---

## 10. Verification and corrections (revision 2)

Verification pass, run `6ea17feb-ba9e-4f02-b49a-1393941265fe`, 2026-09-22T10:37Z–11:09Z.

**How independent this actually is — stated plainly.** The verifier is a *different run of the same agent*, not a different role. The brief was produced by run `f3688904-d4ac-4499-a46e-9e6f1c319385`, which checked AAR-24 out and completed it at 10:55:21Z before the verifying run could take the lock. So this is a second pass by the same agent on its own output — weaker than review by a different owner, and it should not be relied on as independent QA. What it does have is that it was produced without sight of the author's reasoning, and every number was re-derived from the raw gateway captures rather than quoted. AAR-25/AAR-26/AAR-27 or the board should still treat the four corrections below as the *minimum* set of defects, not the complete set.

**Artifact provenance re-checked.** Companion JSON attachment `3b850cf4-b78b-4192-a536-1c067967ed2c` was re-downloaded and
byte-compared: **21,559 bytes, sha256 `bd1d3be164e7fef52a0b5a8ce1735a390d7f6fe907054421e7f27ee099cb7ffa`** — identical to the
attachment registry. The document body was read back from the API and matched.

**Every headline number re-derived from the raw captures and reproduced (37 of 37).** Reach 333 / impressions 409 / likes 25 /
comments 2 / saves 0 / shares 0; reel avg reach 130.5 and carousel-static 18.0 (ratio 7.25×); pooled likes-per-reach 3.07% vs
23.61%; mean ER 3.34 vs 16.39 (4.9×); derived watch surrogate 32.8% and 23.1% of 10 s; account insights 30 d (reach 246, views
406, engaged 9, interactions 28); decay buckets (8.33 / 33.33 / 60.56 / 86.39 / 100.0); follower series 0→22 with the gain on
09-19/09-20; demographics refused with the verbatim *"Requires 100+ followers"* note at 22 followers; six of six posts
`isExternal: true` with no Week 1 metric row; `follows` null on both Reels; `completionRate` 0 on all six.

**Four textual defects found and corrected in this revision:**

1. **T2 called 19.23% "the highest engagement rate of any measured post." False** — the maximum is **20.0%** (2026-09-20
   bookshop post). T2 is second. Corrected in §4.
2. **T3 read "14.71% and 20.0% ER — the top two ER scores after T2", which contradicts itself** (20.0 > 19.23). Corrected:
   the three highest ER posts are 20.0%, 19.23% and 14.71%, and chai/quiet-life content holds all three — which *strengthens*
   the depth finding rather than weakening it.
3. **T8's CTA count was wrong twice.** Revision 1 said a two-option question appears in "5 of 6" posts. The first revision of this verification replaced that with "6 of 6", which was **also wrong** — I had counted the presence of a choice question, not the number of options. Reading every caption ending: **6 of 6 close on a Hinglish option-choice question; 4 of 6 offer exactly two options; 2 of 6 offer three.** The corrected §4 entry states this. (Flagged here rather than silently re-corrected, because a verification pass that introduces its own error should say so.)
4. **The §8 "standard conflict" claim was wrong and is withdrawn** (see §8). It was drafted from AAR-25's *issue description*
   because its documents did not yet exist when this brief's author fetched them (the fetch returned `[]` at 10:41:21Z;
   AAR-25's standard was published at 10:41:31Z). AAR-25 Z-3 in fact permits and Persona Bible §4 requires the on-asset
   `AI-generated` overlay, applied in post-production. Caption-only disclosure is **not** compliant and is no longer
   recommended anywhere in this brief.

**One claim narrowed as overstated but not wrong:** T1 said both highest-reach posts are "exactly" numbered street-food
episodes. Both are street-food / pani-puri content, but only one carries an episode number. T1's numbering convention is
therefore an untested hypothesis, not an observed fact. Corrected in §4.

**No metric, ranking or recommendation was changed by this revision.** The theme order, the format preferences, the
do-not-create list and R1–R5 stand exactly as published; only the four texts above were wrong.

**Nothing was generated, published or spent in the verification pass.**
