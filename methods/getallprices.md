---
description: >-
  getAllPrices method can be used to fetch the latest price for all available
  tokens
---

# getAllPrices

## Get the latest price for all tokens

▸ **getAllPrices**\(`opts?`: GetPriceOptions\): _Promise_&lt;{ \[symbol: string\]: PriceData; }&gt;

Returns the latest price for all the supported symbols

**Parameters:**

| Name | Type | Default value | Description |
| :--- | :--- | :--- | :--- |
| `opts` | GetPriceOptions | {} | Optioanl options object.  _opts.provider: provider name \(string\)_  opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;{ \[symbol: string\]: PriceData; }&gt;

The latest price for all the supported tokens

Defined in: [redstone-api.ts:202](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L202)

## Examples

### Get prices for all available tokens

To fetch the latest prices for all available tokens use the `getAllPrices` method.

```javascript
const prices = await redstone.getAllPrices();

console.log(prices); // Example output below
/*
{
  "BTC": {...},
  "ETH": {...},
  ...
}
*/

console.log(prices["AR"].value); // latest price value for AR
console.log(prices["EUR"].value); // latest price value for EUR
```

