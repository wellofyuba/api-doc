---
description: null
---

# Project

> **Package : spaceone.api.identity.v1**

## Project

{% hint style="info" %}
**Project Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](project%20%281%29.md#create) | [CreateProjectRequest](project%20%281%29.md#createprojectrequest) | [ProjectInfo](project%20%281%29.md#projectinfo) |  |
| 2 | [update](project%20%281%29.md#update) | [UpdateProjectRequest](project%20%281%29.md#updateprojectrequest) | [ProjectInfo](project%20%281%29.md#projectinfo) |  |
| 3 | [delete](project%20%281%29.md#delete) | [ProjectRequest](project%20%281%29.md#projectrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [add\_member](project%20%281%29.md#add_member) | [ProjectMemberRequest](project%20%281%29.md#projectmemberrequest) | [ProjectMemberInfo](project%20%281%29.md#projectmemberinfo) |  |
| 5 | [modify\_member](project%20%281%29.md#modify_member) | [ProjectMemberRequest](project%20%281%29.md#projectmemberrequest) | [ProjectMemberInfo](project%20%281%29.md#projectmemberinfo) |  |
| 6 | [remove\_member](project%20%281%29.md#remove_member) | [RemoveProjectMemberRequest](project%20%281%29.md#removeprojectmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 7 | [get](project%20%281%29.md#get) | [GetProjectRequest](project%20%281%29.md#getprojectrequest) | [ProjectInfo](project%20%281%29.md#projectinfo) |  |
| 8 | [list](project%20%281%29.md#list) | [ProjectQuery](project%20%281%29.md#projectquery) | [ProjectsInfo](project%20%281%29.md#projectsinfo) |  |
| 9 | [stat](project%20%281%29.md#stat) | [ProjectStatQuery](project%20%281%29.md#projectstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 10 | [list\_members](project%20%281%29.md#list_members) | [ProjectMemberQuery](project%20%281%29.md#projectmemberquery) | [ProjectMembersInfo](project%20%281%29.md#projectmembersinfo) |  |

### create

> **POST** /identity/v1/projects

| Type | Message |
| :--- | :--- |
| Request | [CreateProjectRequest](project%20%281%29.md#createprojectrequest) |
| Response | [ProjectInfo](project%20%281%29.md#projectinfo) |

### update

> **PUT** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateProjectRequest](project%20%281%29.md#updateprojectrequest) |
| Response | [ProjectInfo](project%20%281%29.md#projectinfo) |

### delete

> **DELETE** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectRequest](project%20%281%29.md#projectrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### add\_member

> **POST** /identity/v1/project/{project\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberRequest](project%20%281%29.md#projectmemberrequest) |
| Response | [ProjectMemberInfo](project%20%281%29.md#projectmemberinfo) |

### modify\_member

> **PUT** /identity/v1/project/{project\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberRequest](project%20%281%29.md#projectmemberrequest) |
| Response | [ProjectMemberInfo](project%20%281%29.md#projectmemberinfo) |

### remove\_member

> **DELETE** /identity/v1/project/{project\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveProjectMemberRequest](project%20%281%29.md#removeprojectmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetProjectRequest](project%20%281%29.md#getprojectrequest) |
| Response | [ProjectInfo](project%20%281%29.md#projectinfo) |

### list

> **GET** /identity/v1/projects
>
> **POST** /identity/v1/projects/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectQuery](project%20%281%29.md#projectquery) |
| Response | [ProjectsInfo](project%20%281%29.md#projectsinfo) |

### stat

> **POST** /identity/v1/projects/stat

| Type | Message |
| :--- | :--- |
| Request | [ProjectStatQuery](project%20%281%29.md#projectstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### list\_members

> **GET** /identity/v1/project/{project\_id}/members
>
> **POST** /identity/v1/project/{project\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberQuery](project%20%281%29.md#projectmemberquery) |
| Response | [ProjectMembersInfo](project%20%281%29.md#projectmembersinfo) |

## Message

### CreateProjectRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | project\_group\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | template\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### GetProjectRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### ProjectInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | state | string |  |  |
| 4 | project\_group\_info | [ProjectGroupInfo](project%20%281%29.md#projectgroupinfo) |  | {'google.protobuf.Struct template\_data = 4; // TODO': 'Not be implemented template service yet'} |
| 5 | domain\_id | string |  |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | created\_by | string |  |  |
| 8 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 9 | deleted\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ProjectMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_info | [ProjectInfo](project%20%281%29.md#projectinfo) |  |  |
| 2 | user\_info | [UserInfo](project%20%281%29.md#userinfo) |  |  |
| 3 | roles | [RoleInfo](project%20%281%29.md#roleinfo) |  |  |
| 4 | labels | string |  |  |

### ProjectMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | project\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | user\_id | string |  | optional |

### ProjectMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | roles | string |  | required |
| 5 | labels | string |  | required |

### ProjectMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProjectMemberInfo](project%20%281%29.md#projectmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### ProjectQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | project\_id | string |  | optional |
| 3 | project\_group\_id | string |  | optional |
| 4 | domain\_id | string |  | required |
| 5 | name | string |  | optional |

### ProjectRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### ProjectStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### ProjectsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProjectInfo](project%20%281%29.md#projectinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemoveProjectMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### UpdateProjectRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  | required |
| 2 | project\_group\_id | string |  | optional |
| 3 | name | string |  | optional |
| 4 | domain\_id | string |  | required |
| 5 | template\_data | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

