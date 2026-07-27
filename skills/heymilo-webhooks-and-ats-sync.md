---
name: Subscribe to interview events and sync candidates to the ATS
description: Register HeyMilo webhooks for the interview lifecycle, then resolve and push scored candidates back into a connected ATS (Bullhorn, Avionté).
api: openapi/heymilo-openapi-original.json
operations: [createWebhook, listWebhooks, resolveAtsCandidate, pushAtsCandidate, getAtsPushStatus, listAtsConnections]
---

# Subscribe to interview events and sync candidates to the ATS

Event-driven integration flow over the HeyMilo Public API (base `https://api.heymilo.ai`).

## Auth & conventions
- `X-API-KEY: <your key>` on every request (same key for webhook and ATS endpoints).
- Rate limit 300/min; handle `429`.
- ATS push/resolve currently support **Bullhorn** and **Avionté** only.

## Steps
1. **Register a webhook.** `createWebhook` (`POST /api/v2/webhooks`) with `posting_id`, destination `url`, `event_type`, and optional `http_method` (`post` default, or `get`). Event types: `interview_started`, `interview_completed`, `report_available`. Verify with `listWebhooks`.
2. **Confirm ATS connections.** `listAtsConnections` (`GET /api/v2/ats/connections`) to see which ATS integrations are configured for the workspace.
3. **On `report_available`, resolve first.** `resolveAtsCandidate` (`POST /api/v2/ats/candidates/resolve`) by email or ATS candidate id to decide whether to update an existing record or create a new one — this is the dedupe step (the API has no idempotency key).
4. **Push the candidate.** `pushAtsCandidate` (`POST /api/v2/ats/candidates/push`). If `candidate.ats_candidate_id` is null a new ATS record is created. Returns a queue `item_id`.
5. **Poll the push.** `getAtsPushStatus` (`GET /api/v2/ats/candidates/push/{item_id}`) until the queued push completes.

## Notes
`report_available` fires seconds-to-minutes after `interview_completed`; drive ATS writes off `report_available` so scores/transcripts are ready.
