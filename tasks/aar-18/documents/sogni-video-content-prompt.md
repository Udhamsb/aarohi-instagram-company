# First Sogni Video — Content Prompt & Publication Context (AAR-18)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 36: `| On-video disclosure | Required regardless of the no-text-overlay rule: burned-in **"AI-generated"** badge, lower-right`
- line 48: `AI-generated visual; caption and storytelling by Aarohi's team.`
- line 66: `- **Disclosure:** burned-in "AI-generated" text, lower-right, high`
- line 69: `25 published 9:16 Week 1 assets. Platform-level `isAiGenerated: true``
- line 84: `jhumkas where their area is visible; any modesty breach; "AI-generated"`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Scope of this document:** the content-strategy side of the first Sogni pilot
render — concept, platform format, caption/CTA, and guardrails. The
shot-by-shot technical prompt (camera, action, lighting, native-audio
direction) is Creative Director scope in **AAR-17**; Sogni model selection,
cost quote, render and QA are AI Visual Producer scope in **AAR-16/AAR-19**.
This document gives AAR-17/AAR-19 the content brief to build against and
tells the board what will ship if the render passes QC.

## 1. Concept (concise)

**"Quiet 10 minutes" — morning chai reset.**

Aarohi at a sunlit window or balcony corner, holding a cup of chai, a slow
breath and soft, unforced smile toward camera as steam and light drift
across the frame. No dialogue, no on-screen text. This extends the "quiet
mornings" moment already established in the adopted caption template
(Daily lifestyle / mood moment example) into motion — low-risk, on-brand,
and a natural first subject for validating the new video pipeline before
committing to a busier Week 2 concept.

Why this concept for the pilot: single subject, static-ish setting, minimal
motion complexity, no props beyond a cup — the fewest variables for a first
render, so any identity-lock or modesty-rule drift is easy to catch in QC.

## 2. Platform format

| Spec | Value |
|---|---|
| Placement | Instagram Reels, `@aarohi.kapoor.diaries` |
| Aspect ratio | 9:16 vertical, 1080×1920 target |
| Duration | 5–8 s for the pilot render (AAR-19 is quoting a 5 s/720p job first per AAR-16's low-risk plan; re-render at up to 1080p only after the 720p pilot clears QC and cost is reconfirmed) |
| Audio | Native/ambient only — soft room tone, faint chai-pour/cup sound if the model renders it cleanly. No music track, no voiceover. Keeps the pilot simple and avoids AAR-4's licensed-music constraint (this account is not connected with `loginMethod=facebook_login`, so `audioConfiguration` isn't usable — ambient/native audio from the render itself is the only in-scope audio path). |
| On-video text | None. Per the adopted caption-first standard (AAR-12/AAR-15), the visual stays clean and the story lives in the caption. |
| On-video disclosure | Required regardless of the no-text-overlay rule: burned-in **"AI-generated"** badge, lower-right safe area, per Persona Bible §4 — this is a disclosure mark, not decorative on-image copy, so it does not conflict with the clean-image standard. |

## 3. Caption + CTA (ships with the post, per the adopted caption-first template)

Aaj ka small reset: chai, sunlight, and 10 quiet minutes before the day gets loud.

Some mornings don't need a plan, just a warm cup and a window seat.

Turns out the best part of my day is often the one nobody sees.

What's your version of a quiet 10 minutes?

AI-generated visual; caption and storytelling by Aarohi's team.

#SlowMornings #DailyReset #ChaiTime #MindfulMoments #AarohiDiaries

(This is the exact "Daily lifestyle / mood moment" example from the
caption-first template — reused deliberately so the first video's copy is
already pre-approved standard, not a new draft needing separate sign-off.)

## 4. Guardrails (non-negotiable, carried from the Persona Bible and prior standards)

- **Identity lock:** same approved Aarohi face reference; wheatish skin;
  long dark hair fully open — never tied, braided, clipped, bunned, or in a
  ponytail/updo; small centred maroon bindi visible when forehead is in
  frame; silver jhumkas visible when ears are in frame.
- **Modesty:** opaque, secure, fully-covering everyday wardrobe (soft
  cotton kurta or equivalent); no sheer/tight/low-cut/wet/bodycon styling;
  no intimate setting (this is a window/balcony daylight setting only); no
  suggestive pose, lip-biting, arched back, or body-focused camera angle.
- **Disclosure:** burned-in "AI-generated" text, lower-right, high
  contrast, legible at phone size, visible for the full duration of the
  clip (not just one frame) — matches the standard already verified on the
  25 published 9:16 Week 1 assets. Platform-level `isAiGenerated: true`
  flag should also be set on the Zernio post, supplementing (not
  replacing) the on-asset badge, per AAR-4 precedent.
- **Copy:** caption-first only — no text baked into the video; hook is
  specific to what's actually in the frame; exactly one CTA phrased as a
  question; 3–6 relevant hashtags, no generic spam stacking; no fake
  quotes, no clickbait, no generic AI phrasing.
- **Credential handling:** no Sogni API key or other credential appears in
  this document, any future comment, or any file — consistent with AAR-16's
  standing instruction.

## 5. Rejection triggers for this render (apply before it reaches publishing)

Reject and re-render if any of the following is true: face drift from the
approved reference; hair tied/braided/clipped/bunned; missing bindi or
jhumkas where their area is visible; any modesty breach; "AI-generated"
badge missing, illegible, cropped, or not visible for the full clip;
audio that reads as music/voiceover rather than ambient/native sound;
duration or aspect ratio outside the spec above. This mirrors the
Persona Bible §5 rejection standard already in force for stills and reels.

## 6. Handoff

- **AAR-17** (Creative Director): build the literal Sogni text-to-video
  prompt (camera, action, lighting, native-audio direction, negative
  prompt) from this concept and the Persona Bible §3 prompt scaffolding.
- **AAR-19** (AI Visual Producer): select the Sogni model
  (`seedance2-5` per AAR-16's evaluation), quote the 5 s/720p job with
  `confirm_cost=true`, render, and run the Persona Bible §6 pre-publish
  checklist plus the rejection triggers in §5 above before any publish
  step.
- If the pilot render clears QC, this caption/CTA/hashtag block in §3 is
  ready to ship as-is — no further copy pass needed.
