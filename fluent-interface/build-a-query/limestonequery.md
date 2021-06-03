[redstone-api](../README.md) / [Exports](../modules.md) / RedstoneQuery

# Class: RedstoneQuery

## Table of contents

### Constructors

- [constructor](redstonequery.md#constructor)

### Properties

- [params](redstonequery.md#params)

### Methods

- [allSymbols](redstonequery.md#allsymbols)
- [symbol](redstonequery.md#symbol)
- [symbols](redstonequery.md#symbols)

## Constructors

### constructor

\+ **new RedstoneQuery**(`params?`: {}): [*RedstoneQuery*](redstonequery.md)

#### Parameters:

| Name | Type | Default value |
| :------ | :------ | :------ |
| `params` | *object* | {} |

**Returns:** [*RedstoneQuery*](redstonequery.md)

Defined in: [redstone-query.ts:15](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L15)

## Properties

### params

• `Protected` **params**: QueryParams

Defined in: [redstone-query.ts:15](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L15)

## Methods

### allSymbols

▸ **allSymbols**(): [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

Configures query to fetch prices for all supported tokens.
It doesn't support any params

**Returns:** [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

query object

Defined in: [redstone-query.ts:49](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L49)

___

### symbol

▸ **symbol**(`symbol`: *string*): [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

Sets a token symbol to fetch

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `symbol` | *string* | Token symbol string |

**Returns:** [*RedstoneQueryForSingleSymbol*](redstonequeryforsinglesymbol.md)

query object

Defined in: [redstone-query.ts:29](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L29)

___

### symbols

▸ **symbols**(`symbols`: *string*[]): [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

Sets token symbols to fetch

#### Parameters:

| Name | Type | Description |
| :------ | :------ | :------ |
| `symbols` | *string*[] | Array of strings (token symbols) |

**Returns:** [*RedstoneQueryForSeveralSymbols*](redstonequeryforseveralsymbols.md)

query object

Defined in: [redstone-query.ts:40](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L40)
