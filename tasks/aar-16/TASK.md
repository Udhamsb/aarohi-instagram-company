---
name: "Use Sogni API for video generation using best model available"
assignee: "chief-of-staff"
project: "onboarding"
---

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

   API = "https://
