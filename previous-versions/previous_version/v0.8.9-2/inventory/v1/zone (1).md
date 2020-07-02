---
description: null
---

# Zone

> **Package : spaceone.api.inventory.v1**

## Zone

{% hint style="info" %}
**Zone Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](zone%20%281%29.md#create) | [CreateZoneRequest](zone%20%281%29.md#createzonerequest) | [ZoneInfo](zone%20%281%29.md#zoneinfo) |  |
| 2 | [update](zone%20%281%29.md#update) | [UpdateZoneRequest](zone%20%281%29.md#updatezonerequest) | [ZoneInfo](zone%20%281%29.md#zoneinfo) |  |
| 3 | [delete](zone%20%281%29.md#delete) | [ZoneRequest](zone%20%281%29.md#zonerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](zone%20%281%29.md#get) | [GetZoneRequest](zone%20%281%29.md#getzonerequest) | [ZoneInfo](zone%20%281%29.md#zoneinfo) |  |
| 5 | [add\_member](zone%20%281%29.md#add_member) | [ZoneMemberRequest](zone%20%281%29.md#zonememberrequest) | [ZoneMemberInfo](zone%20%281%29.md#zonememberinfo) |  |
| 6 | [modify\_member](zone%20%281%29.md#modify_member) | [ZoneMemberRequest](zone%20%281%29.md#zonememberrequest) | [ZoneMemberInfo](zone%20%281%29.md#zonememberinfo) |  |
| 7 | [remove\_member](zone%20%281%29.md#remove_member) | [RemoveZoneMemberRequest](zone%20%281%29.md#removezonememberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 8 | [list\_members](zone%20%281%29.md#list_members) | [ZoneMemberQuery](zone%20%281%29.md#zonememberquery) | [ZoneMembersInfo](zone%20%281%29.md#zonemembersinfo) |  |
| 9 | [list](zone%20%281%29.md#list) | [ZoneQuery](zone%20%281%29.md#zonequery) | [ZonesInfo](zone%20%281%29.md#zonesinfo) |  |
| 10 | [stat](zone%20%281%29.md#stat) | [ZoneStatQuery](zone%20%281%29.md#zonestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/zones

| Type | Message |
| :--- | :--- |
| Request | [CreateZoneRequest](zone%20%281%29.md#createzonerequest) |
| Response | [ZoneInfo](zone%20%281%29.md#zoneinfo) |

### update

> **PUT** /inventory/v1/zone/{zone\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateZoneRequest](zone%20%281%29.md#updatezonerequest) |
| Response | [ZoneInfo](zone%20%281%29.md#zoneinfo) |

### delete

> **DELETE** /inventory/v1/zone/{zone\_id}

| Type | Message |
| :--- | :--- |
| Request | [ZoneRequest](zone%20%281%29.md#zonerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/zone/{zone\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetZoneRequest](zone%20%281%29.md#getzonerequest) |
| Response | [ZoneInfo](zone%20%281%29.md#zoneinfo) |

### add\_member

> **GET** /inventory/v1/zone/{zone\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [ZoneMemberRequest](zone%20%281%29.md#zonememberrequest) |
| Response | [ZoneMemberInfo](zone%20%281%29.md#zonememberinfo) |

### modify\_member

> **GET** /inventory/v1/zone/{zone\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [ZoneMemberRequest](zone%20%281%29.md#zonememberrequest) |
| Response | [ZoneMemberInfo](zone%20%281%29.md#zonememberinfo) |

### remove\_member

> **GET** /inventory/v1/zone/{zone\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveZoneMemberRequest](zone%20%281%29.md#removezonememberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_members

> **GET** /inventory/v1/zone/{zone\_id}/members
>
> **POST** /inventory/v1/zone/{zone\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [ZoneMemberQuery](zone%20%281%29.md#zonememberquery) |
| Response | [ZoneMembersInfo](zone%20%281%29.md#zonemembersinfo) |

### list

> **GET** /inventory/v1/zones
>
> **POST** /inventory/v1/zones/search

| Type | Message |
| :--- | :--- |
| Request | [ZoneQuery](zone%20%281%29.md#zonequery) |
| Response | [ZonesInfo](zone%20%281%29.md#zonesinfo) |

### stat

> **POST** /inventory/v1/zones/stat

| Type | Message |
| :--- | :--- |
| Request | [ZoneStatQuery](zone%20%281%29.md#zonestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateZoneRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | region\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

### GetZoneRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### RemoveZoneMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdateZoneRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### ZoneInfo

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
      <td style="text-align:left">zone_id</td>
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
        <p>ZoneInfo.State</p>
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
      <td style="text-align:left">region_info</td>
      <td style="text-align:left"> <a href="zone (1).md#regioninfo">RegionInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">deleted_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### ZoneMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_info | [ZoneInfo](zone%20%281%29.md#zoneinfo) |  |  |
| 2 | user\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | labels | string |  |  |

### ZoneMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | zone\_id | string | ❌ |  |
| 3 | user\_id | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### ZoneMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ✅ |  |
| 2 | user\_id | string | ✅ |  |
| 3 | labels | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### ZoneMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ZoneMemberInfo](zone%20%281%29.md#zonememberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### ZoneQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ❌ |  |
| 2 | region\_id | string | ❌ |  |
| 3 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 4 | name | string | ❌ |  |
| 5 | domain\_id | string | ✅ |  |

### ZoneRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | zone\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ZoneStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ZonesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ZoneInfo](zone%20%281%29.md#zoneinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

