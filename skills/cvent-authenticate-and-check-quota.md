---
name: cvent-authenticate-and-check-quota
description: Exchange Cvent client credentials for a bearer token, validate it, and read your live API quota and usage tier before spending calls.
api: Cvent Platform REST API (version ea)
generated: '2026-09-07'
method: generated
source: openapi/_original/cvent-openapi.json; https://developers.cvent.com/docs/rest-api/tutorials/developer-quickstart; https://developers.cvent.com/docs/rest-api/guides/handling-rate-limits
operations:
  - oauth2Token
  - validateToken
  - getUsageTier
  - getUsage
---

# Authenticate and check quota

Every Cvent REST call is a production call against a real account, and every call — including
one that fails with 429 — counts against a daily quota. Get the token, then find out how much
budget you have before you start.

## Host

- North America: `https://api-platform.cvent.com/ea`
- Europe: `https://api-platform-eur.cvent.com/ea`

Picking the wrong region returns 404, not 401.

## Steps

1. **Get a token** — `oauth2Token` (`POST /oauth2/token`).
   Send `Content-Type: application/x-www-form-urlencoded`, an `Authorization: Basic` header
   holding base64 of `client_id:client_secret`, and the body
   `grant_type=client_credentials&client_id=<client_id>`.
   The response carries `access_token`, `expires_in` (3600) and `token_type: Bearer`.
   Cache the token for its full hour; re-minting it on every call wastes quota.
2. **Validate if you are unsure** — `validateToken` (`GET /token-validation`) confirms a token
   is still good without touching business data.
3. **Read your tier** — `getUsageTier` (`GET /usage/tier`). Free = 1,000 calls/day, 2/second,
   burst 1. Standard = 15,000/day, 10/second, burst 10. Premium = 500,000/day, 25/second, burst 25.
4. **Read live consumption** — `getUsage` (`GET /usage`) before a batch run, and watch the
   `X-RateLimit-Limit`, `X-RateLimit-Remaining` and `X-RateLimit-Reset` headers on every response.

## Rules

- **429 means two different things.** Body message `Too Many Requests` is per-second throttling —
  back off 2s plus 1–1000 ms jitter, doubling to a 16s ceiling, at most 5 attempts. Body message
  `Limit Exceeded` is the daily quota — stop until after midnight GMT. Cvent's own SDK retry
  overlay deliberately excludes 429 from automatic retry because the status alone cannot tell
  the two apart.
- **Scopes are least-privilege and additive.** A 403 means the token lacks the operation's scope;
  fix it on the application in the developer console, not in the request. Granting *every* scope
  inflates the token enough to produce HTTP 431.
- Authorization-code flow exists but is limited to Cvent planner administrators; machine
  integrations use client credentials.
