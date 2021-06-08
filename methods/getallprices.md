---
description: >-
  getAllPrices method can be used to fetch the latest price for all the
  available tokens
---

# getAllPrices

## Get the latest price for all tokens

▸ **getAllPrices**\(`opts?`: GetPriceOptions\): _Promise_&lt;{ \[symbol: string\]: PriceData; }&gt;

Returns the latest price for all the supported symbols

**Parameters:**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Default value</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>opts</code>
      </td>
      <td style="text-align:left">GetPriceOptions</td>
      <td style="text-align:left">{}</td>
      <td style="text-align:left">
        <p>An optional options object.</p>
        <ul>
          <li><em>opts.provider:</em> provider name (string)</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;{ \[symbol: string\]: PriceData; }&gt;

The latest price for all the supported tokens

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

