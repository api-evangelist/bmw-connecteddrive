# BMW ConnectedDrive (bmw-connecteddrive)

BMW ConnectedDrive is BMW Group's umbrella for connected vehicle services spanning navigation, remote services, intelligent emergency call, ConnectedDrive Store add-ons, and the My BMW app. Programmatic access for customers, third-party developers, and the repair-and-maintenance ecosystem is consolidated under the BMW Open Data Platform / BMW CarData. CarData exposes an OAuth 2.0 Device Code Flow protected REST API at api-cardata.bmwgroup.com for retrieving static vehicle metadata (basicData), telematics, charging history, smart maintenance tyre diagnosis, location-based charging settings, vehicle images, and managing data "containers" that scope which telematics descriptors a client is authorized to read. A companion MQTT 3.1.1 streaming service at customer.streaming-cardata.bmwgroup.com:9000 (TLS) pushes live container data on the per-VIN topic `{gcid}/{vin}`. CarData is the EU regulatory successor to the legacy BMW ConnectedDrive REST endpoints used by the My BMW app and is the canonical surface for third-party automotive integrations, including independent repair, fleet, charging, and home-automation use cases.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bmw-connecteddrive/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bmw-connecteddrive/refs/heads/main/apis.yml)

## Scope

- **Type:** Provider
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Automotive
- Connected Vehicle
- Telematics
- Vehicle Data
- CarData
- ConnectedDrive
- Electric Vehicles
- Charging
- MQTT
- Streaming
- OAuth
- Device Code Flow
- GDPR
- Right To Repair
- Mobility

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### BMW CarData Customer API

The BMW CarData Customer API lets an authenticated BMW customer (or a delegate acting on their behalf via the customer portal) read vehicle metadata and telematics for the VINs mapped to their BMW ID account. Endpoints cover vehicle mappings, basic data, telematic data, charging history, smart-maintenance tyre diagnosis, location-based charging settings, vehicle images, and CRUD over CarData "containers" that define which descriptors a client subscribes to. Authentication uses the GCDM (Global Customer Data Management) bearer token obtained via the OAuth 2.0 Device Code Flow against the `cardata:api:read` scope. The base URL is `https://api-cardata.bmwgroup.com` with header `x-version: v1`. ID tokens are valid for one hour and must be refreshed via the standard OAuth refresh-token grant.

- **Human URL:** [https://bmw-cardata.bmwgroup.com/customer/public/api-documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)
- **Base URL:** `https://api-cardata.bmwgroup.com`

#### Tags

- CarData
- Vehicles
- Telematics
- Containers
- Charging
- OAuth

#### Properties

- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)
- [OpenAPI](openapi/bmw-cardata-customer-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bmw-cardata-customer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bmw-cardata-customer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-specification)

### BMW CarData Streaming API

The BMW CarData Streaming API delivers near-real-time vehicle telematics over MQTT 3.1.1 with TLS. Clients connect to `customer.streaming-cardata.bmwgroup.com` on port 9000, authenticate with their GCID as the MQTT username and a GCDM access token (scope `cardata:streaming:read`) as the password, and subscribe to the per-vehicle topic `{gcid}/{vin}`. The set of descriptors streamed is controlled by the container(s) the client has registered via the CarData REST API, allowing a customer to scope exactly which signals (e.g. state of charge, mileage, doors, location) flow to each third-party integration. The streaming surface is the recommended path for charging optimizers, home-automation hubs, and fleet telematics back-ends that need event-driven updates instead of polled reads.

- **Human URL:** [https://bmw-cardata.bmwgroup.com/customer/public/api-documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)

#### Tags

- CarData
- Streaming
- MQTT
- Telematics
- Real-Time

#### Properties

- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)
- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-specification)
- [Postman Collection](collections/bmw-cardata-customer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bmw-cardata-customer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### BMW CarData Third-Party API

The third-party variant of BMW CarData targets independent service providers — repair shops, charging operators, fleet platforms, insurance, and aftermarket integrators — who consume vehicle data on behalf of customers who have explicitly consented through the BMW Open Data Platform. Third parties register a client, subscribe to one or more CarData services (which assigns the corresponding scope to the client ID), and then drive their users through the OAuth 2.0 Device Code Flow to obtain customer consent. The third-party surface reuses the same REST and MQTT endpoints as the Customer API but is bounded by the data-minimization rules of the BMW Open Data Platform and the EU Data Act / right-to-repair framework.

- **Human URL:** [https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-documentation)

#### Tags

- CarData
- Third-Party
- Vehicles
- Telematics
- Right To Repair

#### Properties

- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-documentation)
- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-specification)
- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/repair-and-maintenance/technical-configuration/api-documentation)
- [Postman Collection](collections/bmw-cardata-customer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bmw-cardata-customer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.bmw.com)
- [Portal](https://www.bmwgroup.com)
- [Portal](https://bmw-cardata.bmwgroup.com/)
- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-documentation)
- [Documentation](https://bmw-cardata.bmwgroup.com/customer/public/api-specification)
- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-documentation)
- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-specification)
- [Documentation](https://bmw-cardata.bmwgroup.com/thirdparty/public/repair-and-maintenance/technical-configuration/api-documentation)
- [Sign Up](https://bmw-cardata.bmwgroup.com/customer)
- [Sign Up](https://bmw-cardata.bmwgroup.com/thirdparty)
- [Authentication](https://customer.bmwgroup.com/oneid/login)
- [Connected Drive](https://www.bmw.com/en/explore-bmw/connected-drive.html)
- [Connected Drive Store](https://customer.bmwgroup.com/store/)
- [My B M W](https://www.bmw.com/en/footer/my-bmw-app.html)
- [GitHub Organization](https://github.com/bmwcarit)
- [GitHub Organization](https://github.com/bmwgroup)
- [Privacy Policy](https://www.bmw.com/en/footer/metanavigation/privacy-policy.html)
- [Terms of Service](https://www.bmw.com/en/footer/metanavigation/legal-notice-pool/legal-notice.html)
- [Press](https://www.press.bmwgroup.com)
- [Newsroom](https://www.bmwgroup.com/en/news.html)
- [Twitter](https://twitter.com/BMWGroup)
- [LinkedIn](https://www.linkedin.com/company/bmw-group)
- [YouTube](https://www.youtube.com/@BMWGroup)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
