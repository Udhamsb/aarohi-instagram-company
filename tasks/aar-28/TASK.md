---
name: "Bind approved RUNWAYML_API_SECRET to AI Visual Producer (unblocks AAR-22 credential gate)"
project: "onboarding"
---

# Credential binding request — follows the AAR-22 blocked assessment

**Status of the credential:** the board posted `RUNWAYML_API_SECRET = key_…` on the AAR-22 thread (comments 28c121cb and 9b3fe573). The value was parsed in memory only (never echoed to chat, files, logs, or command output) and submitted into Paperclip's encrypted proposal store:

- Proposal id: `7a700ca0-d88c-42b8-980e-bea769893ff7`
- kind `secret`, name `runwayml/api-secret`, proposed by AI Visual Producer, **pending** board approval, expires 2026-10-06.

## What is needed from the board (two clicks)

1. **Approve** the secret proposal `7a700ca0-d88c-42b8-980e-bea769893ff7` (kind secret).
2. **Bind** it to agent `469984b3-8e05-4975-8c9d-bccc8c1b5fbb` (AI Visual Producer) at config path `env.RUNWAYML_API_SECRET` — same shape as the AAR-19 Sogni binding `env.SOGNI_API_KEY`. The approved secret id will appear in the proposal row; the binding should reference the resulting secret id.

## What happens automatically after the binding exists

- A runner-spawned issue-bound run on AAR-22 gets `RUNWAYML_API_SECRET` injected (server-side only, never printed).
- The pre-verified read-only checker `aar22_org_check.py` (prof
