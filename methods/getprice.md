---
description: >-
  getPrice method is used to fetch the latest price for a single or multiple
  tokens
---

# getPrice

## Get the latest price for a single token

▸ **getPrice**\(`symbol`: _string_, `opts?`: GetPriceOptions\): \_Promise&lt;\_PriceData&gt;

Returns the latest price for a single symbol

**Parameters:**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>symbol</code>
      </td>
      <td style="text-align:left"><em>string</em>
      </td>
      <td style="text-align:left">Token symbol (string)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>opts?</code>
      </td>
      <td style="text-align:left">GetPriceOptions</td>
      <td style="text-align:left">
        <p>Optional params (object)</p>
        <ul>
          <li><em>opts.provider:</em> provider name (string)</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;PriceData&gt;

The latest price for the token

## Get the latest price for multiple tokens

▸ **getPrice**\(`symbols`: _string_\[\], `opts?`: GetPriceOptions\): _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

Returns the latest price for several symbols

**Parameters:**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>symbols</code>
      </td>
      <td style="text-align:left"><em>string</em>[]</td>
      <td style="text-align:left">Token symbols (array of strings)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>opts?</code>
      </td>
      <td style="text-align:left">GetPriceOptions</td>
      <td style="text-align:left">
        <p>Optional params (object)</p>
        <ul>
          <li><em>opts.provider:</em> provider name (string)</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

The latest price for the tokens

## Examples

### Get the latest price for a single token

```javascript
const price = await redstone.getPrice("AR");

console.log(price.value); // latest price value for AR token (in USD)
console.log(price.timestamp); // the exact timestamp of the price
```

{% hint style="info" %}
All the prices are denominated in USD. You can fetch price data for BTC, ETH, AR, EUR and any other of  [100+ supported tokens](https://github.com/redstone-finance/redstone-api/blob/main/docs/ALL_SUPPORTED_TOKENS.md)
{% endhint %}

### **Price data format**

```javascript
  {
    value: 123.23, // Number: Price value in USD
    timestamp: 1617146511173, // Number: Timestamp (ms) for price
    provider: "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0", // String: Provider arweave address
    permawebTx: "V8FUU0BG4kVOJwKWHzgkn1aEFm-eanhqqEXfPFY7pmI", // String: Arweave transaction id
    source: {"coingecko": 123,"sushiswap": 123.23,"uniswap": 123.35}, // Object: Prices from different sources
  }
```

### Fetch price using promises

```javascript
  // As async/await is only a syntactic sugar on Javascript
  // Promises you can use them in a "standard" way
  const price = redstone.getPrice("AR").then((price) => {
    console.log(price.value); // latest price value for AR token
  });
```

### Get the latest prices for multiple tokens

To fetch prices for multiple tokens use the `getPrice` method and pass an array with a subset of [supported tokens](https://github.com/redstone-finance/redstone-api/blob/main/docs/ALL_SUPPORTED_TOKENS.md).

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

