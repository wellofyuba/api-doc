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
| 1 | [create](../../../v0.9.0-5/inventory/v1/collector.md#create) | [CreateCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#createcollectorrequest) | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |
| 2 | [update](../../../v0.9.0-5/inventory/v1/collector.md#update) | [UpdateCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#updatecollectorrequest) | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |
| 3 | [delete](../../../v0.9.0-5/inventory/v1/collector.md#delete) | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/inventory/v1/collector.md#get) | [GetCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#getcollectorrequest) | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |
| 5 | [enable](../../../v0.9.0-5/inventory/v1/collector.md#enable) | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |
| 6 | [disable](../../../v0.9.0-5/inventory/v1/collector.md#disable) | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |
| 7 | [list](../../../v0.9.0-5/inventory/v1/collector.md#list) | [CollectorQuery](../../../v0.9.0-5/inventory/v1/collector.md#collectorquery) | [CollectorsInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorsinfo) |  |
| 8 | [stat](../../../v0.9.0-5/inventory/v1/collector.md#stat) | [CollectorStatQuery](../../../v0.9.0-5/inventory/v1/collector.md#collectorstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 9 | [collect](../../../v0.9.0-5/inventory/v1/collector.md#collect) | [CollectRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectrequest) | [JobInfo](../../../v0.9.0-5/inventory/v1/collector.md#jobinfo) |  |
| 10 | [verify\_plugin](../../../v0.9.0-5/inventory/v1/collector.md#verify_plugin) | [VerifyPluginRequest](../../../v0.9.0-5/inventory/v1/collector.md#verifypluginrequest) | [VerifyInfo](../../../v0.9.0-5/inventory/v1/collector.md#verifyinfo) |  |
| 11 | [add\_schedule](../../../v0.9.0-5/inventory/v1/collector.md#add_schedule) | [CreateScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#createschedulerequest) | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |  |
| 12 | [get\_schedule](../../../v0.9.0-5/inventory/v1/collector.md#get_schedule) | [ScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#schedulerequest) | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |  |
| 13 | [update\_schedule](../../../v0.9.0-5/inventory/v1/collector.md#update_schedule) | [UpdateScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#updateschedulerequest) | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |  |
| 14 | [delete\_schedule](../../../v0.9.0-5/inventory/v1/collector.md#delete_schedule) | [DeleteScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#deleteschedulerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 15 | [list\_schedules](../../../v0.9.0-5/inventory/v1/collector.md#list_schedules) | [ScheduleQuery](../../../v0.9.0-5/inventory/v1/collector.md#schedulequery) | [SchedulesInfo](../../../v0.9.0-5/inventory/v1/collector.md#schedulesinfo) |  |

### create

> **POST** /inventory/v1/collectors

| Type | Message |
| :--- | :--- |
| Request | [CreateCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#createcollectorrequest) |
| Response | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |

### update

> **PUT** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#updatecollectorrequest) |
| Response | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |

### delete

> **DELETE** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/collector/{collector\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetCollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#getcollectorrequest) |
| Response | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |

### enable

> **PUT** /inventory/v1/collector/{collector\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) |
| Response | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |

### disable

> **PUT** /inventory/v1/collector/{collector\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [CollectorRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectorrequest) |
| Response | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |

### list

> **GET** /inventory/v1/collectors
>
> **POST** /inventory/v1/collectors/search

| Type | Message |
| :--- | :--- |
| Request | [CollectorQuery](../../../v0.9.0-5/inventory/v1/collector.md#collectorquery) |
| Response | [CollectorsInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorsinfo) |

### stat

> **POST** /inventory/v1/collectors/stat

| Type | Message |
| :--- | :--- |
| Request | [CollectorStatQuery](../../../v0.9.0-5/inventory/v1/collector.md#collectorstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### collect

> **POST** /inventory/v1/collector/{collector\_id}/collect

| Type | Message |
| :--- | :--- |
| Request | [CollectRequest](../../../v0.9.0-5/inventory/v1/collector.md#collectrequest) |
| Response | [JobInfo](../../../v0.9.0-5/inventory/v1/collector.md#jobinfo) |

### verify\_plugin

> **POST** /inventory/v1/collector/{collector\_id}/plugin/verify

| Type | Message |
| :--- | :--- |
| Request | [VerifyPluginRequest](../../../v0.9.0-5/inventory/v1/collector.md#verifypluginrequest) |
| Response | [VerifyInfo](../../../v0.9.0-5/inventory/v1/collector.md#verifyinfo) |

### add\_schedule

> **POST** /inventory/v1/collector/{collector\_id}/schedule

| Type | Message |
| :--- | :--- |
| Request | [CreateScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#createschedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |

### get\_schedule

> **GET** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [ScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#schedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |

### update\_schedule

> **POST** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#updateschedulerequest) |
| Response | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |

### delete\_schedule

> **DELETE** /inventory/v1/collector/{collector\_id}/schedule/{schedule\_id}

| Type | Message |
| :--- | :--- |
| Request | [DeleteScheduleRequest](../../../v0.9.0-5/inventory/v1/collector.md#deleteschedulerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### list\_schedules

> **GET** /inventory/v1/collector/{collector\_id}/schedules
>
> **POST** /inventory/v1/collector/{collector\_id}/schedules/search

| Type | Message |
| :--- | :--- |
| Request | [ScheduleQuery](../../../v0.9.0-5/inventory/v1/collector.md#schedulequery) |
| Response | [SchedulesInfo](../../../v0.9.0-5/inventory/v1/collector.md#schedulesinfo) |

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
      <td style="text-align:left"> <a href="../../../v0.9.0-5/inventory/v1/collector.md#plugininfo">PluginInfo</a>
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
| 1 | collector\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### CollectorStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### CollectorsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### CreateCollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | plugin\_info | [PluginInfo](../../../v0.9.0-5/inventory/v1/collector.md#plugininfo) |  | required |
| 3 | priority | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | domain\_id | string |  | required |

### CreateScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | collector\_id | string |  |  |
| 3 | name | string |  |  |
| 4 | collect\_mode | string |  |  |
| 5 | schedule | [Scheduled](../../../v0.9.0-5/inventory/v1/collector.md#scheduled) |  |  |
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
| 1 | collector\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

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
      <td style="text-align:left"> <a href="../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo">CollectorInfo</a>
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
| 5 | schedule | [Scheduled](../../../v0.9.0-5/inventory/v1/collector.md#scheduled) |  |  |
| 6 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 7 | last\_scheduled\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 8 | collector\_info | [CollectorInfo](../../../v0.9.0-5/inventory/v1/collector.md#collectorinfo) |  |  |
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
| 1 | results | [ScheduleInfo](../../../v0.9.0-5/inventory/v1/collector.md#scheduleinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateCollectorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string |  | required |
| 2 | name | string |  | required |
| 3 | plugin\_info | [PluginInfo](../../../v0.9.0-5/inventory/v1/collector.md#plugininfo) |  | required |
| 4 | priority | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | domain\_id | string |  | required |

### UpdateScheduleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | schedule\_id | string |  |  |
| 3 | collector\_id | string |  |  |
| 4 | name | string |  |  |
| 5 | collect\_mode | string |  |  |
| 6 | schedule | [Scheduled](../../../v0.9.0-5/inventory/v1/collector.md#scheduled) |  |  |
| 7 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### VerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | status | bool |  |  |

### VerifyPluginRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | collector\_id | string |  | required |
| 2 | secret\_id | string |  | required |
| 3 | domain\_id | string |  |  |

