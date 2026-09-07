---
name: cvent-build-event-agenda
description: Build a Cvent event agenda — create sessions and categories, add speakers, attach documents, and record session attendance.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json
operations:
  - listSessions
  - listSessionsPostFilters
  - createSession
  - listSessionsCategories
  - createSessionCategory
  - listSpeakers
  - createSpeaker
  - updateSpeaker
  - addSpeakerDoc
  - deleteSpeaker
  - createProgramItem
  - listProgramItems
  - createSessionProgramSpeaker
  - deleteSessionProgramSpeaker
---

# Build an event agenda

Scopes: `event/sessions:read|write`, `event/session-categories:read|write`,
`event/speakers:read|write|delete`, `event/program-items:read|write|delete`.

## Steps

1. **Categories first** — `listSessionsCategories` (`GET /session-categories`), and
   `createSessionCategory` when the one you need does not exist. Sessions reference categories,
   so creating them in the other order means a second update pass.
2. **Sessions** — `createSession` (`POST /sessions`). A session requires its parent `event`
   object with `event.id`. `listSessions` / `listSessionsPostFilters` read them back;
   `listSessions` supports `sort` and filters on `id` and `name`.
3. **Speakers** — `createSpeaker` (`POST /speakers`), then `updateSpeaker` for edits and
   `addSpeakerDoc` (`PUT /speakers/{id}/docs/{fileId}`) to attach a document uploaded through
   the File API. Files must be under 10 MB and an unassociated upload expires within 30 days.
4. **Program items** — `createProgramItem` (`POST /program-items`) models the agenda slot;
   `createSessionProgramSpeaker` (`PUT /program-items/{programItemId}/speakers/{id}`) binds a
   speaker to it, and `deleteSessionProgramSpeaker` unbinds.

## Rules

- Deletes here are hard deletes of the linkage (`deleteSpeaker`, `deleteProgramItem`) with no
  documented restore path — build the agenda additively and verify before deleting.
- No idempotency key: a retried `createSession` produces a duplicate session on the agenda.
- Filter documentation for these endpoints is reformatted regularly in the biweekly changelog;
  check the current entry before assuming an operator is supported.
