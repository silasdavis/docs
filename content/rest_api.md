## 

This is the REST API group for the Agreements Network.

## Organizations

### Create a New Organization

<p>Creating a new organization also established the primary administrators for that organization If no approvers are provided for the organization, then the currently logged-in user will be registered as an approver.</p>

```endpoint
POST /api/organizations
```

#### Headers

| Name    | Type      | Description                          |
|---------|-----------|--------------------------------------|
| access-key | String | <p>Users unique access-key.</p>|




#### Parameters

| Parameter     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| token | String | <p>JWT token which is acquired via the /register and/or /login endpoints</p>_Size range: 20_<br>|

#### Example Requests


```curl
curl -X POST /api/organizations
```



#### 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Hexadecimal address of the new organization.</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Organizations



```endpoint
GET /api/organizations
```





#### Parameters

| Parameter     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| approver | Address | <p>If the optional query parameter is given causes a JOIN query to retrieve only organizations where the specified user is an approver.</p>|

#### Example Requests


```curl
curl -i /api/organizations
```


#### Success Response

Success Objects Array

```json
[
 {"address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E", "id": "acmecorp92", "name": "ACME Corp"}
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Organization's Controller Contract</p>|
| id | String | <p>Organization's machine readable ID</p>|
| name | String | <p>Organization's human readable name</p>|




### An Organization&#39;s Users



```endpoint
GET /api/organizations/:address/users
```





#### Parameters

| Parameter     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| active | Boolean | <p>The <code>active</code> flag is an optional filter. Leaving it off will return all users associated with the organization.</p>|

#### Example Requests


```curl
curl -i /api/organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E/users
```


#### Success Response

Success Objects Array

```json
[
 {
  "address": "2BFCC5D3FD4CB5FF62CDF101CA9B1CE8F3E9C1DB",
  "id": "AHZZMJvNp6",
  "organization": "771190B939D92AC5C4E668602337DB3B4884B7FD",
  "organizationId": "acmecorp739",
  "organizationName": "ACME Corp",
  "active": false
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Users controller contract</p>|
| id | String | <p>Users's machine readable ID</p>|
| organization | String | <p>Organization's controller contract</p>|
| organizationId | String | <p>Organization's machine readable ID</p>|
| organizationName | String | <p>Organization's human readable name</p>|
| active | Boolean | <p>Whether the user is active with the organization</p>|




### Read a Single Organization



```endpoint
GET /api/organizations/:address
```




#### Example Requests


```curl
curl -i /api/organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E
```


#### Success Response

Success Object

```json
{"address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E", "id": "acmecorp92", "name": "ACME Corp"}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Organization's Controller Contract</p>|
| id | String | <p>Organization's machine readable ID</p>|
| name | String | <p>Organization's human readable name</p>|




