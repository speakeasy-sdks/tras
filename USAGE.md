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