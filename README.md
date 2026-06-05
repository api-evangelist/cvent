# Cvent (cvent)

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
