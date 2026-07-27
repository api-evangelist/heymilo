---
name: Review a candidate pipeline and pull interview results
description: Read HeyMilo interviewer stats, list candidates with scores, and pull full interview data and transcripts for hiring decisions.
api: openapi/heymilo-openapi-original.json
operations: [listPostings, getPostingStats, listCandidates, getInterviewData, getInterviewMetadata]
---

# Review a candidate pipeline and pull interview results

Read-only reporting flow over the HeyMilo Public API (base `https://api.heymilo.ai`). The hosted MCP server (`https://mcp.heymilo.ai/mcp`) exposes these same GET operations as natural-language tools.

## Auth & conventions
- `X-API-KEY: <your key>` on every request.
- List endpoints paginate with `limit` + `starting_after` (cursor); filter with `created_after` / `created_before`.
- Rate limit 300/min; handle `429`.

## Steps
1. **Find the interviewer.** `listPostings` (`GET /api/v2/postings`) to locate the `posting_id`. Use `listPostingSummaries` for a lightweight id/title/name list.
2. **Get aggregate health.** `getPostingStats` (`GET /api/v2/postings/{posting_id}/stats`) → total candidate count, completed interview count, average interview and resume scores.
3. **List candidates with progress.** `listCandidates` (`GET /api/v2/postings/{posting_id}/candidates`) → paginated candidates, each with workflow progress, scores, and agent summaries. Page with `starting_after`.
4. **Pull a full interview.** `getInterviewData` (`GET /api/v2/interviews/{interview_id}/data`) → per-agent results (scorecard, transcript, resume evaluation, SMS screening, form results). Returns status `not_ready` if the candidate has not finished.
5. **Read custom tags.** `getInterviewMetadata` (`GET /api/v2/interviews/{interview_id}/metadata`) for any key-value metadata your systems attached.

## Notes
Scores are produced after AI analysis; if `getInterviewData` returns `not_ready`, wait for the `report_available` webhook rather than polling tightly.
