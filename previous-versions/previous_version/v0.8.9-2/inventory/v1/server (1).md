---
description: null
---

# Server

> **Package : spaceone.api.inventory.v1**

## Server

{% hint style="info" %}
**Server Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](server%20%281%29.md#create) | [CreateServerRequest](server%20%281%29.md#createserverrequest) | [ServerInfo](server%20%281%29.md#serverinfo) |  |
| 2 | [update](server%20%281%29.md#update) | [UpdateServerRequest](server%20%281%29.md#updateserverrequest) | [ServerInfo](server%20%281%29.md#serverinfo) |  |
| 3 | [pin\_data](server%20%281%29.md#pin_data) | [PinServerDataRequest](server%20%281%29.md#pinserverdatarequest) | [ServerInfo](server%20%281%29.md#serverinfo) |  |
| 4 | [delete](server%20%281%29.md#delete) | [ServerRequest](server%20%281%29.md#serverrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 5 | [get](server%20%281%29.md#get) | [GetServerRequest](server%20%281%29.md#getserverrequest) | [ServerInfo](server%20%281%29.md#serverinfo) |  |
| 6 | [list](server%20%281%29.md#list) | [ServerQuery](server%20%281%29.md#serverquery) | [ServersInfo](server%20%281%29.md#serversinfo) |  |
| 7 | [stat](server%20%281%29.md#stat) | [ServerStatQuery](server%20%281%29.md#serverstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### create

> **POST** /inventory/v1/servers

| Type | Message |
| :--- | :--- |
| Request | [CreateServerRequest](server%20%281%29.md#createserverrequest) |
| Response | [ServerInfo](server%20%281%29.md#serverinfo) |

### update

> **PUT** /inventory/v1/server/{server\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateServerRequest](server%20%281%29.md#updateserverrequest) |
| Response | [ServerInfo](server%20%281%29.md#serverinfo) |

### pin\_data

> **PUT** /inventory/v1/server/{server\_id}/pin-data

| Type | Message |
| :--- | :--- |
| Request | [PinServerDataRequest](server%20%281%29.md#pinserverdatarequest) |
| Response | [ServerInfo](server%20%281%29.md#serverinfo) |

### delete

> **DELETE** /inventory/v1/server/{server\_id}

| Type | Message |
| :--- | :--- |
| Request | [ServerRequest](server%20%281%29.md#serverrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /inventory/v1/server/{server\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetServerRequest](server%20%281%29.md#getserverrequest) |
| Response | [ServerInfo](server%20%281%29.md#serverinfo) |

### list

> **GET** /inventory/v1/servers
>
> **POST** /inventory/v1/servers/search

| Type | Message |
| :--- | :--- |
| Request | [ServerQuery](server%20%281%29.md#serverquery) |
| Response | [ServersInfo](server%20%281%29.md#serversinfo) |

### stat

> **POST** /inventory/v1/servers/stat

| Type | Message |
| :--- | :--- |
| Request | [ServerStatQuery](server%20%281%29.md#serverstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### CreateServerRequest

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
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>ServerState</p>
        <ul>
          <li>STATE_NONE</li>
          <li>PENDING</li>
          <li>INSERVICE</li>
          <li>MAINTENANCE</li>
          <li>CLOSED</li>
          <li>DELETED</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">primary_ip_address</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">server_type</td>
      <td style="text-align:left">
        <p>ServerType</p>
        <ul>
          <li>SERVER_TYPE_NONE</li>
          <li>BAREMETAL</li>
          <li>VM</li>
          <li>HYPERVISOR</li>
          <li>UNKNOWN</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">os_type</td>
      <td style="text-align:left">
        <p>ServerOSType</p>
        <ul>
          <li>OS_TYPE_NONE</li>
          <li>LINUX</li>
          <li>WINDOWS</li>
        </ul>
      </td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">data</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">metadata</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">nics</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">disks</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">reference</td>
      <td style="text-align:left"> <a href="server (1).md#serverreference">ServerReference</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">asset_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">pool_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">zone_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">region_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">17</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">18</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### GetServerRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | server\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |
| 3 | only | string | ❌ |  |

### PinServerDataRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | server\_id | string | ✅ |  |
| 2 | keys | string | ✅ |  |
| 3 | domain\_id | string | ✅ |  |

### ServerInfo

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
      <td style="text-align:left">server_id</td>
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
        <p>ServerState</p>
        <ul>
          <li>STATE_NONE</li>
          <li>PENDING</li>
          <li>INSERVICE</li>
          <li>MAINTENANCE</li>
          <li>CLOSED</li>
          <li>DELETED</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">primary_ip_address</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">ip_addresses</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">server_type</td>
      <td style="text-align:left">
        <p>ServerType</p>
        <ul>
          <li>SERVER_TYPE_NONE</li>
          <li>BAREMETAL</li>
          <li>VM</li>
          <li>HYPERVISOR</li>
          <li>UNKNOWN</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">os_type</td>
      <td style="text-align:left">
        <p>ServerOSType</p>
        <ul>
          <li>OS_TYPE_NONE</li>
          <li>LINUX</li>
          <li>WINDOWS</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">data</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">metadata</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">nics</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">disks</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">reference</td>
      <td style="text-align:left"> <a href="server (1).md#serverreference">ServerReference</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">collection_info</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">pool_info</td>
      <td style="text-align:left"> <a href="server (1).md#poolinfo">PoolInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">17</td>
      <td style="text-align:left">zone_info</td>
      <td style="text-align:left"> <a href="server (1).md#zoneinfo">ZoneInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">18</td>
      <td style="text-align:left">region_info</td>
      <td style="text-align:left"> <a href="server (1).md#regioninfo">RegionInfo</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">19</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">20</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">21</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">22</td>
      <td style="text-align:left">updated_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">23</td>
      <td style="text-align:left">deleted_at</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto">google.protobuf.Timestamp</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### ServerQuery

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
      <td style="text-align:left">server_id</td>
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
      <td style="text-align:left">state</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">primary_ip_address</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">ip_addresses</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">server_type</td>
      <td style="text-align:left">
        <p>ServerType</p>
        <ul>
          <li>SERVER_TYPE_NONE</li>
          <li>BAREMETAL</li>
          <li>VM</li>
          <li>HYPERVISOR</li>
          <li>UNKNOWN</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">os_type</td>
      <td style="text-align:left">
        <p>ServerOSType</p>
        <ul>
          <li>OS_TYPE_NONE</li>
          <li>LINUX</li>
          <li>WINDOWS</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">asset_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">pool_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">zone_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">region_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">resource_group_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### ServerReference

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource\_id | string |  |  |
| 2 | external\_link | string |  |  |

### ServerRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | server\_id | string | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ServerStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) | ✅ |  |
| 2 | domain\_id | string | ✅ |  |

### ServersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ServerInfo](server%20%281%29.md#serverinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### UpdateServerRequest

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
      <td style="text-align:left">server_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>ServerState</p>
        <ul>
          <li>STATE_NONE</li>
          <li>PENDING</li>
          <li>INSERVICE</li>
          <li>MAINTENANCE</li>
          <li>CLOSED</li>
          <li>DELETED</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">primary_ip_address</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">server_type</td>
      <td style="text-align:left">
        <p>ServerType</p>
        <ul>
          <li>SERVER_TYPE_NONE</li>
          <li>BAREMETAL</li>
          <li>VM</li>
          <li>HYPERVISOR</li>
          <li>UNKNOWN</li>
        </ul>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">os_type</td>
      <td style="text-align:left">
        <p>ServerOSType</p>
        <ul>
          <li>OS_TYPE_NONE</li>
          <li>LINUX</li>
          <li>WINDOWS</li>
        </ul>
      </td>
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
      <td style="text-align:left">data</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">metadata</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">nics</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">disks</td>
      <td style="text-align:left"> <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">reference</td>
      <td style="text-align:left"> <a href="server (1).md#serverreference">ServerReference</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"> <a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a>
      </td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">asset_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">pool_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">zone_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">17</td>
      <td style="text-align:left">region_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">18</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">19</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x2705;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">20</td>
      <td style="text-align:left">release_region</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">21</td>
      <td style="text-align:left">release_project</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left">&#x274C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

