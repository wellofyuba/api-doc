---
description: null
---

# Domain

> **Package : spaceone.api.identity.v1**

## Domain

{% hint style="info" %}
**Domain Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/identity/v1/domain.md#create) | [CreateDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#createdomainrequest) | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/domain.md#update) | [UpdateDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#updatedomainrequest) | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/domain.md#delete) | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [enable](../../../v0.9.0-5/identity/v1/domain.md#enable) | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |
| 5 | [disable](../../../v0.9.0-5/identity/v1/domain.md#disable) | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |
| 6 | [get](../../../v0.9.0-5/identity/v1/domain.md#get) | [GetDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#getdomainrequest) | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |
| 7 | [list](../../../v0.9.0-5/identity/v1/domain.md#list) | [DomainQuery](../../../v0.9.0-5/identity/v1/domain.md#domainquery) | [DomainsInfo](../../../v0.9.0-5/identity/v1/domain.md#domainsinfo) |  |
| 8 | [stat](../../../v0.9.0-5/identity/v1/domain.md#stat) | [DomainStatQuery](../../../v0.9.0-5/identity/v1/domain.md#domainstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 9 | [get\_public\_key](../../../v0.9.0-5/identity/v1/domain.md#get_public_key) | \[AuthenticationRequest\] | .spaceone.api.core.v1.AuthenticationResponse |  |
| 10 | [get\_domain\_key](../../../v0.9.0-5/identity/v1/domain.md#get_domain_key) | \[AuthenticationRequest\] | [DomainKeyResponse](../../../v0.9.0-5/identity/v1/domain.md#domainkeyresponse) |  |

### create

> **POST** /identity/v1/domains

| Type | Message |
| :--- | :--- |
| Request | [CreateDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#createdomainrequest) |
| Response | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |

### update

> **PUT** /identity/v1/domain/{domain\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#updatedomainrequest) |
| Response | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |

### delete

> **DELETE** /identity/v1/domain/{domain\_id}

| Type | Message |
| :--- | :--- |
| Request | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### enable

> **PUT** /identity/v1/domain/{domain\_id}

| Type | Message |
| :--- | :--- |
| Request | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) |
| Response | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |

### disable

> **PUT** /identity/v1/domain/{domain\_id}

| Type | Message |
| :--- | :--- |
| Request | [DomainRequest](../../../v0.9.0-5/identity/v1/domain.md#domainrequest) |
| Response | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |

### get

> **GET** /identity/v1/domain/{domain\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetDomainRequest](../../../v0.9.0-5/identity/v1/domain.md#getdomainrequest) |
| Response | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |

### list

> **GET** /identity/v1/domains
>
> **POST** /identity/v1/domains/search

| Type | Message |
| :--- | :--- |
| Request | [DomainQuery](../../../v0.9.0-5/identity/v1/domain.md#domainquery) |
| Response | [DomainsInfo](../../../v0.9.0-5/identity/v1/domain.md#domainsinfo) |

### stat

> **POST** /identity/v1/domains/stat

| Type | Message |
| :--- | :--- |
| Request | [DomainStatQuery](../../../v0.9.0-5/identity/v1/domain.md#domainstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### get\_public\_key

| Type | Message |
| :--- | :--- |
| Request | \[AuthenticationRequest\] |
| Response | .spaceone.api.core.v1.AuthenticationResponse |

### get\_domain\_key

| Type | Message |
| :--- | :--- |
| Request | \[AuthenticationRequest\] |
| Response | [DomainKeyResponse](../../../v0.9.0-5/identity/v1/domain.md#domainkeyresponse) |

## Message

### CreateDomainRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | plugin\_info | [PluginInfo](../../../v0.9.0-5/identity/v1/domain.md#plugininfo) |  | optional |
| 3 | config | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### DomainInfo

<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>DomainInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">plugin_info</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/identity/v1/domain.md#plugininfo">PluginInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">config</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">deleted_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### DomainKeyResponse

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  |  |
| 2 | domain\_key | string |  |  |

### DomainQuery

<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>DomainQuery.State</p>
        <ul>
          <li>NONE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
        </ul>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
  </tbody>
</table>

### DomainRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  | required |

### DomainStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |

### DomainsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [DomainInfo](../../../v0.9.0-5/identity/v1/domain.md#domaininfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### GetDomainRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  | required |
| 2 | only | string |  | optional |

### PluginInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin\_id | string |  |  |
| 2 | version | string |  |  |
| 3 | secret\_id | string |  |  |
| 4 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### UpdateDomainRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | domain\_id | string |  | required |
| 2 | plugin\_info | [PluginInfo](../../../v0.9.0-5/identity/v1/domain.md#plugininfo) |  | optional |
| 3 | config | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

