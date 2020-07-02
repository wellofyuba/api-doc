---
description: null
---

# Cloud Service

> **Package : spaceone.api.inventory.v1**

## CloudService

{% hint style="info" %}
**CloudService Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](cloud-service%20%281%29.md#create) | [CreateServiceRequest](cloud-service%20%281%29.md#createservicerequest) | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |  |
| 2 | [update](cloud-service%20%281%29.md#update) | [UpdateCloudServiceRequest](cloud-service%20%281%29.md#updatecloudservicerequest) | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |  |
| 3 | [pin\_data](cloud-service%20%281%29.md#pin_data) | [PinCloudServiceDataRequest](cloud-service%20%281%29.md#pincloudservicedatarequest) | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |  |
| 4 | [delete](cloud-service%20%281%29.md#delete) | [CloudServiceRequest](cloud-service%20%281%29.md#cloudservicerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](cloud-service%20%281%29.md#get) | [GetCloudServiceRequest](cloud-service%20%281%29.md#getcloudservicerequest) | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |  |
| 6 | [list](cloud-service%20%281%29.md#list) | [CloudServiceQuery](cloud-service%20%281%29.md#cloudservicequery) | [CloudServicesInfo](cloud-service%20%281%29.md#cloudservicesinfo) |  |
| 7 | [stat](cloud-service%20%281%29.md#stat) | [CloudServiceStatQuery](cloud-service%20%281%29.md#cloudservicestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/cloud-services

| Type | Message |
| :--- | :--- |
| Request | [CreateServiceRequest](cloud-service%20%281%29.md#createservicerequest) |
| Response | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |

### update

> **PUT** /inventory/v1/cloud-service/{cloud\_service\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateCloudServiceRequest](cloud-service%20%281%29.md#updatecloudservicerequest) |
| Response | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |

### pin\_data

> **PUT** /inventory/v1/cloud-service/{cloud\_service\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinCloudServiceDataRequest](cloud-service%20%281%29.md#pincloudservicedatarequest) |
| Response | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |

### delete

> **DELETE** /inventory/v1/cloud-service/{cloud\_service\_id}

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceRequest](cloud-service%20%281%29.md#cloudservicerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/cloud-service/{cloud\_service\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetCloudServiceRequest](cloud-service%20%281%29.md#getcloudservicerequest) |
| Response | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |

### list

> **GET** /inventory/v1/cloud-services
>
> **POST** /inventory/v1/cloud-services/search

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceQuery](cloud-service%20%281%29.md#cloudservicequery) |
| Response | [CloudServicesInfo](cloud-service%20%281%29.md#cloudservicesinfo) |

### stat

> **POST** /inventory/v1/cloud-services/stat

| Type | Message |
| :--- | :--- |
| Request | [CloudServiceStatQuery](cloud-service%20%281%29.md#cloudservicestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CloudServiceInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_id | string |  |  |
| 2 | cloud\_service\_type | string |  |  |
| 3 | provider | string |  |  |
| 4 | cloud\_service\_group | string |  |  |
| 5 | state | string |  |  |
| 6 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 8 | reference | [CloudServiceReference](cloud-service%20%281%29.md#cloudservicereference) |  |  |
| 9 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 10 | collection\_info | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 11 | region\_info | [RegionInfo](cloud-service%20%281%29.md#regioninfo) |  |  |
| 12 | project\_id | string |  |  |
| 13 | domain\_id | string |  |  |
| 14 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 15 | updated\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 16 | deleted\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### CloudServiceQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) | ❌ |  |
| 2 | cloud\_service\_id | string | ❌ |  |
| 3 | cloud\_service\_type | string | ❌ |  |
| 4 | provider | string | ❌ |  |
| 5 | cloud\_service\_group | string | ❌ |  |
| 6 | region\_id | string | ❌ |  |
| 7 | project\_id | string | ❌ |  |
| 8 | domain\_id | string | ❌ |  |

### CloudServiceReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### CloudServiceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CloudServiceStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### CloudServicesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [CloudServiceInfo](cloud-service%20%281%29.md#cloudserviceinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### CreateServiceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_type | string | ✅ |  |
| 2 | provider | string | ✅ |  |
| 3 | cloud\_service\_group | string | ❌ |  |
| 4 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ✅ |  |
| 5 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | reference | [CloudServiceReference](cloud-service%20%281%29.md#cloudservicereference) | ❌ |  |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 8 | region\_id | string | ❌ |  |
| 9 | project\_id | string | ❌ |  |
| 10 | domain\_id | string | ✅ |  |

### GetCloudServiceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### PinCloudServiceDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### UpdateCloudServiceRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | cloud\_service\_id | string | ✅ |  |
| 2 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 3 | metadata | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | reference | [CloudServiceReference](cloud-service%20%281%29.md#cloudservicereference) | ❌ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 6 | region\_id | string | ❌ |  |
| 7 | project\_id | string | ❌ |  |
| 8 | domain\_id | string | ✅ |  |
| 9 | release\_project | bool | ❌ |  |
| 10 | release\_region | bool | ❌ |  |

