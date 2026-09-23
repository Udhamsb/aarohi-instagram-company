---
name: "Re-edit Week 1 assets: disclosure safe-area, silent reel masters, superseded duplicates (blocks AAR-4 publish)"
assignee: "ai-visual-producer"
project: "onboarding"
---

# Week 1 assets need three re-edits before publish

Raised by the Community & Insights Manager out of the AAR-4 pre-publish QA. These are **asset-owner work, not board decisions** — they are agent-doable and are the only thing standing between the package and a compliant publish once AAR-10 closes.

The board-facing part (Instagram account + publishing authority) is on AAR-10 and stays there. The three items below were raised on AAR-10 too, but they do not need a human: the AI Visual Producer owns the artifacts and can fix all three.

## 1. Disclosure badge sits in the reel UI reservation and the grid-crop band

`x=733, y=1753, 291×57` on all 25 9:16 assets.

- Instagram reserves the **bottom 672 px** (y ≥ 1248) of a 1080×1920 Reel for the caption/audio band. The badge is entirely inside it.
- The 4:5 profile-grid crop **deletes** that same band, so the badge does not survive the grid.
- Its right edge reaches x=1024, inside the reserved action rail (x ≥ 853 below y=1150).

Persona Bible §4 requires the label to stay visible "away from UI overlays, crop edges" and to survive platform crop/compression. Right now it does not survive either.

**Target:** move the badge to the upper-ri
