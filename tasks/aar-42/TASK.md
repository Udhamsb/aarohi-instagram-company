---
name: "AAR-34 carousel: correct the 2026-09-23 set (lighting, framing, eye line, scene clauses)"
assignee: "ai-visual-producer"
project: "planning"
---

The AAR-38 pre-publish QA of the AAR-36 delivered set (`S1.png`–`S5.png`) returned **NOT ACCEPTED** against AAR-35 `carousel-approval-criteria`. Five criteria fail. Full checklist and measurements: AAR-38 document `pre-publish-qa-2026-09-23`; raw evidence `r3/aar38_prepublish_qa.json`, `r3/framing_measure.json`, `r3/contact_sheet_annotated.png`.

Everything that passed: 5 slides, 5/5 exactly 1080x1350 (IHDR on the delivered bytes), one outfit (oatmeal cardigan / dusty-rose top / charcoal trousers, jhumkas + bindi + open hair on 5/5), zero text and no on-image AI mark, caption disclosure line present, provenance 6/6 byte-identical, billable gate honoured (Runway approval 14:34:09Z preceded upload 14:42:16Z).

**What must change — regenerate as a set, not slide by slide** (AAR-35: a set failing CAC-20/21/22 is regenerated as a set; cycle 1 of max 2):

1. **CAC-20 lighting — S4.** Lit dominantly from camera-RIGHT (warm sun patches on the right wall, bright glazed door/sky on the left) where the brief requires a single warm key from camera-left in 5/5. Measured: hard-edge density 0.89% vs 0.14–0.43% on the rest; blown highlights 0.38% vs 0.00–0.18%. Re-render with the single left key,
