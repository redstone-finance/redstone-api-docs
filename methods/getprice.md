---
description: >-
  getPrice method is used to fetch the latest price for a single or several
  tokens
---

# getPrice

### Get the latest price for a single token

▸ **getPrice**\(`symbol`: _string_, `opts?`: GetPriceOptions\): _Promise&lt;_PriceData&gt;

Returns the latest price for a single symbol

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbol` | _string_ | Token symbol \(string\) |
| `opts?` | GetPriceOptions | Optional params \(object\)  _opts.provider: provider name \(string\)_  opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;PriceData&gt;

The latest price for the token

Defined in: [redstone-api.ts:59](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L59)

### Get the latest price for several tokens

▸ **getPrice**\(`symbols`: _string_\[\], `opts?`: GetPriceOptions\): _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

Returns the latest price for several symbols

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbols` | _string_\[\] | Token symbols \(array of strings\) |
| `opts?` | GetPriceOptions | Optional params \(object\)  _opts.provider: provider name \(string\)_  opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

The latest price for the tokens

Defined in: [redstone-api.ts:70](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L70)

### Examples

#### Get the latest price for a single token

```javascript
const price = await redstone.getPrice("AR");

console.log(price.value); // latest price value for AR token (in USD)
console.log(price.timestamp); // the exact timestamp of the price
```

{% hint style="info" %}
All the prices are denominated in USD. You can fetch price data for BTC, ETH, AR, EUR and any other of [ 100+ supported tokens](docs/ALL_SUPPORTED_TOKENS.md)
{% endhint %}

#### **Price data format** 

```javascript
  {
    value: 123.23, // Number: Price value in USD
    timestamp: 1617146511173, // Number: Timestamp (ms) for price
    provider: "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0", // String: Provider arweave address
    permawebTx: "V8FUU0BG4kVOJwKWHzgkn1aEFm-eanhqqEXfPFY7pmI", // String: Arweave transaction id
    source: {"coingecko": 123,"sushiswap": 123.23,"uniswap": 123.35}, // Object: Prices from different sources
  }
```

####  Fetch price using promises

```javascript
  // As async/await is only a syntactic sugar on Javascript
  // Promises you can use them in a "standard" way
  const price = redstone.getPrice("AR").then((price) => {
    console.log(price.value); // latest price value for AR token
  });

```

#### Get the latest prices for several tokens

To fetch prices for several tokens use the `getPrice` method and pass an array with any subset of [supported tokens](docs/ALL_SUPPORTED_TOKENS.md).

```javascript
const prices = await redstone.getPrice(["BTC", "ETH", "AR", "EUR"]);

console.log(prices); // Example output below
/*
{
  "BTC": {
    value: 58953.39,
    timestamp: 1617152802779,
    ...
  },
  "ETH": {
    value: 1856.75,
    timestamp: 1617152802779,
    ...
  },
  ...
}
*/


console.log(prices["BTC"].value); // latest price value for BTC
console.log(prices["ETH"].value); // latest price value for ETH
console.log(prices["AR"].value); // latest price value for AR
```

