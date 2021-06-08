# RedstoneQueryForSeveralSymbols

[redstone-api](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/README.md) / [Exports](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/modules.md) / RedstoneQueryForSeveralSymbols

## Class: RedstoneQueryForSeveralSymbols

### Hierarchy

* [_RedstoneQueryForSingleOrSeveralSymbols_](redstonequeryforsingleorseveralsymbols.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

  ↳ **RedstoneQueryForSeveralSymbols**

### Table of contents

#### Constructors

* [constructor](redstonequeryforseveralsymbols.md#constructor)

#### Properties

* [params](redstonequeryforseveralsymbols.md#params)

#### Methods

* [atDate](redstonequeryforseveralsymbols.md#atdate)
* [getExecutableQuery](redstonequeryforseveralsymbols.md#getexecutablequery)
* [hoursAgo](redstonequeryforseveralsymbols.md#hoursago)
* [latest](redstonequeryforseveralsymbols.md#latest)

### Constructors

#### constructor

+ **new RedstoneQueryForSeveralSymbols**\(`params`: QueryParams\): [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

**Parameters:**

| Name | Type |
| :--- | :--- |
| `params` | QueryParams |

**Returns:** [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

Overrides: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:166](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L166)

### Properties

#### params

• `Protected` **params**: QueryParams

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md).[params](redstonequeryforsingleorseveralsymbols.md#params)

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

### Methods

#### atDate

▸ **atDate**\(`date`: ConvertableToDate\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

Configures query to fetch the price for a specific date.

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `date` | ConvertableToDate | Date for the historical price \(date \| timestamp \| string\) |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:97](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L97)

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

Defined in: [redstone-query.ts:65](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L65)

#### hoursAgo

▸ **hoursAgo**\(`hoursCount`: _number_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

Configures query to fetch the price for X hours ago.

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `hoursCount` | _number_ | Number of hours ago |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:86](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L86)

#### latest

▸ **latest**\(\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

Configures query to fetch the latest price/prices It doesn't support any params

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)&lt;{ \[symbol: string\]: PriceData; }&gt;

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:77](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L77)

