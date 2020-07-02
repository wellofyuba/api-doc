---
description: null
---

# Log

> **Package : spaceone.api.monitoring.plugin**

## Log

{% hint style="info" %}
**Log Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [list](../../../v0.9.0-5/monitoring/plugin/log.md#list) | [LogRequest](../../../v0.9.0-5/monitoring/plugin/log.md#logrequest) | [PluginLogsResponse](../../../v0.9.0-5/monitoring/plugin/log.md#pluginlogsresponse) |  |

### list

| Type | Message |
| :--- | :--- |
| Request | [LogRequest](../../../v0.9.0-5/monitoring/plugin/log.md#logrequest) |
| Response | [PluginLogsResponse](../../../v0.9.0-5/monitoring/plugin/log.md#pluginlogsresponse) |

## Message

### LogRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 3 | filter | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 4 | resource | string |  | optional |
| 5 | start | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  | optional |
| 6 | end | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  | optional |
| 7 | sort | [Sort](../../../v0.9.0-5/monitoring/plugin/log.md#sort) |  | optional |
| 8 | limit | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  | optional |

### LogsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | logs | [google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview) |  |  |

### PluginLogsResponse

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_type | string |  | required |
| 2 | actions | [spaceone.api.core.v1.PluginAction]() |  | optional |
| 3 | result | [LogsInfo](../../../v0.9.0-5/monitoring/plugin/log.md#logsinfo) |  | required |

### Sort

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | key | string |  |  |
| 2 | desc | bool |  |  |

