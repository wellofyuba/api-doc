---
description: null
---

# Provider

> **Package : spaceone.api.identity.v1**

## Provider

{% hint style="info" %}
**Provider Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](provider%20%281%29.md#create) | [CreateProviderRequest](provider%20%281%29.md#createproviderrequest) | [ProviderInfo](provider%20%281%29.md#providerinfo) |  |
| 2 | [update](provider%20%281%29.md#update) | [UpdateProviderRequest](provider%20%281%29.md#updateproviderrequest) | [ProviderInfo](provider%20%281%29.md#providerinfo) |  |
| 3 | [delete](provider%20%281%29.md#delete) | [ProviderRequest](provider%20%281%29.md#providerrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](provider%20%281%29.md#get) | [GetProviderRequest](provider%20%281%29.md#getproviderrequest) | [ProviderInfo](provider%20%281%29.md#providerinfo) |  |
| 5 | [list](provider%20%281%29.md#list) | [ProviderQuery](provider%20%281%29.md#providerquery) | [ProvidersInfo](provider%20%281%29.md#providersinfo) |  |
| 6 | [stat](provider%20%281%29.md#stat) | [ProviderStatQuery](provider%20%281%29.md#providerstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/providers

| Type | Message |
| :--- | :--- |
| Request | [CreateProviderRequest](provider%20%281%29.md#createproviderrequest) |
| Response | [ProviderInfo](provider%20%281%29.md#providerinfo) |

### update

> **PUT** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateProviderRequest](provider%20%281%29.md#updateproviderrequest) |
| Response | [ProviderInfo](provider%20%281%29.md#providerinfo) |

### delete

> **DELETE** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProviderRequest](provider%20%281%29.md#providerrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetProviderRequest](provider%20%281%29.md#getproviderrequest) |
| Response | [ProviderInfo](provider%20%281%29.md#providerinfo) |

### list

> **GET** /identity/v1/providers
>
> **POST** /identity/v1/providers/search

| Type | Message |
| :--- | :--- |
| Request | [ProviderQuery](provider%20%281%29.md#providerquery) |
| Response | [ProvidersInfo](provider%20%281%29.md#providersinfo) |

### stat

> **POST** /identity/v1/providers/stat

| Type | Message |
| :--- | :--- |
| Request | [ProviderStatQuery](provider%20%281%29.md#providerstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string | ✅ |  |
| 2 | name | string | ✅ |  |
| 3 | template | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | capability | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | domain\_id | string | ❌ |  |

### GetProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string | ✅ |  |
| 2 | only | string | ❌ |  |
| 3 | domain\_id | string | ❌ |  |

### ProviderInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string |  |  |
| 2 | name | string |  |  |
| 3 | template | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 5 | capability | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ProviderQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | provider | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | domain\_id | string | ❌ |  |

### ProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string | ✅ |  |
| 2 | domain\_id | string | ❌ |  |

### ProviderStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |

### ProvidersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProviderInfo](provider%20%281%29.md#providerinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | template | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | capability | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | domain\_id | string | ❌ |  |

