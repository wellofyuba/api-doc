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
| 1 | [create](../../../v0.9.0-5/inventory/v1/region.md#create) | [CreateRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#createregionrequest) | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/region.md#update) | [UpdateRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#updateregionrequest) | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |  |
| 3 | [delete](../../../v0.9.0-5/inventory/v1/region.md#delete) | [RegionRequest](../../../v0.9.0-5/inventory/v1/region.md#regionrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/inventory/v1/region.md#get) | [GetRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#getregionrequest) | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |  |
| 5 | [add\_member](../../../v0.9.0-5/inventory/v1/region.md#add_member) | [RegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#regionmemberrequest) | [RegionMemberInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmemberinfo) |  |
| 6 | [modify\_member](../../../v0.9.0-5/inventory/v1/region.md#modify_member) | [RegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#regionmemberrequest) | [RegionMemberInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmemberinfo) |  |
| 7 | [remove\_member](../../../v0.9.0-5/inventory/v1/region.md#remove_member) | [RemoveRegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#removeregionmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 8 | [list\_members](../../../v0.9.0-5/inventory/v1/region.md#list_members) | [RegionMemberQuery](../../../v0.9.0-5/inventory/v1/region.md#regionmemberquery) | [RegionMembersInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmembersinfo) |  |
| 9 | [list](../../../v0.9.0-5/inventory/v1/region.md#list) | [RegionQuery](../../../v0.9.0-5/inventory/v1/region.md#regionquery) | [RegionsInfo](../../../v0.9.0-5/inventory/v1/region.md#regionsinfo) |  |
| 10 | [stat](../../../v0.9.0-5/inventory/v1/region.md#stat) | [RegionStatQuery](../../../v0.9.0-5/inventory/v1/region.md#regionstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/regions

| Type | Message |
| :--- | :--- |
| Request | [CreateRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#createregionrequest) |
| Response | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |

### update

> **PUT** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#updateregionrequest) |
| Response | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |

### delete

> **DELETE** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [RegionRequest](../../../v0.9.0-5/inventory/v1/region.md#regionrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/region/{region\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetRegionRequest](../../../v0.9.0-5/inventory/v1/region.md#getregionrequest) |
| Response | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |

### add\_member

> **GET** /inventory/v1/region/{region\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#regionmemberrequest) |
| Response | [RegionMemberInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmemberinfo) |

### modify\_member

> **GET** /inventory/v1/region/{region\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#regionmemberrequest) |
| Response | [RegionMemberInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmemberinfo) |

### remove\_member

> **GET** /inventory/v1/region/{region\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveRegionMemberRequest](../../../v0.9.0-5/inventory/v1/region.md#removeregionmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_members

> **GET** /inventory/v1/region/{region\_id}/members
>
> **POST** /inventory/v1/region/{region\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [RegionMemberQuery](../../../v0.9.0-5/inventory/v1/region.md#regionmemberquery) |
| Response | [RegionMembersInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmembersinfo) |

### list

> **GET** /inventory/v1/regions
>
> **POST** /inventory/v1/regions/search

| Type | Message |
| :--- | :--- |
| Request | [RegionQuery](../../../v0.9.0-5/inventory/v1/region.md#regionquery) |
| Response | [RegionsInfo](../../../v0.9.0-5/inventory/v1/region.md#regionsinfo) |

### stat

> **POST** /inventory/v1/regions/stat

| Type | Message |
| :--- | :--- |
| Request | [RegionStatQuery](../../../v0.9.0-5/inventory/v1/region.md#regionstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 3 | domain\_id | string |  | required |

### GetRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

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
| 1 | region\_info | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |  |  |
| 2 | user\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | labels | string |  |  |

### RegionMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | region\_id | string |  | optional |
| 3 | user\_id | string |  | optional |
| 4 | domain\_id | string |  |  |

### RegionMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | labels | string |  | optional |
| 4 | domain\_id | string |  | required |

### RegionMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RegionMemberInfo](../../../v0.9.0-5/inventory/v1/region.md#regionmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RegionQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | region\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | domain\_id | string |  | required |

### RegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### RegionStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### RegionsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RegionInfo](../../../v0.9.0-5/inventory/v1/region.md#regioninfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemoveRegionMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### UpdateRegionRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | region\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | domain\_id | string |  | required |

