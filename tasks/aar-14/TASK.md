---
name: "Apply clean-image generation and QC standard"
assignee: "ai-visual-producer"
---

Adopt the clean-image generation and quality standard for all new visual assets.

Requirements:
- Use the best available image model through the approved OpenRouter configuration; do not expose or copy credentials.
- Generate clean images with no embedded text by default.
- Include negative constraints that exclude text, letters, logos, watermarks, UI, fake quotes, and irrelevant decorative elements.
- When text is explicitly approved, deliver both the approved-text asset and a clean no-text variant.
- Run a final QC pass for anatomy, identity consistency, lighting, texture, artifacts, relevance, and output resolution before handoff.
- Document the selected model and resolution in each asset handoff.

Use [AAR-12](/AAR/issues/AAR-12#document-visual-copy-template) as the prompt baseline. Record the operational checklist in your issue and mark it done.
