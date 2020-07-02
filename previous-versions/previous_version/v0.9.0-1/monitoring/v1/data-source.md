---
description: null
---

# Data Source

> **Package : spaceone.api.monitoring.v1**

## DataSource

{% hint style="info" %}
**DataSource Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [register](../../../v0.9.0-5/monitoring/v1/data-source.md#register) | [RegisterDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#registerdatasourcerequest) | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |
| 2 | [update](../../../v0.9.0-5/monitoring/v1/data-source.md#update) | [UpdateDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#updatedatasourcerequest) | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |
| 3 | [enable](../../../v0.9.0-5/monitoring/v1/data-source.md#enable) | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |
| 4 | [disable](../../../v0.9.0-5/monitoring/v1/data-source.md#disable) | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |
| 5 | [deregister](../../../v0.9.0-5/monitoring/v1/data-source.md#deregister) | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 6 | [verify\_plugin](../../../v0.9.0-5/monitoring/v1/data-source.md#verify_plugin) | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) | [VerifyInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#verifyinfo) |  |
| 7 | [get](../../../v0.9.0-5/monitoring/v1/data-source.md#get) | [GetDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#getdatasourcerequest) | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |
| 8 | [list](../../../v0.9.0-5/monitoring/v1/data-source.md#list) | [DataSourceQuery](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcequery) | [DataSourcesInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcesinfo) |  |
| 9 | [stat](../../../v0.9.0-5/monitoring/v1/data-source.md#stat) | [DataSourceStatQuery](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### register

> **POST** /monitoring/v1/data-sources

| Type | Message |
| :--- | :--- |
| Request | [RegisterDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#registerdatasourcerequest) |
| Response | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |

### update

> **PUT** /monitoring/v1/data-source/{data\_source\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#updatedatasourcerequest) |
| Response | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |

### enable

> **PUT** /monitoring/v1/data-source/{data\_source\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) |
| Response | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |

### disable

> **PUT** /monitoring/v1/data-source/{data\_source\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) |
| Response | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |

### deregister

> **DELETE** /monitoring/v1/data-source/{data\_source\_id}

| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### verify\_plugin

> **PUT** /monitoring/v1/data-source/{data\_source\_id}/plugin/verify

| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcerequest) |
| Response | [VerifyInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#verifyinfo) |

### get

> **GET** /monitoring/v1/data-source/{data\_source\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetDataSourceRequest](../../../v0.9.0-5/monitoring/v1/data-source.md#getdatasourcerequest) |
| Response | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |

### list

> **GET** /monitoring/v1/data-sources
>
> **POST** /monitoring/v1/data-sources/search

| Type | Message |
| :--- | :--- |
| Request | [DataSourceQuery](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcequery) |
| Response | [DataSourcesInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcesinfo) |

### stat

> **POST** /monitoring/v1/data-sources/stat

| Type | Message |
| :--- | :--- |
| Request | [DataSourceStatQuery](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourcestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### DataSourceInfo

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
      <td style="text-align:left">data_source_id</td>
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
        <p>DataSourceInfo.State</p>
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
      <td style="text-align:left">monitoring_type</td>
      <td style="text-align:left">
        <p>MonitoringType</p>
        <ul>
          <li>NONE</li>
          <li>METRIC</li>
          <li>LOG</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">capability</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">plugin_info</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/monitoring/v1/data-source.md#plugininfo">PluginInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
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
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### DataSourceQuery

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
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">data_source_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">monitoring_type</td>
      <td style="text-align:left">
        <p>MonitoringType</p>
        <ul>
          <li>NONE</li>
          <li>METRIC</li>
          <li>LOG</li>
        </ul>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### DataSourceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data\_source\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### DataSourceStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### DataSourcesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [DataSourceInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#datasourceinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### GetDataSourceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data\_source\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### PluginInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin\_id | string |  |  |
| 2 | version | string |  |  |
| 3 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | secret\_id | string |  |  |
| 5 | provider | string |  |  |

### RegisterDataSourceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | plugin\_info | [PluginInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#plugininfo) |  | required |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | domain\_id | string |  | required |

### UpdateDataSourceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data\_source\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | plugin\_info | [PluginInfo](../../../v0.9.0-5/monitoring/v1/data-source.md#plugininfo) |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | domain\_id | string |  | required |

### VerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | status | bool |  |  |

