[redstone-api](../README.md) / [Exports](../modules.md) / RedstoneQueryExecutable

# Class: RedstoneQueryExecutable<QueryResultType\>

## Type parameters

| Name |
| :------ |
| `QueryResultType` |

## Table of contents

### Constructors

- [constructor](redstonequeryexecutable.md#constructor)

### Properties

- [params](redstonequeryexecutable.md#params)

### Methods

- [exec](redstonequeryexecutable.md#exec)

## Constructors

### constructor

\+ **new RedstoneQueryExecutable**<QueryResultType\>(`params?`: {}): [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

#### Type parameters:

| Name |
| :------ |
| `QueryResultType` |

#### Parameters:

| Name | Type | Default value |
| :------ | :------ | :------ |
| `params` | *object* | {} |

**Returns:** [*RedstoneQueryExecutable*](redstonequeryexecutable.md)<QueryResultType\>

Defined in: [redstone-query.ts:173](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L173)

## Properties

### params

• `Private` **params**: QueryParams

Defined in: [redstone-query.ts:173](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L173)

## Methods

### exec

▸ **exec**(): *Promise*<QueryResultType\>

Executes the query

**Returns:** *Promise*<QueryResultType\>

Promise resolving the query result (result type depends on the query)

Defined in: [redstone-query.ts:187](https://github.com/redstone-finance/redstone-api/blob/3d4422c/src/redstone-query.ts#L187)
