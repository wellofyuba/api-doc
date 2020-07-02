---
description: null
---

# Pool

> **Package : spaceone.api.inventory.v1**

## Pool

{% hint style="info" %}
**Pool Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/inventory/v1/pool.md#create) | [CreatePoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#createpoolrequest) | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/pool.md#update) | [UpdatePoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#updatepoolrequest) | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |  |
| 3 | [delete](../../../v0.9.0-5/inventory/v1/pool.md#delete) | [PoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/inventory/v1/pool.md#get) | [GetPoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#getpoolrequest) | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |  |
| 5 | [add\_member](../../../v0.9.0-5/inventory/v1/pool.md#add_member) | [PoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberrequest) | [PoolMemberInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberinfo) |  |
| 6 | [modify\_member](../../../v0.9.0-5/inventory/v1/pool.md#modify_member) | [PoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberrequest) | [PoolMemberInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberinfo) |  |
| 7 | [remove\_member](../../../v0.9.0-5/inventory/v1/pool.md#remove_member) | [RemovePoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#removepoolmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 8 | [list\_members](../../../v0.9.0-5/inventory/v1/pool.md#list_members) | [PoolMemberQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberquery) | [PoolMembersInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmembersinfo) |  |
| 9 | [list](../../../v0.9.0-5/inventory/v1/pool.md#list) | [PoolQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolquery) | [PoolsInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolsinfo) |  |
| 10 | [stat](../../../v0.9.0-5/inventory/v1/pool.md#stat) | [PoolStatQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/pools

| Type | Message |
| :--- | :--- |
| Request | [CreatePoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#createpoolrequest) |
| Response | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |

### update

> **PUT** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdatePoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#updatepoolrequest) |
| Response | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |

### delete

> **DELETE** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [PoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetPoolRequest](../../../v0.9.0-5/inventory/v1/pool.md#getpoolrequest) |
| Response | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |

### add\_member

> **GET** /inventory/v1/pool/{pool\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberrequest) |
| Response | [PoolMemberInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberinfo) |

### modify\_member

> **GET** /inventory/v1/pool/{pool\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberrequest) |
| Response | [PoolMemberInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberinfo) |

### remove\_member

> **GET** /inventory/v1/pool/{pool\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemovePoolMemberRequest](../../../v0.9.0-5/inventory/v1/pool.md#removepoolmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_members

> **GET** /inventory/v1/pool/{pool\_id}/members
>
> **POST** /inventory/v1/pool/{pool\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberquery) |
| Response | [PoolMembersInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmembersinfo) |

### list

> **GET** /inventory/v1/pools
>
> **POST** /inventory/v1/pools/search

| Type | Message |
| :--- | :--- |
| Request | [PoolQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolquery) |
| Response | [PoolsInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolsinfo) |

### stat

> **POST** /inventory/v1/pools/stat

| Type | Message |
| :--- | :--- |
| Request | [PoolStatQuery](../../../v0.9.0-5/inventory/v1/pool.md#poolstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreatePoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | zone\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### GetPoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### PoolInfo

<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">pool_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>PoolInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>ACTIVE</li>
          <li>DELETED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">region_info</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/inventory/v1/pool.md#regioninfo">RegionInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">zone_info</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/inventory/v1/pool.md#zoneinfo">ZoneInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">deleted_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### PoolMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_info | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |  |  |
| 2 | user\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | labels | string |  |  |

### PoolMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | pool\_id | string |  | optional |
| 3 | user\_id | string |  | optional |
| 4 | domain\_id | string |  | required |

### PoolMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | labels | string |  | optional |
| 4 | domain\_id | string |  | required |

### PoolMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PoolMemberInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PoolQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | pool\_id | string |  | optional |
| 3 | region\_id | string |  | optional |
| 4 | zone\_id | string |  | optional |
| 5 | domain\_id | string |  | required |
| 6 | name | string |  | optional |

### PoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### PoolStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### PoolsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PoolInfo](../../../v0.9.0-5/inventory/v1/pool.md#poolinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemovePoolMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### UpdatePoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | name | string |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

