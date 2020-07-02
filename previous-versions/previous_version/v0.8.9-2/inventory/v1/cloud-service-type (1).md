---
description: null
---

# Cloud Service Type

> **Package : spaceone.api.inventory.v1**

## CloudServiceType

{% hint style="info" %}
**CloudServiceType Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](cloud-service-type%20%281%29.md#create) | [CreateServiceTypeRequest](cloud-service-type%20%281%29.md#createservicetyperequest) | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |  |
| 2 | [update](cloud-service-type%20%281%29.md#update) | [UpdateCloudServiceTypeRequest](cloud-service-type%20%281%29.md#updatecloudservicetyperequest) | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |  |
| 3 | [pin\_data](cloud-service-type%20%281%29.md#pin_data) | [PinCloudServiceTypeDataRequest](cloud-service-type%20%281%29.md#pincloudservicetypedatarequest) | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |  |
| 4 | [delete](cloud-service-type%20%281%29.md#delete) | [CloudServiceTypeRequest](cloud-service-type%20%281%29.md#cloudservicetyperequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](cloud-service-type%20%281%29.md#get) | [GetCloudServiceTypeRequest](cloud-service-type%20%281%29.md#getcloudservicetyperequest) | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |  |
| 6 | [list](cloud-service-type%20%281%29.md#list) | [CloudServiceTypeQuery](cloud-service-type%20%281%29.md#cloudservicetypequery) | [CloudServiceTypesInfo](cloud-service-type%20%281%29.md#cloudservicetypesinfo) |  |
| 7 | [stat](cloud-service-type%20%281%29.md#stat) | [CloudServiceTypeStatQuery](cloud-service-type%20%281%29.md#cloudservicetypestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/cloud-service-types

| Type | Message |
| :--- | :--- |
| Request | [CreateServiceTypeRequest](cloud-service-type%20%281%29.md#createservicetyperequest) |
| Response | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |

### update

> **PUT** /inventory/v1/cloud-service-type/{cloud\_service\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateCloudServiceTypeRequest](cloud-service-type%20%281%29.md#updatecloudservicetyperequest) |
| Response | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |

### pin\_data

> **PUT** /inventory/v1/cloud-service-type/{cloud\_service\_type\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinCloudServiceTypeDataRequest](cloud-service-type%20%281%29.md#pincloudservicetypedatarequest) |
| Response | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |

### delete

> **DELETE** /inventory/v1/cloud-service-type/{cloud\_service\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceTypeRequest](cloud-service-type%20%281%29.md#cloudservicetyperequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/cloud-service-type/{cloud\_service\_type\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetCloudServiceTypeRequest](cloud-service-type%20%281%29.md#getcloudservicetyperequest) |
| Response | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |

### list

> **GET** /inventory/v1/cloud-service-types
>
> **POST** /inventory/v1/cloud-service-types/search

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceTypeQuery](cloud-service-type%20%281%29.md#cloudservicetypequery) |
| Response | [CloudServiceTypesInfo](cloud-service-type%20%281%29.md#cloudservicetypesinfo) |

### stat

> **POST** /inventory/v1/cloud-service-types/stat

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceTypeStatQuery](cloud-service-type%20%281%29.md#cloudservicetypestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CloudServiceTypeInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | provider | string |  |  |
| 4 | group | string |  |  |
| 5 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | labels | string |  |  |
| 8 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 9 | cloud\_service\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |
| 10 | domain\_id | string |  |  |
| 11 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 12 | updated\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### CloudServiceTypeQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | cloud\_service\_type\_id | string | ❌ |  |
| 3 | name | string | ❌ |  |
| 4 | provider | string | ❌ |  |
| 5 | group | string | ❌ |  |
| 6 | include\_cloud\_service\_count | bool | ❌ |  |
| 7 | domain\_id | string | ❌ |  |

### CloudServiceTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CloudServiceTypeStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CloudServiceTypesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [CloudServiceTypeInfo](cloud-service-type%20%281%29.md#cloudservicetypeinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### CreateServiceTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string | ❌ |  |
| 2 | provider | string | ❌ |  |
| 3 | group | string | ❌ |  |
| 4 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | labels | [google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview) | ❌ |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 7 | domain\_id | string | ✅ |  |

### GetCloudServiceTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### PinCloudServiceTypeDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdateCloudServiceTypeRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type\_id | string | ✅ |  |
| 2 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 3 | labels | [google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview) | ❌ |  |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 5 | domain\_id | string | ✅ |  |

