---
name: Create an interviewer and ingest candidates
description: Stand up a HeyMilo AI interviewer (job posting) with questions, activate it, then push candidates into its agentic workflow.
api: openapi/heymilo-openapi-original.json
operations: [createPosting, createQuestion, listQuestions, activatePosting, ingestCandidate, ingestCandidatesBulk, ingestCandidateAsync]
---

# Create an interviewer and ingest candidates

Use the HeyMilo Public API (base `https://api.heymilo.ai`) to create an AI interviewer and screen candidates end-to-end.

## Auth & conventions
- Send `X-API-KEY: <your key>` on every request. One key = one workspace.
- Rate limit: 300 requests/minute per key; back off on `429`.
- No idempotency key exists — dedupe candidates before ingest (see the ATS-sync skill), or use the async variants and track the returned id.
- Errors come back as `{ "error": { type, code, message } }`; `422` returns a `detail[]` list of validation failures.

## Steps
1. **Create the interviewer.** `createPosting` (`POST /api/v2/postings`) with the title, root-level configs (company/job overview, language, interviewer name), and the `agentic_workflow` (e.g. `resume`, `conversational_sms`, `web_interview`). It returns the new `posting_id`, URLs, and a full posting receipt.
2. **Add questions/criteria.** `createQuestion` (`POST /api/v2/postings/{posting_id}/questions`) once per question; the `modality` field selects the type (`voice`, `sms`, `form`, `resume_eligibility`, `resume_scoring`, `voice_tags`). Confirm with `listQuestions`.
3. **Activate.** `activatePosting` (`POST /api/v2/postings/{posting_id}/activate`) so it begins accepting candidates. It must have a valid workflow configuration.
4. **Ingest candidates.**
   - One at a time: `ingestCandidate` (`POST /api/v2/postings/{posting_id}/candidates`) → returns interview id, interview URL, and a candidate receipt.
   - In bulk: `ingestCandidatesBulk` (`POST /api/v2/postings/{posting_id}/candidates/bulk`).
   - For large jobs use `ingestCandidateAsync` / `ingestCandidatesBulkAsync` and poll the returned ingestion id.

## Next
Register a webhook for `interview_completed` / `report_available` (see the webhooks skill) instead of polling.
