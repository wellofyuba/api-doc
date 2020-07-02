---
description: null
---

# Service Account

> **Package : spaceone.api.identity.v1**

## ServiceAccount

{% hint style="info" %}
**ServiceAccount Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](service-account%20%281%29.md#create) | [CreateServiceAccountRequest](service-account%20%281%29.md#createserviceaccountrequest) | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |  |
| 2 | [update](service-account%20%281%29.md#update) | [UpdateServiceAccountRequest](service-account%20%281%29.md#updateserviceaccountrequest) | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |  |
| 3 | [delete](service-account%20%281%29.md#delete) | [ServiceAccountRequest](service-account%20%281%29.md#serviceaccountrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](service-account%20%281%29.md#get) | [GetServiceAccountRequest](service-account%20%281%29.md#getserviceaccountrequest) | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |  |
| 5 | [list](service-account%20%281%29.md#list) | [ServiceAccountQuery](service-account%20%281%29.md#serviceaccountquery) | [ServiceAccountsInfo](service-account%20%281%29.md#serviceaccountsinfo) |  |
| 6 | [stat](service-account%20%281%29.md#stat) | [ServiceAccountStatQuery](service-account%20%281%29.md#serviceaccountstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/service-accounts

| Type | Message |
| :--- | :--- |
| Request | [CreateServiceAccountRequest](service-account%20%281%29.md#createserviceaccountrequest) |
| Response | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |

### update

> **PUT** /identity/v1/service-account/{service\_account\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateServiceAccountRequest](service-account%20%281%29.md#updateserviceaccountrequest) |
| Response | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |

### delete

> **DELETE** /identity/v1/service-account/{service\_account\_id}

| Type | Message |
| :--- | :--- |
| Request | [ServiceAccountRequest](service-account%20%281%29.md#serviceaccountrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/service-account/{service\_account\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetServiceAccountRequest](service-account%20%281%29.md#getserviceaccountrequest) |
| Response | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |

### list

> **GET** /identity/v1/service-accounts
>
> **POST** /identity/v1/service-accounts/search

| Type | Message |
| :--- | :--- |
| Request | [ServiceAccountQuery](service-account%20%281%29.md#serviceaccountquery) |
| Response | [ServiceAccountsInfo](service-account%20%281%29.md#serviceaccountsinfo) |

### stat

> **POST** /identity/v1/service-accounts/stat

| Type | Message |
| :--- | :--- |
| Request | [ServiceAccountStatQuery](service-account%20%281%29.md#serviceaccountstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateServiceAccountRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ✅ |  |
| 2 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |
| 3 | provider | string | ✅ |  |
| 4 | project\_id | string | ❌ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | domain\_id | string | ✅ |  |

### GetServiceAccountRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | service\_account\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### ServiceAccountInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | service\_account\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | provider | string |  |  |
| 5 | project\_info | [ProjectInfo](service-account%20%281%29.md#projectinfo) |  |  |
| 6 | domain\_id | string |  |  |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ServiceAccountQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | service\_account\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | provider | string | ❌ |  |
| 5 | project\_id | string | ❌ |  |
| 6 | domain\_id | string | ❌ |  |

### ServiceAccountRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | service\_account\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ServiceAccountStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ServiceAccountsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ServiceAccountInfo](service-account%20%281%29.md#serviceaccountinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateServiceAccountRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | service\_account\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | project\_id | string | ❌ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | domain\_id | string | ✅ |  |
| 7 | release\_project | bool | ❌ |  |

