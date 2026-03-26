# Deal Desk AI

**Post-call intelligence for GTM teams — powered by Claude.**

Paste a sales call transcript. Get back a structured intelligence report in seconds: deal summary, objections raised, next steps, risk flags, and a ready-to-send follow-up email.

Built to eliminate the 20 minutes every rep wastes after every call turning notes into CRM entries and follow-up drafts.

---

## Live Demo

🔗 [deal-desk-ai.vercel.app](https://deal-desk-ai.vercel.app)

A sample Bridgit sales call transcript is pre-loaded. Hit **Analyze Call** to see it run — or paste your own transcript to analyze a real call.

---

## What It Does

| Output | Description |
|---|---|
| **Deal Summary** | 2–3 sentence read on the call: who, what problem, where the deal stands |
| **Objections Raised** | Every concern the prospect surfaced, extracted and listed |
| **Next Steps** | Concrete actions with owners, ready to drop into your CRM |
| **Risk Flags** | Deal risk signals the rep may have missed |
| **Follow-Up Email** | Complete, ready-to-send email — one click to copy |

---

## Stack

- **Claude** (claude-sonnet-4-20250514) via Anthropic API
- Vanilla HTML/CSS/JS — no framework, no dependencies
- Vercel serverless function as API proxy (key never exposed client-side)
- Deployed on Vercel

---

## Architecture

```
Browser → /api/analyze (Vercel serverless) → Anthropic API → structured JSON → rendered UI
```

The API key lives in Vercel's environment variables. It never touches the client.

---

## Related Projects

- [meeting-to-jira-pipeline](https://github.com/Moezusb/meeting-to-jira-pipeline) — automated action-item extraction from meeting transcripts into structured Jira tickets
- [oracle-v2](https://github.com/Moezusb) — AI support triage engine: classify, route, and prioritize inbound tickets
- [mathvoice](https://mathvoice-web.vercel.app) — bilingual EN/FR voice math tutor for Grade 1–3

---

Built by [Mohamed Bah](https://github.com/Moezusb)
