---
name: cvent-sync-contacts
description: Read, create and update Cvent address-book contacts with cursor pagination and filters, and register a contact hook so Cvent asks your system for the record of truth.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json; https://developers.cvent.com/docs/rest-api/reference/filters
operations:
  - listContacts
  - listContactsPostFilters
  - getContactById
  - createContacts
  - updateContacts
  - patchContacts
  - updateContactById
  - deleteContactById
  - getChangeHistoryForASpecificContact
  - createContactHook
  - ListContactHooks
  - deleteContactHook
---

# Sync contacts with Cvent

Scopes: `event/contacts:read`, `event/contacts:write`. Hooks need `account/hooks:read` /
`account/hooks:write` / `account/hooks:delete`.

## Read

1. `listContacts` (`GET /contacts`) with `limit` and an optional `filter`, e.g.
   `filter=lastName eq 'Smith'`. Operators: `eq`, `ne`, `lt`, `le`, `gt`, `ge`, `sw`,
   `contains`, combined with `and` / `or`. Use double quotes around a value that contains a
   single quote.
2. Page with the cursor, not an offset: take `paging.nextToken` and pass it as the `token`
   query parameter on the next call. No `nextToken` means the last page. An empty final `data`
   array is possible when the total divides evenly — handle it.
3. When a filter is too long for a query string, use `listContactsPostFilters`
   (`POST /contacts/filter`) with the same grammar in the body.
4. `getContactById` for one record; `getChangeHistoryForASpecificContact` for its audit trail.

## Write

- `createContacts` (`POST /contacts`) and `updateContacts` (`PUT /contacts`) work in batches;
  `patchContacts` (`PATCH /contacts`) applies partial updates; `updateContactById` targets one.
- **There is no idempotency key on any Cvent write.** A retried `POST /contacts` creates a
  second contact. De-duplicate on your side before retrying, or read back with a filter first.
- `deleteContactById` removes the contact from the address book but **does not** remove it from
  events, and deleted/purged contacts remain visible through the `deleted` filter and the
  `includePurged` parameter.

## Push instead of poll

`createContactHook` (`POST /contacts/hooks`) registers a callback URL. Cvent then POSTs a
`contactTransaction` callback to it asking your system for the contact's details; every
non-blank field you return overwrites Cvent's copy. Secure the callback with
`CallbackApiKeyAuth` or `CallbackBasicAuth`. Answer 400 or 404 and Cvent will not retry.
