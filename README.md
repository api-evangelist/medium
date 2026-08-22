# medium (medium)

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

Documentation for Medium's OAuth2 API. Contribute to Medium/medium-api-docs development by creating an account on GitHub.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/medium/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/medium/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-05-19

## APIs

### Medium REST API

The Medium REST API provides programmatic access to the Medium online publishing platform. Developers can authenticate users via OAuth2, retrieve user profile details, list publications a user is associated with, create posts on a user's profile or within a publication, and upload images. The API is JSON-based with all requests made over HTTPS to endpoints under api.medium.com/v1, enabling integrations that automate content publishing workflows on Medium.

- **Human URL:** [https://github.com/Medium/medium-api-docs](https://github.com/Medium/medium-api-docs)
- **Base URL:** `https://api.medium.com/v1`

#### Tags

- Blogging
- Content
- Posts
- Publications
- Publishing
- Social Media
- Writing

#### Properties

- [Documentation](https://github.com/Medium/medium-api-docs)
- [OpenAPI](openapi/medium-rest-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/medium-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/medium-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Medium OAuth2 API

The Medium OAuth2 API enables third-party applications to authenticate and authorize users to act on their behalf on the Medium platform. Applications redirect users to Medium's authorization endpoint to obtain an authorization code, which is then exchanged for an access token and refresh token. The OAuth2 flow supports scoped permissions including basicProfile, publishPost, and listPublications, allowing developers to request only the level of access their application requires.

- **Human URL:** [https://github.com/Medium/medium-api-docs#2-authentication](https://github.com/Medium/medium-api-docs#2-authentication)
- **Base URL:** `https://medium.com/m/oauth`

#### Tags

- Authentication
- Authorization
- Identity
- OAuth

#### Properties

- [Documentation](https://github.com/Medium/medium-api-docs#2-authentication)
- [OpenAPI](openapi/medium-oauth2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/medium-oauth2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/medium-oauth2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/medium-com)
- [JSON-LD](json-ld/medium-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/medium-post-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/medium-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/medium-publication-schema.json) — [JSON Schema](https://json-schema.org/specification)
