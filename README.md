# medium (medium)

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
