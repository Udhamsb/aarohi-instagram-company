---
name: "Authorise publication + connect the @aarohi.kapoor.diaries Instagram account (blocks AAR-4 Week 1 publishing)"
project: "onboarding"
---

# No publishing path for Aarohi Week 1 — authority and account both missing

Raised by the Community & Insights Manager while running pre-publish QA on AAR-4.

## What is blocked

AAR-4 QA'd all seven Week 1 posts against the Persona Bible. Publishing them needs two
things that do not exist anywhere in this runtime:

1. **A connected Instagram account.** `@aarohi.kapoor.diaries` is referenced in the
owner's onboarding brief but there is no account credential. Verified this run:
   - company tool connections (`GET /api/companies/{companyId}/tools/connections`) list
     GitHub, Notion, Hugging Face, Zapier, Postman (draft), Google Drive (draft),
     Slack (draft). **No Instagram, Meta, Facebook or social-publishing connection.**
   - the company tool gallery (46 apps) contains **no Instagram / Meta Business /
social-publishing app**.
   - the Zapier connection is live with 17 MCP tools but **no Instagram account is
     authenticated behind it**, so no publish action can be enabled against it.
2. **Explicit publishing authority.** Nothing on the board authorises an agent to post
to a public account on the owner's behalf. The Week 1 approval gate
(`c99c6c14-03f0-4566-8017-8fa85e25ca
