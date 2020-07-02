---
description: null
---

# Data Source

> **Package : spaceone.api.monitoring.plugin**

## DataSource

{% hint style="info" %}
**DataSource Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [verify](../../../v0.9.0-5/monitoring/plugin/data-source.md#verify) | [PluginVerifyRequest](../../../v0.9.0-5/monitoring/plugin/data-source.md#pluginverifyrequest) | [PluginVerifyResponse](../../../v0.9.0-5/monitoring/plugin/data-source.md#pluginverifyresponse) |  |

### verify

| Type | Message |
| :--- | :--- |
| Request | [PluginVerifyRequest](../../../v0.9.0-5/monitoring/plugin/data-source.md#pluginverifyrequest) |
| Response | [PluginVerifyResponse](../../../v0.9.0-5/monitoring/plugin/data-source.md#pluginverifyresponse) |

## Message

### PluginVerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### PluginVerifyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |

### PluginVerifyResponse

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_type | string |  | required |
| 2 | actions | [spaceone.api.core.v1.PluginAction](../../../v0.9.0-5/core/v1/plugin.md##pluginaction) |  | optional |
| 3 | result | [PluginVerifyInfo](../../../v0.9.0-5/monitoring/plugin/data-source.md#pluginverifyinfo) |  | required |

