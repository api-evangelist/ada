# Ada (ada)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Ada is an AI-powered customer service automation platform that enables enterprises to deploy AI agents capable of resolving customer inquiries across digital channels. The platform exposes a suite of REST APIs for managing knowledge bases, end-user profiles, conversation handling, data export, data compliance, and external integrations. All APIs authenticate via rotatable API keys, return JSON, and support cursor-based pagination. Ada serves global brands including Pinterest, Square, Ancestry, and Zendesk, and has powered more than 6.4 billion customer interactions since 2016.

**APIs.json:** https://raw.githubusercontent.com/api-evangelist/ada/refs/heads/main/apis.yml

**Naftiko:** https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=ada-api-evangelist&utm_content=repo

---

## Tags

`ai` `customer-service` `chatbot` `automation` `conversational-ai` `helpdesk` `crm` `integrations` `knowledge-management` `data-export`

---

## APIs

| Name | Description |
|------|-------------|
| Ada Knowledge API | Import and sync knowledge articles into Ada for AI-generated responses |
| Ada End Users API | Real-time user profile management with webhook events |
| Ada Conversations API | Build custom channels and extend Ada into third-party platforms |
| Ada Data Export API | Access conversation and message records for analytics |
| Ada Data Compliance API | Delete personal data by email for GDPR compliance |
| Ada Integrations API | Connect external applications to Ada via OAuth |

---

## Plans / Rate Limits / FinOps

| Resource | Detail |
|----------|--------|
| Pricing model | Enterprise only; conversation-based ($0.35–$1.50/conversation) or resolution-based ($1.00–$3.50/resolution) |
| Minimum contract | ~$30,000 USD/year |
| Global rate limit | 10 req/sec, 100 req/min, 10,000 req/day |
| End Users & Conversations APIs | 30 req/sec, 300 req/min, 60,000 req/day |
| Data Export API | 10 req/sec/endpoint, 15,000 req/day |
| Throttle response | HTTP 429 Too Many Requests |
| FinOps billing model | Consumption (conversation or resolution units) |

- Plans: [plans/ada-plans-pricing.yml](plans/ada-plans-pricing.yml)
- Rate Limits: [rate-limits/ada-rate-limits.yml](rate-limits/ada-rate-limits.yml)
- FinOps: [finops/ada-finops.yml](finops/ada-finops.yml)

---

## Timestamps

| Field | Value |
|-------|-------|
| Created | 2026-06-12 |
| Modified | 2026-06-12 |

---

## Common Properties

| Type | URL |
|------|-----|
| Website | https://www.ada.cx/ |
| Documentation | https://docs.ada.cx/reference/introduction/overview |
| GitHub Organization | https://github.com/adasupport |
| LinkedIn | https://ca.linkedin.com/company/ada-cx |
| Blog | https://www.ada.cx/blog/ |
| Pricing | https://www.ada.cx/platform/ |
| Status Page | https://status.ada.support/ |
| X (Twitter) | https://x.com/ada_cx |

---

## Maintainers

**Kin Lane** — kin@apievangelist.com
