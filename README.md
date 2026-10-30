# HeyMilo

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

HeyMilo AI is an agentic recruiting platform for high-volume hiring teams — staffing agencies, corporate recruiters, BPOs, franchises, and data-annotation operations. It combines candidate sourcing from your ATS, conversational SMS and smart-form pre-screening, resume analysis, and live AI voice and video interviews (with built-in cheat detection), then scores and ranks candidates with analytics, reporting, and fully white-labeled workflows. The HeyMilo Public API (v2.0.0, base https://api.heymilo.ai) exposes programmatic control over interviewers (postings), candidate ingestion, interview data and transcripts, questions, webhooks, templates, voices, phone numbers, domains, and ATS push/resolve — authenticated with an X-API-KEY header and rate limited to 300 requests per minute. A read-only hosted MCP server at https://mcp.heymilo.ai/mcp lets any MCP client query candidates, jobs, and interviews in natural language. HeyMilo raised $6M to scale agentic recruiting and is backed by Canaan Partners.

**Areas:** Company · Recruiting · Hiring · Human Resources · Artificial Intelligence · AI Agents · Interviewing · Candidate Screening · Voice AI · Webhook · ATS Integration

## HeyMilo on APIs.io

Everything profiled for HeyMilo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/heymilo/](https://apis.io/providers/heymilo/)** — or go straight to one of the APIs or properties below.

### APIs (18)

- [HeyMilo ATS API](https://apis.io/apis/heymilo/heymilo-ats-api/) — The ATS API from HeyMilo — 4 operation(s) for ats.
- [HeyMilo Candidates API](https://apis.io/apis/heymilo/heymilo-candidates-api/) — Ingest candidates into an interviewer's workflow (sync or async, single or bulk) and list candidates with their progress.
- [HeyMilo Design Template Groups API](https://apis.io/apis/heymilo/heymilo-design-template-groups-api/) — View grouped design template configurations.
- [HeyMilo Design Templates API](https://apis.io/apis/heymilo/heymilo-design-templates-api/) — View design templates that control the candidate interview UI.
- [HeyMilo Domains API](https://apis.io/apis/heymilo/heymilo-domains-api/) — Manage custom domains for white-labelled interview URLs.
- [HeyMilo Email Template Groups API](https://apis.io/apis/heymilo/heymilo-email-template-groups-api/) — View grouped email template configurations.
- [HeyMilo Email Templates API](https://apis.io/apis/heymilo/heymilo-email-templates-api/) — View email templates configured for candidate outreach.
- [HeyMilo Health API](https://apis.io/apis/heymilo/heymilo-health-api/) — The Health API from HeyMilo — 1 operation(s) for health.
- [HeyMilo Interview Templates API](https://apis.io/apis/heymilo/heymilo-interview-templates-api/) — View interview templates, reusable agent configurations cloned from a blueprint posting (workflow, questions, criteria, agent settings).
- [HeyMilo Interviewers API](https://apis.io/apis/heymilo/heymilo-interviewers-api/) — Create, read, update, and manage interviewers. An interviewer (posting) combines job details with an AI agent configuration and agentic workflow.
- [HeyMilo Interviews API](https://apis.io/apis/heymilo/heymilo-interviews-api/) — Retrieve full interview results (scorecard, transcript, resume evaluation) and manage per-interview metadata.
- [HeyMilo Phone Numbers API](https://apis.io/apis/heymilo/heymilo-phone-numbers-api/) — List provisioned phone numbers for SMS and voice agents.
- [HeyMilo Questions API](https://apis.io/apis/heymilo/heymilo-questions-api/) — Create, read, update, delete, and reorder questions and criteria for an interviewer's workflow. Covers all modalities: voice, sms, form, resume_eligibility,…
- [HeyMilo Schema Discovery API](https://apis.io/apis/heymilo/heymilo-schema-discovery-api/) — The Schema Discovery API from HeyMilo — 2 operation(s) for schema discovery.
- [HeyMilo Sender Emails API](https://apis.io/apis/heymilo/heymilo-sender-emails-api/) — Manage sender email addresses used for candidate communications.
- [HeyMilo Voices API](https://apis.io/apis/heymilo/heymilo-voices-api/) — Browse the workspace voice registry for AI interviewer voices.
- [HeyMilo Webhooks API](https://apis.io/apis/heymilo/heymilo-webhooks-api/) — Register, list, and manage webhook endpoints that receive real-time event notifications.
- [HeyMilo Workspaces API](https://apis.io/apis/heymilo/heymilo-workspaces-api/) — List the workspaces accessible to the authenticated caller. API-key callers receive a single entry; OAuth callers receive every workspace they are a member of.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [HeyMilo Webhooks](https://apis.io/asyncapis/heymilo/heymilo-webhooks/)

#### Event channels (3)

Individual events and webhooks the provider emits.

- [interview_completed](https://apis.io/channels/heymilo/interview-completed/)
- [interview_started](https://apis.io/channels/heymilo/interview-started/)
- [report_available](https://apis.io/channels/heymilo/report-available/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [heymilo](https://apis.io/servers/heymilo/heymilo/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Heymilo Agentic Access](https://apis.io/agentic-access/heymilo/heymilo-agentic-access/)

#### Collections (18)

Postman and Open Collection request collections.

- [HeyMilo Public ATS API](https://apis.io/collections/heymilo/open-heymilo-ats-api/)
- [HeyMilo Public ATS Candidates API](https://apis.io/collections/heymilo/open-heymilo-candidates-api/)
- [HeyMilo Public ATS Design Template Groups API](https://apis.io/collections/heymilo/open-heymilo-design-template-groups-api/)
- [HeyMilo Public ATS Design Templates API](https://apis.io/collections/heymilo/open-heymilo-design-templates-api/)
- [HeyMilo Public ATS Domains API](https://apis.io/collections/heymilo/open-heymilo-domains-api/)
- [HeyMilo Public ATS Email Template Groups API](https://apis.io/collections/heymilo/open-heymilo-email-template-groups-api/)
- [HeyMilo Public ATS Email Templates API](https://apis.io/collections/heymilo/open-heymilo-email-templates-api/)
- [HeyMilo Public ATS Health API](https://apis.io/collections/heymilo/open-heymilo-health-api/)
- [HeyMilo Public ATS Interview Templates API](https://apis.io/collections/heymilo/open-heymilo-interview-templates-api/)
- [HeyMilo Public ATS Interviewers API](https://apis.io/collections/heymilo/open-heymilo-interviewers-api/)
- [HeyMilo Public ATS Interviews API](https://apis.io/collections/heymilo/open-heymilo-interviews-api/)
- [HeyMilo Public ATS Phone Numbers API](https://apis.io/collections/heymilo/open-heymilo-phone-numbers-api/)
- [HeyMilo Public ATS Questions API](https://apis.io/collections/heymilo/open-heymilo-questions-api/)
- [HeyMilo Public ATS Schema Discovery API](https://apis.io/collections/heymilo/open-heymilo-schema-discovery-api/)
- [HeyMilo Public ATS Sender Emails API](https://apis.io/collections/heymilo/open-heymilo-sender-emails-api/)
- [HeyMilo Public ATS Voices API](https://apis.io/collections/heymilo/open-heymilo-voices-api/)
- [HeyMilo Public ATS Webhooks API](https://apis.io/collections/heymilo/open-heymilo-webhooks-api/)
- [HeyMilo Public ATS Workspaces API](https://apis.io/collections/heymilo/open-heymilo-workspaces-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Heymilo Openapi Overlay](https://apis.io/overlays/heymilo/heymilo-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Heymilo Authentication](https://apis.io/security/heymilo/heymilo-authentication/)
- [Heymilo Domain Security](https://apis.io/security/heymilo/heymilo-domain-security/)
- [Heymilo Trust Center](https://apis.io/security/heymilo/heymilo-trust-center/)

#### Rate limits (1)

Published request limits.

- [Heymilo Rate Limits](https://apis.io/rate-limits/heymilo/heymilo-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.heymilo.ai)
- [Documentation](https://docs.heymilo.ai/documentation/get-started/landing)
- [Getting started](https://docs.heymilo.ai/documentation/get-started/what-is-heymilo)
- [API reference](https://docs.heymilo.ai/api-reference)
- [Sign up](https://www.heymilo.ai/book-a-demo)
- [Support](https://docs.heymilo.ai)
- [Blog](https://www.heymilo.ai/blog)
- [Compliance](https://trust.warden-ai.com/heymilo)
- [Trust centre](https://trust.heymilo.ai)
- [Terms of service](https://www.heymilo.ai/terms-of-service)
- [Privacy policy](https://www.heymilo.ai/privacy-policy)
- [GitHub](https://github.com/heymilo)
- [Status](https://status.heymilo.ai)

## API Evangelist rating

**Kin Score 51.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 57.7 |
| Contract governance | 18.2 |
| Operational transparency | 39.5 |
| Developer ergonomics | 60.1 |
| Access clarity | 46.1 |

**Agent readiness 53.2** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Employment & Payroll

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/heymilo/](https://apis.io/providers/heymilo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for HeyMilo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/heymilo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
