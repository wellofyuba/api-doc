---
description: null
---

# Supervisor

> **Package : spaceone.api.plugin.v1**

## Supervisor

{% hint style="info" %}
**Supervisor Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [publish](supervisor%20%281%29.md#publish) | [PublishSupervisorRequest](supervisor%20%281%29.md#publishsupervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 2 | [register](supervisor%20%281%29.md#register) | [RegisterSupervisorRequest](supervisor%20%281%29.md#registersupervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 3 | [update](supervisor%20%281%29.md#update) | [RegisterSupervisorRequest](supervisor%20%281%29.md#registersupervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 4 | [deregister](supervisor%20%281%29.md#deregister) | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [enable](supervisor%20%281%29.md#enable) | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 6 | [disable](supervisor%20%281%29.md#disable) | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 7 | [recover\_plugin](supervisor%20%281%29.md#recover_plugin) | [RecoverPluginRequest](supervisor%20%281%29.md#recoverpluginrequest) | [PluginInfo](supervisor%20%281%29.md#plugininfo) |  |
| 8 | [get](supervisor%20%281%29.md#get) | [GetSupervisorRequest](supervisor%20%281%29.md#getsupervisorrequest) | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |
| 9 | [list](supervisor%20%281%29.md#list) | [SupervisorQuery](supervisor%20%281%29.md#supervisorquery) | [SupervisorsInfo](supervisor%20%281%29.md#supervisorsinfo) |  |
| 10 | [stat](supervisor%20%281%29.md#stat) | [SupervisorStatQuery](supervisor%20%281%29.md#supervisorstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 11 | [list\_plugins](supervisor%20%281%29.md#list_plugins) | [PluginQuery](supervisor%20%281%29.md#pluginquery) | [PluginsInfo](supervisor%20%281%29.md#pluginsinfo) |  |

### publish

> **POST** /plugin/v1/supervisors

| Type | Message |
| :--- | :--- |
| Request | [PublishSupervisorRequest](supervisor%20%281%29.md#publishsupervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### register

> **POST** /plugin/v1/supervisor/{supervisor\_id}/register

| Type | Message |
| :--- | :--- |
| Request | [RegisterSupervisorRequest](supervisor%20%281%29.md#registersupervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### update

> **PUT** /plugin/v1/supervisor/{supervisor\_id}

| Type | Message |
| :--- | :--- |
| Request | [RegisterSupervisorRequest](supervisor%20%281%29.md#registersupervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### deregister

> **DELETE** /plugin/v1/supervisor/{supervisor\_id}/register

| Type | Message |
| :--- | :--- |
| Request | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### enable

> **PUT** /plugin/v1/supervisor/{supervisor\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### disable

> **PUT** /plugin/v1/supervisor/{supervisor\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [SupervisorRequest](supervisor%20%281%29.md#supervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### recover\_plugin

> **POST** /plugin/v1/supervisor/{supervisor\_id}/plugin/{plugin\_id}/recover

| Type | Message |
| :--- | :--- |
| Request | [RecoverPluginRequest](supervisor%20%281%29.md#recoverpluginrequest) |
| Response | [PluginInfo](supervisor%20%281%29.md#plugininfo) |

### get

> **GET** /plugin/v1/supervisor/{supervisor\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSupervisorRequest](supervisor%20%281%29.md#getsupervisorrequest) |
| Response | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |

### list

> **GET** /plugin/v1/supervisors
>
> **POST** /plugin/v1/supervisors/search

| Type | Message |
| :--- | :--- |
| Request | [SupervisorQuery](supervisor%20%281%29.md#supervisorquery) |
| Response | [SupervisorsInfo](supervisor%20%281%29.md#supervisorsinfo) |

### stat

> **POST** /plugin/v1/supervisors/stat

| Type | Message |
| :--- | :--- |
| Request | [SupervisorStatQuery](supervisor%20%281%29.md#supervisorstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### list\_plugins

> **GET** /plugin/v1/supervisor/{supervisor\_id}/plugins
>
> **POST** /plugin/v1/supervisor/{supervisor\_id}/plugins/search

| Type | Message |
| :--- | :--- |
| Request | [PluginQuery](supervisor%20%281%29.md#pluginquery) |
| Response | [PluginsInfo](supervisor%20%281%29.md#pluginsinfo) |

## Message

### GetSupervisorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | supervisor\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### PluginInfo

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
      <td style="text-align:left">plugin_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">version</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>PluginInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>PROVISIONING</li>
          <li>ACTIVE</li>
          <li>RE_PROVISIONING</li>
          <li>ERROR</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">endpoint</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">supervisor_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">supervisor_name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">managed</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">endpoints</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### PluginQuery

<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">supervisor_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">hostname</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">plugin_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">version</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>PluginQuery.State</p>
        <ul>
          <li>NONE</li>
          <li>PROVISIONING</li>
          <li>ACTIVE</li>
          <li>RE_PROVISIONING</li>
          <li>ERROR</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">endpoint</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### PluginsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PluginInfo](supervisor%20%281%29.md#plugininfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PublishSupervisorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | hostname | string |  | required |
| 3 | secret\_key | string |  | optional |
| 4 | plugin\_info | [PluginInfo](supervisor%20%281%29.md#plugininfo) |  | optional |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | is\_public | bool |  | optional |
| 7 | domain\_id | string |  | required |

### RecoverPluginRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | supervisor\_id | string |  | required |
| 2 | plugin\_id | string |  | required |
| 3 | version | string |  | required |
| 4 | domain\_id | string |  | required |

### RegisterSupervisorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | supervisor\_id | string |  | required |
| 2 | name | string |  | required |
| 3 | is\_public | bool |  | optional |
| 4 | priority | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |
| 5 | labels | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 7 | domain\_id | string |  | required |

### SupervisorInfo

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
      <td style="text-align:left">supervisor_id</td>
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
      <td style="text-align:left">hostname</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>SupervisorInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
          <li>PENDING</li>
          <li>DISCONNECTED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">is_public</td>
      <td style="text-align:left">bool</td>
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
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">labels</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">updated_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### SupervisorQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | supervisor\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | is\_public | bool | ❌ |  |
| 5 | domain\_id | string | ✅ |  |

### SupervisorRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | supervisor\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### SupervisorStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SupervisorsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SupervisorInfo](supervisor%20%281%29.md#supervisorinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

