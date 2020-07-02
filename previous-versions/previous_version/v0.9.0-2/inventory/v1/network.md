---
description: null
---

# Network

> **Package : spaceone.api.inventory.v1**

## Network

{% hint style="info" %}
**Network Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/inventory/v1/network.md#create) | [CreateNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#createnetworkrequest) | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/network.md#update) | [UpdateNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#updatenetworkrequest) | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |  |
| 3 | [pin\_data](../../../v0.9.0-5/inventory/v1/network.md#pin_data) | [PinNetworkDataRequest](../../../v0.9.0-5/inventory/v1/network.md#pinnetworkdatarequest) | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |  |
| 4 | [delete](../../../v0.9.0-5/inventory/v1/network.md#delete) | [NetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#networkrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](../../../v0.9.0-5/inventory/v1/network.md#get) | [GetNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#getnetworkrequest) | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |  |
| 6 | [list](../../../v0.9.0-5/inventory/v1/network.md#list) | [NetworkQuery](../../../v0.9.0-5/inventory/v1/network.md#networkquery) | [NetworksInfo](../../../v0.9.0-5/inventory/v1/network.md#networksinfo) |  |
| 7 | [stat](../../../v0.9.0-5/inventory/v1/network.md#stat) | [NetworkStatQuery](../../../v0.9.0-5/inventory/v1/network.md#networkstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/networks

| Type | Message |
| :--- | :--- |
| Request | [CreateNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#createnetworkrequest) |
| Response | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |

### update

> **PUT** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#updatenetworkrequest) |
| Response | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |

### pin\_data

> **PUT** /inventory/v1/network/{network\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinNetworkDataRequest](../../../v0.9.0-5/inventory/v1/network.md#pinnetworkdatarequest) |
| Response | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |

### delete

> **DELETE** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [NetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#networkrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetNetworkRequest](../../../v0.9.0-5/inventory/v1/network.md#getnetworkrequest) |
| Response | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |

### list

> **GET** /inventory/v1/networks
>
> **POST** /inventory/v1/networks/search

| Type | Message |
| :--- | :--- |
| Request | [NetworkQuery](../../../v0.9.0-5/inventory/v1/network.md#networkquery) |
| Response | [NetworksInfo](../../../v0.9.0-5/inventory/v1/network.md#networksinfo) |

### stat

> **POST** /inventory/v1/networks/stat

| Type | Message |
| :--- | :--- |
| Request | [NetworkStatQuery](../../../v0.9.0-5/inventory/v1/network.md#networkstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | cidr | string |  | required |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | reference | [NetworkReference](../../../v0.9.0-5/inventory/v1/network.md#networkreference) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 7 | zone\_id | string |  | required |
| 8 | domain\_id | string |  | required |

### GetNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### NetworkInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | cidr | string |  |  |
| 4 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 5 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | reference | [NetworkReference](../../../v0.9.0-5/inventory/v1/network.md#networkreference) |  |  |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | region\_info | [RegionInfo](../../../v0.9.0-5/inventory/v1/network.md#regioninfo) |  |  |
| 10 | zone\_info | [ZoneInfo](../../../v0.9.0-5/inventory/v1/network.md#zoneinfo) |  |  |
| 11 | domain\_id | string |  |  |
| 12 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### NetworkQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | network\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | cidr | string |  | optional |
| 5 | zone\_id | string |  | optional |
| 6 | region\_id | string |  | optional |
| 7 | domain\_id | string |  | required |

### NetworkReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### NetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### NetworkStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### NetworksInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [NetworkInfo](../../../v0.9.0-5/inventory/v1/network.md#networkinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PinNetworkDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  | required |
| 2 | keys | string |  | required |
| 3 | domain\_id | string |  | required |

### UpdateNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | reference | [NetworkReference](../../../v0.9.0-5/inventory/v1/network.md#networkreference) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 7 | domain\_id | string |  | required |

