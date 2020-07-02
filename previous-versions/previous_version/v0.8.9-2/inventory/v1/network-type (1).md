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
| 1 | [create](network-type%20%281%29.md#create) | [CreateNetworkTypeRequest](network-type%20%281%29.md#createnetworktyperequest) | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |  |
| 2 | [update](network-type%20%281%29.md#update) | [UpdateNetworkTypeRequest](network-type%20%281%29.md#updatenetworktyperequest) | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |  |
| 3 | [delete](network-type%20%281%29.md#delete) | [NetworkTypeRequest](network-type%20%281%29.md#networktyperequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](network-type%20%281%29.md#get) | [GetNetworkTypeRequest](network-type%20%281%29.md#getnetworktyperequest) | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |  |
| 5 | [list](network-type%20%281%29.md#list) | [NetworkTypeQuery](network-type%20%281%29.md#networktypequery) | [NetworkTypesInfo](network-type%20%281%29.md#networktypesinfo) |  |
| 6 | [stat](network-type%20%281%29.md#stat) | [NetworkTypeStatQuery](network-type%20%281%29.md#networktypestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/network-types

| Type | Message |
| :--- | :--- |
| Request | [CreateNetworkTypeRequest](network-type%20%281%29.md#createnetworktyperequest) |
| Response | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |

### update

> **PUT** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateNetworkTypeRequest](network-type%20%281%29.md#updatenetworktyperequest) |
| Response | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |

### delete

> **DELETE** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeRequest](network-type%20%281%29.md#networktyperequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/network-type/{network\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetNetworkTypeRequest](network-type%20%281%29.md#getnetworktyperequest) |
| Response | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |

### list

> **GET** /inventory/v1/network-types
>
> **POST** /inventory/v1/network-types/search

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeQuery](network-type%20%281%29.md#networktypequery) |
| Response | [NetworkTypesInfo](network-type%20%281%29.md#networktypesinfo) |

### stat

> **POST** /inventory/v1/network-types/stat

| Type | Message |
| :--- | :--- |
| Request | [NetworkTypeStatQuery](network-type%20%281%29.md#networktypestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

### GetNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

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
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | network\_type\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### NetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### NetworkTypeStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### NetworkTypesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [NetworkTypeInfo](network-type%20%281%29.md#networktypeinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateNetworkTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_type\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | domain\_id | string | ✅ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

