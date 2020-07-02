---
description: null
---

# Subnet

> **Package : spaceone.api.inventory.v1**

## Subnet

{% hint style="info" %}
**Subnet Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](subnet%20%281%29.md#create) | [CreateSubnetRequest](subnet%20%281%29.md#createsubnetrequest) | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |  |
| 2 | [update](subnet%20%281%29.md#update) | [UpdateSubnetRequest](subnet%20%281%29.md#updatesubnetrequest) | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |  |
| 3 | [pin\_data](subnet%20%281%29.md#pin_data) | [PinSubnetDataRequest](subnet%20%281%29.md#pinsubnetdatarequest) | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |  |
| 4 | [delete](subnet%20%281%29.md#delete) | [SubnetRequest](subnet%20%281%29.md#subnetrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](subnet%20%281%29.md#get) | [GetSubnetRequest](subnet%20%281%29.md#getsubnetrequest) | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |  |
| 6 | [list](subnet%20%281%29.md#list) | [SubnetQuery](subnet%20%281%29.md#subnetquery) | [SubnetsInfo](subnet%20%281%29.md#subnetsinfo) |  |
| 7 | [stat](subnet%20%281%29.md#stat) | [SubnetStatQuery](subnet%20%281%29.md#subnetstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/subnets

| Type | Message |
| :--- | :--- |
| Request | [CreateSubnetRequest](subnet%20%281%29.md#createsubnetrequest) |
| Response | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |

### update

> **PUT** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSubnetRequest](subnet%20%281%29.md#updatesubnetrequest) |
| Response | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |

### pin\_data

> **PUT** /inventory/v1/subnet/{subnet\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinSubnetDataRequest](subnet%20%281%29.md#pinsubnetdatarequest) |
| Response | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |

### delete

> **DELETE** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [SubnetRequest](subnet%20%281%29.md#subnetrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSubnetRequest](subnet%20%281%29.md#getsubnetrequest) |
| Response | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |

### list

> **GET** /inventory/v1/subnets
>
> **POST** /inventory/v1/subnets/search

| Type | Message |
| :--- | :--- |
| Request | [SubnetQuery](subnet%20%281%29.md#subnetquery) |
| Response | [SubnetsInfo](subnet%20%281%29.md#subnetsinfo) |

### stat

> **POST** /inventory/v1/subnets/stat

| Type | Message |
| :--- | :--- |
| Request | [SubnetStatQuery](subnet%20%281%29.md#subnetstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cidr | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | ip\_ranges | [IPRange](subnet%20%281%29.md#iprange) | ❌ |  |
| 4 | gateway | string | ❌ |  |
| 5 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | ❌ |  |
| 6 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 8 | reference | [SubnetReference](subnet%20%281%29.md#subnetreference) | ❌ |  |
| 9 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 10 | network\_id | string | ✅ |  |
| 11 | network\_type\_id | string | ✅ |  |
| 12 | network\_policy\_id | string | ❌ |  |
| 13 | project\_id | string | ✅ |  |
| 14 | domain\_id | string | ✅ |  |

### GetSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### IPRange

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | start | string |  |  |
| 2 | end | string |  |  |

### PinSubnetDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### SubnetInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | cidr | string |  |  |
| 4 | ip\_ranges | [IPRange](subnet%20%281%29.md#iprange) |  |  |
| 5 | gateway | string |  |  |
| 6 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 7 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | reference | [SubnetReference](subnet%20%281%29.md#subnetreference) |  |  |
| 10 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 11 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 12 | network\_info | [NetworkInfo](subnet%20%281%29.md#networkinfo) |  |  |
| 13 | network\_type\_info | [NetworkTypeInfo](subnet%20%281%29.md#networktypeinfo) |  |  |
| 14 | network\_policy\_info | [NetworkPolicyInfo](subnet%20%281%29.md#networkpolicyinfo) |  |  |
| 15 | region\_info | [RegionInfo](subnet%20%281%29.md#regioninfo) |  |  |
| 16 | zone\_info | [ZoneInfo](subnet%20%281%29.md#zoneinfo) |  |  |
| 17 | project\_id | string |  |  |
| 18 | domain\_id | string |  |  |
| 19 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### SubnetQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | subnet\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | cidr | string | ❌ |  |
| 5 | gateway | string | ❌ |  |
| 6 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | ❌ |  |
| 7 | network\_id | string | ❌ |  |
| 8 | network\_type\_id | string | ❌ |  |
| 9 | network\_policy\_id | string | ❌ |  |
| 10 | zone\_id | string | ❌ |  |
| 11 | region\_id | string | ❌ |  |
| 12 | project\_id | string | ❌ |  |
| 13 | domain\_id | string | ✅ |  |

### SubnetReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### SubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SubnetStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SubnetsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SubnetInfo](subnet%20%281%29.md#subnetinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | ip\_ranges | [IPRange](subnet%20%281%29.md#iprange) | ❌ |  |
| 4 | gateway | string | ❌ |  |
| 5 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | ❌ |  |
| 6 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 8 | reference | [SubnetReference](subnet%20%281%29.md#subnetreference) | ❌ |  |
| 9 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 10 | network\_type\_id | string | ❌ |  |
| 11 | network\_policy\_id | string | ❌ |  |
| 12 | project\_id | string | ❌ |  |
| 13 | domain\_id | string | ✅ |  |
| 14 | release\_project | bool | ❌ |  |

