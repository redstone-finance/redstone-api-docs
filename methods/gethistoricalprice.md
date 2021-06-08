---
description: >-
  getHistoricalPrice method is used to fetch historical prices. It can fetch
  prices in a time range for a single or multiple tokens
---

# getHistoricalPrice

### Get a single historical price for a single token

▸ **getHistoricalPrice**\(`symbol`: _string_, `opts`: GetHistoricalPriceOptions\): _Promise_&lt;PriceData&gt;

Returns the historical price for a single token

**`remarks`** Full list of supported tokens is available [here](https://github.com/redstone-finance/redstone-api/blob/main/docs/ALL_SUPPORTED_TOKENS.md)

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
      <td style="text-align:left"><code>opts</code>
      </td>
      <td style="text-align:left">GetHistoricalPriceOptions</td>
      <td style="text-align:left">
        <p>Optional params (object)</p>
        <ul>
          <li><em>opts.date: </em>Date for the historical price</li>
          <li><em>opts.provider</em>: provider name (string) *</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;PriceData&gt;

The historical price for token

Defined in: [redstone-api.ts:116](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L116)

### Get historical price in a time range for a single token

▸ **getHistoricalPrice**\(`symbol`: _string_, `opts`: GetHistoricalPriceForIntervalOptions\): _Promise_&lt;PriceData\[\]&gt;

Returns the historical prices for a token in a time range with the specified interval

**`remarks`** This method can be used to display charts with historical prices. Full list of supported tokens is available [here](https://github.com/redstone-finance/redstone-api/blob/main/docs/ALL_SUPPORTED_TOKENS.md)

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
      <td style="text-align:left">Token symbol</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>opts</code>
      </td>
      <td style="text-align:left">GetHistoricalPriceForIntervalOptions</td>
      <td style="text-align:left">
        <p>Options object. It must contain <em>startDate</em>, <em>endDate</em>, and <em>interval</em> properties.</p>
        <ul>
          <li><em>opts.startDate: </em>Start time for the time range (date | timestamp
            | string)</li>
          <li><em>opts.endDate</em>: End time for the time range (date | timestamp |
            string) <em> </em>
          </li>
          <li><em>opts.interval: Interval in milliseconds (number) </em>
          </li>
          <li><em>opts.provider:</em> provider name (string)</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;PriceData\[\]&gt;

The historical prices for the symbol with the passed interval

Defined in: [redstone-api.ts:138](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L138)

### Get a single historical price for several tokens

▸ **getHistoricalPrice**\(`symbols`: _string_\[\], `opts`: GetHistoricalPriceOptions\): _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

Returns the historical prices for several tokens

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
      <td style="text-align:left">Array of token symbols</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>opts</code>
      </td>
      <td style="text-align:left">GetHistoricalPriceOptions</td>
      <td style="text-align:left">
        <p>Options object. It must contain the date property.</p>
        <ul>
          <li><em>opts.date: </em>Date for the historical price (date | timestamp |
            string)</li>
          <li><em>opts.provider</em>: provider name (string)</li>
          <li><em>opts.verifySignature</em>: enable signature verification (boolean)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Returns:** _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

The historical prices for multiple tokens

Defined in: [redstone-api.ts:153](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L153)

### Examples

#### Get the historical price for a single token

To get the historical price use the `getHistoricalPrice` method.

```javascript
const price = await redstone.getHistoricalPrice("AR", {
  date: "2021-03-30T12:35:09", // Any convertable to date type
});

console.log(price.value); // AR price for specific time
```

{% hint style="info" %}
The `date` argument must be convertable to the Date type. You may pass a date \(e.g. `new Date(2021-04-01)`\), a timestamp \(e.g. `1617709771289`\), or just a string \(e.g. `2021-04-01` or `2021-04-01T12:30:58`\)
{% endhint %}

#### Get the historical price for several tokens

To fetch the historical price for several tokens pass an array of symbols to `getHistoricalPrice` method.

```javascript
const symbols = ["AR", "BTC", "UNI", "ETH", "EUR"];
const prices = await redstone.getHistoricalPrice(symbols, {
  date: "2021-03-30T12:35:09",
});

console.log(prices["BTC"].value); // BTC price for specific time
```

#### Get the historical prices in a time range

To fetch the historical prices in a time range specify token symbol as the first argument of the `getHistoricalPrice` method, and `startDate`, `endDate` and `interval` as fields of the second argument.

{% hint style="info" %}
Currently Redstone API supports fetching historical prices in a time range only for a single token
{% endhint %}

```javascript
const prices = await redstone.getHistoricalPrice("AR", {
  startDate: "2021-03-29T12:35:09",
  endDate: "2021-03-30T12:35:09",
  interval: 3600 * 1000, // 1 hour
});

console.log(prices); // Example output below
/*
[
  {
    value: 28.8,
    timestamp: 1617016995624,
    ...
  },
  {
    value: 28.59,
    timestamp: 1617014111705,
    ...
  },
  ...
]
*/
```

{% hint style="info" %}
The `startDate` and `endDate` arguments must be convertable to Date type.
{% endhint %}

