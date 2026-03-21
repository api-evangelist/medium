# Medium (medium)
Medium is an online publishing platform where individuals and organizations share ideas, stories, and expertise. Their developer platform offers a REST API and OAuth2 authentication, enabling third-party applications to programmatically publish content, manage user profiles, and interact with publications on the Medium platform.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/medium/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Publishing, Blogging, Content, Writing, Social Media, OAuth

## Timestamps

- **Created:** 2025-03-01
- **Modified:** 2026-03-20

## APIs

### Medium REST API
The Medium REST API provides programmatic access to the Medium online publishing platform. Developers can authenticate users via OAuth2, retrieve user profile details, list publications a user is associated with, create posts on a user's profile or within a publication, and upload images. The API is JSON-based with all requests made over HTTPS to endpoints under api.medium.com/v1, enabling integrations that automate content publishing workflows on Medium.

**Human URL:** [https://github.com/Medium/medium-api-docs](https://github.com/Medium/medium-api-docs)


#### Tags:

 - Publishing, Blogging, Content, Writing, Posts, Publications, Social Media

#### Properties

- [Documentation](https://github.com/Medium/medium-api-docs)
- [OpenAPI](openapi/medium-rest-api-openapi.yml)

### Medium OAuth2 API
The Medium OAuth2 API enables third-party applications to authenticate and authorize users to act on their behalf on the Medium platform. Applications redirect users to Medium's authorization endpoint to obtain an authorization code, which is then exchanged for an access token and refresh token. The OAuth2 flow supports scoped permissions including basicProfile, publishPost, and listPublications, allowing developers to request only the level of access their application requires.

**Human URL:** [https://github.com/Medium/medium-api-docs#2-authentication](https://github.com/Medium/medium-api-docs#2-authentication)


#### Tags:

 - Authentication, OAuth, Authorization, Identity

#### Properties

- [Documentation](https://github.com/Medium/medium-api-docs#2-authentication)
- [OpenAPI](openapi/medium-oauth2-openapi.yml)

## Common Properties

- [Portal](https://github.com/Medium/medium-api-docs)
- [Website](https://medium.com)
- [PrivacyPolicy](https://policy.medium.com/medium-privacy-policy-f03bf92035c9)
- [TermsOfService](https://policy.medium.com/medium-terms-of-service-9db0094a1e0f)
- [Blog](https://blog.medium.com)
- [Login](https://medium.com/m/signin)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
