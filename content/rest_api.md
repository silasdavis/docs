## Agreements Network REST API

This is the REST API group for the Agreements Network.

## Agreements

### Create an Agreement



```endpoint
POST /agreements
```







#### Example Requests


```curl
curl -iX POST /agreements
```



#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>The address of the created Archetype</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read an Agreement

<p>Retrieves Active Agreement information for a single Agreement. Note: if the password provided is incorrect or a hoard reference which does not exist was passed to the posted Active Agreement this get will return a <code>401</code>.</p>

```endpoint
GET /agreements/:address
```







#### Example Requests


```curl
curl -i /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890
```


#### Success Response

Success Object

```json
{
 "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
 "name": "Agreement",
 "archetype": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
 "isPrivate": false,
 "parties": []
 "values": {
    "custom-field-name": custom-field-value,
    ...
  }
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Active Agreement's address</p>|
| name | String | <p>Human readable name of the Active Agreement</p>|
| archetype | String | <p>Address of the parent Archetype of the Active Agreement</p>|
| isPrivate | Boolean | <p>Whether the encryption framework of the Active Agreement is operational or not</p>|
| parties | String[] | <p>The addresses of the parties to the Active Agreement</p>|
| values | Object[] | <p>The &quot;custom-field-name&quot; and values of the parameters.</p>|




### Read Agreements

<p>Retrieves Active Agreement information.</p>

```endpoint
GET /agreements
```







#### Example Requests


```curl
curl -i /agreements
```


#### Success Response

Success Objects Array

```json
[
 {
  "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
  "name": "Agreement",
  "archetype": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
  "isPrivate": false,
  "numberOfParties": 2,
  "hoardAddress": "ABCDEF0123456789ABCDEF0123456789",
  "hoardSecret": "ABCDEF0123456789ABCDEF0123456789"
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Active Agreement's address</p>|
| name | String | <p>Human readable name of the Active Agreement</p>|
| archetype | String | <p>Address of the parent Archetype of the Active Agreement</p>|
| isPrivate | Boolean | <p>Whether the encryption framework of the Active Agreement is operational or not</p>|
| numberOfParties | Number | <p>The number of parties agreeing to the Active Agreement</p>|
| hoardAddress | String | <p>The hoard content-addressable storage address of the Active Agreement</p>|
| hoardSecret | String | <p>The hashed hoard secret key</p>|




### Cancel an Agreement

<p>Cancels an agreement if the authenticated user is a member of the agreement parties, or a member of an organization that is an agreement party</p>

```endpoint
PUT /agreements
```







#### Example Requests


```curl
curl -iX PUT /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/cancel
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Sign an Agreement

<p>Signs an agreement by the authenticated user</p>

```endpoint
PUT /agreements
```







#### Example Requests


```curl
curl -iX PUT /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/sign
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Add a Fulfillment Event to an Agreement



```endpoint
POST /agreements/:address/events/:eventName
```







#### Example Requests


```curl
curl -iX POST /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/events/nameOfEvent
```


#### Success Response

Success Object

```json
{
 "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
 "secretKey": ABCDEF0123456789ABCDEF0123456789,
 "salt": ""
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>The hoard address of the updated event log</p>|
| secretKey | String | <p>The hoard secret key of the updated event log</p>|
| salt | String | <p>The hoard salt of the updated event log</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## Archetypes

### Create an Archetype

<p>Note: <code>fields</code> and <code>documents</code> are optional in the POST and can be added later via the below PUT requests.</p>

```endpoint
POST /archetypes
```







#### Example Requests


```curl
curl -iX POST /archetypes
```



#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>The address of the created Archetype</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read an Archetype

<p>Retrieves archetype information for a single Archetype. Note: if the password provided is incorrect or a hoard reference which does not exist was passed to the posted archetype this get will return a <code>401</code>.</p>

```endpoint
GET /archetypes/:address
```







#### Example Requests


```curl
curl -i /archetypes/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890
```


#### Success Response

Success Object

```json
{
 "address": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
 "name": "TestType1",
 "author": "6EDC6101F0B64156ED867BAE925F6CD240635656",
 "active": false,
 "isPrivate": false,
 "fields": [
  {"name": "NumberOfTeenageDaughters", "type": 4},
  {"name": "ExitClause", "type": 2}
 ],
 "documents": [
  {"name": "Dok1", "hoardAddress": ..., "secretKey": ...}
 ],
 "jurisdictions": [
  {"country": "US", "regions": ["0304CA03C4E9DD0F9676A4463D42BCB686331A5361570D9BF7BC211C1BCA9F1E","04E01B41ABD856ECAE38A06FB81005A911271B4BF483C10F31C539031C399101"]},
  {"country": "CA", "regions": []}
 ]
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Archetype's address</p>|
| name | String | <p>Human readable name of the Archetype</p>|
| author | String | <p>Controller contract of the user or organization that created the Archetype</p>|
| active | Boolean | <p>Whether the Archetype can be used to create new Active Agreements or not</p>|
| isPrivate | Boolean | <p>Whether the encryption framework of the Archetype is operational or not</p>|
| fields | Object[] | <p>The &quot;name&quot; and &quot;type&quot; of all custom parameters used by the Archetype</p>|
| documents | Object[] | <p>The &quot;name&quot;, &quot;hoardAddress&quot; and &quot;secretKey&quot; (if any) sufficient to provide the information regarding the relevant documents associated with the Archetype</p>|
| jurisdictions | Object[] | <p>The &quot;country&quot; and &quot;regions&quot; which the Archetype has been registered as relevant to. The &quot;country&quot; is registered as an ISO standard two character string and &quot;regions&quot; is an array of addresses relating to the controlling contracts for the region (see <a href="#">ISO standards manipulation</a> section).</p>|




### Read Archetypes

<p>Retrieves archetype information. Within the Agreements Network, Archetypes are the fundamental, top level objects. They are holders for a set of information which allows users to creat Active Agreements within the Platform.</p>

```endpoint
GET /archetypes
```







#### Example Requests


```curl
curl -i /archetypes
```


#### Success Response

Success Objects Array

```json
[
 {
  "address": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
  "name": "TestType1",
  "author": "6EDC6101F0B64156ED867BAE925F6CD240635656",
  "active": false,
  "isPrivate": false,
  "numberOfFields": 2,
  "numberOfDocuments": 1,
  "countries": ["US","CA"]
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Archetype's address</p>|
| name | String | <p>Human readable name of the Archetype</p>|
| author | String | <p>Controller contract of the user or organization that created the Archetype</p>|
| active | Boolean | <p>Whether the Archetype can be used to create new Active Agreements or not</p>|
| isPrivate | Boolean | <p>Whether the encryption framework of the Archetype is operational or not</p>|
| numberOfFields | Number | <p>The number of custom parameters used by the Archetype</p>|
| numberOfDocuments | Number | <p>The number of documents registered against the Archetype</p>|
| countries | String[] | <p>The jurisdictions in which the Archetype has been registered to be active</p>|




### Update an Archetype

<p>Note that the object sent should meet the definition located in the CreateOrganization section and should match the configurationSection endpoint given. Currently the following configurationFields are the <strong>only</strong> fields which can be updated</p> <ul> <li>configuration</li> <li>fields</li> <li>documents</li> </ul>

```endpoint
PUT /archetypes/:address/:configurationSection
```







#### Example Requests


```curl
curl -iX PUT /archetypes/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/fields
```



#### 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Success |  | |



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## Authorizations

### Log in as a User



```endpoint
POST /login
```







#### Example Requests


```curl
curl -iX POST /login
```


#### Success Response

Success Object

```json
{
   "userData": {
        address: "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
        id: "username/id"
    },
    "orgData" {
        address: "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
        id: "organization id",
        name: "organization Name"
    },
    "token": "longtokenstringneededforpostrequests"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| userData | Object | <p>The &quot;address&quot; and &quot;id&quot; of the User</p>|
| orgData | Object | <p>The &quot;address&quot; &quot;id&quot; and &quot;name&quot; of the User's organizations</p>|
| token | String | <p>The user's authorization token for the session</p>|




### Log out a User



```endpoint
POST /logout
```







#### Example Requests


```curl
curl -iX POST /logout
```






### Request password reset for a user account

<p>Sends an email with a password recovery code to the given email address</p>

```endpoint
POST /password-recovery
```







#### Example Requests


```curl
curl -iX POST /password-recovery
```






### Register a User



```endpoint
POST /register
```







#### Example Requests


```curl
curl -iX POST /register
```



#### 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Success |  | |



#### 403

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| User |  | <p>Exists</p>|


### Reset password for user account

<p>Resets the user's password with the given password, if the recovery code is valid</p>

```endpoint
PUT /password-recovery/:recoveryCode
```







#### Example Requests


```curl
curl -iX PUT /password-recovery/vdk7bd2esdf3234...
```






### Validates the given password recovery code

<p>Checks if the given password recovery code is valid</p>

```endpoint
GET /password-recovery/:recoveryCode
```







#### Example Requests


```curl
curl -iX GET /password-recovery/vdk7bd2esdf3234...
```






## Content

### Create Dummy Content



```endpoint
POST /dummy
```







#### Example Requests


```curl
curl -iX POST /dummy
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Content Object



```endpoint
GET /hoard
```







#### Example Requests


```curl
curl -i /hoard
```






## Models

### Create Model



```endpoint
POST /models
```







#### Example Requests


```curl
curl -iX POST /models
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Create a process definition

<p>Creates a process definition with info passed in the request body: { modelAddress: 'AC1E0E841141FFF510350D04696174C8B4BDF53A', id: 'myProcess1', name: 'My Process 1', hoardAddress: 'd71376de29b408f82974d4ca5685db9e6f415ea13c66b774a86429e80f341131', hoardSecret: '52f57f5997d5c1bb088e7de4720709179059ca394ef81247c7a691ea44924717', }</p>

```endpoint
POST /process
```







#### Example Requests


```curl
curl -i /process
```


#### Success Response

1EC5F9ABE8053D87526786F98957AC6631206E7C

```json
1EC5F9ABE8053D87526786F98957AC6631206E7C
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Address | text | <p>of process definition</p>|




### Read Activities

<p>Read all activities. Accepts an optional query string parameter <code>processInstance</code> to read only the activities with the given process addess.</p>

```endpoint
GET /activity-instances
```







#### Example Requests


```curl
curl -i /activity-instances?processInstance=150D431B160790B2462D8CC683C87FEA2F1C3C61
```






### Read All Process Definitions



```endpoint
GET /definitions
```







#### Example Requests


```curl
curl -i /definitions
```


#### Success Response

Success Objects Array

```json
[
  {
      "modelAddress":"912A82D4C72847EF1EC76426544EAA992993EE20",
      "processDefinitionAddress":"81A817870C6C6A209150FA26BC52D835CA6E17D2",
      "id":"defaultFormationProcess",
      "name":"Default Formation Process",
      "interfaceId":"Agreement Formation",
      "diagramAddress":"7D85BB76DB402B752F84792FF50B40483922673CF277CD2045D3D9637D4CE8F9",
      "diagramSecret":"4AF3A863BF6F2AD79E4919F562252866CBDA58E3E5AA27E2C5C94BAE9931BE74"
  },{
      "modelAddress":"912A82D4C72847EF1EC76426544EAA992993EE20",
      "processDefinitionAddress":"A043C06EB2FB91F4811F51F6500744906FD0903E",
      "id":"defaultExecutionProcess",
      "name":"Default Execution Process",
      "interfaceId":"Agreement Execution",
      "diagramAddress":"7D85BB76DB402B752F84792FF50B40483922673CF277CD2045D3D9637D4CE8F9",
      "diagramSecret":"4AF3A863BF6F2AD79E4919F562252866CBDA58E3E5AA27E2C5C94BAE9931BE74"
  }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| object | Object[] | <p>Process Definition object</p>|




### Read Execution Process Definition



```endpoint
GET /definitions/execution
```







#### Example Requests


```curl
curl -i /definitions/execution
```






### Read Single Field Type



```endpoint
GET /fieldTypes/:id
```







#### Example Requests


```curl
curl -i /fieldTypes/:id
```






### Read Field Types



```endpoint
GET /fieldTypes
```







#### Example Requests


```curl
curl -i /fieldTypes
```






### Read Formation Process Definition



```endpoint
GET /definitions/formation
```







#### Example Requests


```curl
curl -i /definitions/formation
```


#### Success Response

Success Objects Array

```json
[
    {
        "modelAddress":"912A82D4C72847EF1EC76426544EAA992993EE20",
        "processDefinitionAddress":"81A817870C6C6A209150FA26BC52D835CA6E17D2",
        "id":"defaultFormationProcess",
        "name":"Default Formation Process",
        "interfaceId":"Agreement Formation",
        "diagramAddress":"7D85BB76DB402B752F84792FF50B40483922673CF277CD2045D3D9637D4CE8F9",
        "diagramSecret":"4AF3A863BF6F2AD79E4919F562252866CBDA58E3E5AA27E2C5C94BAE9931BE74"
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| object | Object[] | <p>Process Definition object</p>|




### Read Instance Count



```endpoint
GET /processInstanceCount
```







#### Example Requests


```curl
curl -i /processInstanceCount
```






### Read Models



```endpoint
GET /models
```







#### Example Requests


```curl
curl -iX POST /models
```


#### Success Response

Success Object Array

```json
[
    {
        "modelAddress":"912A82D4C72847EF1EC76426544EAA992993EE20",
        "id":"0000000000000000000000000000000000000000000000000000000000000000",
        "name":"0000000000000000000000000000000000000000000000000000000000000000",
        "versionMajor":0,
        "versionMinor":0,
        "versionPatch":0,
        "active":true
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| modelAddress | String | |
| id | String | |
| name | String | |
| versionMajor | Number | |
| versionMinor | Number | |
| versionPatch | Number | |
| active | Boolean | |




### Read Tasks

<p>Retrieves an array of tasks assigned to the user at address provided in the route.</p>

```endpoint
GET /tasks
```







#### Example Requests


```curl
curl -i /tasks
```


#### Success Response

Success Objects Array

```json
[
    {
        "activityId": "userActivity",
        "assignee": "AC1E0E841141FFF510350D04696174C8B4BDF53A",
        "created": 1498768880,
        "processId": "testProcessId",
        "processName": "testProcessName",
        "application": "",
        "state": "SUSPENDED"
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| object | Object[] | <p>Array of task objects</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Begin a Business Process



```endpoint
POST /startProcess
```







#### Example Requests


```curl
curl -iX POST /startProcess
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Validate a Business Process



```endpoint
POST /validateProcess
```







#### Example Requests


```curl
curl -iX POST /validateProcess
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## Models_BPMN_XML_needs_to_be_passed_in_the_request_body_as_plain_text_or_application_xml

### Parse BPMN XML and from it create a process model and definition



```endpoint
POST /bpmn/model
```







#### Example Requests


```curl
curl -i /bpmn/model
```


#### Success Response

Success Object

```json
{
    "model": {
        "id": "model_10",
        "address": "3650839FB751186AC9B1B2BBDD30E23D7926D6E6"
    },
    "processes": [
        {
            "id": "Process_1",
            "address": "B19BA0D61DD95958C4B6B8F11B03477C24738D53",
            "startActivity": "Task_0m3bxv3"
            "interfaceId": "Agreement Formation",
            "name": "Process Name",
            "modelAddress": "234AC325FEAD83822BCDDE83813223DEA3AD",
            "participants": "[{"id":"Lane_0dcbbm2","name":"Lane Label 1","tasks":[null],"conditionalPerformer":true,"dataStorageId":"agreement","dataPath":"seller"}]"
        },
        {
            "id": "Process_2",
            "address": "696133F794C0B87C0E40FEE4144648798C508379",
            "startActivity": "Task_0a1ijkc"
            "interfaceId": "Agreement Execution",
            "name": "Process Name",
            "modelAddress": "234AC325FEAD83822BCDDE83813223DEA3AD",
            "participants": "[{"id":"Lane_0dcttm4","name":"Lane Label 2","tasks":[null],"conditionalPerformer":true,"dataStorageId":"agreement","dataPath":"buyer"}]"
        }
    ]
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Address | Object | <p>of process model, process definition(s) and start activity id(s)</p>|




## Organizations

### Create a New Organization

<p>Creating a new organization also established the primary administrators for that organization If no approvers are provided for the organization, then the currently logged-in user will be registered as an approver.</p>

```endpoint
POST /organizations
```







#### Example Requests


```curl
curl -iX POST /organizations
```



#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Organization's Controller Contract</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Organizations



```endpoint
GET /organizations
```







#### Example Requests


```curl
curl -i /organizations
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
GET /organizations/:address/users
```







#### Example Requests


```curl
curl -i /organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E/users
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
GET /organizations/:address
```







#### Example Requests


```curl
curl -i /organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E
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




### Removes a user from Organization



```endpoint
DELETE /organizations/:orgid/users/:userAccount
```







#### Example Requests


```curl
curl -iX DELETE /organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E/users/10DA7307DA7E74BC54D1E829764E2DE7AD0D8DBB4
```



#### 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Success |  | |



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Adds user to Organization



```endpoint
PUT /organizations/:orgid/users/:userAccount
```







#### Example Requests


```curl
curl -iX PUT /organizations/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E/users/10DA7307DA7E74BC54D1E829764E2DE7AD0D8DBB4
```



#### 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| Success |  | |



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## Runtime

### Complete task identified by the given task id

<p>Completes the activity identified by the activityInstanceId. The activityInstanceId needs to be passed as a param.</p>

```endpoint
PUT /tasks/:id/complete
```







#### Example Requests


```curl
curl -i /task/:id/complete
```






## Standards

### Read Countries



```endpoint
GET /iso/countries
```







#### Example Requests


```curl
curl -i /iso/countries
```


#### Success Response

Success Objects Array

```json
[
    {
        "country": "US",
        "alpha2": "US",
        "alpha3": "USA",
        "m49": "840",
        "name": "United States of America"
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| countries | Object[] | <p>An array of countries objects (see below)</p>|




### Read Country

<p>Retrieves the country whose <code>alpha2</code> code matches the one passed as parameter.</p>

```endpoint
GET /iso/countries/:alpha2
```







#### Example Requests


```curl
curl -i /iso/countries/:alpha2
```


#### Success Response

Success Object

```json
{
    "country": "US",
    "alpha2": "US",
    "alpha3": "USA",
    "m49": "840",
    "name": "United States of America"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| country | Object | <p>A single countries objects (see below)</p>|




### Read Currencies



```endpoint
GET /iso/currencies
```







#### Example Requests


```curl
curl -i /iso/currencies
```


#### Success Response

Success Objects Array

```json
[
    {
        "currency": "AED",
        "alpha3": "AED",
        "m49": "784",
        "name": "United Arab Emirates dirham"
    },
    {
        "currency": "AFN",
        "alpha3": "AFN",
        "m49": "971",
        "name": "Afghan afghani"
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| currencies | Object[] | <p>An array of currencies objects (see below)</p>|




### Read Currency

<p>Retrieves the currency whose <code>alpha3</code> code matches the one passed as parameter.</p>

```endpoint
GET /iso/currencies/:alpha3
```







#### Example Requests


```curl
curl -i /iso/currencies/:alpha3
```


#### Success Response

Success Objects Array

```json
{
    "currency": "USD",
    "alpha3": "USD",
    "m49": "840",
    "name": "United States dollar"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| currency | Object | <p>A single currency objects (see below)</p>|




### Read a Country&#39;s Regions

<p>Retrieves an array of regions belonging to the country whose <code>alpha2</code> code matches the one passed as parameter. Note that a region may have its <code>code2</code> OR <code>code3</code> property populated, NOT both. Thus to represent regions in the UI dropdown, we can use <code>&lt;alpha2&gt;-&lt;code2 or code3&gt;</code> followed by the name.</p>

```endpoint
GET /iso/countries/:alpha2/regions
```







#### Example Requests


```curl
curl -i /iso/countries/:alpha2/regions
```


#### Success Response

Success Objects Array

```json
[
    {
        "country": "CA",
        "region": "0798FDAD71114ABA2A3CD6B4BD503410F8EF6B9208B889CC0BB33CD57CEEAA9C",
        "alpha2": "CA",
        "code2": "AB",
        "code3": "",
        "name": "Alberta"
    },
    {
        "country": "CA",
        "region": "1C16E32AED9920491BFED16E1396344027C8D6916833C64CE7F8CCF541398F3B",
        "alpha2": "CA",
        "code2": "NT",
        "code3": "",
        "name": "Northwest Territories"
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| regions | Object[] | <p>An array of regions objects (see below)</p>|




## Users

### Read Single User

<p>Retrieves a single users information.</p>

```endpoint
GET /users
```







#### Example Requests


```curl
curl -i /users/9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E
```


#### Success Response

Success Object

```json
{
 "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
 "id": "j.smith",
 "organization": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
 "organizationId": "acmecorp92",
 "organizationName": "ACME Corp"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Users's Controller Contract</p>|
| id | String | <p>Users's machine readable ID</p>|
| organization | String | <p>Organization's Controller Contract</p>|
| organizationId | String | <p>Organization's machine readable ID</p>|
| organizationName | String | <p>Organization's human readable name</p>|




### Read Users

<p>Retrieves user information. The <code>organization</code> query parameter is optional. It can be used to filter users belonging to a specific organization or retrieving users not belonging to an organization, yet (via <code>?organization=null</code>).</p> <p>Note: The organization address is returned as &quot;0000000000000000000000000000000000000000&quot; for user that do not belong to an organization.</p>

```endpoint
GET /users
```







#### Example Requests


```curl
curl -i /users
```


#### Success Response

Success Objects Array

```json
[
 {
  "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
  "id": "j.smith",
  "organization": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
  "organizationId": "acmecorp92",
  "organizationName": "ACME Corp"
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Users's Controller Contract</p>|
| id | String | <p>Users's machine readable ID</p>|
| organization | String | <p>Organization's Controller Contract</p>|
| organizationId | String | <p>Organization's machine readable ID</p>|
| organizationName | String | <p>Organization's human readable name</p>|




### Read User&#39;s Agreements



```endpoint
GET /users/:address/agreements
```







#### Example Requests


```curl
curl -iX POST /users/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/agreements
```



#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| agreement | Object | <p>Agreement object array (see <a href="#">Agreements section</a>)</p>|




