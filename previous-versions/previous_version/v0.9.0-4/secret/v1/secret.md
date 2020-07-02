---
description: null
---

# Secret

> **Package : spaceone.api.secret.v1**

## Secret

{% hint style="info" %}
**Secret Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/secret/v1/secret.md#create) | [CreateSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#createsecretrequest) | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |  |
| 2 | [update](../../../v0.9.0-5/secret/v1/secret.md#update) | [UpdateSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#updatesecretrequest) | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |  |
| 3 | [delete](../../../v0.9.0-5/secret/v1/secret.md#delete) | [SecretRequest](../../../v0.9.0-5/secret/v1/secret.md#secretrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get\_data](../../../v0.9.0-5/secret/v1/secret.md#get_data) | [SecretRequest](../../../v0.9.0-5/secret/v1/secret.md#secretrequest) | [SecretDataInfo](../../../v0.9.0-5/secret/v1/secret.md#secretdatainfo) |  |
| 5 | [get](../../../v0.9.0-5/secret/v1/secret.md#get) | [GetSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#getsecretrequest) | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |  |
| 6 | [list](../../../v0.9.0-5/secret/v1/secret.md#list) | [SecretQuery](../../../v0.9.0-5/secret/v1/secret.md#secretquery) | [SecretsInfo](../../../v0.9.0-5/secret/v1/secret.md#secretsinfo) |  |
| 7 | [stat](../../../v0.9.0-5/secret/v1/secret.md#stat) | [SecretStatQuery](../../../v0.9.0-5/secret/v1/secret.md#secretstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /secret/v1/secrets

| Type | Message |
| :--- | :--- |
| Request | [CreateSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#createsecretrequest) |
| Response | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |

### update

> **PUT** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#updatesecretrequest) |
| Response | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |

### delete

> **DELETE** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [SecretRequest](../../../v0.9.0-5/secret/v1/secret.md#secretrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get\_data

> **GET** /secret/v1/secret/{secret\_id}/get-data

| Type | Message |
| :--- | :--- |
| Request | [SecretRequest](../../../v0.9.0-5/secret/v1/secret.md#secretrequest) |
| Response | [SecretDataInfo](../../../v0.9.0-5/secret/v1/secret.md#secretdatainfo) |

### get

> **GET** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSecretRequest](../../../v0.9.0-5/secret/v1/secret.md#getsecretrequest) |
| Response | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |

### list

> **GET** /secret/v1/secrets
>
> **POST** /secret/v1/secrets/search

| Type | Message |
| :--- | :--- |
| Request | [SecretQuery](../../../v0.9.0-5/secret/v1/secret.md#secretquery) |
| Response | [SecretsInfo](../../../v0.9.0-5/secret/v1/secret.md#secretsinfo) |

### stat

> **POST** /secret/v1/secrets/stat

| Type | Message |
| :--- | :--- |
| Request | [SecretStatQuery](../../../v0.9.0-5/secret/v1/secret.md#secretstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateSecretRequest

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
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">data</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">secret_type</td>
      <td style="text-align:left">
        <p>SecretType</p>
        <ul>
          <li>NONE</li>
          <li>CREDENTIALS</li>
        </ul>
      </td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">schema</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">service_account_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### GetSecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### SecretDataInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### SecretInfo

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
      <td style="text-align:left">secret_id</td>
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
      <td style="text-align:left">secret_type</td>
      <td style="text-align:left">
        <p>SecretType</p>
        <ul>
          <li>NONE</li>
          <li>CREDENTIALS</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">secret_groups</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">schema</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">service_account_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### SecretQuery

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
      <td style="text-align:left">secret_id</td>
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
      <td style="text-align:left">secret_type</td>
      <td style="text-align:left">
        <p>SecretType</p>
        <ul>
          <li>NONE</li>
          <li>CREDENTIALS</li>
        </ul>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">secret_group_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">schema</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">service_account_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">include_secret_group</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### SecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### SecretStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### SecretsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SecretInfo](../../../v0.9.0-5/secret/v1/secret.md#secretinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 4 | project\_id | string |  | required |
| 5 | domain\_id | string |  | required |
| 6 | release\_project | bool |  | optional |

