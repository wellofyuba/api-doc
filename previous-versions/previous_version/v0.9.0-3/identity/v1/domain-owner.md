---
description: null
---

# Domain Owner

> **Package : spaceone.api.identity.v1**

## DomainOwner

{% hint style="info" %}
**DomainOwner Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/identity/v1/domain-owner.md#create) | [CreateDomainOwner](../../../v0.9.0-5/identity/v1/domain-owner.md#createdomainowner) | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/domain-owner.md#update) | [UpdateDomainOwner](../../../v0.9.0-5/identity/v1/domain-owner.md#updatedomainowner) | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/domain-owner.md#delete) | [DomainOwnerRequest](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/identity/v1/domain-owner.md#get) | [GetDomainOwnerRequest](../../../v0.9.0-5/identity/v1/domain-owner.md#getdomainownerrequest) | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |  |

### create

> **POST** /identity/v1/domain/{domain\_id}/owner

| Type | Message |
| :--- | :--- |
| Request | [CreateDomainOwner](../../../v0.9.0-5/identity/v1/domain-owner.md#createdomainowner) |
| Response | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |

### update

> **PUT** /identity/v1/domain/{domain\_id}/owner

| Type | Message |
| :--- | :--- |
| Request | [UpdateDomainOwner](../../../v0.9.0-5/identity/v1/domain-owner.md#updatedomainowner) |
| Response | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |

### delete

> **DELETE** /identity/v1/domain/{domain\_id}/owner

| Type | Message |
| :--- | :--- |
| Request | [DomainOwnerRequest](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/domain/{domain\_id}/owner

| Type | Message |
| :--- | :--- |
| Request | [GetDomainOwnerRequest](../../../v0.9.0-5/identity/v1/domain-owner.md#getdomainownerrequest) |
| Response | [DomainOwnerInfo](../../../v0.9.0-5/identity/v1/domain-owner.md#domainownerinfo) |

## Message

### CreateDomainOwner

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | owner\_id | string |  | required |
| 2 | password | string |  | required |
| 3 | name | string |  | optional |
| 4 | email | string |  | optional |
| 5 | mobile | string |  | optional |
| 6 | language | string |  | optional |
| 7 | timezone | string |  | optional |
| 8 | domain\_id | string |  | required |

### DomainOwnerInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | owner\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | email | string |  |  |
| 4 | mobile | string |  |  |
| 5 | language | string |  |  |
| 6 | timezone | string |  |  |
| 7 | last\_accessed\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 8 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 9 | domain\_id | string |  |  |

### DomainOwnerRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  | required |
| 2 | owner\_id | string |  | required |

### GetDomainOwnerRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  | required |
| 2 | owner\_id | string |  | required |
| 3 | only | string |  | optional |

### UpdateDomainOwner

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | owner\_id | string |  | required |
| 2 | password | string |  | optional |
| 3 | name | string |  | optional |
| 4 | email | string |  | optional |
| 5 | mobile | string |  | optional |
| 6 | language | string |  | optional |
| 7 | timezone | string |  | optional |
| 8 | domain\_id | string |  | required |

