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
| 1 | [issue](../../../v0.9.0-5/identity/v1/token.md#issue) | [IssueTokenRequest](../../../v0.9.0-5/identity/v1/token.md#issuetokenrequest) | [TokenInfo](../../../v0.9.0-5/identity/v1/token.md#tokeninfo) |  |
| 2 | [refresh](../../../v0.9.0-5/identity/v1/token.md#refresh) | \[Empty\] | [TokenInfo](../../../v0.9.0-5/identity/v1/token.md#tokeninfo) |  |

### issue

> **POST** /identity/v1/token/issue

| Type | Message |
| :--- | :--- |
| Request | [IssueTokenRequest](../../../v0.9.0-5/identity/v1/token.md#issuetokenrequest) |
| Response | [TokenInfo](../../../v0.9.0-5/identity/v1/token.md#tokeninfo) |

### refresh

> **POST** /identity/v1/token/refresh

| Type | Message |
| :--- | :--- |
| Request | \[Empty\] |
| Response | [TokenInfo](../../../v0.9.0-5/identity/v1/token.md#tokeninfo) |

## Message

### IssueTokenRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | credentials | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | domain\_id | string |  | required |

### TokenInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | access\_token | string |  |  |
| 2 | refresh\_token | string |  |  |

