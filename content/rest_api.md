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


#### Success Response

Success-Response:

```json
{
	"address": "6EDC6101F0B64156ED867BAE925F6CD240635656"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| The | json | <p>address of the created Agreement</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Create a Agreement Collection

<p>Creates an Active Agreement Collection.</p>

```endpoint
GET /agreement-collections
```







#### Example Requests


```curl
curl -iX POST /agreement-collections
```


#### Success Response

Success Object

```json
{
	"id": "9FBC54D1E8224307DA7E74BC54D1E829764E2DE7AD0D8DF6EBC54D1E82ADBCFF"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| name | String | <p>Active Agreement Collection name</p>|
| author | String | <p>Address of the creator (user account or org), logged in user address will be used if none supplied</p>|
| collectionType | Number | <p>Type of collection</p>|
| packageId | String | <p>The packageId of the archetype package from which the collection was created</p>|



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
				  "eventLogHoardAddress": "0000000000000000000000000000000000000000000000000000000000000000",
   				  "eventLogHoardSecret": "0000000000000000000000000000000000000000000000000000000000000000",
				  "maxNumberOfEvents": 0,
				  "legalState": 1,
				  "formationProcessInstance": "413AC7610E6A4E0ACEB29596FFC52D243A2E7CD7",
  				  "executionProcessInstance": "0000000000000000000000000000000000000000",
				  "parties": [
					  "address": "A072341D3BBD4FDD3CD5D0EBADB0EB37887E3311",
					  "organizationName": "Drones Delight"
					  "signatureTimestamp": 1529588821427,
					  "completedBy": "BE98345FEDCD465D0EBADB0EB3789F234ECBD"
				  ],
				  "parameters": {
				     "parameterName": "parameterValue",
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
| eventLogHoardAddress | String | <p>Hoard address of where event log is stored</p>|
| eventLogHoardSecret | String | <p>Hoard secret of where event log is stored</p>|
| maxNumberOfEvents | Number | <p>Max number of fulfillment events that can be stored in the event log</p>|
| legalState | Number | <p>Legal state of the agreement</p>|
| formationProcessInstance | Number | <p>Address of the agreement's formation process instance</p>|
| executionProcessInstance | Number | <p>Address of the agreement's execution process instance</p>|
| parties | Object[] | <p>An array of objects with each party member's address, user id or organization name, signature timestamp, and address of the user that has signed for the party</p>|
| parameters | Object[] | <p>The &quot;parameter-name&quot; and values of the parameters.</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read an Agreement Collection

<p>Retrieves information for a single Agreement Collection.</p>

```endpoint
GET /agreement-collections/:id
```







#### Example Requests


```curl
curl -i /agreement-collections/7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD
```


#### Success Response

Success Object

```json
	{
		"id": "7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD",
		"name": "Agreement Collection 1",
		"author": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
		"collectionType": 2,
		"packageId": "9FBC54D1E8224307DA7E74BC54D1E829764E2DE7AD0D8DF6EBC54D1E82ADBCFF",
		"agreements": [
			{
				"name": "Agreement 1",
				"address": "E615D0EC4BB0EDDE615D0EC4BB0EB3D909F66890",
				"archetype": "42B7AC86A84DD3AA054F567BCF5D27D9622FCD0B"
			}
		]
  }
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| id | String | <p>Agreement Collection id</p>|
| name | String | <p>Human readable name of the Agreement Collection</p>|
| author | String | <p>Controller contract of the user or organization</p>|
| collectionType | Number | <p>Type of collection</p>|
| packageId | String | <p>The packageId of the archetype package from which the collection was created</p>|
| agreements | Object[] | <p>Array of agreement objects included in the collection</p>|




### Read Agreement Collections

<p>Retrieves Active Agreement Collection information.</p>

```endpoint
GET /agreement-collections
```







#### Example Requests


```curl
curl -i /agreement-collections
```


#### Success Response

Success Objects Array

```json
[
 {
  "id": "9FBC54D1E8224307DA7E74BC54D1E829764E2DE7AD0D8DF6EBC54D1E82ADBCFF",
  "name": "Agreement Collection 1",
  "author": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
  "collectionType": 2,
  "packageId": "7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD"
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| id | String | <p>Active Agreement Collection id</p>|
| name | String | <p>Human readable name of the Active Agreement Collection</p>|
| author | String | <p>Address of the creator (user account or org)</p>|
| collectionType | Number | <p>Type of collection</p>|
| packageId | String | <p>The packageId of the archetype package from which the collection was created.</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Tasks of an Agreement

<p>Retrieves completed task information for a single Agreement.</p>

```endpoint
GET /agreements/:address/tasks
```







#### Example Requests


```curl
curl -i /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/tasks
```


#### Success Response

Success Object

```json
 {
	"agreementAddress": "391F69095A291E21079A78F0F67EE167D7628AE2",
	"agreementName": "Agreement Name"
	"processDefinitionAddress": "0506903B34830785168D840BB70D7D48D31A5C1F",
	"processAddress": "5128E9E1776CB45F351E226A3DC476964A07BBC0",
	"processName": "Ship",
	"activityId": "buyItem",
	"activityInstanceId": "DA3745AD5DCD2E53854ED699AD73E2C550BA5AB3E484AACCCC0FDBF959C8A3FF",
	"created": 1528923353,
	"performer": "36ADA22D3A4B841EFB73414CD97C35C0A660C1C2",
	"completedBy": "36ADA22D3A4B841EFB73414CD97C35C0A660C1C2",
	"state": 2,
 }
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| agreementAddress | String | <p>Active Agreement's address</p>|
| agreementName | String | <p>Human readable name of the Active Agreement</p>|
| processDefinitionAddress | String | |
| processAddress | String | |
| processName | String | <p>Human readable name of process</p>|
| activityId | String | <p>Human readable name of activity</p>|
| activityInstanceId | String | <p>address of activity instance</p>|
| created | Integer | <p>Unix timestamp of activity creation</p>|
| performer | String | <p>Address of assignee</p>|
| completedBy | String | <p>Address of contract that completed task</p>|
| state | Integer | <p>Number that maps to the state of the task</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


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
PUT /agreements/:address/events
```







#### Example Requests


```curl
curl -iX POST /agreements/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890/events -d '{"eventName":"eventName"}'
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

### Add an archetype to a package



```endpoint
PUT /archetype-packages/:id/archetype/:address
```







#### Example Requests


```curl
curl -iX PUT /archetype-packages/7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD/archetype/707791D3BBD4FDDE615D0EC4BB0EB3D909F66890
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Create an Archetype



```endpoint
POST /archetypes
```







#### Example Requests


```curl
curl -iX POST /archetypes
```


#### Success Response

Success-Response:

```json
{
	"address": "6EDC6101F0B64156ED867BAE925F6CD240635656"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| The | json | <p>address of the created Archetype</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Create an Archetype Package



```endpoint
POST /archetypes/packages
```







#### Example Requests


```curl
curl -iX POST /archetype-packages
```


#### Success Response

Success-Response:

```json
{
	"id": "7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| The | json | <p>id of the created Archetype Package</p>|



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
 "parameters": [
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
| parameters | Object[] | <p>The &quot;name&quot; and &quot;type&quot; of all custom parameters used by the Archetype</p>|
| documents | Object[] | <p>The &quot;name&quot;, &quot;hoardAddress&quot; and &quot;secretKey&quot; (if any) sufficient to provide the information regarding the relevant documents associated with the Archetype</p>|
| jurisdictions | Object[] | <p>The &quot;country&quot; and &quot;regions&quot; which the Archetype has been registered as relevant to. The &quot;country&quot; is registered as an ISO standard two character string and &quot;regions&quot; is an array of addresses relating to the controlling contracts for the region (see <a href="#">ISO standards manipulation</a> section).</p>|




### Read an Archetype Package

<p>Retrieves information for a single archetype package.</p>

```endpoint
GET /archetype-packages/:id
```







#### Example Requests


```curl
curl -i /archetype-packages/7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD
```


#### Success Response

Success Object

```json
{
  "id": "7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD",
  "name": "Package1",
  "description": "Package Description",
	"author": "6EDC6101F0B64156ED867BAE925F6CD240635656",
	"archetypes": [
		{
			"name": "Archetype 1",
			"address": "4156ED867BAE4156ED867BAE925F6CD240635656"
		},
		{
			"name": "Archetype 2",
			"address": "406356867BAE4156ED867BAE925F6CD240635656"
		}
	]
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| id | String | <p>Archetype Package id</p>|
| name | String | <p>Human readable name of the Archetype Package</p>|
| description | String | <p>Human readable description of the Archetype Package</p>|
| author | String | <p>Controller contract of the user or organization</p>|
| archetypes | Object[] | <p>Array of archetypes with name and address pairs that created the Archetype Package</p>|




### Read Archetype Packages

<p>Retrieves archetype package information. Within the Agreements Network, Archetype Packages are collections of archetypes that are related in some way.</p>

```endpoint
GET /archetypes
```







#### Example Requests


```curl
curl -i /archetype-packages
```


#### Success Response

Success Objects Array

```json
[
 {
  "id": "7F2CA849A318E7FA2473B3442B7AC86A84DD3AA054F567BCF5D27D9622FCD0BD",
  "name": "Package1",
  "author": "6EDC6101F0B64156ED867BAE925F6CD240635656"
 }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| id | String | <p>Archetype Package id</p>|
| name | String | <p>Human readable name of the Archetype Pacakge</p>|
| author | String | <p>Controller contract of the user or organization that created the package</p>|




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
  "numberOfParameters": 2,
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
| numberOfParameters | Number | <p>The number of custom parameters used by the Archetype</p>|
| numberOfDocuments | Number | <p>The number of documents registered against the Archetype</p>|
| countries | String[] | <p>The jurisdictions in which the Archetype has been registered to be active</p>|




## BPMModel

### Read All Process Definitions



```endpoint
GET /bpm/process-definitions
```







#### Example Requests


```curl
curl -i /bpm/process-definitions
curl -i /bpm/process-definitions?interfaceId=Default%20Formation%20Process
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Single Process Definition



```endpoint
GET /bpm/process-definitions/:address
```







#### Example Requests


```curl
curl -i /bpm/process-definitions/81A817870C6C6A209150FA26BC52D835CA6E17D2
```


#### Success Response

Success Object

```json
{
    "modelAddress":"912A82D4C72847EF1EC76426544EAA992993EE20",
    "processDefinitionAddress":"81A817870C6C6A209150FA26BC52D835CA6E17D2",
    "id":"defaultFormationProcess",
    "name":"Default Formation Process",
    "interfaceId":"Agreement Formation",
    "diagramAddress":"7D85BB76DB402B752F84792FF50B40483922673CF277CD2045D3D9637D4CE8F9",
    "diagramSecret":"4AF3A863BF6F2AD79E4919F562252866CBDA58E3E5AA27E2C5C94BAE9931BE74"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| modelAddress | String | <p>Address of the model the process definition was created under</p>|
| processDefinitionAddress | String | <p>Address of the process definition</p>|
| id | String | <p>Id of the process definition</p>|
| name | String | <p>Human-readable name of the process definition</p>|
| interfaceId | String | <p>'Agreement Formation' or 'Agreement Execution'</p>|
| diagramAddress | String | <p>Hoard address for the xml file representing the process</p>|
| diagramSecret | String | <p>Hoard secret for the xml file representing the process</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Diagram of Process Model

<p>Reads the diagram of the specified process model in the requested MIME type. The 'Accept' header in the request should be set to either 'application/xml' or 'application/json'.</p>

```endpoint
GET /bpm/process-models/:address/diagram
```







#### Example Requests


```curl
curl -i -H "Accept: application/json" /bpm/process-models/912A82D4C72847EF1EC76426544EAA992993EE20/diagram
```


#### Success Response

Success Object

```json
[
    {
        "id":"Process_1rywjij",
        "name":"Process Name",
        "interface":"Agreement Formation",
        "participants":[{
            "id":"Lane_1mjalez",
            "name":"Assignee",
            "tasks":[
                "Task Name"
            ],
            "conditionalPerformer":true,
            "dataStorageId":"agreement",
            "dataPath":"Assignee"
        }],
        "tasks":[],
        "userTasks":[{
            "id":"Task Name",
            "name":"Task Name",
            "assignee":"Lane_1mjalez",
            "activityType":0,
            "taskType":1,
            "behavior":1,
            "multiInstance":false,
            "application":"",
            "subProcessModelId":"",
            "subProcessDefinitionId":""
        }],
        "sendTasks":[],
        "receiveTasks":[],
        "serviceTasks":[],
        "subProcesses":[],
        "transitions":[]
    }
]
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| object | Object[] | <p>Object representing the process definition</p>|
| id | String | <p>Id of the process definition</p>|
| name | String | <p>Human-readable name of the process definition</p>|
| interface | String | <p>'Agreement Formation' or 'Agreement Execution'</p>|
| participants | Array | <p>Array of participant objects</p>|
| tasks | Array | <p>Array of task objects</p>|
| userTasks | Array | <p>Array of user tasks</p>|
| sendTasks | Array | <p>Array of send tasks</p>|
| receiveTasks | Array | <p>Array of receive tasks</p>|
| serviceTasks | Array | <p>Array of service tasks</p>|
| subProcesses | Array | <p>Array of subprocesses</p>|
| transitions | Array | <p>Array of transitions</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Process Models



```endpoint
GET /bpm/process-models
```







#### Example Requests


```curl
curl -iX GET /bpm/process-models
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## BPMModel_BPMN_XML_needs_to_be_passed_in_the_request_body_as_plain_text_or_application_xml

### Parse BPMN XML and from it create a process model and definition



```endpoint
POST /bpm/process-models
```







#### Example Requests


```curl
curl -i /bpm/process-models
curl -i /bpm/process-models?format=bpmn
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## BPMRuntime

### Complete task identified by the activityInstanceId

<p>Completes the activity identified by the activityInstanceId.</p>

```endpoint
PUT /tasks/:activityInstanceId/complete
```







#### Example Requests


```curl
curl -i /task/:activityInstanceId/complete
```






### Read Activities

<p>Read all activities.</p>

```endpoint
GET /activity-instances
```







#### Example Requests


```curl
curl -i /activity-instances?processInstance=150D431B160790B2462D8CC683C87FEA2F1C3C61
```





#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Tasks

<p>Retrieves an array of tasks assigned to the logged in user</p>

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


## Content

### Read Content Object



```endpoint
GET /hoard
```







#### Example Requests


```curl
curl -i /hoard
```






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


#### Success Response

Success-Response:

```json
{
	"address": "6EDC6101F0B64156ED867BAE925F6CD240635656"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| The | json | <p>address of the created Organization</p>|



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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Removes a user from Organization



```endpoint
DELETE /organizations/:orgId/users/:userAddress
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
PUT /organizations/:orgId/users/:userAddress
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

### Sign the agreement and complete the activity

<p>Signs the agreement at the given address and then completes the activity identified by the activityInstanceId.</p>

```endpoint
PUT /tasks/:activityInstanceId/complete/:agreementAddress/sign
```







#### Example Requests


```curl
curl -i /tasks/:activityInstanceId/complete/:agreementAddress/sign
```






## StaticData

### Read Countries



```endpoint
GET /static-data/iso/countries
```







#### Example Requests


```curl
curl -i /static-data/iso/countries
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Country

<p>Retrieves the country whose <code>alpha2</code> code matches the one passed as parameter.</p>

```endpoint
GET /static-data/iso/countries/:alpha2
```







#### Example Requests


```curl
curl -i /static-data/iso/countries/:alpha2
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Currencies



```endpoint
GET /static-data/iso/currencies
```







#### Example Requests


```curl
curl -i /static-data/iso/currencies
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Currency

<p>Retrieves the currency whose <code>alpha3</code> code matches the one passed as parameter.</p>

```endpoint
GET /static-data/iso/currencies/:alpha3
```







#### Example Requests


```curl
curl -i /static-data/iso/currencies/:alpha3
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read Parameter Types



```endpoint
GET /static-data/parameter-types
```







#### Example Requests


```curl
curl -i /static-data/parameter-types
```


#### Success Response

Success Objects Array

```json
[
    {"parameterType": 0, "label": "Boolean"},
    {"parameterType": 1, "label": "String"},
    {"parameterType": 2, "label": "Number"},
    {"parameterType": 3, "label": "Date"},
    {"parameterType": 4, "label": "Monetary Amount"},
    {"parameterType": 5, "label": "User/Organization"},
    {"parameterType": 6, "label": "Contract Address"},
    {"parameterType": 7, "label": "Signing Party"}
]
```




#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Read a Country&#39;s Regions

<p>Retrieves an array of regions belonging to the country whose <code>alpha2</code> code matches the one passed as parameter. Note that a region may have its <code>code2</code> OR <code>code3</code> property populated, NOT both. Thus to represent regions in the UI dropdown, we can use <code>&lt;alpha2&gt;-&lt;code2 or code3&gt;</code> followed by the name.</p>

```endpoint
GET /static-data/iso/countries/:alpha2/regions
```







#### Example Requests


```curl
curl -i /static-data/iso/countries/:alpha2/regions
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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


## Users

### Update User Profile of currently logged in user

<p>Updates a single users profile identified by the access token.</p>

```endpoint
PUT /users/profile
```







#### Example Requests


```curl
curl -iX PUT /users/profile
```


#### Success Response

Success Object

```json
{
	"address": "605401BB8B9E597CC40C35D1F0185DE94DBCE533",
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Users's Controller Contract</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Log out a User



```endpoint
POST /users/logout
```







#### Example Requests


```curl
curl -iX PUT /users/logout
```






### Request password reset for a user account

<p>Sends an email with a password recovery code to the given email address</p>

```endpoint
POST /users/password-recovery
```







#### Example Requests


```curl
curl -iX POST /users/password-recovery
```






### Read User Profile of currently logged in user

<p>Retrieves a single users profile identified by the access token.</p>

```endpoint
GET /users/profile
```







#### Example Requests


```curl
curl -i /users/profile
```


#### Success Response

Success Object

```json
			 {
			  "address": "9F24307DA7E74BC54D1E829764E2DE7AD0D8DF6E",
			  "id": "j.smith",
			  "email": "jsmith@monax.io",
			  "organization": "707791D3BBD4FDDE615D0EC4BB0EB3D909F66890",
			  "organizationId": "acmecorp92",
			  "organizationName": "ACME Corp",
			  "firstName": "Joe",
 			  "lastName": "Smith",
			  "country": "CA",
			  "region": "1232SDFF3EC680332BEFDDC3CA12CBBD",
			  "isProducer": false,
			  "onboarding": true,
			  "createdAt": ""
			 }
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>Users's Controller Contract</p>|
| id | String | <p>Users's human readable ID</p>|
| email | String | <p>Users's email address</p>|
| organization | String | <p>Organization's Controller Contract</p>|
| organizationId | String | <p>Organization's machine readable ID</p>|
| organizationName | String | <p>Organization's human readable name</p>|
| firstName | String | <p>User's first name</p>|
| lastName | String | <p>User's last name</p>|
| country | String | <p>User's country code</p>|
| region | String | <p>Contract address of user's region</p>|
| isProducer | Boolean | <p>Boolean representing whether user account is producer type (as opposed to consumer type)</p>|
| onboarding | Boolean | <p>Boolean representing whether user prefers to see onboarding screens</p>|
| createdAt | String | <p>Timestamp of user account creation</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


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



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Create a New User

<p>Creating a new user</p>

```endpoint
POST /users
```







#### Example Requests


```curl
curl -iX POST /users
```


#### Success Response

Success Object

```json
{
	"address": "605401BB8B9E597CC40C35D1F0185DE94DBCE533",
	"id": "johnsmith"
}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| userData | Object | <p>The &quot;address&quot; and &quot;id&quot; of the User</p>|



#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


### Reset password for user account

<p>Resets the user's password with the given password, if the recovery code is valid</p>

```endpoint
PUT /users/password-recovery/:recoveryCode
```







#### Example Requests


```curl
curl -iX PUT /users/password-recovery/vdk7bd2esdf3234...
```






### Log in as a User



```endpoint
POST /users/login
```







#### Example Requests


```curl
curl -iX PUT /users/login
```


#### Success Response

Success Object

```json
 {
		"address": "41D6BC9143DF87A07F65FCAF642FB89E16D26548",
		"id": "jsmith",
		"createdAt": "2018-06-25T13:44:26.925Z"
	}
```


#### Success 200

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| address | String | <p>The address of the user</p>|
| id | String | <p>The id (username) of the user</p>|
| A | String | <p>timestamp of the account creation</p>|




### Validates the given password recovery code

<p>Checks if the given password recovery code is valid</p>

```endpoint
GET /users/password-recovery/:recoveryCode
```







#### Example Requests


```curl
curl -iX GET /users/password-recovery/vdk7bd2esdf3234...
```






### Validate user token

<p>This route validates the JWT <code>access_token</code> which should be set as cookie in the request</p>

```endpoint
GET /users/token/validate
```







#### Example Requests


```curl
curl -iX GET /users/token/validate
```


#### Success Response

Success Object

```json
 {
		"address": "41D6BC9143DF87A07F65FCAF642FB89E16D26548",
		"id": "jsmith",
	}
```




#### Error 4xx

| Name     | Type       | Description                           |
|:---------|:-----------|:--------------------------------------|
| NotLoggedIn |  | <p>The user making the request does not have a proper authentication token.</p>|


