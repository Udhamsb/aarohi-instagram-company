# Continuation Summary

- Issue: AAR-19 — Generate and QA first Sogni video using selected model
- Status: done
- Priority: medium
- Current mode: review
- Last updated by run: 746fa58c-e53d-455c-9226-c320001453bc
- Agent: AI Visual Producer (hermes_gateway)

## Objective

Execute the first Sogni API video render after a creative brief arrives. Current catalog validation identifies Seedance 2.5 (Creative Agent selector seedance2-5) as the current storyboard-default premium model; use a 5-second 720p native-audio text-to-video test unless the approved brief requires otherwise. Query and record the live cost estimate before submission; submit with confirm_cost=true; poll to terminal status; save the resulting MP4 outside the ephemeral 24-hour URL and post the durable asset location, workflow ID, status, model, resolution, duration, and cost. Do not copy or expose credentials. The parent task contains the supplied credential; use a managed secret/env injection rather than putting it in comments, files, commands, or logs. If no managed secret is available, report the exact secure-configuration blocker here without attempting a render.

## Acceptance Criteria

No explicit acceptance criteria captured.

## Recent Concrete Actions

- Run `746fa58c-e53d-455c-9226-c320001453bc` finished with status `succeeded` at 2026-09-22T07:37:07.087Z.
- AAR-19 closed done. The first Sogni API video render was executed, QA-passed, and durably delivered.

Render: Seedance 2.5 (selector seedance2-5), 5s text-to-video with native audio, 1280×720 @ 24fps, h264 + AAC. Workflow wf_durable_workflow_96549bad-a72c-48dd-bb1c-dec23bb0e1e9 reached status completed in ~3.5 minutes.

Cost: live estimate recorded pre-submission via socket.sogni.ai (300.456 Spark / $1.50228, premium coverage 394.997 confirmed first); submitted with confirm_cost=true and a persisted idempotency key; actual billed matched exactly — 300.456 Spark ($1.50228), settlement tx 1790062072466-0.

QA: three sampled frames match the brief (puppy, bubble lands on nose and pops, sunlit room, clean identity continuity), zero embedded text/watermarks, no visible artifacts; native audio verified non-silent (AAC stereo, max −11.1 dB); container 5.06s. Mechanical self-QA only, per the disclosure-QA skill's second-party rule.

Durable asset (vendor URL is signed/48h): MP4 + QA report uploaded as AAR-19 board attachments and byte-verified on re-download — aarohi_seedance25_5s_720p.mp4 (attachment 8861ad08-89ab-400e-80d1-2a020ae5bb3d, sha256 aab44875…d1907e5) and AA
[truncated]

## Files / Routes Touched

- No file or route paths were detected in the captured run summary.

## Commands Run

- Heartbeat run `746fa58c-e53d-455c-9226-c320001453bc` invoked adapter `hermes_gateway`.
- Detailed shell/tool commands remain in the run log and transcript.

## Blockers / Decisions

- No new blocker was recorded by the latest run.

## Next Action

- Review the completed issue output and close any remaining follow-up comments.