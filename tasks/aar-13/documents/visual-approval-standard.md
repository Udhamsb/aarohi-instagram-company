**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 24: `- If the rendered text drifts from the approved copy in any way — spelling, spacing, glyph shape — the image f`
- line 35: `- Resolution: output meets the platform spec (minimum 1080px on the short edge for feed; 1080x1920 for reels),`

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# Visual Approval Standard — Clean-Image (Aarohi)

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

Applies the shared [Clean-Image + Caption Template](/AAR/issues/AAR-12#document-visual-copy-template) (AAR-12) to the visual approval workflow. An image is not approved unless every section below passes. Approve the clean variant by default and treat text on image as the exception, never the default.

## 1. Default: text-free imagery

- Generated imagery is text-free by default. The visual carries mood, subject, and setting; the caption carries the words.
- Any readable text baked into the image — headings, fake quotes, labels, watermarks, captions, CTAs, hashtags, decorative typography, or signage with legible words — is an automatic reject in review, unless the campaign-text exception in §2 has been explicitly granted.
- AI-looking typography is rejected even when the words are correct: warped letterforms, melted or inconsistent glyphs, gibberish pseudo-text, garbled sign text, and hallucinated alphabets all fail this check.
- Logos, UI chrome, posters, and screens with legible words count as baked-in text. Regenerate without them or crop them out.
- Irrelevant baked-in text fails relevance even if it is typographically clean: text unrelated to the scene, the brand, or the approved story concept is a reject.

## 2. Exception path: explicitly approved campaign text

- Exception first, render second: campaign text on an image requires the exact copy to be approved (by Aarohi or the responsible user) before generation. Approval of a concept is not approval of text on image.
- Use only the exact approved copy — no rewording, no extra words, no added hashtags or CTAs on the image.
- Keep it minimal and legible: one short line reads as design; stacked lines read as AI.
- A clean no-text variant of every text-bearing image is required before approval. The text version ships only alongside its clean variant, so scheduling can fall back if rendering drifts.
- Record the approval (who, when, exact copy) in the asset record; unapproved text on image blocks publish.
- If the rendered text drifts from the approved copy in any way — spelling, spacing, glyph shape — the image fails and must be regenerated or the text moved to the caption / reel-native text layer.

## 3. Visual quality checks (each one must pass)

- Composition: subject placement, framing, and negative space serve the story; no awkward crops, cut-off limbs, or cluttered edges.
- Anatomy: hands, fingers, limbs, teeth, eyes, and reflections are plausible and correctly formed; no duplicated or fused features.
- Skin texture: natural pores and tone variation; plastic-smooth, waxy, or over-blended skin is a reject.
- Lighting: consistent direction, color temperature, and shadow logic across the scene; no impossible glow or halo edges.
- Realism: fabric, hair, props, and background behave physically; the image reads as a photograph, not a render, unless a stylized look was explicitly approved.
- Artifacts: no oversharpening halos, compression mush, ghosted edges, duplicated objects, or watermark-like smudges.
- Relevance: subject, setting, wardrobe, and props match the brief and the caption; the image supports the caption rather than repeating or contradicting it.
- Resolution: output meets the platform spec (minimum 1080px on the short edge for feed; 1080x1920 for reels), is sharp at 100% zoom, and survives the platform's compression without visible degradation. Model selection and resolution are documented in the asset record.

## 4. Approval checklist (review gate)

1. Image is text-free by default; any text on image has a recorded, explicit approval and an exact-copy match.
2. Every text-bearing image has a clean no-text variant attached.
3. All §3 quality checks pass.
4. Image has no unintended text or AI artifacts (per AAR-12 pre-publish check).
5. Caption is concise, natural, and relevant; CTA is specific and optional; disclosure and hashtags live in the caption.
6. Model selection and output resolution are documented in the asset record.

One unchecked item = not approved. Rejection feedback must name the failing section and the specific defect so the next generation brief can fix it.
