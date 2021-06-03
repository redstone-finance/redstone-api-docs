[redstone-api](../README.md) / [Exports](../modules.md) / RedstoneQueryForSeveralSymbols

# Class: RedstoneQueryForSeveralSymbols

## Hierarchy

* [*RedstoneQueryForSingleOrSeveralSymbols*](redstonequeryforsingleorseveralsymbols.md)<{ [symbol: string]: PriceData;  }\>

  ↳ **RedstoneQueryForSeveralSymbols**

## Table of contents

### Constructors

- [constructor](redstonequeryforseveralsymbols.md#constructor)

### Properties

- [params](redstonequeryforseveralsymbols.md#params)

### Methods

- [atDate](redstonequeryforseveralsymbols.md#atdate)
- [getExecutableQuery](redstonequeryforseveralsymbols.md#getexecutablequery)
- [hoursAgo](redstonequeryforseveralsymbols.md#hoursago)
- [latest](redstonequeryforseveralsymbols.md#latest)

## Constructors

### constructor

\+ **new RedstoneQueryForSeveralSymbols**(`params`: QueryParams): [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

#### Parameters:

| Name | Type |
| :------ | :------ |
| `params` | QueryParams |

**Returns:** [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

Overrides: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:166](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L166)

## Properties

### params

• `Protected` **params**: QueryParams

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md).[params](redstonequeryforsingleorseveralsymbols.md#params)

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

## Methods

### atDate

▸ **atDate**(`date`: ConvertableToDate): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

Configures query to fetch the price for a specific date.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | ConvertableToDate | Date for the historical price (date \| timestamp \| string) |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:97](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L97)

___

### getExecutableQuery

▸ `Protected`**getExecutableQuery**<T\>(`update`: *any*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<T\>

#### Type parameters:

| Name |
| :------ |
| `T` |

#### Parameters:

| Name | Type |
| :------ | :------ |
| `update` | *any* |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<T\>

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:65](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L65)

___

### hoursAgo

▸ **hoursAgo**(`hoursCount`: *number*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

Configures query to fetch the price for X hours ago.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `hoursCount` | *number* | Number of hours ago |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:86](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L86)

___

### latest

▸ **latest**(): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

Configures query to fetch the latest price/prices
It doesn't support any params

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<{ [symbol: string]: PriceData;  }\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:77](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L77)
