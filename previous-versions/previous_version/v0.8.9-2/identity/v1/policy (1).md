---
description: null
---

# Policy

> **Package : spaceone.api.identity.v1**

## Policy

{% hint style="info" %}
**Policy Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](policy%20%281%29.md#create) | [CreatePolicyRequest](policy%20%281%29.md#createpolicyrequest) | [PolicyInfo](policy%20%281%29.md#policyinfo) |  |
| 2 | [update](policy%20%281%29.md#update) | [UpdatePolicyRequest](policy%20%281%29.md#updatepolicyrequest) | [PolicyInfo](policy%20%281%29.md#policyinfo) |  |
| 3 | [delete](policy%20%281%29.md#delete) | [PolicyRequest](policy%20%281%29.md#policyrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](policy%20%281%29.md#get) | [GetPolicyRequest](policy%20%281%29.md#getpolicyrequest) | [PolicyInfo](policy%20%281%29.md#policyinfo) |  |
| 5 | [list](policy%20%281%29.md#list) | [PolicyQuery](policy%20%281%29.md#policyquery) | [PoliciesInfo](policy%20%281%29.md#policiesinfo) |  |
| 6 | [stat](policy%20%281%29.md#stat) | [PolicyStatQuery](policy%20%281%29.md#policystatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/policies

| Type | Message |
| :--- | :--- |
| Request | [CreatePolicyRequest](policy%20%281%29.md#createpolicyrequest) |
| Response | [PolicyInfo](policy%20%281%29.md#policyinfo) |

### update

> **PUT** /identity/v1/policy/{policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdatePolicyRequest](policy%20%281%29.md#updatepolicyrequest) |
| Response | [PolicyInfo](policy%20%281%29.md#policyinfo) |

### delete

> **DELETE** /identity/v1/policy/{policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [PolicyRequest](policy%20%281%29.md#policyrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/policy/{policy\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetPolicyRequest](policy%20%281%29.md#getpolicyrequest) |
| Response | [PolicyInfo](policy%20%281%29.md#policyinfo) |

### list

> **GET** /identity/v1/policies
>
> **POST** /identity/v1/policies/search

| Type | Message |
| :--- | :--- |
| Request | [PolicyQuery](policy%20%281%29.md#policyquery) |
| Response | [PoliciesInfo](policy%20%281%29.md#policiesinfo) |

### stat

> **POST** /identity/v1/policies/stat

| Type | Message |
| :--- | :--- |
| Request | [PolicyStatQuery](policy%20%281%29.md#policystatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreatePolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | permissions | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

### GetPolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | policy\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### PoliciesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [PolicyInfo](policy%20%281%29.md#policyinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### PolicyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | policy\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | permissions | string |  |  |
| 4 | domain\_id | string |  |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### PolicyQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | policy\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |

### PolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | policy\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### PolicyStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### UpdatePolicyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | policy\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | permissions | string | ❌ |  |
| 4 | domain\_id | string | ✅ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

