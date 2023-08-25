# price

<!-- Start SDK Installation -->
## SDK Installation

### NPM

```bash
npm add https://github.com/speakeasy-sdks/tras
```

### Yarn

```bash
yarn add https://github.com/speakeasy-sdks/tras
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->


```typescript
import { Price } from "price";
import { GetPingResponse } from "price/dist/sdk/models/operations";

const sdk = new Price({
  security: {
    application: "",
  },
});

sdk.getPing().then((res: GetPingResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## Available Resources and Operations

### [Price SDK](docs/sdks/price/README.md)

* [getPing](docs/sdks/price/README.md#getping) - Server heartbeat operation
* [postPrice](docs/sdks/price/README.md#postprice) - get indicative quote price
<!-- End SDK Available Operations -->

### Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

### Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
