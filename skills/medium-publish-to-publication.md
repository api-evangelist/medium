---
name: medium-publish-to-publication
description: Publish into a Medium publication — resolve the user's publications, check the caller's role, and create the post with the publish status that role actually permits.
api: medium
operations:
  - getAuthenticatedUser
  - listUserPublications
  - listPublicationContributors
  - createPublicationPost
generated: '2026-09-17'
method: generated
source: openapi/medium-users-api-openapi.yml, openapi/medium-publications-api-openapi.yml, openapi/medium-posts-api-openapi.yml, data-model/medium-data-model.yml
---

# Publish into a Medium publication

Same warnings as `medium-publish-post`: no sandbox, no idempotency key, no delete. In addition,
publication posts are governed by a **role** the API will not infer for you — get it wrong and the
call is a 403, or the post lands publicly when you meant it to be reviewed.

## Steps

1. **Resolve the user id.** `getAuthenticatedUser` — `GET /v1/me`. Keep `data.id`.

2. **List the publications.** `listUserPublications` —
   `GET /v1/users/{userId}/publications` with the id from step 1.
   The response is `{"data": [ {id, name, description, url, imageUrl} ]}`. Match the publication the
   user named against `name`, and keep its `id`.
   - `403` means you asked for someone else's publications — you may only pass your own user id.
   - The list is capped at 200 non-authored publications and **cannot be paged**. If the target is
     not in the list, ask the user for it rather than assuming the API is wrong.

3. **Check the caller's role.** `listPublicationContributors` —
   `GET /v1/publications/{publicationId}/contributors`.
   Find the row whose `userId` equals the id from step 1 and read `role`:
   - `editor` — may create posts with any `publishStatus`; `public` and `unlisted` appear in the
     publication immediately.
   - `writer` — may only create a `draft`, which stays pending until an editor approves it.
   - absent — the user is neither; step 4 will 403. Stop and tell them.

4. **Create the post.** `createPublicationPost` —
   `POST /v1/publications/{publicationId}/posts`, body `CreatePostRequest`, max three `tags`.
   Set `publishStatus` to what step 3 permits — `draft` unless a human has explicitly asked for
   `public` and the role is `editor`. Success is **201** with `{"data": {...Post}}`; the returned
   `Post` carries `publicationId`.

## Rules

- A `writer` requesting `public` is a `403`, not a downgrade. Read the role first; do not probe.
- The write is irreversible and non-idempotent. On a timeout, stop — do not re-POST.
- `403` on step 4 means the `publicationId` is not one the user can publish into. Re-run step 2
  rather than guessing another id.
