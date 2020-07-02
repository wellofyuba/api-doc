---
description: null
---

# Network Policy

> **Package : spaceone.api.inventory.v1**

## NetworkPolicy

{% hint style="info" %}
**NetworkPolicy Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](network-policy%20%281%29.md#create) | [CreateNetworkPolicyRequest](network-policy%20%281%29.md#createnetworkpolicyrequest) | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |  |
| 2 | [update](network-policy%20%281%29.md#update) | [UpdateNetworkPolicyRequest](network-policy%20%281%29.md#updatenetworkpolicyrequest) | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |  |
| 3 | [pin\_data](network-policy%20%281%29.md#pin_data) | [PinNetworkPolicyDataRequest](network-policy%20%281%29.md#pinnetworkpolicydatarequest) | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |  |
| 4 | [delete](network-policy%20%281%29.md#delete) | [NetworkPolicyRequest](network-policy%20%281%29.md#networkpolicyrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](network-policy%20%281%29.md#get) | [GetNetworkPolicyRequest](network-policy%20%281%29.md#getnetworkpolicyrequest) | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |  |
| 6 | [list](network-policy%20%281%29.md#list) | [NetworkPolicyQuery](network-policy%20%281%29.md#networkpolicyquery) | [NetworkPoliciesInfo](network-policy%20%281%29.md#networkpoliciesinfo) |  |
| 7 | [stat](network-policy%20%281%29.md#stat) | [NetworkPolicyStatQuery](network-policy%20%281%29.md#networkpolicystatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/network-policies

| Type | Message |
| :--- | :--- |
| Request | [CreateNetworkPolicyRequest](network-policy%20%281%29.md#createnetworkpolicyrequest) |
| Response | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |

### update

> **PUT** /inventory/v1/network-policy/{network\_policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateNetworkPolicyRequest](network-policy%20%281%29.md#updatenetworkpolicyrequest) |
| Response | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |

### pin\_data

> **PUT** /inventory/v1/network-policy/{network\_policy\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinNetworkPolicyDataRequest](network-policy%20%281%29.md#pinnetworkpolicydatarequest) |
| Response | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |

### delete

> **DELETE** /inventory/v1/network-policy/{network\_policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [NetworkPolicyRequest](network-policy%20%281%29.md#networkpolicyrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/network-policy/{network\_policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetNetworkPolicyRequest](network-policy%20%281%29.md#getnetworkpolicyrequest) |
| Response | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |

### list

> **GET** /inventory/v1/network-policies
>
> **POST** /inventory/v1/network-policies/search

| Type | Message |
| :--- | :--- |
| Request | [NetworkPolicyQuery](network-policy%20%281%29.md#networkpolicyquery) |
| Response | [NetworkPoliciesInfo](network-policy%20%281%29.md#networkpoliciesinfo) |

### stat

> **POST** /inventory/v1/network-policies/stat

| Type | Message |
| :--- | :--- |
| Request | [NetworkPolicyStatQuery](network-policy%20%281%29.md#networkpolicystatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateNetworkPolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | routing\_tables | [RoutingTable](network-policy%20%281%29.md#routingtable) | ❌ |  |
| 3 | dns | string | ❌ |  |
| 4 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | reference | [NetworkPolicyReference](network-policy%20%281%29.md#networkpolicyreference) | ❌ |  |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 8 | zone\_id | string | ✅ |  |
| 9 | domain\_id | string | ✅ |  |

### GetNetworkPolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_policy\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### NetworkPoliciesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [NetworkPolicyInfo](network-policy%20%281%29.md#networkpolicyinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### NetworkPolicyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_policy\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | routing\_tables | [RoutingTable](network-policy%20%281%29.md#routingtable) |  |  |
| 4 | dns | string |  |  |
| 5 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | reference | [NetworkPolicyReference](network-policy%20%281%29.md#networkpolicyreference) |  |  |
| 8 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 10 | region\_info | [RegionInfo](network-policy%20%281%29.md#regioninfo) |  |  |
| 11 | zone\_info | [ZoneInfo](network-policy%20%281%29.md#zoneinfo) |  |  |
| 12 | domain\_id | string |  |  |
| 13 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### NetworkPolicyQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | network\_policy\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | zone\_id | string | ❌ |  |
| 5 | region\_id | string | ❌ |  |
| 6 | domain\_id | string | ✅ |  |

### NetworkPolicyReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### NetworkPolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_policy\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### NetworkPolicyStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### PinNetworkPolicyDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_policy\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### RoutingTable

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cidr | string |  |  |
| 2 | destination | string |  |  |
| 3 | interface | string |  |  |

### UpdateNetworkPolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | network\_policy\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | routing\_tables | [RoutingTable](network-policy%20%281%29.md#routingtable) | ❌ |  |
| 4 | dns | string | ❌ |  |
| 5 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | reference | [NetworkPolicyReference](network-policy%20%281%29.md#networkpolicyreference) | ❌ |  |
| 8 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 9 | domain\_id | string | ✅ |  |

