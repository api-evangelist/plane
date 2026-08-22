# Plane (plane)

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

Plane is an open-source, AI-native project management platform that enables teams to manage issues, cycles, modules, pages, analytics, and workspace members through a comprehensive REST API. Available as a fully managed cloud service or self-hosted on your own infrastructure using Docker or Kubernetes, Plane provides 180+ REST endpoints organized around predictable resource-oriented URLs with JSON request and response bodies. The API supports OAuth 2.0 for third-party app authorization, personal access token authentication, HMAC-signed webhooks for real-time event notifications, and typed SDKs for Python and Node.js. Plane also ships an official Model Context Protocol (MCP) server to enable AI agents to interact with your workspace programmatically.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/plane/refs/heads/main/apis.yml
- Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=plane-api-evangelist&utm_content=repo

## Tags

- Project Management
- Issues
- Cycles
- Modules
- Pages
- Analytics
- Workspace
- Open Source
- Self-Hosted
- AI

## APIs

### Plane REST API

The Plane REST API provides 180+ endpoints for managing all aspects of project management workspaces including projects, work items, cycles, modules, pages, analytics, intake, and team members. The API uses standard HTTP verbs, cursor-based pagination, and JSON request/response bodies with predictable resource-oriented URLs. Authentication is supported via personal access tokens (X-API-Key header) or OAuth 2.0 bearer tokens for third-party applications.

- Documentation: https://developers.plane.so/api-reference/introduction
- Base URL: https://api.plane.so/api/v1/

## Plans, Rate Limits, and FinOps

### Plans and Pricing

Plane offers four tiers billed per seat per month:

| Plan | Price | Seats | Key Features |
|------|-------|-------|-------------|
| Free | $0/seat/month | Up to 12 | Core PM, 500 AI credits/seat |
| Pro | $6/seat/month | Unlimited | Custom types, Wiki, time tracking, SSO, 1,000 AI credits/seat |
| Business | $13/seat/month | Unlimited | Recurring items, intake email, nested pages, 2,000 AI credits/seat |
| Enterprise Grid | Custom | Unlimited | LDAP, GAC, audit logs, managed deployments |

Full details: [plans/plane-plans-pricing.yml](plans/plane-plans-pricing.yml)

### Rate Limits

- 60 requests per minute per API key (cloud default)
- Response headers: `X-RateLimit-Remaining`, `X-RateLimit-Reset`
- HTTP 429 returned when limit is exceeded
- Self-hosted deployments can override via `env.api_key_rate_limit`

Full details: [rate-limits/plane-rate-limits.yml](rate-limits/plane-rate-limits.yml)

### FinOps

Billing is per seat via Stripe. Guest slots (5 per paid seat on Pro/Business) are free. AI credits are pooled workspace-wide and roll over one month; top-ups are $2 per 1,000 credits. Annual billing saves 25% on Pro and ~13% on Business. Self-hosting eliminates AI credit costs by using your own provider API keys.

Full details: [finops/plane-finops.yml](finops/plane-finops.yml)

## Timestamps

- Created: 2026-06-13
- Modified: 2026-06-13

## Common

| Type | URL |
|------|-----|
| Website | https://plane.so/ |
| Documentation | https://developers.plane.so/ |
| GitHub Org | https://github.com/makeplane |
| LinkedIn | https://www.linkedin.com/company/planepowers/ |
| Blog | https://plane.so/blog |
| Pricing | https://plane.so/pricing |
| Status Page | https://status.plane.so/ |
| X / Twitter | https://twitter.com/planepowers |

## Maintainers

- Kin Lane — kin@apievangelist.com
