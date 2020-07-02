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
| 1 | [create](network%20%281%29.md#create) | [CreateNetworkRequest](network%20%281%29.md#createnetworkrequest) | [NetworkInfo](network%20%281%29.md#networkinfo) |  |
| 2 | [update](network%20%281%29.md#update) | [UpdateNetworkRequest](network%20%281%29.md#updatenetworkrequest) | [NetworkInfo](network%20%281%29.md#networkinfo) |  |
| 3 | [pin\_data](network%20%281%29.md#pin_data) | [PinNetworkDataRequest](network%20%281%29.md#pinnetworkdatarequest) | [NetworkInfo](network%20%281%29.md#networkinfo) |  |
| 4 | [delete](network%20%281%29.md#delete) | [NetworkRequest](network%20%281%29.md#networkrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](network%20%281%29.md#get) | [GetNetworkRequest](network%20%281%29.md#getnetworkrequest) | [NetworkInfo](network%20%281%29.md#networkinfo) |  |
| 6 | [list](network%20%281%29.md#list) | [NetworkQuery](network%20%281%29.md#networkquery) | [NetworksInfo](network%20%281%29.md#networksinfo) |  |
| 7 | [stat](network%20%281%29.md#stat) | [NetworkStatQuery](network%20%281%29.md#networkstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/networks

| Type | Message |
| :--- | :--- |
| Request | [CreateNetworkRequest](network%20%281%29.md#createnetworkrequest) |
| Response | [NetworkInfo](network%20%281%29.md#networkinfo) |

### update

> **PUT** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateNetworkRequest](network%20%281%29.md#updatenetworkrequest) |
| Response | [NetworkInfo](network%20%281%29.md#networkinfo) |

### pin\_data

> **PUT** /inventory/v1/network/{network\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinNetworkDataRequest](network%20%281%29.md#pinnetworkdatarequest) |
| Response | [NetworkInfo](network%20%281%29.md#networkinfo) |

### delete

> **DELETE** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [NetworkRequest](network%20%281%29.md#networkrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/network/{network\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetNetworkRequest](network%20%281%29.md#getnetworkrequest) |
| Response | [NetworkInfo](network%20%281%29.md#networkinfo) |

### list

> **GET** /inventory/v1/networks
>
> **POST** /inventory/v1/networks/search

| Type | Message |
| :--- | :--- |
| Request | [NetworkQuery](network%20%281%29.md#networkquery) |
| Response | [NetworksInfo](network%20%281%29.md#networksinfo) |

### stat

> **POST** /inventory/v1/networks/stat

| Type | Message |
| :--- | :--- |
| Request | [NetworkStatQuery](network%20%281%29.md#networkstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | cidr | string | ✅ |  |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | reference | [NetworkReference](network%20%281%29.md#networkreference) | ❌ |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | zone\_id | string | ✅ |  |
| 8 | domain\_id | string | ✅ |  |

### GetNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### NetworkInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | cidr | string |  |  |
| 4 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 5 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | reference | [NetworkReference](network%20%281%29.md#networkreference) |  |  |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | region\_info | [RegionInfo](network%20%281%29.md#regioninfo) |  |  |
| 10 | zone\_info | [ZoneInfo](network%20%281%29.md#zoneinfo) |  |  |
| 11 | domain\_id | string |  |  |
| 12 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### NetworkQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | network\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | cidr | string | ❌ |  |
| 5 | zone\_id | string | ❌ |  |
| 6 | region\_id | string | ❌ |  |
| 7 | domain\_id | string | ✅ |  |

### NetworkReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### NetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### NetworkStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### NetworksInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [NetworkInfo](network%20%281%29.md#networkinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PinNetworkDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdateNetworkRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | reference | [NetworkReference](network%20%281%29.md#networkreference) | ❌ |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | domain\_id | string | ✅ |  |

