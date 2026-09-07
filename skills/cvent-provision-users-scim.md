---
name: cvent-provision-users-scim
description: Provision and de-provision Cvent users over SCIM 2.0 — discover the service provider config and schemas, then create, update and delete users and read groups.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json; https://developers.cvent.com/docs/platform/data-models/user-scim
operations:
  - getServiceProviderConfig
  - getSchemas
  - getSchema
  - getResourceTypes
  - getResourceType
  - listUsers
  - createUser
  - getUser
  - updateUser
  - deleteUser
  - getUserGroups
---

# Provision Cvent users over SCIM 2.0

Cvent implements SCIM 2.0 (RFC 7643 / RFC 7644) for user lifecycle, which means an identity
platform that already speaks SCIM needs no bespoke Cvent connector. The schemas carry the
registered URNs `urn:ietf:params:scim:schemas:core:2.0:User` and
`urn:ietf:params:scim:schemas:extension:enterprise:2.0:User`; list and error payloads use
`urn:ietf:params:scim:api:messages:2.0:ListResponse` and `...:2.0:Error`.

Scopes: `account/users:read`, `account/users:write`, `account/users:delete`.

## Steps

1. **Discover** — `getServiceProviderConfig` (`GET /scim/v2/ServiceProviderConfig`) tells you
   what Cvent's SCIM implementation supports. `getSchemas` and `getResourceTypes` enumerate the
   attribute model. Do this once per integration rather than assuming the base schema.
2. **Read** — `listUsers` (`GET /scim/v2/Users`), `getUser` (`GET /scim/v2/Users/{id}`),
   `getUserGroups` (`GET /scim/v2/Groups`).
3. **Create** — `createUser` (`POST /scim/v2/Users`). The changelog records a `sendLoginDetails`
   behaviour on create and the enterprise extension on the User resource; check the current
   entry before relying on either.
4. **Update** — `updateUser` (`PUT /scim/v2/Users/{id}`), a full replace.
5. **De-provision** — `deleteUser` (`DELETE /scim/v2/Users/{id}`), which needs the separate
   `account/users:delete` scope. There is no documented restore.

## Rules

- SCIM errors come back in the SCIM error envelope, not the Cvent `ErrorResponse` envelope —
  handle both shapes in one client.
- The SCIM surface obeys the same account-wide rate limits as the rest of the API; a full
  directory sync on the Free tier (1,000 calls/day) will not fit.
