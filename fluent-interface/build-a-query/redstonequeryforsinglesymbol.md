# RedstoneQueryForSingleSymbol

[redstone-api](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/README.md) / [Exports](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/modules.md) / RedstoneQueryForSingleSymbol

## Class: RedstoneQueryForSingleSymbol

### Hierarchy

* [_RedstoneQueryForSingleOrSeveralSymbols_](redstonequeryforsingleorseveralsymbols.md)

  ↳ **RedstoneQueryForSingleSymbol**

### Table of contents

#### Constructors

* [constructor](redstonequeryforsinglesymbol.md#constructor)

#### Properties

* [params](redstonequeryforsinglesymbol.md#params)

#### Methods

* [atDate](redstonequeryforsinglesymbol.md#atdate)
* [forLastDays](redstonequeryforsinglesymbol.md#forlastdays)
* [forLastHours](redstonequeryforsinglesymbol.md#forlasthours)
* [fromDate](redstonequeryforsinglesymbol.md#fromdate)
* [getExecutableQuery](redstonequeryforsinglesymbol.md#getexecutablequery)
* [hoursAgo](redstonequeryforsinglesymbol.md#hoursago)
* [latest](redstonequeryforsinglesymbol.md#latest)
* [toDate](redstonequeryforsinglesymbol.md#todate)

### Constructors

#### constructor

* **new RedstoneQueryForSingleSymbol**\(`params`: QueryParams\): [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

**Parameters:**

| Name | Type |
| :--- | :--- |
| `params` | QueryParams |

**Returns:** [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

Overrides: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

### Properties

#### params

• `Protected` **params**: QueryParams

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md).[params](redstonequeryforsingleorseveralsymbols.md#params)

### Methods

#### atDate

▸ **atDate**\(`date`: ConvertableToDate\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price for a specific date.

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `date` | ConvertableToDate | Date for the historical price \(date \| timestamp \| string\) |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

#### forLastDays

▸ **forLastDays**\(`daysCount`: _number_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price for the last few days

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `daysCount` | _number_ | Number of days in the time range |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

#### forLastHours

▸ **forLastHours**\(`hoursCount`: _number_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price for the last few hours

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `hoursCount` | _number_ | Number of hours in the time range |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

#### fromDate

▸ **fromDate**\(`date`: ConvertableToDate\): [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

Configures query to fetch the price in a time range. It is important to use fromDate with toDate query methods

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `date` | ConvertableToDate | Start date/time for the time range |

**Returns:** [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

query object

#### getExecutableQuery

▸ `Protected`**getExecutableQuery**\(`update`: _any_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

**Type parameters:**

| Name |
| :--- |
| `T` |

**Parameters:**

| Name | Type |
| :--- | :--- |
| `update` | _any_ |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

#### hoursAgo

▸ **hoursAgo**\(`hoursCount`: _number_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price for X hours ago.

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `hoursCount` | _number_ | Number of hours ago |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

#### latest

▸ **latest**\(\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the latest price/prices It doesn't support any params

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

#### toDate

▸ **toDate**\(`date`: ConvertableToDate\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price in a time range. toDate method should go after the fromDate

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `date` | ConvertableToDate | End date/time for the time range |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

