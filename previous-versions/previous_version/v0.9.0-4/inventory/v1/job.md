---
description: null
---

# Job

> **Package : spaceone.api.inventory.v1**

## Job

{% hint style="info" %}
**Job Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [list](../../../v0.9.0-5/inventory/v1/job.md#list) | [JobsQuery](../../../v0.9.0-5/inventory/v1/job.md#jobsquery) | [JobsInfo](../../../v0.9.0-5/inventory/v1/job.md#jobsinfo) |  |
| 2 | [stat](../../../v0.9.0-5/inventory/v1/job.md#stat) | [JobStatQuery](../../../v0.9.0-5/inventory/v1/job.md#jobstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |

### list

> **GET** /inventory/v1/jobs
>
> **POST** /inventory/v1/jobs/search

| Type | Message |
| :--- | :--- |
| Request | [JobsQuery](../../../v0.9.0-5/inventory/v1/job.md#jobsquery) |
| Response | [JobsInfo](../../../v0.9.0-5/inventory/v1/job.md#jobsinfo) |

### stat

> **POST** /inventory/v1/jobs/stat

| Type | Message |
| :--- | :--- |
| Request | [JobStatQuery](../../../v0.9.0-5/inventory/v1/job.md#jobstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

## Message

### JobStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### JobsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [JobInfo](../../../v0.9.0-5/inventory/v1/job.md#jobinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### JobsQuery

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
      <td style="text-align:left">job_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left">
        <p>JobState</p>
        <ul>
          <li>JOB_STATE_NONE</li>
          <li>CREATED</li>
          <li>CANCELED</li>
          <li>IN_PROGRESS</li>
          <li>FINISHED</li>
          <li>FAILURE</li>
          <li>TIMEOUT</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">collector_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">resource_type</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">resource_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>
