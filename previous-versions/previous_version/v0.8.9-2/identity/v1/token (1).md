---
description: null
---

# Token

> **Package : spaceone.api.identity.v1**

## Token

{% hint style="info" %}
**Token Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [issue](token%20%281%29.md#issue) | [IssueTokenRequest](token%20%281%29.md#issuetokenrequest) | [TokenInfo](token%20%281%29.md#tokeninfo) |  |
| 2 | [refresh](token%20%281%29.md#refresh) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) | [TokenInfo](token%20%281%29.md#tokeninfo) |  |

### issue

> **POST** /identity/v1/token/issue

| Type | Message |
| :--- | :--- |
| Request | [IssueTokenRequest](token%20%281%29.md#issuetokenrequest) |
| Response | [TokenInfo](token%20%281%29.md#tokeninfo) |

### refresh

> **POST** /identity/v1/token/refresh

| Type | Message |
| :--- | :--- |
| Request | \[Empty\] |
| Response | [TokenInfo](token%20%281%29.md#tokeninfo) |

## Message

### IssueTokenRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | credentials | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### TokenInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | access\_token | string |  |  |
| 2 | refresh\_token | string |  |  |

