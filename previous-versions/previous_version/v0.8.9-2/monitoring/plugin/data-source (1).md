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
| 1 | [verify](data-source%20%281%29.md#verify) | [PluginVerifyRequest](data-source%20%281%29.md#pluginverifyrequest) | [PluginVerifyResponse](data-source%20%281%29.md#pluginverifyresponse) |  |

### verify

| Type | Message |
| :--- | :--- |
| Request | [PluginVerifyRequest](data-source%20%281%29.md#pluginverifyrequest) |
| Response | [PluginVerifyResponse](data-source%20%281%29.md#pluginverifyresponse) |

## Message

### PluginVerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### PluginVerifyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |

### PluginVerifyResponse

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_type | string | ✅ |  |
| 2 | actions | [spaceone.api.core.v1.PluginAction](../../core/v1/plugin%20%281%29.md##pluginaction) | ❌ |  |
| 3 | result | [PluginVerifyInfo](data-source%20%281%29.md#pluginverifyinfo) | ✅ |  |

