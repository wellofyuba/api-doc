---
description: null
---

# Role

> **Package : spaceone.api.identity.v1**

## Role

{% hint style="info" %}
**Role Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](role%20%281%29.md#create) | [CreateRoleRequest](role%20%281%29.md#createrolerequest) | [RoleInfo](role%20%281%29.md#roleinfo) |  |
| 2 | [update](role%20%281%29.md#update) | [UpdateRoleRequest](role%20%281%29.md#updaterolerequest) | [RoleInfo](role%20%281%29.md#roleinfo) |  |
| 3 | [delete](role%20%281%29.md#delete) | [RoleRequest](role%20%281%29.md#rolerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](role%20%281%29.md#get) | [GetRoleRequest](role%20%281%29.md#getrolerequest) | [RoleInfo](role%20%281%29.md#roleinfo) |  |
| 5 | [list](role%20%281%29.md#list) | [RoleQuery](role%20%281%29.md#rolequery) | [RolesInfo](role%20%281%29.md#rolesinfo) |  |
| 6 | [stat](role%20%281%29.md#stat) | [RoleStatQuery](role%20%281%29.md#rolestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/roles

| Type | Message |
| :--- | :--- |
| Request | [CreateRoleRequest](role%20%281%29.md#createrolerequest) |
| Response | [RoleInfo](role%20%281%29.md#roleinfo) |

### update

> **PUT** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateRoleRequest](role%20%281%29.md#updaterolerequest) |
| Response | [RoleInfo](role%20%281%29.md#roleinfo) |

### delete

> **DELETE** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [RoleRequest](role%20%281%29.md#rolerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetRoleRequest](role%20%281%29.md#getrolerequest) |
| Response | [RoleInfo](role%20%281%29.md#roleinfo) |

### list

> **GET** /identity/v1/roles
>
> **POST** /identity/v1/roles/search

| Type | Message |
| :--- | :--- |
| Request | [RoleQuery](role%20%281%29.md#rolequery) |
| Response | [RolesInfo](role%20%281%29.md#rolesinfo) |

### stat

> **POST** /identity/v1/roles/stat

| Type | Message |
| :--- | :--- |
| Request | [RoleStatQuery](role%20%281%29.md#rolestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateRoleRequest

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
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">role_type</td>
      <td style="text-align:left">
        <p>RoleType</p>
        <ul>
          <li>NONE</li>
          <li>SYSTEM</li>
          <li>DOMAIN</li>
          <li>PROJECT</li>
        </ul>
      </td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">policies</td>
      <td style="text-align:left"> <a href="role (1).md#rolepolicy">RolePolicy</a>
      </td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### GetRoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### RoleInfo

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
      <td style="text-align:left">role_id</td>
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
      <td style="text-align:left">role_type</td>
      <td style="text-align:left">
        <p>RoleType</p>
        <ul>
          <li>NONE</li>
          <li>SYSTEM</li>
          <li>DOMAIN</li>
          <li>PROJECT</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">policies</td>
      <td style="text-align:left"> <a href="role (1).md#rolepolicy">RolePolicy</a>
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
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
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

### RolePolicy

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
      <td style="text-align:left">policy_type</td>
      <td style="text-align:left">
        <p>RolePolicy.PolicyType</p>
        <ul>
          <li>NONE</li>
          <li>MANAGED</li>
          <li>CUSTOM</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">url</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">policy_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### RoleQuery

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
      <td style="text-align:left">role_id</td>
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
      <td style="text-align:left">role_type</td>
      <td style="text-align:left">
        <p>RoleType</p>
        <ul>
          <li>NONE</li>
          <li>SYSTEM</li>
          <li>DOMAIN</li>
          <li>PROJECT</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### RoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### RoleStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### RolesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RoleInfo](role%20%281%29.md#roleinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateRoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string | ✅ |  |
| 2 | name | string | ❌ |  |
| 3 | domain\_id | string | ✅ |  |
| 4 | policies | [RolePolicy](role%20%281%29.md#rolepolicy) | ✅ |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | ❌ |  |

