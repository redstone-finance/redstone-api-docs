# RedstoneQueryExecutable

[redstone-api](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/README.md) / [Exports](https://github.com/redstone-finance/redstone-docs/tree/e56f4e97ffe8229804276eb19e84c082fe4e179e/fluent-interface/modules.md) / RedstoneQueryExecutable

## Class: RedstoneQueryExecutable

### Type parameters

| Name |
| :--- |
| `QueryResultType` |

### Table of contents

#### Constructors

* [constructor](redstonequeryexecutable.md#constructor)

#### Properties

* [params](redstonequeryexecutable.md#params)

#### Methods

* [exec](redstonequeryexecutable.md#exec)

### Constructors

#### constructor

+ **new RedstoneQueryExecutable**\(`params?`: {}\): [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

**Type parameters:**

| Name |
| :--- |
| `QueryResultType` |

**Parameters:**

| Name | Type | Default value |
| :--- | :--- | :--- |
| `params` | _object_ | {} |

**Returns:** [_RedstoneQueryExecutable_](redstonequeryexecutable.md)

Defined in: [redstone-query.ts:173](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L173)

### Properties

#### params

• `Private` **params**: QueryParams

Defined in: [redstone-query.ts:173](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L173)

### Methods

#### exec

▸ **exec**\(\): _Promise_

Executes the query

**Returns:** _Promise_

Promise resolving the query result \(result type depends on the query\)

Defined in: [redstone-query.ts:187](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L187)

