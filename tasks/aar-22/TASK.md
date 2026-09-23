---
name: "Adopt Runway Dev Models for visual generation"
assignee: "ai-visual-producer"
project: "onboarding"
---

Replace the retired Sogni generation workflow with Runway Dev for photo and video work. Selected tool surface: Runway Dev Models, not Model Routers, Characters, or Recipes, because the current need is direct image/video generation. The shared workspace already contains .agents/skills/runway-dev and .agents/skills/runway-dev-models; read both before acting. Follow https://dev.runwayml.com/quickstart.txt and the linked current Runway docs. Inspect the workspace first. If no existing app/integration target exists, recommend the smallest web-app integration and request product direction rather than scaffolding an unspecified product. Use the Runway Dev MCP endpoint https://dev.runwayml.com/mcp only for live account discovery/management; OAuth must be completed by a human in a normal browser and no API key belongs in MCP config. For SDK generation, require a Paperclip-managed RUNWAYML_API_SECRET behind the server boundary; never request or paste it in chat or source. Do not make a billable generation unless explicitly approved after checking current model constraints, credit balance, and pricing. Deliver: verified workspace assessment, selected model endpoint/model based on current docs
