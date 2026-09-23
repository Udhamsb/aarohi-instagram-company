# AAR-4 — can Zernio MCP publish Aarohi Week 1?

**[AAR-33 hard rule — applied 2026-09-22. This block supersedes the on-image disclosure requirements in the text below.]** The on-image `AI-generated` badge/overlay is **retired for good**: never request it in a prompt, never render it, never burn, composite or overlay disclosure text into the frame, and never require, measure or QC-gate it on a delivered asset. An asset carrying an on-image `AI-generated` mark is now a **FAIL**. Disclosure moves entirely outside the frame: the plain-language note stays in the **caption** and the platform AI-content label (Instagram `isAiGenerated: true` + the profile-level "AI-generated profile" label) stays enabled at publish — both remain mandatory. Source of truth: AAR-33 document `disclosure-policy`.

Lines above that this block supersedes (they stand as history, not as instructions):
- line 70: `3. **Instagram's own AI label.** Zernio supports `isAiGenerated: true`, which makes`
- line 71: `Instagram label the post as containing AI-generated media (feed, Reels, Stories,`

Amended by the Chief of Staff on AAR-33 at the board's direct instruction. Nothing else in this document changes.

**Question asked (board owner, 2026-09-22T05:15Z):** "Can we use zernio mcp for this"

**Answer: yes — it is a working path and the best one currently available, but it
does not by itself remove the blocker. It replaces "there is no way to connect an
Instagram account from this runtime" with "a connection path exists, and the
owner must sign in to Zernio once and connect the account."**

Everything below was checked in this run, not assumed.

## What Zernio's MCP server actually is (verified)

| Check | Result |
|---|---|
| Endpoint | `https://mcp.zernio.com/mcp` — responds, `Zernio MCP Server v1.2.1` |
| Transport | streamable HTTP (`/mcp`), legacy SSE also served |
| Health | `GET /health` → `{"status":"healthy"}` |
| Auth | OAuth 2.1 + PKCE. Unauthenticated `initialize` and `tools/list` both return **401** with `WWW-Authenticate: Bearer resource_metadata=…`, i.e. discovery works correctly |
| Dynamic client registration | supported — `POST https://zernio.com/api/oauth/register` returned **201** with a client id |
| Authorization server | `https://zernio.com/oauth/authorize`, token at `/api/oauth/token` |
| Scopes exposed | `posts:read`, `posts:write`, `accounts:read`, `accounts:write`, `analytics:read`, `messaging:write`, … |
| Instagram support | yes — feed posts, carousels, Stories, **Reels**, analytics, comments and DMs |
| Agent path | API key as `Authorization: Bearer $ZERNIO_API_KEY` for headless agents that cannot open a browser |
| Tools | ~50 visible + `search_tools` / `call_tool` for the long tail |

## It is not connected here yet (verified)

- **Not in the Paperclip tool gallery or connections.** The company gallery has 46
  apps and no Zernio (no Instagram/Meta/social publisher either); the company's 7
  tool connections are GitHub, Notion, Hugging Face, Zapier, Postman/Google
  Drive/Slack (draft). So Zernio cannot be added through Paperclip's app connection
  flow today — it would be a Hermes-side MCP server, not a Paperclip connection.
- **Not in the Hermes MCP catalog.** 73 catalog entries, no Zernio, so it is a
  manual `hermes mcp add`, not a one-click install.
- **No MCP server is configured at all** in this profile (`hermes mcp list` →
  "No MCP servers configured").
- **No Zernio credential exists** anywhere: not in the environment, not in the
  profile `.env`, not in the instance `.env` or the Paperclip secrets dir.

## What I tried, and exactly where it stops

```
hermes mcp add zernio --url "https://mcp.zernio.com/mcp" --auth oauth
  → Starting OAuth flow for 'zernio'...
  → OAuth error: non-interactive environment and no cached tokens found.
    Run `hermes mcp login zernio` interactively first to complete initial authorization.
  → Failed to connect: HTTP 401 from POST https://mcp.zernio.com/mcp
  → Save config anyway? [y/N] → declined
```

`config.yaml` is unchanged — I deliberately did not save a server entry that would
fail its connection probe on every future startup. The OAuth grant needs a human at
a browser (or the device-code flow), and this run has no interactive session.

## What it would fix, if connected

1. **The Instagram account gap (AAR-10 item 1).** Connect
   `@aarohi.kapoor.diaries` through Zernio's OAuth, then `accounts_list` returns its
   `accountId` and `posts_create` can publish to it. This is the whole blocker on
   AAR-4 and Zernio is a supported way to clear it.
2. **Rights-safe audio, properly.** The five masters have no audio track at all.
   Zernio exposes Instagram's licensed audio catalogue
   (`search-instagram-audio` → `audioId`) and `platformSpecificData.audioConfiguration`
   attaches a licensed track to a Reel. That is a cleaner answer to the package's
   audio lane than shipping silent reels — **but it requires
   `loginMethod=facebook_login`**; accounts connected by Instagram Login get a 400
   `instagram_audio_requires_facebook_login`. So connect through Facebook Login if
   the catalogue audio matters.
3. **Instagram's own AI label.** Zernio supports `isAiGenerated: true`, which makes
   Instagram label the post as containing AI-generated media (feed, Reels, Stories,
   carousels). This is a useful belt-and-braces signal, **but it does not satisfy
   Persona Bible §4**, which requires a readable on-asset disclosure that survives
   platform crop — the badge-placement defect from the QA still has to be fixed on
   the files.

## What it does not fix

- **Publishing authority.** Connecting Zernio is an account-credential action, not
  an authorisation to post to a public account on the owner's behalf. That still has
  to be granted explicitly.
- **§4 badge placement.** Zernio moves nothing on the asset. The badge at
  `x=733, y=1753` is still 100% inside Instagram's caption band and 100 % inside the
  4:5 grid-crop band on those files.
- **The superseded attachments** under live filenames on AAR-3.
- **The Instagram account type.** Instagram requires a **Business or Creator**
  account for API publishing; a personal account cannot post this way. If
  `@aarohi.kapoor.diaries` is personal it must be converted first.

**Correction to my own earlier claim.** In the previous run I wrote that Instagram
"treats a silent 9:16 MP4 as a photo/clip upload, not a Reel, so the Reels tab
doesn't apply." That was stronger than my evidence. What I verified is: the masters
carry no audio stream and no voiceover, and Meta's Reels spec lists an **AAC audio
codec**, so the audio lane is non-compliant either way. Whether Meta rejects a
container built from a track-less MP4 outright is not something I tested. The
defect stands (no voiceover, non-compliant audio); the mechanism I asserted does
not, and I am not repeating it as fact.

## Cost

Zernio bills per connected account, all features included: **1–2 accounts free, no
card**, then $6/account/month for 3–10. Connecting one Instagram account is free.
That is an owner decision, not mine to make.

## Exact steps to unblock, and who owns each

| # | Step | Owner |
|---|---|---|
| 1 | Create/confirm a Zernio account at zernio.com (free tier covers 1 account) | Board owner |
| 2 | Confirm `@aarohi.kapoor.diaries` is a **Business or Creator** account; convert if personal | Board owner |
| 3 | `hermes mcp add zernio --url https://mcp.zernio.com/mcp --auth oauth`, then complete the browser sign-in — or set `ZERNIO_API_KEY` in the profile `.env` for headless use | Board owner (needs a browser); I can run the CLI once the grant is offered |
| 4 | Connect the Instagram account; choose **Facebook Login** if the licensed catalogue audio is wanted | Board owner |
| 5 | Grant explicit publishing authority for this account and agent | Board owner |
| 6 | Fix the §4 badge placement (`x=700, y=1210, 291×57` clears the caption band, the action rail and the 4:5 trim on all 25 assets) | Asset owner |
| 7 | Delete or rename the superseded 18:47 attachments on AAR-3 | Producer |
| 8 | Publish, then re-measure the badge off the published asset | Me, on AAR-4 |

Steps 1–5 are the AAR-10 blocker. Steps 6–7 are the re-edits. Only then does AAR-4
resume.
