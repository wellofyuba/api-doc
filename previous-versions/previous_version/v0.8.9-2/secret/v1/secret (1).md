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
| 1 | [create](secret%20%281%29.md#create) | [CreateSecretRequest](secret%20%281%29.md#createsecretrequest) | [SecretInfo](secret%20%281%29.md#secretinfo) |  |
| 2 | [update](secret%20%281%29.md#update) | [UpdateSecretRequest](secret%20%281%29.md#updatesecretrequest) | [SecretInfo](secret%20%281%29.md#secretinfo) |  |
| 3 | [delete](secret%20%281%29.md#delete) | [SecretRequest](secret%20%281%29.md#secretrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get\_data](secret%20%281%29.md#get_data) | [SecretRequest](secret%20%281%29.md#secretrequest) | [SecretDataInfo](secret%20%281%29.md#secretdatainfo) |  |
| 5 | [get](secret%20%281%29.md#get) | [GetSecretRequest](secret%20%281%29.md#getsecretrequest) | [SecretInfo](secret%20%281%29.md#secretinfo) |  |
| 6 | [list](secret%20%281%29.md#list) | [SecretQuery](secret%20%281%29.md#secretquery) | [SecretsInfo](secret%20%281%29.md#secretsinfo) |  |
| 7 | [stat](secret%20%281%29.md#stat) | [SecretStatQuery](secret%20%281%29.md#secretstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /secret/v1/secrets

| Type | Message |
| :--- | :--- |
| Request | [CreateSecretRequest](secret%20%281%29.md#createsecretrequest) |
| Response | [SecretInfo](secret%20%281%29.md#secretinfo) |

### update

> **PUT** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateSecretRequest](secret%20%281%29.md#updatesecretrequest) |
| Response | [SecretInfo](secret%20%281%29.md#secretinfo) |

### delete

> **DELETE** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [SecretRequest](secret%20%281%29.md#secretrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get\_data

> **GET** /secret/v1/secret/{secret\_id}/get-data

| Type | Message |
| :--- | :--- |
| Request | [SecretRequest](secret%20%281%29.md#secretrequest) |
| Response | [SecretDataInfo](secret%20%281%29.md#secretdatainfo) |

### get

> **GET** /secret/v1/secret/{secret\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetSecretRequest](secret%20%281%29.md#getsecretrequest) |
| Response | [SecretInfo](secret%20%281%29.md#secretinfo) |

### list

> **GET** /secret/v1/secrets
>
> **POST** /secret/v1/secrets/search

| Type | Message |
| :--- | :--- |
| Request | [SecretQuery](secret%20%281%29.md#secretquery) |
| Response | [SecretsInfo](secret%20%281%29.md#secretsinfo) |

### stat

> **POST** /secret/v1/secrets/stat

| Type | Message |
| :--- | :--- |
| Request | [SecretStatQuery](secret%20%281%29.md#secretstatquery) |
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
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">data</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x2705;</td>
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
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">schema</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">service_account_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### GetSecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

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
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"> <a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">secret_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
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
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">secret_group_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">schema</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">service_account_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">include_secret_group</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### SecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SecretStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### SecretsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [SecretInfo](secret%20%281%29.md#secretinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateSecretRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | secret\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |
| 4 | project\_id | string | ✅ |  |
| 5 | domain\_id | string | ✅ |  |
| 6 | release\_project | bool | ❌ |  |

