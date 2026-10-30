# Medium

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

Medium is an online publishing platform where writers publish stories and readers follow topics, publications and authors. Its developer surface is a small OAuth2 REST API at api.medium.com/v1 that lets an integration read the authenticated user's profile, list the publications they write to or edit, upload images, and publish posts to a profile or into a publication. Medium states the API is no longer supported and does not accept new integrations: existing tokens continue to work, but new integration tokens have not been issued since 2023 and the documentation repository was archived in 2023.

**Areas:** Publishing · Content · Blogging · Media · Social · Writing · Authentication · Deprecated API

## Medium on APIs.io

Everything profiled for Medium is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/medium/](https://apis.io/providers/medium/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [medium Authorization API](https://apis.io/apis/medium/medium-authorization-api/) — Endpoints for initiating the OAuth2 authorization flow by redirecting users to Medium's authorization page.
- [medium Images API](https://apis.io/apis/medium/medium-images-api/) — Operations for uploading images to Medium for use in posts. Supports JPEG, PNG, GIF, and TIFF formats.
- [medium Posts API](https://apis.io/apis/medium/medium-posts-api/) — Operations for creating new posts on a user's profile or within a publication, supporting HTML and Markdown content formats.
- [medium Publications API](https://apis.io/apis/medium/medium-publications-api/) — Operations for listing publications a user is associated with and retrieving contributors for a given publication.
- [medium Tokens API](https://apis.io/apis/medium/medium-tokens-api/) — Endpoints for exchanging authorization codes for access tokens and refreshing expired access tokens.
- [medium Users API](https://apis.io/apis/medium/medium-users-api/) — Operations for retrieving authenticated user profile information including username, name, URL, and avatar image.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [medium-mcp.yml](https://apis.io/servers/medium/medium-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Medium Agentic Access](https://apis.io/agentic-access/medium/medium-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Medium Post](https://apis.io/schemas/medium/medium-post/)
- [Medium Publication](https://apis.io/schemas/medium/medium-publication/)
- [Medium User](https://apis.io/schemas/medium/medium-user/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Medium Context](https://apis.io/jsonld/medium/medium-context/)

#### Collections (8)

Postman and Open Collection request collections.

- [Medium OAuth2 Authorization API](https://apis.io/collections/medium/open-medium-authorization-api/)
- [Medium OAuth2 Authorization Images API](https://apis.io/collections/medium/open-medium-images-api/)
- [Medium OAuth2 API](https://apis.io/collections/medium/open-medium-oauth2/)
- [Medium OAuth2 Authorization Posts API](https://apis.io/collections/medium/open-medium-posts-api/)
- [Medium OAuth2 Authorization Publications API](https://apis.io/collections/medium/open-medium-publications-api/)
- [Medium REST API](https://apis.io/collections/medium/open-medium-rest-api/)
- [Medium OAuth2 Authorization Tokens API](https://apis.io/collections/medium/open-medium-tokens-api/)
- [Medium OAuth2 Authorization Users API](https://apis.io/collections/medium/open-medium-users-api/)

#### Overlays (6)

OpenAPI overlays, including conversational phrasing for each operation.

- [Medium Authorization Api Overlay](https://apis.io/overlays/medium/medium-authorization-api-overlay/)
- [Medium Images Api Overlay](https://apis.io/overlays/medium/medium-images-api-overlay/)
- [Medium Posts Api Overlay](https://apis.io/overlays/medium/medium-posts-api-overlay/)
- [Medium Publications Api Overlay](https://apis.io/overlays/medium/medium-publications-api-overlay/)
- [Medium Tokens Api Overlay](https://apis.io/overlays/medium/medium-tokens-api-overlay/)
- [Medium Users Api Overlay](https://apis.io/overlays/medium/medium-users-api-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Medium — jsonschema rules](https://apis.io/rules/medium/medium-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Medium Authentication](https://apis.io/security/medium/medium-authentication/)
- [Medium Domain Security](https://apis.io/security/medium/medium-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Medium Scopes](https://apis.io/scopes/medium/medium-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Medium Plans Pricing](https://apis.io/plans/medium/medium-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Medium Rate Limits](https://apis.io/rate-limits/medium/medium-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Medium Finops](https://apis.io/finops/medium/medium-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://medium.com)
- [Documentation](https://github.com/Medium/medium-api-docs)
- [Getting started](https://github.com/Medium/medium-api-docs#2-authentication)
- [API reference](https://github.com/Medium/medium-api-docs#3-resources)
- [Support](https://help.medium.com/)
- [Blog](https://medium.com/feed/blog)
- [GitHub](https://github.com/Medium)
- [Status](https://status.medium.com/)

## API Evangelist rating

**Kin Score 36.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 52.5 |
| Contract governance | 14.4 |
| Operational transparency | 18.4 |
| Developer ergonomics | 56.5 |
| Access clarity | 0.0 |

**Agent readiness 26.4** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 26.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/medium/](https://apis.io/providers/medium/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Medium: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/medium/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
