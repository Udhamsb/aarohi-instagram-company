**[AAR-34 hard rule — applied 2026-09-22. This block supersedes the daily-format specifications in the text below.]** The Aarohi daily plan changes to **image carousel only**: one post per day, a **4:5 portrait carousel of stills (1080×1350, 4–6 slides)**, and **one outfit worn across every slide of that day's carousel**, rotating day to day from the AAR-7 §4 approved wardrobe list. Reels, video posts and single-static posts are **discontinued as daily formats** — they are not a default deliverable and must not be produced speculatively. Reel scripts, video prompts, silent-master and audio-stream requirements, 9:16 masters and the reel-format QC gates in the text below stand as history and as the QC basis only if the board explicitly re-authorises a video asset; they are not current instructions. Everything else is unchanged: text-free frames (AAR-12 / AAR-13 / AAR-25 zero-text), **no on-image AI-generated disclosure** (AAR-33 `disclosure-policy`), the mandatory caption disclosure line plus the platform AI-content label, the locked identity and modesty rules, and the billable-render gate. Source of truth: AAR-34 document `daily-format-standard`.

Lines below that this block supersedes (they stand as history, not as instructions):
- line 98: `| 1 | Kurta + relaxed trousers | Tue (lifestyle carousel) · Fri (lifestyle static) |`
- line 101: `| 4 | Relaxed top + straight trousers | Fri (lifestyle static) · general daytime |`
- line 103: `| 6 | Fitness — opaque crew tee + full-length track pants, sports bra never visible | Mon · Thu · Sun (fitness`
- line 157: `- [ ] **B10** Every carousel slide or reel shot that appears onscreen complies; **no undisclosed cutaway**.`
- line 200: `Frames that need **new scene photography** — the five reel b-roll sets, and any genuinely`

Amended by the Chief of Staff on AAR-34 at the board's direct instruction. Nothing else in this document changes.

# Aarohi — Reference-Pack Criteria & Preflight Checklist  v1.0

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 14: `| §7.1 primary face anchor + supporting angles, **with visible `AI-generated` disclosure** | `AAROHI_REFERENCE_PACK_v2_F`
- line 37: `each band, alongside the `AI-generated` badge. The binding rule:`
- line 43: `preflight** in §5 applies and the `AI-generated` badge must be verifiably present on that crop.`
- line 63: `| RC-8 | Disclosure | Exact lower-right string `AI-generated`, high contrast, readable, surviving crop and compression. `
- line 116: ``AI-generated`. Pixel-exact match proves the exact hyphenated string is burned in — no OCR.`
- line 149: `- [ ] **C1** The asset carries its own `AI-generated` badge, verified by Stage A on that exact file.`
- line 164: `* **Disclosure breach** — `AI-generated` missing, obscured, cropped, illegible, low contrast, or not on`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Owner:** Creative Director, Aarohi_Instagram_company
**Issue:** AAR-7 (re-issued reference pack for AAR-3)
**Supersedes:** the §7 handoff rows in `AAROHI_PERSONA_BIBLE.md` §7 for the reference pack itself.
**Status:** Locked approval standard. Producers must not reinterpret the **non-negotiable** rows.

---

## 1. What the approved reference pack now contains

| §7 slot | Deliverable file | Status |
|---|---|---|
| §7.1 primary face anchor + supporting angles, **with visible `AI-generated` disclosure** | `AAROHI_REFERENCE_PACK_v2_FACE_BODY_SHEET.png` | **RE-ISSUED v2.1** — disclosure band appended |
| §7.1 identity anchor, face / hair / expression | `AAROHI_REFERENCE_PACK_v2_CHARACTER_SHEET.png` | **RE-ISSUED v2.1** — disclosure band appended |
| §7.2 hair-detail reference (long open hair) | "Hair Variations" row, character sheet v2.1 | Supplied — see the **hair-only** rule in §3 below |
| §7.3 wardrobe / modesty reference | `AAROHI_WARDROBE_REFERENCE_v1.png` | **NEW** — 8 approved silhouettes + usage rules |
| §7.4 persona bible + fixed exclusion block | `AAROHI_PERSONA_BIBLE.md` | Supplied |
| Machine evidence for the above | `qa_reference_pack.json` | 3 / 3 PASS |

**How the disclosure was applied — byte-preserving, not painted over.**
The original sheet pixels are **not modified**. The §7.1 disclosure is appended as a footer band
below the sheet, so no panel, label or face is covered. Verified by hashing the original region of
each re-issued file against the owner-supplied source in `qa_reference_pack.py` (check
`source_integrity`): **byte-identical on both sheets**.

> **Why not burned into the original pixels?** Covering the sheet's own footer/caption areas would
> destroy the reference content the pack exists to carry. Appending preserves both the reference and
> the disclosure. If the owner requires the label *inside* the original sheet art instead, that is a
> one-line change to the production script — but it will cover part of the existing sheet.

---

## 2. §7.1 handling decision on the anchor sheets (explicit, recorded)

The anchor sheets are **INTERNAL ANCHOR SHEETS — NOT FOR PUBLICATION**. That string is burned into
each band, alongside the `AI-generated` badge. The binding rule:

* The re-issued anchor sheets (`*_REFERENCE_PACK_v2_*.png`) may be used **internally** as the identity
  anchor for generation, and may be attached to internal issues/threads as reference material.
* They must **never** be published, posted, story-posted, or reposted **on any outward-facing surface**.
* If any sheet, or any crop of one, is ever intended to go outward-facing, the **§7.1 outward
  preflight** in §5 applies and the `AI-generated` badge must be verifiably present on that crop.

This closes the §7.1 gap in the reference pack itself. It does **not** relax §4 for delivered assets:
every published frame still carries its own badge (§4), which is unchanged.

---

## 3. Reference criteria (pass conditions)

A reference asset is approved only if **every** row below is true.

| ID | Criterion | Pass condition |
|---|---|---|
| RC-1 | One consistent person | Same fictional North Indian woman, 22–26, in every panel. No second face, no blended identity. |
| RC-2 | Complexion | Wheatish with natural even texture; neither lightened nor darkened between panels; no beauty-filter plasticity. |
| RC-3 | Hair | Long, open, dark, **visibly down** — never tied, braided, clipped, bunned, ponytail or updo. |
| RC-4 | Identity markers | Small centred maroon bindi visible where the forehead is in frame; silver jhumkas visible where the ears are in frame (natural hair/angle occlusion allowed). |
| RC-5 | Wardrobe | Only silhouettes listed in `AAROHI_WARDROBE_REFERENCE_v1.png`. Opaque, secure, non-body-emphasising. Chest, midriff, hips and upper thighs covered. |
| RC-6 | Framing and setting | Eye-level or neutral; medium/waist-up/seated/walking/reading; plausible public or domestic, non-intimate. No body-focused crop. |
| RC-7 | Posture and expression | Natural, comfortable, everyday. No reclining, arched back, sultry gaze, or body display. |
| RC-8 | Disclosure | Exact lower-right string `AI-generated`, high contrast, readable, surviving crop and compression. |
| RC-9 | Anchor provenance | Every generated frame names its anchor ID and the anchor crop's SHA-256, so continuity is provable rather than asserted. |
| RC-10 | Non-sexualised copy | Caption, on-screen text, hashtags and CTA contain no sexualised, flirtatious or appearance-led engagement language. |

### The hair-only rule (non-negotiable)

The character sheet's **"Hair Variations — Open Hair (default)"** panel is a **HAIR-ONLY** reference.
That panel shows a thin camisole strap over a bare shoulder. That garment fails Persona Bible §2 and §5
and is **not an approved silhouette**.

* Crop head and hair from that panel. **Never inherit its garment.**
* No generation may anchor on that panel and carry its garment into frame.
* This rule is burned onto the re-issued character sheet band so it travels with the file.

---

## 4. Approved wardrobe — the Week 1 calendar may use these and nothing else

Full specification, per-item reject lists and usage rules: `AAROHI_WARDROBE_REFERENCE_v1.png`.

| # | Silhouette | Where the Week 1 calendar uses it |
|---|---|---|
| 1 | Kurta + relaxed trousers | Tue (lifestyle carousel) · Fri (lifestyle static) |
| 2 | Salwar (kurta + salwar) | Standing festive / home slot |
| 3 | Secure-drape sari (double-pinned pallu, sleeved high-neck blouse, full petticoat) | Festive / occasion slot |
| 4 | Relaxed top + straight trousers | Fri (lifestyle static) · general daytime |
| 5 | Long cardigan layer, over an approved base (1 or 4) | Wed (fashion, desk-to-dinner) |
| 6 | Fitness — opaque crew tee + full-length track pants, sports bra never visible | Mon · Thu · Sun (fitness reels) |
| 7 | Festive kurta + secure dupatta (both shoulders pinned) + sneakers | Sat (fashion, festive kurta + sneakers) |
| 8 | Accessory and jewellery lock: jhumkas, bindi, hair open, one small bag | Every post |

**Any garment not on this list is unapproved.** A frame showing an unapproved garment is a §2/§5
modesty breach and is **REJECT — regenerate**, regardless of how good the frame otherwise is.

**Scope honesty.** `AAROHI_WARDROBE_REFERENCE_v1.png` is a **garment specification sheet**, not
silhouette photography. No image-generation provider is reachable from the agent runtime (no image
model credential; the only configured model provider is a text LLM — tracked on AAR-8). So this sheet
defines *what may be worn* with enough precision to generate or shoot from, and the photographic
silhouette reference is deferred to whoever owns AAR-8. It closes the §7.3 governance gap; it does not
by itself produce a rendered full-outfit editorial frame.

---

## 5. Preflight checklist

Run in order. **All boxes must be true.** Any false or uncertain box is
**REJECT — regenerate or re-edit**; a caption disclaimer is never a remedy (Persona Bible §5).

### Stage A — automated (run before a human looks at the file)

`python3 qa_reference_pack.py` → writes `qa_reference_pack.json`. Reference pack currently: **3/3 PASS**.

- [ ] **A1 exact disclosure string.** Badge region bit-matches a template rendered from the literal
      `AI-generated`. Pixel-exact match proves the exact hyphenated string is burned in — no OCR.
      *Current: 0 mismatched pixels on all three files.*
- [ ] **A2 contrast.** Badge contrast ≥ 4.5 on the delivered-asset convention (`(Lmax+5)/(Lmin+5)`),
      with the WCAG 2.1 figure reported alongside. *Current: 7.22:1 delivered convention / 16.48:1 WCAG.*
- [ ] **A3 placement.** Fully inside canvas, lower-right, right and bottom margins ≥ 24 px.
      *Current: right 56 px, bottom 51–139 px.*
- [ ] **A4 phone round-trip.** Re-rendered at 420 px phone canvas width, JPEG q26, re-measured on the
      degraded copy. *Current: 52.0:1 after JPEG on all three, glyph coverage 9.1–13.1 %.*
- [ ] **A5 source integrity** (anchor sheets only). Original sheet region byte-identical to the
      owner-supplied source. *Current: byte-identical on both sheets.*
- [ ] **A6 badge/text separation.** No text ink inside a 30 px guard band immediately left of the badge
      plate. *Current: 0 dark pixels on all three.*
- [ ] **A7 band margins.** No appended text ink inside a 24 px hard margin, the declared full-bleed
      accent hairline excepted. *Current: 0 dark pixels on all three.*

### Stage B — visual (human or vision review, at full size)

- [ ] **B1** Face unmistakably matches the approved Aarohi reference; no face drift, no identity blending.
- [ ] **B2** Reads as a North Indian woman aged 22–26 with wheatish, naturally textured skin.
- [ ] **B3** Hair is completely open/down — not tied, braided, clipped up, bunned, ponytail or updo.
- [ ] **B4** Small maroon bindi visible if the forehead is visible.
- [ ] **B5** Silver jhumkas visible if the ears are visible, subject only to natural hair/angle occlusion.
- [ ] **B6** Wardrobe is on the §4 approved list, opaque, secure and non-body-emphasising; chest,
      midriff, hips and upper thighs covered.
- [ ] **B7** Pose, expression, angle, crop, motion and setting are everyday and non-suggestive.
- [ ] **B8** Caption, on-screen text, hashtags and CTA carry no sexualised, flirtatious or
      appearance-led engagement language.
- [ ] **B9** No panel inherits the `hair_open` camisole garment (see the hair-only rule, §3).
- [ ] **B10** Every carousel slide or reel shot that appears onscreen complies; **no undisclosed cutaway**.
- [ ] **B11** Checked at full size **and** in platform preview.

### Stage C — outward-facing preflight (only if the asset leaves the company)

- [ ] **C1** The asset carries its own `AI-generated` badge, verified by Stage A on that exact file.
- [ ] **C2** The asset is not an internal anchor sheet, and no crop of an anchor sheet has been used
      outward-facing without C1 passing on that crop.
- [ ] **C3** Publishing is explicitly authorised by an approved task and the account connection is ready.
      The Creative Director does not publish and does not handle credentials.

---

## 6. Rejection triggers (immediate, no exceptions)

REJECT and regenerate or re-edit if any of these is true:

* **Face drift** — the subject no longer unmistakably matches the approved reference identity.
* **Hair breach** — hair tied, braided, clipped up, bunned, ponytail, updo, or not visibly long and open.
* **Identity marker breach** — bindi or jhumkas absent when their area is visible.
* **Disclosure breach** — `AI-generated` missing, obscured, cropped, illegible, low contrast, or not on
  the visual itself.
* **Modesty breach** — styling, garment (including any garment not on the §4 list), framing, pose,
  setting, animation, edit or copy is sexualised, suggestive, voyeuristic or body-emphasising.
* **Continuity breach** — inconsistent age read, complexion, or hair colour/length; a fashion or beauty
  treatment that breaks the grounded diary identity.

---

## 7. Reproduce the evidence

```
python3 build_reference_pack.py     # rebuilds the 3 reference deliverables from the sources
python3 qa_reference_pack.py        # writes qa_reference_pack.json  → expect 3/3 PASS
```

Sources (owner-supplied, unmodified): `sheet_char.png` (character sheet v2.0),
`sheet_facebody.png` (face & body reference).

---

## 8. Open item carried forward, not hidden here

Frames that need **new scene photography** — the five reel b-roll sets, and any genuinely
full-outfit editorial frame — still need an image-generation provider or a shoot. That is tracked on
**AAR-8**, owned by the Chief of Staff. This reference pack closes the §7.3 governance gap and the
§7.1 disclosure gap; it does not manufacture a generator. The delivered Week 1 stills remain
portrait-led and compliant, as recorded on AAR-3.
