---
description: null
---

# Repository

> **Package : spaceone.api.repository.v1**

## Repository

{% hint style="info" %}
**Repository Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [register](../../../v0.9.0-5/repository/v1/repository.md#register) | [CreateRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#createrepositoryrequest) | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |  |
| 2 | [update](../../../v0.9.0-5/repository/v1/repository.md#update) | [UpdateRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#updaterepositoryrequest) | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |  |
| 3 | [deregister](../../../v0.9.0-5/repository/v1/repository.md#deregister) | [RepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#repositoryrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/repository/v1/repository.md#get) | [GetRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#getrepositoryrequest) | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |  |
| 5 | [list](../../../v0.9.0-5/repository/v1/repository.md#list) | [RepositoryQuery](../../../v0.9.0-5/repository/v1/repository.md#repositoryquery) | [RepositoriesInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoriesinfo) |  |
| 6 | [stat](../../../v0.9.0-5/repository/v1/repository.md#stat) | [RepositoryStatQuery](../../../v0.9.0-5/repository/v1/repository.md#repositorystatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### register

> **POST** /repository/v1/repositories

| Type | Message |
| :--- | :--- |
| Request | [CreateRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#createrepositoryrequest) |
| Response | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |

### update

> **PUT** /repository/v1/repository/{repository\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#updaterepositoryrequest) |
| Response | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |

### deregister

> **DELETE** /repository/v1/repository/{repository\_id}

| Type | Message |
| :--- | :--- |
| Request | [RepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#repositoryrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /repository/v1/repositories/{repository\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetRepositoryRequest](../../../v0.9.0-5/repository/v1/repository.md#getrepositoryrequest) |
| Response | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |

### list

> **GET** /repository/v1/repositories
>
> **POST** /repository/v1/repositories/search

| Type | Message |
| :--- | :--- |
| Request | [RepositoryQuery](../../../v0.9.0-5/repository/v1/repository.md#repositoryquery) |
| Response | [RepositoriesInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoriesinfo) |

### stat

> **POST** /repository/v1/repositories/stat

| Type | Message |
| :--- | :--- |
| Request | [RepositoryStatQuery](../../../v0.9.0-5/repository/v1/repository.md#repositorystatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateRepositoryRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | repository\_type | string |  | required |
| 3 | endpoint | string |  | optional |
| 4 | version | string |  | optional |
| 5 | secret\_id | string |  | optional |

### GetRepositoryRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository\_id | string |  | required |
| 2 | only | string |  | optional |

### RepositoriesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RepositoryInfo](../../../v0.9.0-5/repository/v1/repository.md#repositoryinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RepositoryInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | repository\_type | string |  |  |
| 4 | endpoint | string |  |  |
| 5 | version | string |  |  |
| 6 | secret\_id | string |  |  |
| 7 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### RepositoryQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | repository\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | repository\_type | string |  | optional |

### RepositoryRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository\_id | string |  | required |

### RepositoryStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### UpdateRepositoryRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository\_id | string |  | required |
| 2 | name | string |  | required |

