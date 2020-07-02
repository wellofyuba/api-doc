---
description: null
---

# Schema

> **Package : spaceone.api.repository.v1**

## Schema

{% hint style="info" %}
**Schema Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](schema%20%281%29.md#create) | [CreateSchemaRequest](schema%20%281%29.md#createschemarequest) | [SchemaInfo](schema%20%281%29.md#schemainfo) |  |
| 2 | [update](schema%20%281%29.md#update) | [UpdateSchemaRequest](schema%20%281%29.md#updateschemarequest) | [SchemaInfo](schema%20%281%29.md#schemainfo) |  |
| 3 | [delete](schema%20%281%29.md#delete) | [SchemaRequest](schema%20%281%29.md#schemarequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](schema%20%281%29.md#get) | [GetRepositorySchemaRequest](schema%20%281%29.md#getrepositoryschemarequest) | [SchemaInfo](schema%20%281%29.md#schemainfo) |  |
| 5 | [list](schema%20%281%29.md#list) | [SchemaQuery](schema%20%281%29.md#schemaquery) | [SchemasInfo](schema%20%281%29.md#schemasinfo) |  |
| 6 | [stat](schema%20%281%29.md#stat) | [SchemaStatQuery](schema%20%281%29.md#schemastatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /repository/v1/schemas

| Type | Message |
| :--- | :--- |
| Request | [CreateSchemaRequest](schema%20%281%29.md#createschemarequest) |
| Response | [SchemaInfo](schema%20%281%29.md#schemainfo) |

### update

> **PUT** /repository/v1/schema/{schema}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSchemaRequest](schema%20%281%29.md#updateschemarequest) |
| Response | [SchemaInfo](schema%20%281%29.md#schemainfo) |

### delete

> **DELETE** /repository/v1/schema/{schema}

| Type | Message |
| :--- | :--- |
| Request | [SchemaRequest](schema%20%281%29.md#schemarequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /repository/v1/schemas/{schema}

| Type | Message |
| :--- | :--- |
| Request | [GetRepositorySchemaRequest](schema%20%281%29.md#getrepositoryschemarequest) |
| Response | [SchemaInfo](schema%20%281%29.md#schemainfo) |

### list

> **GET** /repository/v1/schemas
>
> **POST** /repository/v1/schemas/search

| Type | Message |
| :--- | :--- |
| Request | [SchemaQuery](schema%20%281%29.md#schemaquery) |
| Response | [SchemasInfo](schema%20%281%29.md#schemasinfo) |

### stat

> **POST** /repository/v1/schemas/stat

| Type | Message |
| :--- | :--- |
| Request | [SchemaStatQuery](schema%20%281%29.md#schemastatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | service\_type | string | ✅ |  |
| 3 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |
| 4 | labels | string | ❌ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | project\_id | string | ❌ |  |
| 7 | domain\_id | string | ✅ |  |

### GetRepositorySchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | repository\_id | string | ❌ |  |
| 4 | only | string | ❌ |  |

### SchemaInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  |  |
| 2 | service\_type | string |  |  |
| 3 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | labels | string |  |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | repository\_info | [RepositoryInfo](schema%20%281%29.md#repositoryinfo) |  |  |
| 7 | project\_id | string |  |  |
| 8 | domain\_id | string |  |  |
| 9 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### SchemaQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | name | string | ❌ |  |
| 3 | service\_type | string | ❌ |  |
| 4 | project\_id | string | ✅ |  |
| 5 | repository\_id | string | ✅ |  |
| 6 | domain\_id | string | ✅ |  |

### SchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SchemaStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | repository\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### SchemasInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SchemaInfo](schema%20%281%29.md#schemainfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 3 | labels | string | ❌ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | domain\_id | string | ✅ |  |

