# Price SDK

## Overview

Brolli Application Flow OAuth2 Project: This is an example of using OAuth2 Application Flow in a specification to describe security to your API.

### Available Operations

* [getPing](#getping) - Server heartbeat operation
* [postPrice](#postprice) - get indicative quote price

## getPing

Heart beat function to check if the server is up and running.

### Example Usage

```typescript
import { Price } from "price";
import { GetPingResponse } from "price/dist/sdk/models/operations";

const sdk = new Price({
  security: {
    application: "",
  },
});

sdk.price.getPing().then((res: GetPingResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

### Parameters

| Parameter                                                    | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `config`                                                     | [AxiosRequestConfig](https://axios-http.com/docs/req_config) | :heavy_minus_sign:                                           | Available config options for making requests.                |


### Response

**Promise<[operations.GetPingResponse](../../models/operations/getpingresponse.md)>**


## postPrice

This is get price with request body

### Example Usage

```typescript
import { Price } from "price";
import { PostPriceResponse } from "price/dist/sdk/models/operations";
import { PropertyDetailsProduct } from "price/dist/sdk/models/shared";

const sdk = new Price({
  security: {
    application: "",
  },
});

sdk.price.postPrice({
  calimsHistory: {
    perilLastthreeyrs: 548814,
    perillastyear: 592845,
  },
  policyHolders: [
    {
      policyHoldersAge: 8442.66,
    },
    {
      policyHoldersAge: 6027.63,
    },
    {
      policyHoldersAge: 8579.46,
    },
  ],
  propertyAddress: {
    city: "Roselynview",
    country: "Netherlands Antilles",
    postCode: "34280-9234",
    state: "minus",
    street: "545 Tianna Stream",
    street2: "ab",
  },
  propertyDetails: {
    buildingAge: 3373.96,
    builtYear: 871.29,
    campaginCode: "deserunt",
    coverageType: [
      "["Contents Only","Building Only"]",
    ],
    dwellingType: [
      "["Freestanding house","Unit, flat or apartment","Townhouse or villa","Semi detached, duplex or terrace","Caravan, mobile or relocatable home","Triplex or fourplex","Block of units, flats, or apartments","Houseboat","Shipping container or shed"]",
      "["Freestanding house","Unit, flat or apartment","Townhouse or villa","Semi detached, duplex or terrace","Caravan, mobile or relocatable home","Triplex or fourplex","Block of units, flats, or apartments","Houseboat","Shipping container or shed"]",
    ],
    loggingId: "dfc2ddf7-cc78-4ca1-ba92-8fc816742cb7",
    numberOfStoreys: 2165.5,
    occupancyType: [
      "["Landord","Formal Lease"]",
      "["Landord","Formal Lease"]",
      "["Landord","Formal Lease"]",
    ],
    partner: "20592939-6fea-4759-aeb1-0faaa2352c59",
    product: [
      PropertyDetailsProduct.Home,
      PropertyDetailsProduct.Landlord,
    ],
    roofType: [
      "["that","this"]",
    ],
    starteOrTerritory: "iure",
    strataTitle: false,
    swimmingPool: [
      "["Pool or spa in-ground or with fixed decking","Pool or spa relocatable above ground"]",
      "["Pool or spa in-ground or with fixed decking","Pool or spa relocatable above ground"]",
      "["Pool or spa in-ground or with fixed decking","Pool or spa relocatable above ground"]",
    ],
    wallType: [
      "["that","this"]",
      "["that","this"]",
      "["that","this"]",
      "["that","this"]",
    ],
  },
}).then((res: PostPriceResponse) => {
  if (res.statusCode == 200) {
    // handle response
  }
});
```

### Parameters

| Parameter                                                    | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `request`                                                    | [shared.Price](../../models/shared/price.md)                 | :heavy_check_mark:                                           | The request object to use for the request.                   |
| `config`                                                     | [AxiosRequestConfig](https://axios-http.com/docs/req_config) | :heavy_minus_sign:                                           | Available config options for making requests.                |


### Response

**Promise<[operations.PostPriceResponse](../../models/operations/postpriceresponse.md)>**

