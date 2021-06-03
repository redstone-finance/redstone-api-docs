[redstone-api](../README.md) / [Exports](../modules.md) / RedstoneQueryForSingleOrSeveralSymbols

# Class: RedstoneQueryForSingleOrSeveralSymbols<QueryResultType\>

## Type parameters

| Name |
| :------ |
| `QueryResultType` |

## Hierarchy

* **RedstoneQueryForSingleOrSeveralSymbols**

  ↳ [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

  ↳ [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

## Table of contents

### Constructors

- [constructor](redstonequeryforsingleorseveralsymbols.md#constructor)

### Properties

- [params](redstonequeryforsingleorseveralsymbols.md#params)

### Methods

- [atDate](redstonequeryforsingleorseveralsymbols.md#atdate)
- [getExecutableQuery](redstonequeryforsingleorseveralsymbols.md#getexecutablequery)
- [hoursAgo](redstonequeryforsingleorseveralsymbols.md#hoursago)
- [latest](redstonequeryforsingleorseveralsymbols.md#latest)

## Constructors

### constructor

\+ **new RedstoneQueryForSingleOrSeveralSymbols**<QueryResultType\>(`params`: QueryParams): [*RedstoneQueryForSingleOrSeveralSymbols*](redstonequeryforsingleorseveralsymbols.md)<QueryResultType\>

#### Type parameters:

| Name |
| :------ |
| `QueryResultType` |

#### Parameters:

| Name | Type |
| :------ | :------ |
| `params` | QueryParams |

**Returns:** [*RedstoneQueryForSingleOrSeveralSymbols*](redstonequeryforsingleorseveralsymbols.md)<QueryResultType\>

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

## Properties

### params

• `Protected` **params**: QueryParams

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

## Methods

### atDate

▸ **atDate**(`date`: ConvertableToDate): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

Configures query to fetch the price for a specific date.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | ConvertableToDate | Date for the historical price (date \| timestamp \| string) |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

query object

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

Defined in: [redstone-query.ts:65](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L65)

___

### hoursAgo

▸ **hoursAgo**(`hoursCount`: *number*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

Configures query to fetch the price for X hours ago.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `hoursCount` | *number* | Number of hours ago |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

query object

Defined in: [redstone-query.ts:86](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L86)

___

### latest

▸ **latest**(): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

Configures query to fetch the latest price/prices
It doesn't support any params

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

query object

Defined in: [redstone-query.ts:77](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L77)
