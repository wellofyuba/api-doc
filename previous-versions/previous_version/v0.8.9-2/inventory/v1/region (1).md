---
description: null
---

# Region

> **Package : spaceone.api.inventory.v1**

## Region

{% hint style="info" %}
**Region Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](region%20%281%29.md#create) | [CreateRegionRequest](region%20%281%29.md#createregionrequest) | [RegionInfo](region%20%281%29.md#regioninfo) |  |
| 2 | [update](region%20%281%29.md#update) | [UpdateRegionRequest](region%20%281%29.md#updateregionrequest) | [RegionInfo](region%20%281%29.md#regioninfo) |  |
| 3 | [delete](region%20%281%29.md#delete) | [RegionRequest](region%20%281%29.md#regionrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](region%20%281%29.md#get) | [GetRegionRequest](region%20%281%29.md#getregionrequest) | [RegionInfo](region%20%281%29.md#regioninfo) |  |
| 5 | [add\_member](region%20%281%29.md#add_member) | [RegionMemberRequest](region%20%281%29.md#regionmemberrequest) | [RegionMemberInfo](region%20%281%29.md#regionmemberinfo) |  |
| 6 | [modify\_member](region%20%281%29.md#modify_member) | [RegionMemberRequest](region%20%281%29.md#regionmemberrequest) | [RegionMemberInfo](region%20%281%29.md#regionmemberinfo) |  |
| 7 | [remove\_member](region%20%281%29.md#remove_member) | [RemoveRegionMemberRequest](region%20%281%29.md#removeregionmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 8 | [list\_members](region%20%281%29.md#list_members) | [RegionMemberQuery](region%20%281%29.md#regionmemberquery) | [RegionMembersInfo](region%20%281%29.md#regionmembersinfo) |  |
| 9 | [list](region%20%281%29.md#list) | [RegionQuery](region%20%281%29.md#regionquery) | [RegionsInfo](region%20%281%29.md#regionsinfo) |  |
| 10 | [stat](region%20%281%29.md#stat) | [RegionStatQuery](region%20%281%29.md#regionstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/regions

| Type | Message |
| :--- | :--- |
| Request | [CreateRegionRequest](region%20%281%29.md#createregionrequest) |
| Response | [RegionInfo](region%20%281%29.md#regioninfo) |

### update

> **PUT** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateRegionRequest](region%20%281%29.md#updateregionrequest) |
| Response | [RegionInfo](region%20%281%29.md#regioninfo) |

### delete

> **DELETE** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [RegionRequest](region%20%281%29.md#regionrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetRegionRequest](region%20%281%29.md#getregionrequest) |
| Response | [RegionInfo](region%20%281%29.md#regioninfo) |

### add\_member

> **GET** /inventory/v1/region/{region\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberRequest](region%20%281%29.md#regionmemberrequest) |
| Response | [RegionMemberInfo](region%20%281%29.md#regionmemberinfo) |

### modify\_member

> **GET** /inventory/v1/region/{region\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberRequest](region%20%281%29.md#regionmemberrequest) |
| Response | [RegionMemberInfo](region%20%281%29.md#regionmemberinfo) |

### remove\_member

> **GET** /inventory/v1/region/{region\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveRegionMemberRequest](region%20%281%29.md#removeregionmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_members

> **GET** /inventory/v1/region/{region\_id}/members
>
> **POST** /inventory/v1/region/{region\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberQuery](region%20%281%29.md#regionmemberquery) |
| Response | [RegionMembersInfo](region%20%281%29.md#regionmembersinfo) |

### list

> **GET** /inventory/v1/regions
>
> **POST** /inventory/v1/regions/search

| Type | Message |
| :--- | :--- |
| Request | [RegionQuery](region%20%281%29.md#regionquery) |
| Response | [RegionsInfo](region%20%281%29.md#regionsinfo) |

### stat

> **POST** /inventory/v1/regions/stat

| Type | Message |
| :--- | :--- |
| Request | [RegionStatQuery](region%20%281%29.md#regionstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 3 | domain\_id | string | ✅ |  |

### GetRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### RegionInfo

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
      <td style="text-align:left">region_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>RegionInfo.State</p>
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
      <td style="text-align:left">3</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
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
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">deleted_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### RegionMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_info | [RegionInfo](region%20%281%29.md#regioninfo) |  |  |
| 2 | user\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | labels | string |  |  |

### RegionMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | region\_id | string | ❌ |  |
| 3 | user\_id | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### RegionMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | labels | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### RegionMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RegionMemberInfo](region%20%281%29.md#regionmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RegionQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | region\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### RegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### RegionStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### RegionsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RegionInfo](region%20%281%29.md#regioninfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemoveRegionMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdateRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

