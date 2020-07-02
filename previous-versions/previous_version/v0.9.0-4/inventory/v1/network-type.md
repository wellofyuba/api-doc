---
description: null
---

# Network Type

> **Package : spaceone.api.inventory.v1**

## NetworkType

{% hint style="info" %}
**NetworkType Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/inventory/v1/network-type.md#create) | [CreateNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#createnetworktyperequest) | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/network-type.md#update) | [UpdateNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#updatenetworktyperequest) | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |  |
| 3 | [delete](../../../v0.9.0-5/inventory/v1/network-type.md#delete) | [NetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#networktyperequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/inventory/v1/network-type.md#get) | [GetNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#getnetworktyperequest) | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |  |
| 5 | [list](../../../v0.9.0-5/inventory/v1/network-type.md#list) | [NetworkTypeQuery](../../../v0.9.0-5/inventory/v1/network-type.md#networktypequery) | [NetworkTypesInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypesinfo) |  |
| 6 | [stat](../../../v0.9.0-5/inventory/v1/network-type.md#stat) | [NetworkTypeStatQuery](../../../v0.9.0-5/inventory/v1/network-type.md#networktypestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/network-types

| Type | Message |
| :--- | :--- |
| Request | [CreateNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#createnetworktyperequest) |
| Response | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |

### update

> **PUT** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#updatenetworktyperequest) |
| Response | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |

### delete

> **DELETE** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#networktyperequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetNetworkTypeRequest](../../../v0.9.0-5/inventory/v1/network-type.md#getnetworktyperequest) |
| Response | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |

### list

> **GET** /inventory/v1/network-types
>
> **POST** /inventory/v1/network-types/search

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeQuery](../../../v0.9.0-5/inventory/v1/network-type.md#networktypequery) |
| Response | [NetworkTypesInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypesinfo) |

### stat

> **POST** /inventory/v1/network-types/stat

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeStatQuery](../../../v0.9.0-5/inventory/v1/network-type.md#networktypestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### GetNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### NetworkTypeInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | domain\_id | string |  |  |
| 5 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### NetworkTypeQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | network\_type\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | domain\_id | string |  | required |

### NetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### NetworkTypeStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### NetworkTypesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/network-type.md#networktypeinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | domain\_id | string |  | required |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

