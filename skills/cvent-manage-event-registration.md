---
name: cvent-manage-event-registration
description: Find a Cvent event, register attendees, update their status and email subscriptions, and check them in or reverse a check-in.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json
operations:
  - getEvents
  - getEventsPostFilters
  - getEventById
  - createAttendee
  - listAttendees
  - listAttendeesPostFilter
  - getAttendeeById
  - updateAttendee
  - updateAttendeeSubscriptionStatus
  - eventCheckIn
  - deleteEventCheckIn
---

# Manage event registration

Scopes: `event/events:read`, `event/attendees:read`, `event/attendees:write`.

## Steps

1. **Find the event** — `getEvents` (`GET /events`) with a filter such as
   `filter=eventName eq "Annual Summit"`, or `getEventsPostFilters` (`POST /events/filter`) for
   long filters. `getEventById` returns one event's full configuration.
2. **Register an attendee** — `createAttendee` (`POST /attendees`). The attendee is the person
   across the registration lifecycle; the contact record in the address book is a separate
   entity (see `cvent-sync-contacts`).
3. **List and inspect** — `listAttendees` (`GET /attendees`) or `listAttendeesPostFilter`
   (`POST /attendees/filter`), then `getAttendeeById`.
4. **Change status** — `updateAttendee` (`PUT /attendees/{id}`). Status transitions are
   constrained and Cvent has changed them in released updates (Pending Approval → Cancelled,
   Waitlisted → Accepted): read the current changelog entry before relying on one.
5. **Email preferences** — `updateAttendeeSubscriptionStatus`
   (`PUT /attendees/{id}/email-subscriptions`). The old `unsubscribed` field on the attendee
   object is deprecated in favour of this operation.
6. **Onsite** — `eventCheckIn` (`POST /events/{id}/check-in`) and, to reverse it,
   `deleteEventCheckIn` (`DELETE /events/{id}/check-in/{attendeeId}`).

## Rules

- No idempotency key exists: a retried `createAttendee` registers the person twice. Read back
  with a filter before retrying a write you are unsure about.
- A check-in is reversible; a sent email is not. Cvent documents no time window on any
  reversal, so treat "can I undo this" as "yes, but nobody promised for how long".
- Every list response paginates with `paging.nextToken`; every response carries the
  `X-RateLimit-*` headers.
