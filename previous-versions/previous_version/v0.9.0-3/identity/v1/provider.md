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
| 1 | [create](../../../v0.9.0-5/identity/v1/provider.md#create) | [CreateProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#createproviderrequest) | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/provider.md#update) | [UpdateProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#updateproviderrequest) | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/provider.md#delete) | [ProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#providerrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/identity/v1/provider.md#get) | [GetProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#getproviderrequest) | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |  |
| 5 | [list](../../../v0.9.0-5/identity/v1/provider.md#list) | [ProviderQuery](../../../v0.9.0-5/identity/v1/provider.md#providerquery) | [ProvidersInfo](../../../v0.9.0-5/identity/v1/provider.md#providersinfo) |  |
| 6 | [stat](../../../v0.9.0-5/identity/v1/provider.md#stat) | [ProviderStatQuery](../../../v0.9.0-5/identity/v1/provider.md#providerstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/providers

| Type | Message |
| :--- | :--- |
| Request | [CreateProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#createproviderrequest) |
| Response | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |

### update

> **PUT** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#updateproviderrequest) |
| Response | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |

### delete

> **DELETE** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#providerrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/provider/{provider\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetProviderRequest](../../../v0.9.0-5/identity/v1/provider.md#getproviderrequest) |
| Response | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |

### list

> **GET** /identity/v1/providers
>
> **POST** /identity/v1/providers/search

| Type | Message |
| :--- | :--- |
| Request | [ProviderQuery](../../../v0.9.0-5/identity/v1/provider.md#providerquery) |
| Response | [ProvidersInfo](../../../v0.9.0-5/identity/v1/provider.md#providersinfo) |

### stat

> **POST** /identity/v1/providers/stat

| Type | Message |
| :--- | :--- |
| Request | [ProviderStatQuery](../../../v0.9.0-5/identity/v1/provider.md#providerstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string |  | required |
| 2 | name | string |  | required |
| 3 | template | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | capability | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### GetProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string |  | required |
| 2 | only | string |  | optional |

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
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | provider | string |  | optional |
| 3 | name | string |  | optional |

### ProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string |  | required |

### ProviderStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |

### ProvidersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProviderInfo](../../../v0.9.0-5/identity/v1/provider.md#providerinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateProviderRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider | string |  | required |
| 2 | name | string |  | optional |
| 3 | template | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | capability | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

