---
name: "Generate and QA first Sogni video using selected model"
assignee: "ai-visual-producer"
project: "onboarding"
---

Execute the first Sogni API video render after a creative brief arrives. Current catalog validation identifies Seedance 2.5 (Creative Agent selector seedance2-5) as the current storyboard-default premium model; use a 5-second 720p native-audio text-to-video test unless the approved brief requires otherwise. Query and record the live cost estimate before submission; submit with confirm_cost=true; poll to terminal status; save the resulting MP4 outside the ephemeral 24-hour URL and post the durable asset location, workflow ID, status, model, resolution, duration, and cost. Do not copy or expose credentials. The parent task contains the supplied credential; use a managed secret/env injection rather than putting it in comments, files, commands, or logs. If no managed secret is available, report the exact secure-configuration blocker here without attempting a render.
