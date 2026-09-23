# Sogni Video — Production Prompt & Publication Context

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 17: `- **On-screen text:** none, except the mandatory "AI-generated" disclosure overlay (see §5). All storytelling, CTA, and `
- line 25: `> A realistic editorial diary video of the same fictional North Indian woman, age 22–26, wheatish skin, long open dark h`
- line 29: `> Do not change her face, apparent age, complexion, hairline, or facial proportions across frames. No tied hair, braid, `
- line 41: `> AI-generated visual; caption and storytelling by Aarohi's team.`
- line 52: `- **Disclosure:** “AI-generated” is missing, obscured, cropped, illegible, or not continuously visible for the full clip`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Scope:** content-side spec for the *first* Sogni render only — concept, platform format, production prompt, caption/CTA, and guardrails. Execution (API call, model selection confirmation, cost estimate, polling, asset storage) is AAR-19's job; full camera/technical brief ownership is AAR-17. This issue supplies the copy/creative layer those two need to stay consistent with Aarohi's locked voice.

No credentials are referenced or required below.

## 1. Concept (concise)

Aarohi's quiet morning reset: she's at a sunlit window with a cup of chai, glancing down to journal for a few seconds, then looking up with a small, natural smile. Grounded, ordinary, undramatic — consistent with the "warm, grounded, everyday North Indian diary voice" locked in the persona bible. No plot, no dialogue — a single lived-in beat.

## 2. Platform & format

- **Primary platform:** Instagram Reels on `@aarohi.kapoor.diaries`.
- **Orientation/resolution:** 9:16 vertical, 1080×1920 (720p acceptable for the first test render per AAR-19's current default).
- **Duration:** 5 seconds for the initial test (matches AAR-19's default 5s/720p/native-audio test scope). Extend to 8–10s only if the approved brief changes.
- **Audio:** native/ambient sound only — soft room tone, faint chai-cup/paper sounds. No music track, no voiceover, no dialogue for this first render.
- **On-screen text:** none, except the mandatory "AI-generated" disclosure overlay (see §5). All storytelling, CTA, and hashtags live in the caption — consistent with the adopted clean-image/caption-first standard (AAR-14/AAR-15).

## 3. Production prompt (content-side draft)

This is the copy-layer input for whoever finalizes the technical/motion brief (AAR-17) and submits the render (AAR-19). Camera/lighting technical parameters should be reconciled with AAR-17's brief before submission; the identity, wardrobe, and disclosure language below are non-negotiable regardless.

**Positive prompt (base, extend with AAR-17's camera/motion detail as needed):**

> A realistic editorial diary video of the same fictional North Indian woman, age 22–26, wheatish skin, long open dark hair worn fully down, a small centred maroon bindi, and silver jhumkas. She sits at a sunlit window with a cup of chai, glances down to journal for a moment, then looks up with a small natural smile. Warm daylight, soft cotton kurta, modest everyday styling, neutral eye-level medium framing, calm natural posture, realistic skin texture and motion, respectful lifestyle editorial tone. Ambient native audio only — quiet room tone, faint cup/paper sounds, no music, no dialogue. Include a clearly readable on-video disclosure: “AI-generated,” visible continuously in the lower-right safe area for the full duration.

**Negative prompt / exclusion block (reuse from the locked persona bible, unchanged):**

> Do not change her face, apparent age, complexion, hairline, or facial proportions across frames. No tied hair, braid, ponytail, bun, clip-up, or updo. No missing maroon bindi or silver jhumkas. No glamorised or sexualised styling; no sheer, tight, low-cut, strapless, wet, lingerie-like, or bodycon clothing. No seductive pose/expression, reclining, bedroom/bathroom/bed setting, body-focused crop, low-angle chest/hip emphasis, or suggestive motion. No frame-to-frame identity drift, flicker, morphing, extra/duplicated limbs, or warped hands. No absent, hidden, cropped, illegible, or low-contrast AI-generated disclosure. No on-screen text other than the disclosure.

## 4. Caption / CTA (caption-first template, daily lifestyle type)

> Aaj ka small reset: chai, sunlight, and a few quiet minutes with my journal before the day gets loud.
>
> Some mornings don't need a plan, just a warm cup and a window seat.
>
> Turns out the calmest part of my day is usually the one nobody sees.
>
> What's your version of a quiet few minutes?
>
> AI-generated visual; caption and storytelling by Aarohi's team.
>
> #SlowMornings #DailyReset #ChaiTime #MindfulMoments #AarohiDiaries

(One CTA, no clickbait, hashtags specific to the setting — matches the adopted caption-first standard from AAR-15.)

## 5. Guardrails (condensed from the locked persona bible — full detail there)

Reject and re-render before any publish step if any of these is true:

- **Identity:** face, age read, complexion, or hair does not match the approved Aarohi reference across every frame; hair is tied/braided/updo at any point; bindi or jhumkas are missing when their area is in frame.
- **Disclosure:** “AI-generated” is missing, obscured, cropped, illegible, or not continuously visible for the full clip.
- **Modesty:** any framing, motion, pose, or crop reads as sexualised, suggestive, body-emphasising, or is set in an intimate space (bedroom/bathroom/etc.).
- **Continuity/artifacts:** visible morphing, flicker, warped hands, duplicated objects, or plastic/oversharpened skin.
- **Copy:** caption/CTA contains generic AI phrasing, clickbait, more than one CTA, or appearance-led/flirtatious language.

If any box fails, the correct remedy is a new render or a copy revision — not a disclaimer bolted onto a near-miss asset.

## 6. Handoff notes

- AAR-17 owns the final technical/motion camera brief; reconcile any camera-language conflicts against this doc's identity/modesty/disclosure lines, which are locked and take precedence.
- AAR-19 owns execution (cost estimate, `confirm_cost=true` submission, polling, durable asset storage) and must not embed the SOGNI_API_KEY in comments, files, commands, or logs.
- This document does not authorize spend or execution by itself — it is the content/copy input those two issues consume.
