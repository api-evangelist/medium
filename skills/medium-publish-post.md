---
name: medium-publish-post
description: Publish a post to a Medium user's own profile using Medium's REST API, safely — draft-first, because the API has no delete and no idempotency key.
api: medium
operations:
  - getAuthenticatedUser
  - uploadImage
  - createUserPost
generated: '2026-09-17'
method: generated
source: openapi/medium-users-api-openapi.yml, openapi/medium-images-api-openapi.yml, openapi/medium-posts-api-openapi.yml, conventions/medium-conventions.yml, errors/medium-problem-types.yml
---

# Publish a post to a Medium profile

**Read this first.** Medium states its API is no longer supported and does not accept new
integrations. This skill only works if you already hold a valid integration token. Every write lands
on a real, public medium.com profile: there is **no sandbox**, **no idempotency key**, and **no
delete, unpublish or update operation anywhere in the contract**. Default to `draft`.

## Preconditions

- A Medium self-issued integration token, or an OAuth2 access token with the `publishPost` scope
  (plus `uploadImage` if the post carries images — that scope is *extended* and requires Medium's
  prior permission).
- Send it as `Authorization: Bearer <token>` on every request. Base URL `https://api.medium.com/v1`.

## Steps

1. **Resolve the author id.** `getAuthenticatedUser` — `GET /v1/me`.
   The response is `{"data": {"id", "username", "name", "url", "imageUrl"}}`. Keep `data.id`; it is
   the `authorId` path parameter in step 3. There is no other way to obtain it — Medium publishes no
   user lookup operation.
   A 401 here means the token is invalid or revoked, and is terminal for a new integration.

2. **Upload images, if any.** `uploadImage` — `POST /v1/images`, `multipart/form-data`.
   Accepts JPEG, PNG, GIF and TIFF. The response is `{"data": {"url", "md5"}}`. Embed `data.url`
   into the post body yourself; there is no typed reference from a post to an image.
   Uploads are also irreversible — record every returned `md5` so you can recognise a re-upload.

3. **Create the post.** `createUserPost` — `POST /v1/users/{authorId}/posts`, `application/json`.
   Body is `components.schemas.CreatePostRequest`:
   - `title` (required), `contentFormat` (`html` or `markdown`), `content` (required)
   - `tags` — **a maximum of three**; a fourth is a 400
   - `canonicalUrl`, `license`, `notifyFollowers`
   - `publishStatus` — **set this to `draft` on the first call.** Publish by hand, or on a second
     deliberate call, once a human has read the draft on medium.com.
   Success is **201** with `{"data": {...Post}}`. Keep `data.url` and `data.id`.

## Rules

- **Never retry a 5xx or a timeout on step 3 blindly.** There is no idempotency key; a retry
  publishes a second post. If a write times out, stop and have a human check the profile.
- **Never publish `public` on an agent's own initiative.** Reversal is impossible through the API.
- Errors are `{"errors":[{"message":"...","code":<int>}]}` — not RFC 9457. The numeric codes are
  undocumented; branch on the HTTP status, show `message` to the user.
  - `400` invalid or missing required fields, more than three tags, unsupported `contentFormat`
  - `401` invalid, missing or revoked token, or missing scope
  - `403` the `authorId` is not the authenticated user
- No rate limits are published and no `Retry-After` is documented. Pace yourself conservatively.
