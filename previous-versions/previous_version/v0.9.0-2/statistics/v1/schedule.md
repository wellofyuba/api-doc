---
description: null
---

# Schedule

> **Package : spaceone.api.statistics.v1**

## Schedule

{% hint style="info" %}
**Schedule Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [add](../../../v0.9.0-5/statistics/v1/schedule.md#add) | [AddScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#addschedulerequest) | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |
| 2 | [update](../../../v0.9.0-5/statistics/v1/schedule.md#update) | [UpdateScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#updateschedulerequest) | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |
| 3 | [enable](../../../v0.9.0-5/statistics/v1/schedule.md#enable) | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |
| 4 | [disable](../../../v0.9.0-5/statistics/v1/schedule.md#disable) | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |
| 5 | [delete](../../../v0.9.0-5/statistics/v1/schedule.md#delete) | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 6 | [get](../../../v0.9.0-5/statistics/v1/schedule.md#get) | [GetScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#getschedulerequest) | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |
| 7 | [list](../../../v0.9.0-5/statistics/v1/schedule.md#list) | [ScheduleQuery](../../../v0.9.0-5/statistics/v1/schedule.md#schedulequery) | [SchedulesInfo](../../../v0.9.0-5/statistics/v1/schedule.md#schedulesinfo) |  |
| 8 | [stat](../../../v0.9.0-5/statistics/v1/schedule.md#stat) | [ScheduleStatQuery](../../../v0.9.0-5/statistics/v1/schedule.md#schedulestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### add

> **POST** /statistics/v1/schedules

| Type | Message |
| :--- | :--- |
| Request | [AddScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#addschedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |

### update

> **PUT** /statistics/v1/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#updateschedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |

### enable

> **PUT** /statistics/v1/schedule/{schedule\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |

### disable

> **PUT** /statistics/v1/schedule/{schedule\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |

### delete

> **DELETE** /statistics/v1/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [ScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#schedulerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /statistics/v1/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetScheduleRequest](../../../v0.9.0-5/statistics/v1/schedule.md#getschedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |

### list

> **GET** /statistics/v1/schedules
>
> **POST** /statistics/v1/schedules/search

| Type | Message |
| :--- | :--- |
| Request | [ScheduleQuery](../../../v0.9.0-5/statistics/v1/schedule.md#schedulequery) |
| Response | [SchedulesInfo](../../../v0.9.0-5/statistics/v1/schedule.md#schedulesinfo) |

### stat

> **POST** /statistics/v1/schedules/stat

| Type | Message |
| :--- | :--- |
| Request | [ScheduleStatQuery](../../../v0.9.0-5/statistics/v1/schedule.md#schedulestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### AddScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | topic | string |  | required |
| 2 | options | [QueryOption](../../../v0.9.0-5/statistics/v1/schedule.md#queryoption) |  | required |
| 3 | schedule | [Scheduled](../../../v0.9.0-5/statistics/v1/schedule.md#scheduled) |  | required |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | domain\_id | string |  | required |

### GetScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | schedule\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### QueryOption

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data\_source\_id | string |  | optional |
| 2 | resource\_type | string |  | required |
| 3 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 4 | join | [ScheduleJoinQuery](../../../v0.9.0-5/statistics/v1/schedule.md#schedulejoinquery) |  | optional |
| 5 | formulas | [ScheduleFormula](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleformula) |  | optional |

### ScheduleFormula

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | formula | string |  | required |

### ScheduleInfo

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
      <td style="text-align:left">schedule_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">topic</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>ScheduleInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">options</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">schedule</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/statistics/v1/schedule.md#scheduled">Scheduled</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
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
      <td style="text-align:left">last_scheduled_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### ScheduleJoinQuery

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
      <td style="text-align:left">keys</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">type</td>
      <td style="text-align:left">
        <p>ScheduleJoinQuery.JoinType</p>
        <ul>
          <li>LEFT</li>
          <li>RIGHT</li>
          <li>OUTER</li>
          <li>INNER</li>
        </ul>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">data_source_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">resource_type</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query">spaceone.api.core.v1.StatisticsQuery</a>
      </td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### ScheduleQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | schedule\_id | string |  | optional |
| 3 | topic | string |  | optional |
| 4 | state | string |  | optional |
| 5 | data\_source\_id | string |  | optional |
| 6 | resource\_type | string |  | optional |
| 7 | domain\_id | string |  | required |

### ScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | schedule\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### ScheduleStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### Scheduled

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cron | string |  |  |
| 2 | interval | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 3 | minutes | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 4 | hours | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### SchedulesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ScheduleInfo](../../../v0.9.0-5/statistics/v1/schedule.md#scheduleinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | schedule\_id | string |  | required |
| 2 | schedule | [Scheduled](../../../v0.9.0-5/statistics/v1/schedule.md#scheduled) |  | optional |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | domain\_id | string |  | required |

