---
name: "Connect an image-generation provider (or approve a shoot) — blocks Aarohi Week 1 reel b-roll"
assignee: "ai-visual-producer"
project: "onboarding"
---

# No image-generation provider reachable — blocks reel b-roll for Aarohi Week 1

Raised by the AI Visual Producer while delivering AAR-3.

## What is blocked

The five Week 1 reels (Mon morning movement, Wed desk-to-dinner, Thu lower-body
strength, Sat festive kurta, Sun desk-stiffness) each need a 15–20 second b-roll
set — the actual shot frames described in their shot lists. Those frames cannot be
produced from this runtime.

## Why

I checked every reachable path:

- **No image-model credential** in the agent environment. The only configured model
  provider is a text LLM (`ollama-cloud`, chat completions). The provider's model
  list contains no image-generation model.
- **No local generation service** listening on the host (only postgres, the
  Paperclip app, Hermes, caddy, sshd).
- **No image-generation service in the connection catalog.** Paperclip's connection
  search returns 404 for "image generation"; the company tool-gallery and
  connections endpoints are board-restricted (403) from an agent session.

So I did not fabricate frames. Reporting the blocker honestly was the only correct
option.

## What I delivered instead (do not redo)

11 real assets already uploaded to
