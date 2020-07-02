---
description: null
---

# Query

> **Package : spaceone.api.core.v1**

## Message

### AggregateCount

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  |  |

### AggregateGroup

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | keys | [AggregateGroupKey](../../../v0.9.0-5/core/v1/query.md#aggregategroupkey) |  |  |
| 2 | fields | [AggregateGroupField](../../../v0.9.0-5/core/v1/query.md#aggregategroupfield) |  |  |

### AggregateGroupField

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | key | string |  |  |
| 2 | k | string |  |  |
| 3 | name | string |  |  |
| 4 | n | string |  |  |
| 5 | operator | string |  |  |
| 6 | o | string |  |  |

### AggregateGroupKey

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | key | string |  |  |
| 2 | k | string |  |  |
| 3 | name | string |  |  |
| 4 | n | string |  |  |

### AggregateUnwind

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | path | string |  |  |

### Filter

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | key | string |  |  |
| 2 | k | string |  |  |
| 3 | value | [google.protobuf.Value](https://developers.google.com/protocol-buffers/docs/reference/overview) |  |  |
| 4 | v | [google.protobuf.Value](https://developers.google.com/protocol-buffers/docs/reference/overview) |  |  |
| 5 | operator | string |  |  |
| 6 | o | string |  |  |

### Page

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | start | [uint32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 2 | limit | [uint32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### Query

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | filter | [Filter](../../../v0.9.0-5/core/v1/query.md#filter) |  |  |
| 2 | filter\_or | [Filter](../../../v0.9.0-5/core/v1/query.md#filter) |  |  |
| 3 | sort | [Sort](../../../v0.9.0-5/core/v1/query.md#sort) |  |  |
| 4 | page | [Page](../../../v0.9.0-5/core/v1/query.md#page) |  |  |
| 5 | minimal | bool |  |  |
| 6 | count\_only | bool |  |  |
| 7 | only | string |  |  |
| 8 | keyword | string |  |  |

### Sort

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | key | string |  |  |
| 2 | desc | bool |  |  |

### StatisticsAggregate

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | unwind | [AggregateUnwind](../../../v0.9.0-5/core/v1/query.md#aggregateunwind) |  |  |
| 2 | group | [AggregateGroup](../../../v0.9.0-5/core/v1/query.md#aggregategroup) |  |  |
| 3 | count | [AggregateCount](../../../v0.9.0-5/core/v1/query.md#aggregatecount) |  |  |

### StatisticsQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | filter | [Filter](../../../v0.9.0-5/core/v1/query.md#filter) |  |  |
| 2 | filter\_or | [Filter](../../../v0.9.0-5/core/v1/query.md#filter) |  |  |
| 3 | aggregate | [StatisticsAggregate](../../../v0.9.0-5/core/v1/query.md#statisticsaggregate) |  |  |
| 4 | sort | [StatisticsSort](../../../v0.9.0-5/core/v1/query.md#statisticssort) |  |  |
| 5 | page | [Page](../../../v0.9.0-5/core/v1/query.md#page) |  |  |
| 6 | limit | [uint32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### StatisticsSort

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  |  |
| 2 | desc | bool |  |  |

