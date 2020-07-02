---
description: null
---

# Secret Group

> **Package : spaceone.api.secret.v1**

## SecretGroup

{% hint style="info" %}
**SecretGroup Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/secret/v1/secret-group.md#create) | [CreateSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#createsecretgrouprequest) | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |  |
| 2 | [update](../../../v0.9.0-5/secret/v1/secret-group.md#update) | [UpdateSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#updatesecretgrouprequest) | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |  |
| 3 | [add\_secret](../../../v0.9.0-5/secret/v1/secret-group.md#add_secret) | [SecretGroupSecretRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretrequest) | [SecretGroupSecretInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretinfo) |  |
| 4 | [remove\_secret](../../../v0.9.0-5/secret/v1/secret-group.md#remove_secret) | [SecretGroupSecretRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [delete](../../../v0.9.0-5/secret/v1/secret-group.md#delete) | [SecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgrouprequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 6 | [get](../../../v0.9.0-5/secret/v1/secret-group.md#get) | [GetSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#getsecretgrouprequest) | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |  |
| 7 | [list](../../../v0.9.0-5/secret/v1/secret-group.md#list) | [SecretGroupQuery](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupquery) | [SecretGroupsInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsinfo) |  |
| 8 | [stat](../../../v0.9.0-5/secret/v1/secret-group.md#stat) | [SecretGroupStatQuery](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /secret/v1/secret-groups

| Type | Message |
| :--- | :--- |
| Request | [CreateSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#createsecretgrouprequest) |
| Response | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |

### update

> **PUT** /secret/v1/secret-group/{secret\_group\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#updatesecretgrouprequest) |
| Response | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |

### add\_secret

> **POST** /secret/v1/secret-group/{secret\_group\_id}/secrets

| Type | Message |
| :--- | :--- |
| Request | [SecretGroupSecretRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretrequest) |
| Response | [SecretGroupSecretInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretinfo) |

### remove\_secret

> **DELETE** /secret/v1/secret-group/{secret\_group\_id}/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [SecretGroupSecretRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsecretrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### delete

> **DELETE** /secret/v1/secret-group/{secret\_group\_id}

| Type | Message |
| :--- | :--- |
| Request | [SecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#secretgrouprequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /secret/v1/secret-group/{secret\_group\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSecretGroupRequest](../../../v0.9.0-5/secret/v1/secret-group.md#getsecretgrouprequest) |
| Response | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |

### list

> **GET** /secret/v1/secret-groups
>
> **POST** /secret/v1/secret-groups/search

| Type | Message |
| :--- | :--- |
| Request | [SecretGroupQuery](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupquery) |
| Response | [SecretGroupsInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupsinfo) |

### stat

> **POST** /secret/v1/secret-groups/stat

| Type | Message |
| :--- | :--- |
| Request | [SecretGroupStatQuery](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSecretGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 3 | domain\_id | string |  | required |

### GetSecretGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### SecretGroupInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 4 | domain\_id | string |  |  |
| 5 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### SecretGroupQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | secret\_group\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | secret\_id | string |  | optional |
| 5 | domain\_id | string |  | required |

### SecretGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### SecretGroupSecretInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_info | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |  |  |
| 2 | secret\_info | [SecretInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretinfo) |  |  |
| 3 | domain\_id | string |  |  |

### SecretGroupSecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_id | string |  | required |
| 2 | secret\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### SecretGroupStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### SecretGroupsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SecretGroupInfo](../../../v0.9.0-5/secret/v1/secret-group.md#secretgroupinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSecretGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_group\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | domain\_id | string |  | required |

