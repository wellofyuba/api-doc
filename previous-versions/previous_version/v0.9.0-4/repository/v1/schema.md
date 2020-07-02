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
| 1 | [create](../../../v0.9.0-5/repository/v1/schema.md#create) | [CreateSchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#createschemarequest) | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |  |
| 2 | [update](../../../v0.9.0-5/repository/v1/schema.md#update) | [UpdateSchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#updateschemarequest) | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |  |
| 3 | [delete](../../../v0.9.0-5/repository/v1/schema.md#delete) | [SchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#schemarequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/repository/v1/schema.md#get) | [GetRepositorySchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#getrepositoryschemarequest) | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |  |
| 5 | [list](../../../v0.9.0-5/repository/v1/schema.md#list) | [SchemaQuery](../../../v0.9.0-5/repository/v1/schema.md#schemaquery) | [SchemasInfo](../../../v0.9.0-5/repository/v1/schema.md#schemasinfo) |  |
| 6 | [stat](../../../v0.9.0-5/repository/v1/schema.md#stat) | [SchemaStatQuery](../../../v0.9.0-5/repository/v1/schema.md#schemastatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /repository/v1/schemas

| Type | Message |
| :--- | :--- |
| Request | [CreateSchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#createschemarequest) |
| Response | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |

### update

> **PUT** /repository/v1/schema/{schema}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#updateschemarequest) |
| Response | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |

### delete

> **DELETE** /repository/v1/schema/{schema}

| Type | Message |
| :--- | :--- |
| Request | [SchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#schemarequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /repository/v1/schemas/{schema}

| Type | Message |
| :--- | :--- |
| Request | [GetRepositorySchemaRequest](../../../v0.9.0-5/repository/v1/schema.md#getrepositoryschemarequest) |
| Response | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |

### list

> **GET** /repository/v1/schemas
>
> **POST** /repository/v1/schemas/search

| Type | Message |
| :--- | :--- |
| Request | [SchemaQuery](../../../v0.9.0-5/repository/v1/schema.md#schemaquery) |
| Response | [SchemasInfo](../../../v0.9.0-5/repository/v1/schema.md#schemasinfo) |

### stat

> **POST** /repository/v1/schemas/stat

| Type | Message |
| :--- | :--- |
| Request | [SchemaStatQuery](../../../v0.9.0-5/repository/v1/schema.md#schemastatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | service\_type | string |  | required |
| 3 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 4 | labels | string |  | optional |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | project\_id | string |  | optional |
| 7 | domain\_id | string |  | required |

### GetRepositorySchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | repository\_id | string |  | optional |
| 4 | only | string |  | optional |

### SchemaInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  |  |
| 2 | service\_type | string |  |  |
| 3 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | labels | string |  |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | repository\_info | [RepositoryInfo](../../../v0.9.0-5/repository/v1/schema.md#repositoryinfo) |  |  |
| 7 | project\_id | string |  |  |
| 8 | domain\_id | string |  |  |
| 9 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### SchemaQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | name | string |  | optional |
| 3 | service\_type | string |  | optional |
| 4 | project\_id | string |  | required |
| 5 | repository\_id | string |  | required |
| 6 | domain\_id | string |  | required |

### SchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | domain\_id | string |  | required |

### SchemaStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | repository\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### SchemasInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SchemaInfo](../../../v0.9.0-5/repository/v1/schema.md#schemainfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSchemaRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | schema | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 3 | labels | string |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | domain\_id | string |  | required |

