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
| 1 | [create](pool%20%281%29.md#create) | [CreatePoolRequest](pool%20%281%29.md#createpoolrequest) | [PoolInfo](pool%20%281%29.md#poolinfo) |  |
| 2 | [update](pool%20%281%29.md#update) | [UpdatePoolRequest](pool%20%281%29.md#updatepoolrequest) | [PoolInfo](pool%20%281%29.md#poolinfo) |  |
| 3 | [delete](pool%20%281%29.md#delete) | [PoolRequest](pool%20%281%29.md#poolrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](pool%20%281%29.md#get) | [GetPoolRequest](pool%20%281%29.md#getpoolrequest) | [PoolInfo](pool%20%281%29.md#poolinfo) |  |
| 5 | [add\_member](pool%20%281%29.md#add_member) | [PoolMemberRequest](pool%20%281%29.md#poolmemberrequest) | [PoolMemberInfo](pool%20%281%29.md#poolmemberinfo) |  |
| 6 | [modify\_member](pool%20%281%29.md#modify_member) | [PoolMemberRequest](pool%20%281%29.md#poolmemberrequest) | [PoolMemberInfo](pool%20%281%29.md#poolmemberinfo) |  |
| 7 | [remove\_member](pool%20%281%29.md#remove_member) | [RemovePoolMemberRequest](pool%20%281%29.md#removepoolmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 8 | [list\_members](pool%20%281%29.md#list_members) | [PoolMemberQuery](pool%20%281%29.md#poolmemberquery) | [PoolMembersInfo](pool%20%281%29.md#poolmembersinfo) |  |
| 9 | [list](pool%20%281%29.md#list) | [PoolQuery](pool%20%281%29.md#poolquery) | [PoolsInfo](pool%20%281%29.md#poolsinfo) |  |
| 10 | [stat](pool%20%281%29.md#stat) | [PoolStatQuery](pool%20%281%29.md#poolstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/pools

| Type | Message |
| :--- | :--- |
| Request | [CreatePoolRequest](pool%20%281%29.md#createpoolrequest) |
| Response | [PoolInfo](pool%20%281%29.md#poolinfo) |

### update

> **PUT** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdatePoolRequest](pool%20%281%29.md#updatepoolrequest) |
| Response | [PoolInfo](pool%20%281%29.md#poolinfo) |

### delete

> **DELETE** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [PoolRequest](pool%20%281%29.md#poolrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/pool/{pool\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetPoolRequest](pool%20%281%29.md#getpoolrequest) |
| Response | [PoolInfo](pool%20%281%29.md#poolinfo) |

### add\_member

> **GET** /inventory/v1/pool/{pool\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberRequest](pool%20%281%29.md#poolmemberrequest) |
| Response | [PoolMemberInfo](pool%20%281%29.md#poolmemberinfo) |

### modify\_member

> **GET** /inventory/v1/pool/{pool\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberRequest](pool%20%281%29.md#poolmemberrequest) |
| Response | [PoolMemberInfo](pool%20%281%29.md#poolmemberinfo) |

### remove\_member

> **GET** /inventory/v1/pool/{pool\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemovePoolMemberRequest](pool%20%281%29.md#removepoolmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_members

> **GET** /inventory/v1/pool/{pool\_id}/members
>
> **POST** /inventory/v1/pool/{pool\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [PoolMemberQuery](pool%20%281%29.md#poolmemberquery) |
| Response | [PoolMembersInfo](pool%20%281%29.md#poolmembersinfo) |

### list

> **GET** /inventory/v1/pools
>
> **POST** /inventory/v1/pools/search

| Type | Message |
| :--- | :--- |
| Request | [PoolQuery](pool%20%281%29.md#poolquery) |
| Response | [PoolsInfo](pool%20%281%29.md#poolsinfo) |

### stat

> **POST** /inventory/v1/pools/stat

| Type | Message |
| :--- | :--- |
| Request | [PoolStatQuery](pool%20%281%29.md#poolstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreatePoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | zone\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

### GetPoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

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
      <td style="text-align:left"> <a href="pool (1).md#regioninfo">RegionInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">zone_info</td>
      <td style="text-align:left"> <a href="pool (1).md#zoneinfo">ZoneInfo</a>
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
| 1 | pool\_info | [PoolInfo](pool%20%281%29.md#poolinfo) |  |  |
| 2 | user\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | labels | string |  |  |

### PoolMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | pool\_id | string | ❌ |  |
| 3 | user\_id | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### PoolMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | labels | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### PoolMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PoolMemberInfo](pool%20%281%29.md#poolmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PoolQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | pool\_id | string | ❌ |  |
| 3 | region\_id | string | ❌ |  |
| 4 | zone\_id | string | ❌ |  |
| 5 | domain\_id | string | ✅ |  |
| 6 | name | string | ❌ |  |

### PoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### PoolStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### PoolsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PoolInfo](pool%20%281%29.md#poolinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemovePoolMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdatePoolRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | pool\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | name | string | ❌ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

