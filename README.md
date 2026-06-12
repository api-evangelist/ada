# Ada (ada)

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
