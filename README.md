# Cvent (cvent)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Cvent is a leading meetings, events, and hospitality technology provider with over 4,800 employees and 22,000+ customers worldwide. The Cvent platform spans Event Cloud (event management, registration, mobile event apps, virtual and hybrid events, Attendee Hub, surveys, Diagramming, and analytics) and Hospitality Cloud (Cvent Supplier Network, Passkey, Venue Sourcing, and Sales & Catering). Programmatic access is delivered through the unified Cvent Platform REST API (api-platform.cvent.com) using OAuth 2.0 client credentials, with legacy SOAP, BadgeKit, Jifflenow, and CSN APIs documented for historical integrations. The developer portal at developers.cvent.com hosts API references, guides, OpenAPI downloads, webhooks, SSO, custom widgets, white-label, and integration documentation.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cvent/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cvent/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Attendee Hub
- Attendee Management
- Conferences
- Diagramming
- Event Management
- Event Marketing
- Events
- Exhibitors
- Hospitality
- Hospitality Cloud
- Hybrid Events
- Meetings
- OAuth 2.0
- Passkey
- Registration
- REST API
- SOAP API
- SSO
- Supplier Network
- Surveys
- Venue Management
- Venue Sourcing
- Virtual Events
- Webhooks
- White Label

## Timestamps

- **Created:** 2025-11-19
- **Modified:** 2026-04-28

## APIs

### Cvent REST API

The unified Cvent Platform REST API providing programmatic access to events, contacts, registrations, attendees, sessions, speakers, exhibitors, surveys, webhooks, and Attendee Hub resources. OAuth 2.0 client credentials with the token endpoint at api-platform.cvent.com/ea/oauth2/token.

- **Human URL:** [https://developers.cvent.com/docs/rest-api/overview](https://developers.cvent.com/docs/rest-api/overview)
- **Base URL:** `https://api-platform.cvent.com`

#### Tags

- Attendees
- Contacts
- Events
- OAuth 2.0
- Registration
- REST
- Sessions
- Surveys
- Webhooks

#### Properties

- [Documentation](https://developers.cvent.com/docs/rest-api/overview)
- [API Reference](https://developers.cvent.com/docs/rest-api/reference/reference)
- [Getting Started](https://developers.cvent.com/docs/rest-api/tutorials/developer-quickstart)
- [Concepts](https://developers.cvent.com/docs/rest-api/explanation/concepts)
- [Changelog](https://developers.cvent.com/docs/rest-api/changelog)
- [Migration Guide](https://developers.cvent.com/docs/rest-api/migration-guide/benefits)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Webhooks API

Cvent Webhooks notify external applications when actions occur in Cvent and send relevant data to a specified URL, automatically pushing event, attendee, speaker, and meeting request data to subscriber endpoints for real-time integration.

- **Human URL:** [https://developers.cvent.com/docs/webhooks/overview](https://developers.cvent.com/docs/webhooks/overview)

#### Tags

- Attendees
- Events
- Notifications
- Sessions
- Webhooks

#### Properties

- [Documentation](https://developers.cvent.com/docs/webhooks/overview)
- [Guide](https://developers.cvent.com/docs/webhooks/understanding-webhooks)
- [Getting Started](https://developers.cvent.com/docs/webhooks/tutorials/account-setup)
- [Technical Requirements](https://developers.cvent.com/docs/webhooks/technical-requirements)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Supplier Network (CSN) API

The Cvent Supplier Network (CSN) API provides integration with a database of 280,000+ hotels, suppliers, and destinations worldwide. Planners search and compare venues and manage RFPs; suppliers create and update proposals via a push-pull workflow.

- **Human URL:** [https://developers.cvent.com/docs/legacy-api/csn/overview](https://developers.cvent.com/docs/legacy-api/csn/overview)

#### Tags

- Hospitality
- Proposals
- RFP
- Suppliers
- Venues

#### Properties

- [Documentation](https://developers.cvent.com/docs/legacy-api/csn/overview)
- [Planner Guide](https://developers.cvent.com/docs/legacy-api/csn/planner-guide/overview)
- [Supplier Guide](https://developers.cvent.com/docs/legacy-api/csn/supplier-guide/authentication)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Passkey RegLink API

Passkey RegLink APIs are RESTful JSON APIs (with legacy URL-based and SOAP options) connecting Cvent registration with Passkey hotel reservations. Send registrant info, fetch event and hotel availability, retrieve reservations, and create / update / cancel hotel bookings.

- **Human URL:** [https://developers.cvent.com/docs/passkey/REST/overview](https://developers.cvent.com/docs/passkey/REST/overview)

#### Tags

- Accommodations
- Hotels
- Registration
- Reservations

#### Properties

- [Documentation](https://developers.cvent.com/docs/passkey/REST/overview)
- [Getting Started](https://developers.cvent.com/docs/passkey/REST/getting-started)
- [Callbacks](https://developers.cvent.com/docs/passkey/REST/callbacks)
- [F A Q](https://developers.cvent.com/docs/passkey/REST/faq)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent SOAP API (Legacy)

The Cvent SOAP API is the original legacy API for pushing and pulling data between Cvent and internal systems. Supports contact and event management, custom fields, address book, and metadata. Being sunset in favor of the REST API.

- **Human URL:** [https://developers.cvent.com/docs/legacy-api/soap-api/overview](https://developers.cvent.com/docs/legacy-api/soap-api/overview)

#### Tags

- Contacts
- Deprecated
- Events
- Legacy
- Registration
- SOAP

#### Properties

- [Documentation](https://developers.cvent.com/docs/legacy-api/soap-api/overview)
- [API Reference](https://developers.cvent.com/docs/legacy-api/soap-api/call-definitions/overview)
- [Object Definitions](https://developers.cvent.com/docs/legacy-api/soap-api/object-definitions/overview)
- [Migration Guide](https://developers.cvent.com/docs/rest-api/migration-guide/benefits)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Custom Widgets API

The Cvent Custom Widgets API allows developers to build custom interactive widgets for Cvent Event Registration pages. SDK for widget elements, configuration files, and navigation methods.

- **Human URL:** [https://developers.cvent.com/docs/custom-widgets/overview](https://developers.cvent.com/docs/custom-widgets/overview)

#### Tags

- Customization
- Embedding
- Registration
- Widgets

#### Properties

- [Documentation](https://developers.cvent.com/docs/custom-widgets/overview)
- [GitHub Repository](https://github.com/cvent/custom-widgets-labs)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Single Sign-On (SSO) Integration

Cvent SSO enables identity provider integration via SAML and OpenID Connect for planner login, access portals, event registrant and Attendee Hub, Events+, and portal applications.

- **Human URL:** [https://developers.cvent.com/docs/sso/overview](https://developers.cvent.com/docs/sso/overview)

#### Tags

- Authentication
- Identity
- OpenID Connect
- SAML
- SSO

#### Properties

- [Documentation](https://developers.cvent.com/docs/sso/overview)
- [Concepts](https://developers.cvent.com/docs/sso/explanation/concepts)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent White Label API

The Cvent White Label API enables venues and suppliers to embed Cvent RFP functionality into their own websites with custom branding, theming, and analytics for embedded RFP forms.

- **Human URL:** [https://developers.cvent.com/docs/white-label/overview](https://developers.cvent.com/docs/white-label/overview)

#### Tags

- Branding
- RFP
- White Label
- Widgets

#### Properties

- [Documentation](https://developers.cvent.com/docs/white-label/overview)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cvent Salesforce App

The Cvent Salesforce App integrates Cvent event data with Salesforce CRM, enabling users to view events from Salesforce, invite contacts and leads, and sync attendee data bidirectionally.

- **Human URL:** [https://developers.cvent.com/docs/cvent-salesforce-app/overview](https://developers.cvent.com/docs/cvent-salesforce-app/overview)

#### Tags

- CRM
- Events
- Integration
- Salesforce

#### Properties

- [Documentation](https://developers.cvent.com/docs/cvent-salesforce-app/overview)
- [Getting Started](https://developers.cvent.com/docs/cvent-salesforce-app/app-installation)
- [Authentication](https://developers.cvent.com/docs/cvent-salesforce-app/salesforce-oauth)
- [Postman Collection](collections/cvent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cvent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.cvent.com/)
- [Developer Portal](https://developers.cvent.com/)
- [API Reference](https://developers.cvent.com/docs/rest-api/reference/reference)
- [Authentication](https://developers.cvent.com/docs/rest-api/explanation/authentication)
- [O Auth Token Endpoint](https://api-platform.cvent.com/ea/oauth2/token)
- [Sign Up](https://developers.cvent.com/register)
- [Standards](https://developers.cvent.com/docs/rest-api/reference/api-standards)
- [Changelog](https://developers.cvent.com/docs/rest-api/changelog)
- [Status Page](https://status.cvent.com)
- [Support](https://support.cvent.com/)
- [Pricing](https://www.cvent.com/en/event-management-software/cvent-pricing)
- [Terms of Service](https://www.cvent.com/en/terms-of-use)
- [Privacy Policy](https://www.cvent.com/en/privacy-policy)
- [Security](https://www.cvent.com/en/security)
- [Training](https://www.cvent.com/en/academy)
- [Community](https://community.cvent.com/home)
- [Blog](https://www.cvent.com/en/blog)
- [Git Hub](https://github.com/cvent)
- [Twitter](https://twitter.com/cvent)
- [LinkedIn](https://www.linkedin.com/company/cvent)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**FN:** Cvent Developer Relations
**Email:** developersupport@cvent.com
**URL:** https://developers.cvent.com
