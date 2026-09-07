---
name: cvent-bulk-load-data
description: Load large data sets into Cvent through the Bulk API — create a job, upload data, run it, read per-row results, and cancel a job that is going wrong.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json; https://developers.cvent.com/docs/rest-api/guides/bulk-api-user-guide
operations:
  - createBulkJob
  - uploadBulkJobData
  - runBulkJob
  - getBulkJobById
  - listBulkJobResult
  - cancelBulkJob
---

# Bulk-load data into Cvent

Scopes: `bulk/bulk-jobs:read`, `bulk/bulk-jobs:write`.

Use this instead of a loop of single-record writes: a 50,000-row import through `createContacts`
would exhaust even the Premium daily quota of 500,000 calls far faster than the Bulk API, which
spends a handful of calls for the whole load.

## Steps

1. `createBulkJob` (`POST /bulk-jobs`) — declare the job's `name`, `mode`, `ttl` and the
   properties being loaded. Keep the returned job id.
2. `uploadBulkJobData` (`POST /bulk-jobs/{id}/data`) — push the payload.
3. `runBulkJob` (`POST /bulk-jobs/{id}/run`) — start processing.
4. `getBulkJobById` (`GET /bulk-jobs/{id}`) — poll status. Poll on an interval that respects
   your per-second limit (2/s on Free); each poll costs a call.
5. `listBulkJobResult` (`GET /bulk-jobs/{id}/results`) — returns **207 Multi-Status**: rows
   succeed and fail independently. Read the per-row `failed` flag; a 2xx on the job is not a
   guarantee that every row landed.

## Reversal

`cancelBulkJob` (`POST /bulk-jobs/{id}/cancel`) stops the job **after it finishes its current
batch**. Rows already written are not rolled back — there is no undo for a bulk load, so
validate the payload before step 3 rather than after.
