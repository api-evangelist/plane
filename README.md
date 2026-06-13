# Plane (plane)

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
