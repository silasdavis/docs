# Agreements Network REST API Documentation

# Organizations

### Create a New Organization

<p>Creating a new organization also established the primary administrators for that organization If no approvers are provided for the organization, then the currently logged-in user will be registered as an approver.</p>

```endpoint
POST /api/organizations
```

#### Headers

| Name    | Type      | Description                          |
|---------|-----------|--------------------------------------|
| access-key | String | <p>Users unique access-key.</p>|



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


### Information on Multiple Organizations



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






