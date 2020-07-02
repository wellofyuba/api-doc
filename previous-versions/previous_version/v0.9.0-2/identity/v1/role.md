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
| 1 | [create](../../../v0.9.0-5/identity/v1/role.md#create) | [CreateRoleRequest](../../../v0.9.0-5/identity/v1/role.md#createrolerequest) | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/role.md#update) | [UpdateRoleRequest](../../../v0.9.0-5/identity/v1/role.md#updaterolerequest) | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/role.md#delete) | [RoleRequest](../../../v0.9.0-5/identity/v1/role.md#rolerequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [get](../../../v0.9.0-5/identity/v1/role.md#get) | [GetRoleRequest](../../../v0.9.0-5/identity/v1/role.md#getrolerequest) | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |  |
| 5 | [list](../../../v0.9.0-5/identity/v1/role.md#list) | [RoleQuery](../../../v0.9.0-5/identity/v1/role.md#rolequery) | [RolesInfo](../../../v0.9.0-5/identity/v1/role.md#rolesinfo) |  |
| 6 | [stat](../../../v0.9.0-5/identity/v1/role.md#stat) | [RoleStatQuery](../../../v0.9.0-5/identity/v1/role.md#rolestatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /identity/v1/roles

| Type | Message |
| :--- | :--- |
| Request | [CreateRoleRequest](../../../v0.9.0-5/identity/v1/role.md#createrolerequest) |
| Response | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |

### update

> **PUT** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateRoleRequest](../../../v0.9.0-5/identity/v1/role.md#updaterolerequest) |
| Response | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |

### delete

> **DELETE** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [RoleRequest](../../../v0.9.0-5/identity/v1/role.md#rolerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/roles/{role\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetRoleRequest](../../../v0.9.0-5/identity/v1/role.md#getrolerequest) |
| Response | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |

### list

> **GET** /identity/v1/roles
>
> **POST** /identity/v1/roles/search

| Type | Message |
| :--- | :--- |
| Request | [RoleQuery](../../../v0.9.0-5/identity/v1/role.md#rolequery) |
| Response | [RolesInfo](../../../v0.9.0-5/identity/v1/role.md#rolesinfo) |

### stat

> **POST** /identity/v1/roles/stat

| Type | Message |
| :--- | :--- |
| Request | [RoleStatQuery](../../../v0.9.0-5/identity/v1/role.md#rolestatquery) |
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
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
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
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">policies</td>
      <td style="text-align:left"> <a href="../../../v0.9.0-5/identity/v1/role.md#rolepolicy">RolePolicy</a>
      </td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
  </tbody>
</table>

### GetRoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

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
      <td style="text-align:left"> <a href="../../../v0.9.0-5/identity/v1/role.md#rolepolicy">RolePolicy</a>
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
      <td style="text-align:left">role_id</td>
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
      <td style="text-align:left">optional</td>
      <td style="text-align:left">optional</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">required</td>
      <td style="text-align:left">required</td>
    </tr>
  </tbody>
</table>

### RoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### RoleStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### RolesInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [RoleInfo](../../../v0.9.0-5/identity/v1/role.md#roleinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateRoleRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | role\_id | string |  | required |
| 2 | name | string |  | optional |
| 3 | domain\_id | string |  | required |
| 4 | policies | [RolePolicy](../../../v0.9.0-5/identity/v1/role.md#rolepolicy) |  | required |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

