---
description: >-
  getHistoricalPrice method is used to fetch historical prices data. It can
  fetch prices in a time range for a single token or a historical price for
  single or several tokens
---

# getHistoricalPrice

## Get a single historical price for a single token

▸ **getHistoricalPrice**\(`symbol`: _string_, `opts`: GetHistoricalPriceOptions\): _Promise_&lt;PriceData&gt;

Returns the historical price for a single token

**`remarks`** Full list of supported tokens is available at [https://github.com/redstone-finance/redstone-api/blob/main/ALL\_SUPPORTED\_TOKENS.md](https://github.com/redstone-finance/redstone-api/blob/main/ALL_SUPPORTED_TOKENS.md)

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbol` | _string_ | Token symbol \(string\) |
| `opts` | GetHistoricalPriceOptions | Optional params \(object\)  _opts.date: Date for the historical price_  opts.provider: provider name \(string\) \* opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;PriceData&gt;

The historical price for token

Defined in: [redstone-api.ts:116](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L116)

## Get historical price in a time range for a single token

▸ **getHistoricalPrice**\(`symbol`: _string_, `opts`: GetHistoricalPriceForIntervalOptions\): _Promise_&lt;PriceData\[\]&gt;

Returns the historical prices for a token in a time range with the specified interval

**`remarks`** This method can be used to display charts with historical prices. Full list of supported tokens is available at [https://github.com/redstone-finance/redstone-api/blob/main/ALL\_SUPPORTED\_TOKENS.md](https://github.com/redstone-finance/redstone-api/blob/main/ALL_SUPPORTED_TOKENS.md)

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbol` | _string_ | Token symbol |
| `opts` | GetHistoricalPriceForIntervalOptions | Options object. It must contain startDate, endDate, and interval properties.  _opts.startDate: Start time for the time range \(date \| timestamp \| string\)_  opts.endDate: End time for the time range \(date \| timestamp \| string\)  _opts.interval: Interval in milliseconds \(number\)_  opts.provider: provider name \(string\) \* opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;PriceData\[\]&gt;

The historical prices for the symbol with the passed interval

Defined in: [redstone-api.ts:138](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L138)

## Get a single historical price for several tokens

▸ **getHistoricalPrice**\(`symbols`: _string_\[\], `opts`: GetHistoricalPriceOptions\): _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

Returns the historical prices for several tokens

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbols` | _string_\[\] | Array of token symbols |
| `opts` | GetHistoricalPriceOptions | Options object. It must contain the date property.  _opts.date: Date for the historical price \(date \| timestamp \| string\)_  opts.provider: provider name \(string\) \* opts.verifySignature: enable signature verification \(boolean\) |

**Returns:** _Promise_&lt;{ \[token: string\]: PriceData; }&gt;

The historical prices for several tokens

Defined in: [redstone-api.ts:153](https://github.com/redstone-finance/redstone-api/blob/6ba5e3a/src/redstone-api.ts#L153)

## Examples

### Get the historical price for a single token

To get the historical price use the `getHistoricalPrice` method.

```javascript
const price = await redstone.getHistoricalPrice("AR", {
  date: "2021-03-30T12:35:09", // Any convertable to date type
});

console.log(price.value); // AR price for specific time
```

{% hint style="info" %}
The `date` argument must be convertable to Date type. You may pass date \(e.g. `new Date(2021-04-01)`\), timestamp \(e.g. `1617709771289`\), or just string \(e.g. `2021-04-01` or `2021-04-01T12:30:58`\)
{% endhint %}

### Get the historical price for several tokens

To fetch the historical price for several tokens pass an array of symbols to `getHistoricalPrice` method.

```javascript
const symbols = ["AR", "BTC", "UNI", "ETH", "EUR"];
const prices = await redstone.getHistoricalPrice(symbols, {
  date: "2021-03-30T12:35:09",
});

console.log(prices["BTC"].value); // BTC price for specific time
```

### Get the historical prices in a time range

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

