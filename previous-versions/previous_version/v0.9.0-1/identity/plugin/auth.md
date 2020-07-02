---
description: null
---

# Auth

> **Package : spaceone.api.identity.plugin**

## Auth

{% hint style="info" %}
**Auth Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [verify](../../../v0.9.0-5/identity/plugin/auth.md#verify) | [VerifyRequest](../../../v0.9.0-5/identity/plugin/auth.md#verifyrequest) | [AuthVerifyInfo](../../../v0.9.0-5/identity/plugin/auth.md#authverifyinfo) |  |
| 2 | [find](../../../v0.9.0-5/identity/plugin/auth.md#find) | [FindRequest](../../../v0.9.0-5/identity/plugin/auth.md#findrequest) | [UsersInfo](../../../v0.9.0-5/identity/plugin/auth.md#usersinfo) |  |
| 3 | [login](../../../v0.9.0-5/identity/plugin/auth.md#login) | [LoginRequest](../../../v0.9.0-5/identity/plugin/auth.md#loginrequest) | [UserInfo](../../../v0.9.0-5/identity/plugin/auth.md#userinfo) |  |

### verify

| Type | Message |
| :--- | :--- |
| Request | [VerifyRequest](../../../v0.9.0-5/identity/plugin/auth.md#verifyrequest) |
| Response | [AuthVerifyInfo](../../../v0.9.0-5/identity/plugin/auth.md#authverifyinfo) |

### find

| Type | Message |
| :--- | :--- |
| Request | [FindRequest](../../../v0.9.0-5/identity/plugin/auth.md#findrequest) |
| Response | [UsersInfo](../../../v0.9.0-5/identity/plugin/auth.md#usersinfo) |

### login

| Type | Message |
| :--- | :--- |
| Request | [LoginRequest](../../../v0.9.0-5/identity/plugin/auth.md#loginrequest) |
| Response | [UserInfo](../../../v0.9.0-5/identity/plugin/auth.md#userinfo) |

## Message

### AuthVerifyInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |

### FindRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 3 | user\_id | string |  | optional |
| 4 | keyword | string |  | optional |

### LoginRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 3 | user\_credentials | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |

### UserInfo

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
      <td style="text-align:left">user_id</td>
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
      <td style="text-align:left">email</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">mobile</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">group</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>UserInfo.State</p>
        <ul>
          <li>NONE</li>
          <li>ENABLED</li>
          <li>DISABLED</li>
          <li>UNIDENTIFIED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### UsersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [UserInfo](../../../v0.9.0-5/identity/plugin/auth.md#userinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### VerifyRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | options | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |
| 2 | secret\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | required |

