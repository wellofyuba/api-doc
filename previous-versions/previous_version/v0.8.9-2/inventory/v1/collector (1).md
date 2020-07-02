---
description: null
---

# Collector

> **Package : spaceone.api.inventory.v1**

## Collector

{% hint style="info" %}
**Collector Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](collector%20%281%29.md#create) | [CreateCollectorRequest](collector%20%281%29.md#createcollectorrequest) | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |
| 2 | [update](collector%20%281%29.md#update) | [UpdateCollectorRequest](collector%20%281%29.md#updatecollectorrequest) | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |
| 3 | [delete](collector%20%281%29.md#delete) | [CollectorRequest](collector%20%281%29.md#collectorrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](collector%20%281%29.md#get) | [GetCollectorRequest](collector%20%281%29.md#getcollectorrequest) | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |
| 5 | [enable](collector%20%281%29.md#enable) | [CollectorRequest](collector%20%281%29.md#collectorrequest) | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |
| 6 | [disable](collector%20%281%29.md#disable) | [CollectorRequest](collector%20%281%29.md#collectorrequest) | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |
| 7 | [list](collector%20%281%29.md#list) | [CollectorQuery](collector%20%281%29.md#collectorquery) | [CollectorsInfo](collector%20%281%29.md#collectorsinfo) |  |
| 8 | [stat](collector%20%281%29.md#stat) | [CollectorStatQuery](collector%20%281%29.md#collectorstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 9 | [collect](collector%20%281%29.md#collect) | [CollectRequest](collector%20%281%29.md#collectrequest) | [JobInfo](collector%20%281%29.md#jobinfo) |  |
| 10 | [verify\_plugin](collector%20%281%29.md#verify_plugin) | [VerifyPluginRequest](collector%20%281%29.md#verifypluginrequest) | [VerifyInfo](collector%20%281%29.md#verifyinfo) |  |
| 11 | [add\_schedule](collector%20%281%29.md#add_schedule) | [CreateScheduleRequest](collector%20%281%29.md#createschedulerequest) | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |  |
| 12 | [get\_schedule](collector%20%281%29.md#get_schedule) | [ScheduleRequest](collector%20%281%29.md#schedulerequest) | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |  |
| 13 | [update\_schedule](collector%20%281%29.md#update_schedule) | [UpdateScheduleRequest](collector%20%281%29.md#updateschedulerequest) | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |  |
| 14 | [delete\_schedule](collector%20%281%29.md#delete_schedule) | [DeleteScheduleRequest](collector%20%281%29.md#deleteschedulerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 15 | [list\_schedules](collector%20%281%29.md#list_schedules) | [ScheduleQuery](collector%20%281%29.md#schedulequery) | [SchedulesInfo](collector%20%281%29.md#schedulesinfo) |  |

### create

> **POST** /inventory/v1/collectors

| Type | Message |
| :--- | :--- |
| Request | [CreateCollectorRequest](collector%20%281%29.md#createcollectorrequest) |
| Response | [CollectorInfo](collector%20%281%29.md#collectorinfo) |

### update

> **PUT** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateCollectorRequest](collector%20%281%29.md#updatecollectorrequest) |
| Response | [CollectorInfo](collector%20%281%29.md#collectorinfo) |

### delete

> **DELETE** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](collector%20%281%29.md#collectorrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetCollectorRequest](collector%20%281%29.md#getcollectorrequest) |
| Response | [CollectorInfo](collector%20%281%29.md#collectorinfo) |

### enable

> **PUT** /inventory/v1/collector/{collector\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](collector%20%281%29.md#collectorrequest) |
| Response | [CollectorInfo](collector%20%281%29.md#collectorinfo) |

### disable

> **PUT** /inventory/v1/collector/{collector\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](collector%20%281%29.md#collectorrequest) |
| Response | [CollectorInfo](collector%20%281%29.md#collectorinfo) |

### list

> **GET** /inventory/v1/collectors
>
> **POST** /inventory/v1/collectors/search

| Type | Message |
| :--- | :--- |
| Request | [CollectorQuery](collector%20%281%29.md#collectorquery) |
| Response | [CollectorsInfo](collector%20%281%29.md#collectorsinfo) |

### stat

> **POST** /inventory/v1/collectors/stat

| Type | Message |
| :--- | :--- |
| Request | [CollectorStatQuery](collector%20%281%29.md#collectorstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### collect

> **POST** /inventory/v1/collector/{collector\_id}/collect

| Type | Message |
| :--- | :--- |
| Request | [CollectRequest](collector%20%281%29.md#collectrequest) |
| Response | [JobInfo](collector%20%281%29.md#jobinfo) |

### verify\_plugin

> **POST** /inventory/v1/collector/{collector\_id}/plugin/verify

| Type | Message |
| :--- | :--- |
| Request | [VerifyPluginRequest](collector%20%281%29.md#verifypluginrequest) |
| Response | [VerifyInfo](collector%20%281%29.md#verifyinfo) |

### add\_schedule

> **POST** /inventory/v1/collector/{collector\_id}/schedule

| Type | Message |
| :--- | :--- |
| Request | [CreateScheduleRequest](collector%20%281%29.md#createschedulerequest) |
| Response | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |

### get\_schedule

> **GET** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [ScheduleRequest](collector%20%281%29.md#schedulerequest) |
| Response | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |

### update\_schedule

> **POST** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateScheduleRequest](collector%20%281%29.md#updateschedulerequest) |
| Response | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |

### delete\_schedule

> **DELETE** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [DeleteScheduleRequest](collector%20%281%29.md#deleteschedulerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_schedules

> **GET** /inventory/v1/collector/{collector\_id}/schedules
>
> **POST** /inventory/v1/collector/{collector\_id}/schedules/search

| Type | Message |
| :--- | :--- |
| Request | [ScheduleQuery](collector%20%281%29.md#schedulequery) |
| Response | [SchedulesInfo](collector%20%281%29.md#schedulesinfo) |

## Message

### CollectRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string |  |  |
| 2 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 3 | secret\_id | string |  |  |
| 4 | collect\_mode | string |  |  |
| 5 | domain\_id | string |  |  |
| 6 | use\_cache | bool |  | optional |

### CollectorInfo

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
      <td style="text-align:left">collector_id</td>
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
        <p>CollectorInfo.State</p>
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
      <td style="text-align:left">plugin_info</td>
      <td style="text-align:left"> <a href="collector (1).md#plugininfo">PluginInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">priority</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a>
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
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">last_collected_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">capability</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### CollectorQuery

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
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">collector_id</td>
      <td style="text-align:left">string</td>
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
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>CollectorQuery.State</p>
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
      <td style="text-align:left">5</td>
      <td style="text-align:left">priority</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">plugin_id</td>
      <td style="text-align:left">string</td>
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
  </tbody>
</table>

### CollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CollectorStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CollectorsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### CreateCollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | plugin\_info | [PluginInfo](collector%20%281%29.md#plugininfo) | ✅ |  |
| 3 | priority | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | ❌ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | domain\_id | string | ✅ |  |

### CreateScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | collector\_id | string |  |  |
| 3 | name | string |  |  |
| 4 | collect\_mode | string |  |  |
| 5 | schedule | [Scheduled](collector%20%281%29.md#scheduled) |  |  |
| 6 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### DeleteScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | schedule\_id | string |  |  |
| 3 | collector\_id | string |  |  |

### GetCollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### JobInfo

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
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">job_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>JobInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>CREATED</li>
          <li>CANCELED</li>
          <li>IN_PROGRESS</li>
          <li>FINISHED</li>
          <li>FAILURE</li>
          <li>TIMEOUT</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">created_count</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">updated_count</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">collect_mode</td>
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
      <td style="text-align:left">finished_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">collector_info</td>
      <td style="text-align:left"> <a href="collector (1).md#collectorinfo">CollectorInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">filter</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">collected_resources</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### PluginInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin\_id | string |  |  |
| 2 | version | string |  |  |
| 3 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | secret\_id | string |  |  |
| 5 | secret\_group\_id | string |  |  |
| 6 | provider | string |  |  |

### ScheduleInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | schedule\_id | string |  |  |
| 3 | name | string |  |  |
| 4 | collect\_mode | string |  |  |
| 5 | schedule | [Scheduled](collector%20%281%29.md#scheduled) |  |  |
| 6 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 7 | last\_scheduled\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 8 | collector\_info | [CollectorInfo](collector%20%281%29.md#collectorinfo) |  |  |
| 9 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### ScheduleQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  |  |
| 2 | collector\_id | string |  |  |
| 3 | schedule\_id | string |  |  |
| 4 | domain\_id | string |  |  |

### ScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | schedule\_id | string |  |  |
| 3 | collector\_id | string |  |  |

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
| 1 | results | [ScheduleInfo](collector%20%281%29.md#scheduleinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateCollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string | ✅ |  |
| 2 | name | string | ✅ |  |
| 3 | plugin\_info | [PluginInfo](collector%20%281%29.md#plugininfo) | ✅ |  |
| 4 | priority | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | ❌ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | domain\_id | string | ✅ |  |

### UpdateScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | schedule\_id | string |  |  |
| 3 | collector\_id | string |  |  |
| 4 | name | string |  |  |
| 5 | collect\_mode | string |  |  |
| 6 | schedule | [Scheduled](collector%20%281%29.md#scheduled) |  |  |
| 7 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### VerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | status | bool |  |  |

### VerifyPluginRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string | ✅ |  |
| 2 | secret\_id | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

