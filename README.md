# GoGuardian (goguardian)

GoGuardian is a K-12 education technology company. Its suite - **Admin** (DNS and device content filtering for CIPA compliance across ChromeOS, Windows, and macOS), **Teacher** (classroom management and student engagement), and **Beacon** (student safety and suicide / self-harm risk detection) - is administered through web dashboards rather than a broadly published public developer API.

**Access model (important):** GoGuardian's own outbound developer API surface is **partner / district gated**. There is no public self-serve developer signup that yields an API key against a documented GoGuardian REST catalog. GoGuardian's documented integration model is primarily *consumer-side roster ingestion*: it syncs organizations (OUs), students, teachers, guardians, classes, and enrollments from a district's Student Information System via the 1EdTech **OneRoster 1.1 REST API** (using a Consumer ID / Secret and a OneRoster URL), and via **Clever**, **ClassLink**, and **Google Classroom**. The "Enable API Access" help articles concern enabling **Google Workspace / Google Admin APIs for GoGuardian to consume**, not exposing a GoGuardian API. A developer / partner documentation portal exists at **based.goguardian.com** ("GoGuardian Based Docs"), but it did not expose an openly enumerable public REST reference, base URL, or self-serve API-key flow at review time.

The API entries below are **honestly modeled logical surfaces (`endpointsModeled`)**, not a confirmed public REST endpoint catalog.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/goguardian/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/goguardian/refs/heads/main/apis.yml)

## Tags

- Education
- EdTech
- K-12
- Content Filtering
- Classroom Management
- Student Safety
- Rostering
- OneRoster
- Partner API

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs (modeled)

### GoGuardian Rostering Integration (OneRoster / Clever / ClassLink)

Consumer-side roster synchronization. GoGuardian ingests organizations (OUs), students, teachers, guardians, classes, and enrollments from a district's Student Information System via the OneRoster 1.1 REST API (configured with a Consumer ID, Consumer Secret, and a OneRoster base URL), or via Clever, ClassLink, and Google Classroom. This is GoGuardian pulling standards-based roster data, not a GoGuardian-owned REST API.

- **Human URL:** [https://support.goguardian.com/s/article/Integration-with-OneRoster](https://support.goguardian.com/s/article/Integration-with-OneRoster)

#### Properties

- [Documentation - OneRoster Integration](https://support.goguardian.com/s/article/Integration-with-OneRoster)
- [Documentation - Clever & ClassLink FAQ](https://support.goguardian.com/s/article/Clever-and-ClassLink-Integrations-FAQ-1629765161385)
- [Documentation - OneRoster Announcement](https://www.goguardian.com/product-update/oneroster-integration)

### GoGuardian Based Developer / Partner API

GoGuardian maintains a developer / integration documentation portal at based.goguardian.com ("GoGuardian Based Docs"). Access to GoGuardian's outbound developer surface is partner-gated - there is no openly enumerable public REST reference, base URL, or self-serve API key flow published for third-party developers as of the review date. Documented as a gated developer surface; endpoints modeled, not confirmed.

- **Human URL:** [https://based.goguardian.com/](https://based.goguardian.com/)

#### Properties

- [Documentation - Based Docs](https://based.goguardian.com/)
- [Documentation - Enable API Access](https://support.goguardian.com/s/article/Enable-API-Access-1629763558239)

### GoGuardian Beacon Alerts (Student Safety)

GoGuardian Beacon analyzes student browsing (and, via a Google Docs API integration, document) activity to detect signals of suicide, self-harm, and other safety risk, then routes time-stamped alerts through dashboard, email, and SMS notifications with configurable escalation paths. Beacon's alerting is configured and consumed through the Admin dashboard and notification channels rather than a published public alerts REST API.

- **Human URL:** [https://support.goguardian.com/s/goguardian-beacon](https://support.goguardian.com/s/goguardian-beacon)

#### Properties

- [Documentation - Beacon](https://support.goguardian.com/s/goguardian-beacon)
- [Documentation - Beacon Google Docs API Integration](https://www.goguardian.com/product-update/beacon-adds-google-docs-api-integration)

## Common Properties

- [GitHub Organization](https://github.com/goguardian)
- [LinkedIn](https://www.linkedin.com/company/goguardian)
- [Website](https://www.goguardian.com/)
- [Documentation - Based Docs](https://based.goguardian.com/)
- [Support / Help Center](https://support.goguardian.com/s/)
- [Pricing](https://www.goguardian.com/pricing)
- [Blog](https://www.goguardian.com/blog)

## Pricing

GoGuardian does not publish standard pricing. It is **contact-sales, per-student**, with volume and multi-year term discounts (widely reported in the roughly $1.50-$6.00 per student / month range depending on bundle and term). There is no published developer API plan or metered API pricing.

## WebSocket Review

Does GoGuardian expose a documented public WebSocket API? **No.** See `review.yml`. GoGuardian publishes no WebSocket (ws:// / wss://) API; realtime behavior (live class views, Beacon alerts) is delivered inside GoGuardian's own hosted UI and notification channels, not as a public server-push transport.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
