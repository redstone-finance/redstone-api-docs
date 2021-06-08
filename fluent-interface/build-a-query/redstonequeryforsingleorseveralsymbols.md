# RedstoneQueryForSingleOrSeveralSymbols

[redstone-api](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/README.md) / [Exports](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/modules.md) / RedstoneQueryForSingleOrSeveralSymbols

## Class: RedstoneQueryForSingleOrSeveralSymbols

### Type parameters

| Name |
| :--- |
| `QueryResultType` |

### Hierarchy

* **RedstoneQueryForSingleOrSeveralSymbols**

  ↳ [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

  ↳ [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

### Table of contents

#### Constructors

* [constructor](redstonequeryforsingleorseveralsymbols.md#constructor)

#### Properties

* [params](redstonequeryforsingleorseveralsymbols.md#params)

#### Methods

* [atDate](redstonequeryforsingleorseveralsymbols.md#atdate)
* [getExecutableQuery](redstonequeryforsingleorseveralsymbols.md#getexecutablequery)
* [hoursAgo](redstonequeryforsingleorseveralsymbols.md#hoursago)
* [latest](redstonequeryforsingleorseveralsymbols.md#latest)

### Constructors

#### constructor

+ **new RedstoneQueryForSingleOrSeveralSymbols**\(`params`: QueryParams\): [_RedstoneQueryForSingleOrSeveralSymbols_](redstonequeryforsingleorseveralsymbols.md)

**Type parameters:**

| Name |
| :--- |
| `QueryResultType` |

**Parameters:**

| Name | Type |
| :--- | :--- |
| `params` | QueryParams |

**Returns:** [_RedstoneQueryForSingleOrSeveralSymbols_](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

### Properties

#### params

• `Protected` **params**: QueryParams

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

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

Defined in: [redstone-query.ts:65](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L65)

#### hoursAgo

▸ **hoursAgo**\(`hoursCount`: _number_\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the price for X hours ago.

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `hoursCount` | _number_ | Number of hours ago |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

Defined in: [redstone-query.ts:86](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L86)

#### latest

▸ **latest**\(\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Configures query to fetch the latest price/prices It doesn't support any params

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

query object

Defined in: [redstone-query.ts:77](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L77)

