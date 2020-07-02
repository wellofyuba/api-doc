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
| 1 | [create](../../../v0.9.0-5/identity/v1/project.md#create) | [CreateProjectRequest](../../../v0.9.0-5/identity/v1/project.md#createprojectrequest) | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/project.md#update) | [UpdateProjectRequest](../../../v0.9.0-5/identity/v1/project.md#updateprojectrequest) | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/project.md#delete) | [ProjectRequest](../../../v0.9.0-5/identity/v1/project.md#projectrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [add\_member](../../../v0.9.0-5/identity/v1/project.md#add_member) | [ProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#projectmemberrequest) | [ProjectMemberInfo](../../../v0.9.0-5/identity/v1/project.md#projectmemberinfo) |  |
| 5 | [modify\_member](../../../v0.9.0-5/identity/v1/project.md#modify_member) | [ProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#projectmemberrequest) | [ProjectMemberInfo](../../../v0.9.0-5/identity/v1/project.md#projectmemberinfo) |  |
| 6 | [remove\_member](../../../v0.9.0-5/identity/v1/project.md#remove_member) | [RemoveProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#removeprojectmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 7 | [get](../../../v0.9.0-5/identity/v1/project.md#get) | [GetProjectRequest](../../../v0.9.0-5/identity/v1/project.md#getprojectrequest) | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |  |
| 8 | [list](../../../v0.9.0-5/identity/v1/project.md#list) | [ProjectQuery](../../../v0.9.0-5/identity/v1/project.md#projectquery) | [ProjectsInfo](../../../v0.9.0-5/identity/v1/project.md#projectsinfo) |  |
| 9 | [stat](../../../v0.9.0-5/identity/v1/project.md#stat) | [ProjectStatQuery](../../../v0.9.0-5/identity/v1/project.md#projectstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 10 | [list\_members](../../../v0.9.0-5/identity/v1/project.md#list_members) | [ProjectMemberQuery](../../../v0.9.0-5/identity/v1/project.md#projectmemberquery) | [ProjectMembersInfo](../../../v0.9.0-5/identity/v1/project.md#projectmembersinfo) |  |

### create

> **POST** /identity/v1/projects

| Type | Message |
| :--- | :--- |
| Request | [CreateProjectRequest](../../../v0.9.0-5/identity/v1/project.md#createprojectrequest) |
| Response | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |

### update

> **PUT** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateProjectRequest](../../../v0.9.0-5/identity/v1/project.md#updateprojectrequest) |
| Response | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |

### delete

> **DELETE** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectRequest](../../../v0.9.0-5/identity/v1/project.md#projectrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### add\_member

> **POST** /identity/v1/project/{project\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#projectmemberrequest) |
| Response | [ProjectMemberInfo](../../../v0.9.0-5/identity/v1/project.md#projectmemberinfo) |

### modify\_member

> **PUT** /identity/v1/project/{project\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#projectmemberrequest) |
| Response | [ProjectMemberInfo](../../../v0.9.0-5/identity/v1/project.md#projectmemberinfo) |

### remove\_member

> **DELETE** /identity/v1/project/{project\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveProjectMemberRequest](../../../v0.9.0-5/identity/v1/project.md#removeprojectmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/project/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetProjectRequest](../../../v0.9.0-5/identity/v1/project.md#getprojectrequest) |
| Response | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |

### list

> **GET** /identity/v1/projects
>
> **POST** /identity/v1/projects/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectQuery](../../../v0.9.0-5/identity/v1/project.md#projectquery) |
| Response | [ProjectsInfo](../../../v0.9.0-5/identity/v1/project.md#projectsinfo) |

### stat

> **POST** /identity/v1/projects/stat

| Type | Message |
| :--- | :--- |
| Request | [ProjectStatQuery](../../../v0.9.0-5/identity/v1/project.md#projectstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### list\_members

> **GET** /identity/v1/project/{project\_id}/members
>
> **POST** /identity/v1/project/{project\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectMemberQuery](../../../v0.9.0-5/identity/v1/project.md#projectmemberquery) |
| Response | [ProjectMembersInfo](../../../v0.9.0-5/identity/v1/project.md#projectmembersinfo) |

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
| 4 | project\_group\_info | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project.md#projectgroupinfo) |  | {'google.protobuf.Struct template\_data = 4; // TODO': 'Not be implemented template service yet'} |
| 5 | domain\_id | string |  |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | created\_by | string |  |  |
| 8 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 9 | deleted\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ProjectMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_info | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |  |  |
| 2 | user\_info | [UserInfo](../../../v0.9.0-5/identity/v1/project.md#userinfo) |  |  |
| 3 | roles | [RoleInfo](../../../v0.9.0-5/identity/v1/project.md#roleinfo) |  |  |
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
| 1 | results | [ProjectMemberInfo](../../../v0.9.0-5/identity/v1/project.md#projectmemberinfo) |  |  |
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
| 1 | results | [ProjectInfo](../../../v0.9.0-5/identity/v1/project.md#projectinfo) |  |  |
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

