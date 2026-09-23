# Continuation Summary

- Issue: AAR-14 — Apply clean-image generation and QC standard
- Status: done
- Priority: high
- Current mode: review
- Last updated by run: dd0343fa-8d3e-4c2e-bb57-eda334702f70
- Agent: AI Visual Producer (hermes_gateway)

## Objective

Adopt the clean-image generation and quality standard for all new visual assets.

Requirements:
- Use the best available image model through the approved OpenRouter configuration; do not expose or copy credentials.
- Generate clean images with no embedded text by default.
- Include negative constraints that exclude text, letters, logos, watermarks, UI, fake quotes, and irrelevant decorative elements.
- When text is explicitly approved, deliver both the approved-text asset and a clean no-text variant.
- Run a final QC pass for anatomy, identity consistency, lighting, texture, artifacts, relevance, and output resolution before handoff.
- Document the selected model and resolution in each asset handoff.

Use [AAR-12](/AAR/issues/AAR-12#document-visual-copy-template) as the prompt baseline. Record the operational checklist in your issue and mark it done.

## Acceptance Criteria

No explicit acceptance criteria captured.

## Recent Concrete Actions

- Run `dd0343fa-8d3e-4c2e-bb57-eda334702f70` finished with status `succeeded` at 2026-09-22T06:58:24.976Z.
- AAR-14 is closed done, with the standard proven end-to-end rather than just documented.

What happened this run:

- Model selection: probed three OpenRouter image models against the same text-free brief. Selected google/gemini-3-pro-image as the standing default (native 928×1152 4:5, ~$0.14/image); gemini-3.1-flash-image recorded as a budget alternative that passed the same QC; openai/gpt-5.4-image-2 rejected (square-only, 5× latency). Key validated via /api/v1/key and sourced from the profile env at call time only — never exposed or copied.
- Operational checklist: recorded as a comment on AAR-14 — verbatim negative-constraint block, identity/marker locks on anchor crops, clean no-text default, dual-delivery rule for approved text, and the final QC gate (anatomy, identity consistency, lighting, texture, artifacts, relevance, resolution, zero-text check), plus a mandatory rejection loop.
- Evidence: generated a clean variant and an approved-text variant ("Slow mornings, strong starts.") of the same café scene. QC pass 1 caught a real violation in both — a background chalkboard menu with illegible scribbles — so both were rejected, regenerated with explicit backg
[truncated]

## Files / Routes Touched

- No file or route paths were detected in the captured run summary.

## Commands Run

- Heartbeat run `dd0343fa-8d3e-4c2e-bb57-eda334702f70` invoked adapter `hermes_gateway`.
- Detailed shell/tool commands remain in the run log and transcript.

## Blockers / Decisions

- No new blocker was recorded by the latest run.

## Next Action

- Review the completed issue output and close any remaining follow-up comments.