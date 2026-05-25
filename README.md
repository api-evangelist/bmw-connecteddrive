# bmw-connecteddrive

BMW ConnectedDrive — connected vehicle services and the BMW CarData API (REST + MQTT streaming) over OAuth 2.0 Device Code Flow against GCDM.

## APIs

- **BMW CarData Customer API** — REST at `https://api-cardata.bmwgroup.com` (header `x-version: v1`) for vehicle mappings, basic data, telematic data, charging history, smart maintenance tyre diagnosis, location-based charging settings, vehicle images, and CarData container management. See [`openapi/bmw-cardata-customer-api-openapi.json`](openapi/bmw-cardata-customer-api-openapi.json).
- **BMW CarData Streaming API** — MQTT 3.1.1 over TLS at `customer.streaming-cardata.bmwgroup.com:9000`, topic `{gcid}/{vin}`, gated by the `cardata:streaming:read` scope and a container subscription.
- **BMW CarData Third-Party API** — same REST/MQTT surface for independent service providers, repair shops, charging operators, and fleet platforms acting under customer consent and the EU Data Act / right-to-repair framework.

## Authentication

OAuth 2.0 Device Code Flow against BMW GCDM. Scopes: `cardata:api:read`, `cardata:streaming:read`, plus `openid` and `authenticate_user`. ID tokens expire after one hour and are refreshed via the standard OAuth refresh-token grant. After client-ID generation a developer must subscribe the client to each CarData service so the matching scope is provisioned.

## Links

- Open Data Platform / CarData: https://bmw-cardata.bmwgroup.com/
- Customer API docs: https://bmw-cardata.bmwgroup.com/customer/public/api-documentation
- Third-party API docs: https://bmw-cardata.bmwgroup.com/thirdparty/public/car-data/technical-configuration/api-documentation
- BMW Car IT GitHub (joynr, ramses, MoCOCrW, python-dlt): https://github.com/bmwcarit
