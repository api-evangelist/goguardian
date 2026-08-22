# GoGuardian (goguardian)

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
