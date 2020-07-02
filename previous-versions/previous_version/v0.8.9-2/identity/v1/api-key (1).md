---
description: null
---

# Api Key

> **Package : spaceone.api.identity.v1**

## APIKey

{% hint style="info" %}
**APIKey Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](api-key%20%281%29.md#create) | [CreateAPIKeyRequest](api-key%20%281%29.md#createapikeyrequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 2 | [enable](api-key%20%281%29.md#enable) | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 3 | [disable](api-key%20%281%29.md#disable) | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 4 | [update\_role](api-key%20%281%29.md#update_role) | [UpdateAPIKeyRoleRequest](api-key%20%281%29.md#updateapikeyrolerequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 5 | [update\_allowed\_hosts](api-key%20%281%29.md#update_allowed_hosts) | [UpdateAPIKeyHostsRequest](api-key%20%281%29.md#updateapikeyhostsrequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 6 | [delete](api-key%20%281%29.md#delete) | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 7 | [get](api-key%20%281%29.md#get) | [GetAPIKeyRequest](api-key%20%281%29.md#getapikeyrequest) | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |
| 8 | [list](api-key%20%281%29.md#list) | [APIKeyQuery](api-key%20%281%29.md#apikeyquery) | [APIKeysInfo](api-key%20%281%29.md#apikeysinfo) |  |
| 9 | [stat](api-key%20%281%29.md#stat) | [APIKeyStatQuery](api-key%20%281%29.md#apikeystatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/api-keys

| Type | Message |
| :--- | :--- |
| Request | [CreateAPIKeyRequest](api-key%20%281%29.md#createapikeyrequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### enable

> **PUT** /identity/v1/api-key/{api\_key\_id}/enable

| Type | Message |
| :--- | :--- |
| Request | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### disable

> **PUT** /identity/v1/api-key/{api\_key\_id}/disable

| Type | Message |
| :--- | :--- |
| Request | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### update\_role

> **PUT** /identity/v1/api-key/{api\_key\_id}/roles

| Type | Message |
| :--- | :--- |
| Request | [UpdateAPIKeyRoleRequest](api-key%20%281%29.md#updateapikeyrolerequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### update\_allowed\_hosts

> **PUT** /identity/v1/api-key/{api\_key\_id}/allowed-hosts

| Type | Message |
| :--- | :--- |
| Request | [UpdateAPIKeyHostsRequest](api-key%20%281%29.md#updateapikeyhostsrequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### delete

> **DELETE** /identity/v1/api-key/{api\_key\_id}

| Type | Message |
| :--- | :--- |
| Request | [APIKeyRequest](api-key%20%281%29.md#apikeyrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/api-key/{api\_key\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetAPIKeyRequest](api-key%20%281%29.md#getapikeyrequest) |
| Response | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |

### list

> **GET** /identity/v1/api-keys
>
> **POST** /identity/v1/api-keys/search

| Type | Message |
| :--- | :--- |
| Request | [APIKeyQuery](api-key%20%281%29.md#apikeyquery) |
| Response | [APIKeysInfo](api-key%20%281%29.md#apikeysinfo) |

### stat

> **POST** /identity/v1/api-keys/stat

| Type | Message |
| :--- | :--- |
| Request | [APIKeyStatQuery](api-key%20%281%29.md#apikeystatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### APIKeyInfo

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
      <td style="text-align:left">api_key_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">api_key</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>APIKeyInfo.State</p>
        <ul>
          <li>NONE_STATE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">user_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">APIKeyType api_key_type = 4;</td>
      <td style="text-align:left">APIKeyType api_key_type = 4;</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">allowed_hosts</td>
      <td style="text-align:left"> <a href="api-key (1).md#acls">Acls</a>
      </td>
      <td style="text-align:left">repeated spaceone.api.identity.v1.RoleInfo roles = 7;</td>
      <td style="text-align:left">repeated spaceone.api.identity.v1.RoleInfo roles = 7;</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">last_accessed_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### APIKeyQuery

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
      <td style="text-align:left">api_key_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>APIKeyQuery.State</p>
        <ul>
          <li>NONE_STATE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">api_key_type</td>
      <td style="text-align:left">
        <p>APIKeyQuery.APIKeyType</p>
        <ul>
          <li>NONE_TYPE</li>
          <li>USER</li>
          <li>SYSTEM</li>
          <li>DELEGATION</li>
          <li>DOMAIN</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">user_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### APIKeyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | api\_key\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### APIKeyStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### APIKeysInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [APIKeyInfo](api-key%20%281%29.md#apikeyinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### Acls

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | optional |
| 2 | cidr | string |  | required |

### CreateAPIKeyRequest

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
      <td style="text-align:left">api_key_type</td>
      <td style="text-align:left">
        <p>CreateAPIKeyRequest.APIKeyType</p>
        <ul>
          <li>NONE</li>
          <li>USER</li>
          <li>SYSTEM</li>
          <li>DELEGATION</li>
          <li>DOMAIN</li>
        </ul>
      </td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">user_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### GetAPIKeyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | api\_key\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### UpdateAPIKeyHostsRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | api\_key\_id | string |  |  |
| 2 | allowed\_hosts | [Acls](api-key%20%281%29.md#acls) |  |  |
| 3 | domain\_id | string |  |  |

### UpdateAPIKeyRoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | api\_key\_id | string |  |  |
| 2 | roles | [google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview) |  |  |
| 3 | domain\_id | string |  |  |

