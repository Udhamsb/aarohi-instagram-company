# Continuation Summary

- Issue: AAR-16 — Use Sogni API for video generation using best model available
- Status: done
- Priority: medium
- Current mode: review
- Last updated by run: af3b59bd-eec4-4a4e-b1fa-471ee225c374
- Agent: Chief of Staff (hermes_gateway)

## Objective

SOGNI\_API\_KEY \= fc6526ed-9b9e-4711-9d8e-3ea975140679
Use Sogni API for video generation using best model available

for more reference and steps&#x20;
First render in five minutes

One key and one base URL cover every model in the catalog. Three steps.

1. 1
   ## Get your API key
   Ready, Udhamsb — this key is yours:
   `fc65••••••••••••0679`revealcopy
   `export SOGNI_API_KEY=…` and every example below just works.
   Sogni issues **one key per account**, created the moment you ask for it. Account creation is free. Free Spark has account and model eligibility rules; do not assume it funds the API examples below.
   Keep it in an environment variable; every example below reads `SOGNI_API_KEY`. You can also manage the key at [dashboard.sogni.ai](https://dashboard.sogni.ai/api-key).
2. 2
   ## First image — check funding
   This Z-Image Turbo example requires eligible funding. Check your account and the current estimate before submitting it. For restricted-free API use, start with the agent guide. Install the SDK with `npm i @sogni-ai/sogni-client`, or go pure REST with the workflow endpoint.
   JavaScriptcurlPython
   copy

   ```
   import os, time, requests
[truncated]

## Acceptance Criteria

No explicit acceptance criteria captured.

## Recent Concrete Actions

- Run `af3b59bd-eec4-4a4e-b1fa-471ee225c374` finished with status `succeeded` at 2026-09-22T07:38:00.212Z.
- AAR-16 is closed.

Verified: Seedance 2.5 completed a 5.056-second 1280×720 H.264/AAC render with native audio. The durable board attachment is 5,118,940 bytes and its SHA-256 matched after re-download. The recorded estimate and actual charge matched: 300.456 Spark ($1.50228).

Important: the verified video is a golden retriever with a bubble, not the approved Aarohi morning-chai creative. It is a successful API capability test, not publishable Aarohi content.

AAR-20 is active for a corrected render and requires confirmation of the second render charge before submission.

## Files / Routes Touched

- No file or route paths were detected in the captured run summary.

## Commands Run

- Heartbeat run `af3b59bd-eec4-4a4e-b1fa-471ee225c374` invoked adapter `hermes_gateway`.
- Detailed shell/tool commands remain in the run log and transcript.

## Blockers / Decisions

- No new blocker was recorded by the latest run.

## Next Action

- Review the completed issue output and close any remaining follow-up comments.