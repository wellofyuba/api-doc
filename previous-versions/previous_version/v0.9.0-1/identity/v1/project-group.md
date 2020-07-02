---
description: null
---

# Project Group

> **Package : spaceone.api.identity.v1**

## ProjectGroup

{% hint style="info" %}
**ProjectGroup Methods:**
{% endhint %}

| NO | Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [create](../../../v0.9.0-5/identity/v1/project-group.md#create) | [CreateProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#createprojectgrouprequest) | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  |
| 2 | [update](../../../v0.9.0-5/identity/v1/project-group.md#update) | [UpdateProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#updateprojectgrouprequest) | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  |
| 3 | [delete](../../../v0.9.0-5/identity/v1/project-group.md#delete) | [ProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgrouprequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 4 | [add\_member](../../../v0.9.0-5/identity/v1/project-group.md#add_member) | [ProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberrequest) | [ProjectGroupMemberInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberinfo) |  |
| 5 | [modify\_member](../../../v0.9.0-5/identity/v1/project-group.md#modify_member) | [ProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberrequest) | [ProjectGroupMemberInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberinfo) |  |
| 6 | [remove\_member](../../../v0.9.0-5/identity/v1/project-group.md#remove_member) | [RemoveProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#removeprojectgroupmemberrequest) | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |  |
| 7 | [get](../../../v0.9.0-5/identity/v1/project-group.md#get) | [GetProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#getprojectgrouprequest) | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  |
| 8 | [list](../../../v0.9.0-5/identity/v1/project-group.md#list) | [ProjectGroupQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupquery) | [ProjectGroupsInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupsinfo) |  |
| 9 | [stat](../../../v0.9.0-5/identity/v1/project-group.md#stat) | [ProjectGroupStatQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupstatquery) | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |
| 10 | [list\_members](../../../v0.9.0-5/identity/v1/project-group.md#list_members) | [ProjectGroupMemberQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberquery) | [ProjectGroupMembersInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmembersinfo) |  |
| 11 | [list\_projects](../../../v0.9.0-5/identity/v1/project-group.md#list_projects) | [ProjectGroupProjectQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupprojectquery) | [ProjectGroupProjectsInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupprojectsinfo) |  |

### create

> **POST** /identity/v1/project-groups

| Type | Message |
| :--- | :--- |
| Request | [CreateProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#createprojectgrouprequest) |
| Response | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |

### update

> **PUT** /identity/v1/project-group/{project\_group\_id}

| Type | Message |
| :--- | :--- |
| Request | [UpdateProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#updateprojectgrouprequest) |
| Response | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |

### delete

> **DELETE** /identity/v1/project-group/{project\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgrouprequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### add\_member

> **POST** /identity/v1/project-group/{project\_group\_id}/members

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberrequest) |
| Response | [ProjectGroupMemberInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberinfo) |

### modify\_member

> **PUT** /identity/v1/project-group/{project\_group\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberrequest) |
| Response | [ProjectGroupMemberInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberinfo) |

### remove\_member

> **DELETE** /identity/v1/project-group/{project\_group\_id}/member/{user\_id}

| Type | Message |
| :--- | :--- |
| Request | [RemoveProjectGroupMemberRequest](../../../v0.9.0-5/identity/v1/project-group.md#removeprojectgroupmemberrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |

### get

> **GET** /identity/v1/project-group/{project\_group\_id}

| Type | Message |
| :--- | :--- |
| Request | [GetProjectGroupRequest](../../../v0.9.0-5/identity/v1/project-group.md#getprojectgrouprequest) |
| Response | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |

### list

> **GET** /identity/v1/project-groups
>
> **POST** /identity/v1/project-groups/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupquery) |
| Response | [ProjectGroupsInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupsinfo) |

### stat

> **POST** /identity/v1/project-groups/stat

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupStatQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |

### list\_members

> **GET** /identity/v1/project-group/{project\_group\_id}/members
>
> **POST** /identity/v1/project-group/{project\_id}/members/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupMemberQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberquery) |
| Response | [ProjectGroupMembersInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmembersinfo) |

### list\_projects

> **GET** /identity/v1/project-group/{project\_group\_id}/projects
>
> **POST** /identity/v1/project-group/{project\_id}/projects/search

| Type | Message |
| :--- | :--- |
| Request | [ProjectGroupProjectQuery](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupprojectquery) |
| Response | [ProjectGroupProjectsInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupprojectsinfo) |

## Message

### CreateProjectGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name | string |  | required |
| 2 | parent\_project\_group\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | template\_id | string |  | optional |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

### GetProjectGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  | required |
| 2 | domain\_id | string |  | required |
| 3 | only | string |  | optional |

### ProjectGroupInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | parent\_project\_group\_info | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  | {'repeated Template fields = 3;                 // TODO': 'Not be implemented TEMPLATE yet', 'string template\_id = 4;                       // TODO': 'Not be implemented TEMPLATE yet'} |
| 4 | domain\_id | string |  |  |
| 5 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 6 | created\_by | string |  |  |
| 7 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 8 | deleted\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ProjectGroupMemberInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_info | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  |  |
| 2 | user\_info | [UserInfo](../../../v0.9.0-5/identity/v1/project-group.md#userinfo) |  |  |
| 3 | roles | [RoleInfo](../../../v0.9.0-5/identity/v1/project-group.md#roleinfo) |  |  |
| 4 | labels | string |  |  |

### ProjectGroupMemberQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | project\_group\_id | string |  | required |
| 3 | user\_id | string |  | optional |
| 4 | domain\_id | string |  | required |

### ProjectGroupMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |
| 4 | roles | string |  | required |
| 5 | labels | string |  | required |

### ProjectGroupMembersInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProjectGroupMemberInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupmemberinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### ProjectGroupProjectInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_id | string |  |  |
| 2 | name | string |  |  |
| 3 | state | string |  |  |
| 4 | project\_group\_info | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  | {'google.protobuf.Struct template\_data = 4; // TODO': 'Not be implemented template service yet'} |
| 5 | domain\_id | string |  |  |
| 6 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  |  |
| 7 | created\_by | string |  |  |
| 8 | created\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |
| 9 | deleted\_at | [google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) |  |  |

### ProjectGroupProjectQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | project\_group\_id | string |  | required |
| 3 | recursive | bool |  | optional |
| 4 | domain\_id | string |  | required |

### ProjectGroupProjectsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProjectGroupProjectInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupprojectinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### ProjectGroupQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query) |  | optional |
| 2 | project\_group\_id | string |  | optional |
| 3 | parent\_project\_group\_id | string |  | optional |
| 4 | name | string |  | optional |
| 5 | template\_id | string |  | optional |
| 6 | domain\_id | string |  | required |

### ProjectGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  | required |
| 2 | domain\_id | string |  | required |

### ProjectGroupStatQuery

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query | [spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query) |  | required |
| 2 | domain\_id | string |  | required |

### ProjectGroupsInfo

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | results | [ProjectGroupInfo](../../../v0.9.0-5/identity/v1/project-group.md#projectgroupinfo) |  |  |
| 2 | total\_count | [int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) |  |  |

### RemoveProjectGroupMemberRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  | required |
| 2 | user\_id | string |  | required |
| 3 | domain\_id | string |  | required |

### UpdateProjectGroupRequest

| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | project\_group\_id | string |  | required |
| 2 | parent\_project\_group\_id | string |  | required |
| 3 | name | string |  | optional |
| 4 | release\_parent\_project\_group | bool |  | optional |
| 5 | domain\_id | string |  | required |
| 6 | template\_id | string |  | optional |
| 7 | tags | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |  | optional |

