# BMW ConnectedDrive

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

BMW ConnectedDrive is BMW Group's umbrella for connected vehicle services spanning navigation, remote services, intelligent emergency call, ConnectedDrive Store add-ons, and the My BMW app. Programmatic access for customers, third-party developers, and the repair-and-maintenance ecosystem is consolidated under the BMW Open Data Platform / BMW CarData. CarData exposes an OAuth 2.0 Device Code Flow protected REST API at api-cardata.bmwgroup.com for retrieving static vehicle metadata (basicData), telematics, charging history, smart maintenance tyre diagnosis, location-based charging settings, vehicle images, and managing data "containers" that scope which telematics descriptors a client is authorized to read. A companion MQTT 3.1.1 streaming service at customer.streaming-cardata.bmwgroup.com:9000 (TLS) pushes live container data on the per-VIN topic `{gcid}/{vin}`. CarData is the EU regulatory successor to the legacy BMW ConnectedDrive REST endpoints used by the My BMW app and is the canonical surface for third-party automotive integrations, including independent repair, fleet, charging, and home-automation use cases.

**Areas:** Automotive · Connected Vehicles · Telematics · Vehicle Data · CarData · ConnectedDrive · Electric Vehicles · Charging · MQTT · Streaming · Authentication · Device Code Flow

## BMW ConnectedDrive on APIs.io

Everything profiled for BMW ConnectedDrive is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bmw-connecteddrive/](https://apis.io/providers/bmw-connecteddrive/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [BMW CarData Streaming API](https://apis.io/apis/bmw-connecteddrive/bmw-cardata-streaming-api/) — The BMW CarData Streaming API delivers near-real-time vehicle telematics over MQTT 3.1.1 with TLS. Clients connect to…
- [BMW CarData Third-Party API](https://apis.io/apis/bmw-connecteddrive/bmw-cardata-thirdparty-api/) — The third-party variant of BMW CarData targets independent service providers — repair shops, charging operators, fleet platforms, insurance, and aftermarket…
- [BMW ConnectedDrive Containers API](https://apis.io/apis/bmw-connecteddrive/bmw-connecteddrive-containers-api/) — Management of containers
- [BMW ConnectedDrive Vehicles API](https://apis.io/apis/bmw-connecteddrive/bmw-connecteddrive-vehicles-api/) — Access vehicle data and information

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bmw Connecteddrive Agentic Access](https://apis.io/agentic-access/bmw-connecteddrive/bmw-connecteddrive-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [CARDATA API](https://apis.io/collections/bmw-connecteddrive/open-bmw-cardata-customer-api/)
- [CARDATA Containers API](https://apis.io/collections/bmw-connecteddrive/open-bmw-connecteddrive-containers-api/)
- [CARDATA Containers Vehicles API](https://apis.io/collections/bmw-connecteddrive/open-bmw-connecteddrive-vehicles-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Bmw Connecteddrive Authentication](https://apis.io/security/bmw-connecteddrive/bmw-connecteddrive-authentication/)
- [Bmw Connecteddrive Domain Security](https://apis.io/security/bmw-connecteddrive/bmw-connecteddrive-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.bmwgroup.com/)
- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)
- [Blog](https://www.press.bmwgroup.com/global/rss)
- [Terms of service](https://www.bmw.com/en/footer/metanavigation/legal-notice-pool/legal-notice.html)
- [Privacy policy](https://www.bmw.com/en/footer/metanavigation/privacy-policy.html)
- [GitHub](https://github.com/bmwcarit)

## API Evangelist rating

**Kin Score 28.7** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 58.0 |
| Contract quality | 47.1 |
| Contract governance | 0.0 |
| Operational transparency | 2.6 |
| Developer ergonomics | 33.3 |
| Access clarity | 23.7 |

**Agent readiness 23.0** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bmw-connecteddrive/](https://apis.io/providers/bmw-connecteddrive/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for BMW ConnectedDrive: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bmw-connecteddrive/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
