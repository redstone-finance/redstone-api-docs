[redstone-api](../README.md) / [Exports](../modules.md) / RedstoneQueryForSingleSymbol

# Class: RedstoneQueryForSingleSymbol

## Hierarchy

* [*RedstoneQueryForSingleOrSeveralSymbols*](redstonequeryforsingleorseveralsymbols.md)<PriceData\>

  ↳ **RedstoneQueryForSingleSymbol**

## Table of contents

### Constructors

- [constructor](redstonequeryforsinglesymbol.md#constructor)

### Properties

- [params](redstonequeryforsinglesymbol.md#params)

### Methods

- [atDate](redstonequeryforsinglesymbol.md#atdate)
- [forLastDays](redstonequeryforsinglesymbol.md#forlastdays)
- [forLastHours](redstonequeryforsinglesymbol.md#forlasthours)
- [fromDate](redstonequeryforsinglesymbol.md#fromdate)
- [getExecutableQuery](redstonequeryforsinglesymbol.md#getexecutablequery)
- [hoursAgo](redstonequeryforsinglesymbol.md#hoursago)
- [latest](redstonequeryforsinglesymbol.md#latest)
- [toDate](redstonequeryforsinglesymbol.md#todate)

## Constructors

### constructor

\+ **new RedstoneQueryForSingleSymbol**(`params`: QueryParams): [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

#### Parameters:

| Name | Type |
| :------ | :------ |
| `params` | QueryParams |

**Returns:** [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

Overrides: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:102](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L102)

## Properties

### params

• `Protected` **params**: QueryParams

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md).[params](redstonequeryforsingleorseveralsymbols.md#params)

Defined in: [redstone-query.ts:58](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L58)

## Methods

### atDate

▸ **atDate**(`date`: ConvertableToDate): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

Configures query to fetch the price for a specific date.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | ConvertableToDate | Date for the historical price (date \| timestamp \| string) |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:97](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L97)

___

### forLastDays

▸ **forLastDays**(`daysCount`: *number*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

Configures query to fetch the price for the last few days

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `daysCount` | *number* | Number of days in the time range |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

query object

Defined in: [redstone-query.ts:154](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L154)

___

### forLastHours

▸ **forLastHours**(`hoursCount`: *number*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

Configures query to fetch the price for the last few hours

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `hoursCount` | *number* | Number of hours in the time range |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

query object

Defined in: [redstone-query.ts:139](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L139)

___

### fromDate

▸ **fromDate**(`date`: ConvertableToDate): [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

Configures query to fetch the price in a time range. It is important to use fromDate with toDate query methods

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | ConvertableToDate | Start date/time for the time range |

**Returns:** [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

query object

Defined in: [redstone-query.ts:113](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L113)

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

▸ **hoursAgo**(`hoursCount`: *number*): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

Configures query to fetch the price for X hours ago.

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `hoursCount` | *number* | Number of hours ago |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:86](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L86)

___

### latest

▸ **latest**(): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

Configures query to fetch the latest price/prices
It doesn't support any params

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData\>

query object

Inherited from: [RedstoneQueryForSingleOrSeveralSymbols](redstonequeryforsingleorseveralsymbols.md)

Defined in: [redstone-query.ts:77](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L77)

___

### toDate

▸ **toDate**(`date`: ConvertableToDate): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

Configures query to fetch the price in a time range. toDate method should go after the fromDate

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `date` | ConvertableToDate | End date/time for the time range |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<PriceData[]\>

query object

Defined in: [redstone-query.ts:126](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L126)
