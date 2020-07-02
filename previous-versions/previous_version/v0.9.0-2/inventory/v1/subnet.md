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
| 1 | [create](../../../v0.9.0-5/inventory/v1/subnet.md#create) | [CreateSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#createsubnetrequest) | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/subnet.md#update) | [UpdateSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#updatesubnetrequest) | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |  |
| 3 | [pin\_data](../../../v0.9.0-5/inventory/v1/subnet.md#pin_data) | [PinSubnetDataRequest](../../../v0.9.0-5/inventory/v1/subnet.md#pinsubnetdatarequest) | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |  |
| 4 | [delete](../../../v0.9.0-5/inventory/v1/subnet.md#delete) | [SubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#subnetrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](../../../v0.9.0-5/inventory/v1/subnet.md#get) | [GetSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#getsubnetrequest) | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |  |
| 6 | [list](../../../v0.9.0-5/inventory/v1/subnet.md#list) | [SubnetQuery](../../../v0.9.0-5/inventory/v1/subnet.md#subnetquery) | [SubnetsInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetsinfo) |  |
| 7 | [stat](../../../v0.9.0-5/inventory/v1/subnet.md#stat) | [SubnetStatQuery](../../../v0.9.0-5/inventory/v1/subnet.md#subnetstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/subnets

| Type | Message |
| :--- | :--- |
| Request | [CreateSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#createsubnetrequest) |
| Response | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |

### update

> **PUT** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#updatesubnetrequest) |
| Response | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |

### pin\_data

> **PUT** /inventory/v1/subnet/{subnet\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinSubnetDataRequest](../../../v0.9.0-5/inventory/v1/subnet.md#pinsubnetdatarequest) |
| Response | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |

### delete

> **DELETE** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [SubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#subnetrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/subnet/{subnet\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSubnetRequest](../../../v0.9.0-5/inventory/v1/subnet.md#getsubnetrequest) |
| Response | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |

### list

> **GET** /inventory/v1/subnets
>
> **POST** /inventory/v1/subnets/search

| Type | Message |
| :--- | :--- |
| Request | [SubnetQuery](../../../v0.9.0-5/inventory/v1/subnet.md#subnetquery) |
| Response | [SubnetsInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetsinfo) |

### stat

> **POST** /inventory/v1/subnets/stat

| Type | Message |
| :--- | :--- |
| Request | [SubnetStatQuery](../../../v0.9.0-5/inventory/v1/subnet.md#subnetstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cidr | string |  | required |
| 2 | name | string |  | optional |
| 3 | ip\_ranges | [IPRange](../../../v0.9.0-5/inventory/v1/subnet.md#iprange) |  | optional |
| 4 | gateway | string |  | optional |
| 5 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 6 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 7 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 8 | reference | [SubnetReference](../../../v0.9.0-5/inventory/v1/subnet.md#subnetreference) |  | optional |
| 9 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 10 | network\_id | string |  | required |
| 11 | network\_type\_id | string |  | required |
| 12 | network\_policy\_id | string |  | optional |
| 13 | project\_id | string |  | required |
| 14 | domain\_id | string |  | required |

### GetSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### IPRange

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | start | string |  |  |
| 2 | end | string |  |  |

### PinSubnetDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  | required |
| 2 | keys | string |  | required |
| 3 | domain\_id | string |  | required |

### SubnetInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | cidr | string |  |  |
| 4 | ip\_ranges | [IPRange](../../../v0.9.0-5/inventory/v1/subnet.md#iprange) |  |  |
| 5 | gateway | string |  |  |
| 6 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 7 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | reference | [SubnetReference](../../../v0.9.0-5/inventory/v1/subnet.md#subnetreference) |  |  |
| 10 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 11 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 12 | network\_info | [NetworkInfo](../../../v0.9.0-5/inventory/v1/subnet.md#networkinfo) |  |  |
| 13 | network\_type\_info | [NetworkTypeInfo](../../../v0.9.0-5/inventory/v1/subnet.md#networktypeinfo) |  |  |
| 14 | network\_policy\_info | [NetworkPolicyInfo](../../../v0.9.0-5/inventory/v1/subnet.md#networkpolicyinfo) |  |  |
| 15 | region\_info | [RegionInfo](../../../v0.9.0-5/inventory/v1/subnet.md#regioninfo) |  |  |
| 16 | zone\_info | [ZoneInfo](../../../v0.9.0-5/inventory/v1/subnet.md#zoneinfo) |  |  |
| 17 | project\_id | string |  |  |
| 18 | domain\_id | string |  |  |
| 19 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### SubnetQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | subnet\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | cidr | string |  | optional |
| 5 | gateway | string |  | optional |
| 6 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 7 | network\_id | string |  | optional |
| 8 | network\_type\_id | string |  | optional |
| 9 | network\_policy\_id | string |  | optional |
| 10 | zone\_id | string |  | optional |
| 11 | region\_id | string |  | optional |
| 12 | project\_id | string |  | optional |
| 13 | domain\_id | string |  | required |

### SubnetReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### SubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### SubnetStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### SubnetsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SubnetInfo](../../../v0.9.0-5/inventory/v1/subnet.md#subnetinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSubnetRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | subnet\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | ip\_ranges | [IPRange](../../../v0.9.0-5/inventory/v1/subnet.md#iprange) |  | optional |
| 4 | gateway | string |  | optional |
| 5 | vlan | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 6 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 7 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 8 | reference | [SubnetReference](../../../v0.9.0-5/inventory/v1/subnet.md#subnetreference) |  | optional |
| 9 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 10 | network\_type\_id | string |  | optional |
| 11 | network\_policy\_id | string |  | optional |
| 12 | project\_id | string |  | optional |
| 13 | domain\_id | string |  | required |
| 14 | release\_project | bool |  | optional |

