# RedstoneQuery

[redstone-api](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/README.md) / [Exports](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/modules.md) / RedstoneQuery

## Class: RedstoneQuery

### Table of contents

#### Constructors

* [constructor](redstonequery.md#constructor)

#### Properties

* [params](redstonequery.md#params)

#### Methods

* [allSymbols](redstonequery.md#allsymbols)
* [symbol](redstonequery.md#symbol)
* [symbols](redstonequery.md#symbols)

### Constructors

#### constructor

* **new RedstoneQuery**\(`params?`: {}\): [_RedstoneQuery_](redstonequery.md)

**Parameters:**

| Name | Type | Default value |
| :--- | :--- | :--- |
| `params` | _object_ | {} |

**Returns:** [_RedstoneQuery_](redstonequery.md)

### Properties

#### params

• `Protected` **params**: QueryParams

### Methods

#### allSymbols

▸ **allSymbols**\(\): [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

Configures query to fetch prices for all supported tokens. It doesn't support any params

**Returns:** [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

query object

#### symbol

▸ **symbol**\(`symbol`: _string_\): [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

Sets a token symbol to fetch

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbol` | _string_ | Token symbol string |

**Returns:** [_RedstoneQueryForSingleSymbol_](redstonequeryforsinglesymbol.md)

query object

#### symbols

▸ **symbols**\(`symbols`: _string_\[\]\): [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

Sets token symbols to fetch

**Parameters:**

| Name | Type | Description |
| :--- | :--- | :--- |
| `symbols` | _string_\[\] | Array of strings \(token symbols\) |

**Returns:** [_RedstoneQueryForSeveralSymbols_](redstonequeryforseveralsymbols.md)

query object

