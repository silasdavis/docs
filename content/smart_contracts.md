## Agreements Network Contracts


Here's a description


## AbstractDocument


The AbstractDocument contract is found within the documents-commons bundle.

### AbstractDocument >> addVersion(string)


Adds the specified hash as a new version of the document. The msg.sender is registered as owner and the version creation date is set to now.

```endpoint
CALL addVersion(string)
```

#### Parameters

```solidity
_hash // the version hash

```

#### Return

```json
BaseErrors.NO_ERROR, BaseErrors.INSUFFICIENT_PRIVILEGES (as determined by calling canAddVersion(), or BaseErrors.RESOURCE_ALREADY_EXISTS if the version has been added before.
```

### AbstractDocument >> getName()


Returns the document's name

```endpoint
CALL getName()
```

### AbstractDocument >> getNumberOfVersions()


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```

### AbstractDocument >> getVersionCreated(string)


Returns the creation date of the specified version hash.

```endpoint
CALL getVersionCreated(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creation date, or 0 if the version does not exist
```

### AbstractDocument >> getVersionCreator(string)


Returns the address registered as the creator of the specified version hash.

```endpoint
CALL getVersionCreator(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creator address, or 0x0 if the version does not exist
```

## AbstractEventListener


The AbstractEventListener contract is found within the bpm-model bundle.

### AbstractEventListener >> eventFired(bytes32,address)


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```

### AbstractEventListener >> eventFired(bytes32,address,address)


Invoked by an EventEmitter for a named event with an additional address payload.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### AbstractEventListener >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### AbstractEventListener >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### AbstractEventListener >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

## AbstractNamedElement


The AbstractNamedElement contract is found within the bpm-model bundle.

### AbstractNamedElement >> getId()


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### AbstractNamedElement >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

## AccountsManager Interface


The AccountsManager Interface contract is found within the commons-auth bundle.

### AccountsManager Interface >> addBusinessAccount(address)


Adds the specified BusinessAccount

```endpoint
CALL addBusinessAccount(address)
```

#### Return

```json
an error code
```

### AccountsManager Interface >> addFunds(address,bytes32,uint256)


Adds the specified fund amount to the specified organization's business account.

```endpoint
CALL addFunds(address,bytes32,uint256)
```

#### Parameters

```solidity
_funds // the amount to add
_name // the business account name
_organization // the organization's address

```

#### Return

```json
error code
```

### AccountsManager Interface >> addUserAccount(address)


Adds the specified UserAccount

```endpoint
CALL addUserAccount(address)
```

#### Return

```json
an error code
```

### AccountsManager Interface >> addUserToOrganization(address,address)


Associates the given user with the specified organization.

```endpoint
CALL addUserToOrganization(address,address)
```

#### Parameters

```solidity
_organization // the organization
_userAccount // the user

```

#### Return

```json
error code indicating success or failure
```

### AccountsManager Interface >> businessAccountExists(address,bytes32)


Indicates whether the specified business account exists for the given organization ID

```endpoint
CALL businessAccountExists(address,bytes32)
```

#### Parameters

```solidity
_name // businessAccount name
_organization // the organization's address

```

#### Return

```json
bool exists
```

### AccountsManager Interface >> createUserAccount(address,bytes32,bytes32)


Creates and adds a user account

```endpoint
CALL createUserAccount(address,bytes32,bytes32)
```

#### Parameters

```solidity
_id // id (optional)
_owner // owner (optional)
_secret // secret

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RUNTIME_ERROR() if a runtime erroruserAccount user account
```

### AccountsManager Interface >> getBusinessAccount(address,bytes32)


Returns the business account address for the specified organization ID and business account name.

```endpoint
CALL getBusinessAccount(address,bytes32)
```

#### Parameters

```solidity
_name // businessAccount name
_organization // the organization's address

```

#### Return

```json
(error, address)
```

### AccountsManager Interface >> getBusinessAccount(bytes32)


Returns the business account address for the specified business account ID.

```endpoint
CALL getBusinessAccount(bytes32)
```

### AccountsManager Interface >> getUserAccount(bytes32)


Returns the user account address for the specified user account ID.

```endpoint
CALL getUserAccount(bytes32)
```

### AccountsManager Interface >> removeUserFromOrganization(address,address)


Removes (deactivates) the given user from the specified organization.

```endpoint
CALL removeUserFromOrganization(address,address)
```

#### Parameters

```solidity
_organization // the organization
_userAccount // the user

```

#### Return

```json
error code indicating success or failure
```

### AccountsManager Interface >> userAccountExists(bytes32)


Indicates whether the specified user account exists for the given userAccount ID

```endpoint
CALL userAccountExists(bytes32)
```

#### Parameters

```solidity
_id // userAccount ID

```

#### Return

```json
bool exists
```

### AccountsManager Interface >> withdrawFunds(address,bytes32,uint256)


Subtracts the specified fund amount to the specified organization's business account.

```endpoint
CALL withdrawFunds(address,bytes32,uint256)
```

#### Parameters

```solidity
_funds // the amount to withdraw
_name // the business account name
_organization // the organization's address

```

#### Return

```json
error code
```

## ActiveAgreement Interface


The ActiveAgreement Interface contract is found within the agreements bundle.

### ActiveAgreement Interface >> getArchetype()


Returns the archetype

```endpoint
CALL getArchetype()
```

#### Return

```json
the archetype address
```

### ActiveAgreement Interface >> getCreator()


Returns the creator

```endpoint
CALL getCreator()
```

#### Return

```json
the creator

```

### ActiveAgreement Interface >> getHoardAddress()


Returns the Hoard Address

```endpoint
CALL getHoardAddress()
```

#### Return

```json
the Hoard Address

```

### ActiveAgreement Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### ActiveAgreement Interface >> getNumberOfParties()


Gets number of parties

```endpoint
CALL getNumberOfParties()
```

#### Return

```json
size number of parties
```

### ActiveAgreement Interface >> getParty(uint256)


Gets party

```endpoint
CALL getParty(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index out of boundsparty party
```

### ActiveAgreement Interface >> gethoardSecret()


Returns the Hoard Secret

```endpoint
CALL gethoardSecret()
```

#### Return

```json
the Hoard Secret
```

### ActiveAgreement Interface >> isPrivate()


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
the private flag 
```

### ActiveAgreement Interface >> setName(bytes32)


Sets name

```endpoint
CALL setName(bytes32)
```

#### Parameters

```solidity
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR()
```

## ActiveAgreementRegistry Interface


The ActiveAgreementRegistry Interface contract is found within the agreements bundle.

### ActiveAgreementRegistry Interface >> create(address,bytes32,address,bytes32,bytes32,bool,address[])


Creates an Active Agreement with the given parameters

```endpoint
CALL create(address,bytes32,address,bytes32,bytes32,bool,address[])
```

#### Parameters

```solidity
_archetype // archetype
_name // name
_parties // parties

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if _name is null, or BaseErrors.RUNTIME_ERROR() if runtime errora return code indicating success or failure and the new activeAgreement's address, if successfully created
```

### ActiveAgreementRegistry Interface >> getActiveAgreementAtIndex(uint256)


Gets activeAgreement address at given index

```endpoint
CALL getActiveAgreementAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
the Active Agreement address
```

### ActiveAgreementRegistry Interface >> getActiveAgreementData(address)


Returns data about the Active Agreement at the specified address

```endpoint
CALL getActiveAgreementData(address)
```

#### Parameters

```solidity
activeAgreement // activeAgreement

```

#### Return

```json
archetype archetypename name
```

### ActiveAgreementRegistry Interface >> getActiveAgreementsSize()


Gets number of activeAgreements

```endpoint
CALL getActiveAgreementsSize()
```

#### Return

```json
size size
```

### ActiveAgreementRegistry Interface >> getPartiesByActiveAgreementSize(address)


Gets parties size for given Active Agreement

```endpoint
CALL getPartiesByActiveAgreementSize(address)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement

```

#### Return

```json
size size
```

### ActiveAgreementRegistry Interface >> getPartyByActiveAgreementAtIndex(address,uint256)


Gets getPartyByActiveAgreementAtIndex

```endpoint
CALL getPartyByActiveAgreementAtIndex(address,uint256)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement
_index // index

```

#### Return

```json
party party
```

### ActiveAgreementRegistry Interface >> getPartyByActiveAgreementData(address,address)


Returns data about the party at the specified address. Placeholder function due to SQLSOL requirements.

```endpoint
CALL getPartyByActiveAgreementData(address,address)
```

#### Parameters

```solidity
_activeAgreement // active agreement
_party // party

```

#### Return

```json
bool placeholder
```

### ActiveAgreementRegistry Interface >> setName(address,bytes32)


Sets name for given Active Agreement

```endpoint
CALL setName(address,bytes32)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RUNTIME_ERROR() if runtime error
```

## Agreement


The Agreement contract is found within the documents-commons bundle.

### Agreement >> addSignatories(address[])


Adds the specified signatories to this agreement, if they are valid, and returns the number of added signatories. Empty addresses and already registered signatories are rejected.

```endpoint
CALL addSignatories(address[])
```

#### Parameters

```solidity
_addresses // the signatories

```

#### Return

```json
the number of added signatories
```

### Agreement >> addSignatory(address)


Adds a single signatory to this agreement

```endpoint
CALL addSignatory(address)
```

#### Parameters

```solidity
_address // the address to add

```

#### Return

```json
NO_ERROR, INVALID_PARAM_VALUE if address is empty, RESOURCE_ALREADY_EXISTS if address has already been registered
```

### Agreement >> addVersion(string)


Adds the specified hash as a new version of the document. The msg.sender is registered as owner and the version creation date is set to now.

```endpoint
CALL addVersion(string)
```

#### Parameters

```solidity
_hash // the version hash

```

#### Return

```json
BaseErrors.NO_ERROR, BaseErrors.INSUFFICIENT_PRIVILEGES (as determined by calling canAddVersion(), or BaseErrors.RESOURCE_ALREADY_EXISTS if the version has been added before.
```

### Agreement >> confirmExecutionVersion(string)


Registers the msg.sender as having confirmed/endorsed the specified document version as the execution version.

```endpoint
CALL confirmExecutionVersion(string)
```

#### Parameters

```solidity
_version // the version

```

#### Return

```json
BaseErrors.NO_ERROR(), BaseErrors.INVALID_PARAM_VALUE() if given version is empty, or BaseErrors.RESOURCE_NOT_FOUND() if the version does not exist
```

### Agreement >> getConfirmedVersion()


Returns the confirmed version of this agreement, if it has been set.

```endpoint
CALL getConfirmedVersion()
```

### Agreement >> getEndorsedVersion(address)


Get the document version endorsed by the specified signatory.

```endpoint
CALL getEndorsedVersion(address)
```

#### Parameters

```solidity
_signatory // the signatory

```

#### Return

```json
the version hash, if an endorsed version exists, or an uninitialized string
```

### Agreement >> getName()


Returns the document's name

```endpoint
CALL getName()
```

### Agreement >> getNumberOfVersions()


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```

### Agreement >> getSignatoriesSize()


Returns the number of signatories of this agreement.

```endpoint
CALL getSignatoriesSize()
```

#### Return

```json
the number of signatories
```

### Agreement >> getVersionCreated(string)


Returns the creation date of the specified version hash.

```endpoint
CALL getVersionCreated(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creation date, or 0 if the version does not exist
```

### Agreement >> getVersionCreator(string)


Returns the address registered as the creator of the specified version hash.

```endpoint
CALL getVersionCreator(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creator address, or 0x0 if the version does not exist
```

### Agreement >> isConfirmedVersion(string)


Verify if the specified version hash is the confirmed version.

```endpoint
CALL isConfirmedVersion(string)
```

#### Parameters

```solidity
_version // the version

```

#### Return

```json
true if the version matches the confirmed one, false otherwise
```

### Agreement >> isEffective()


Returns whether this agreement is effective or not

```endpoint
CALL isEffective()
```

### Agreement >> isFullyConfirmed(string)


Determines if the submitted version has been signed by all signatories.

```endpoint
CALL isFullyConfirmed(string)
```

#### Parameters

```solidity
_version // the version

```

#### Return

```json
true if all configured signatories have signed that version, false otherwise
```

## Archetype Interface


The Archetype Interface contract is found within the agreements bundle.

### Archetype Interface >> activate()


Activates this archetype

```endpoint
CALL activate()
```

#### Return

```json
error code indicating success or failure
```

### Archetype Interface >> addCustomField(uint8,bytes32)


Adds a custom field with the specified type and name to the archetype

```endpoint
CALL addCustomField(uint8,bytes32)
```

#### Parameters

```solidity
_customField // customField
_dataType // data type (enum)

```

#### Return

```json
error code indicating success or failure
```

### Archetype Interface >> addDocument(bytes32,bytes32,bytes32)


Adds the document specified by the given parameters to the archetype

```endpoint
CALL addDocument(bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_hoardAddress // hoard address
_name // name
_secretKey // secret key

```

#### Return

```json
error code indicating success or failure
```

### Archetype Interface >> addJurisdiction(bytes2,bytes32)


Adds the given jurisdiction in the form of a country code and region identifier to this archetype. References codes defined via IsoCountries interface implementations.

```endpoint
CALL addJurisdiction(bytes2,bytes32)
```

#### Parameters

```solidity
_country // a ISO- code, e.g. 'US'
_region // a region identifier from a IsoCountries contract

```

#### Return

```json
error code indicating success or failure
key of the jurisdiction just added
```

### Archetype Interface >> deactivate()


Deactivates this archetype

```endpoint
CALL deactivate()
```

#### Return

```json
error code indicating success or failure
```

### Archetype Interface >> getAuthor()


Gets Author

```endpoint
CALL getAuthor()
```

#### Return

```json
author author
```

### Archetype Interface >> getCustomFieldAtIndex(uint256)


Gets custom field at index

```endpoint
CALL getCustomFieldAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error error TBDcustomField custom field
```

### Archetype Interface >> getCustomFieldDataType(bytes32)


Gets custom field data type

```endpoint
CALL getCustomFieldDataType(bytes32)
```

#### Parameters

```solidity
_customField // custom field

```

#### Return

```json
error error TBDdataType data type
```

### Archetype Interface >> getDescription()


Gets description

```endpoint
CALL getDescription()
```

#### Return

```json
description
```

### Archetype Interface >> getDocument(bytes32)


Gets document with given name

```endpoint
CALL getDocument(bytes32)
```

#### Parameters

```solidity
_name // document name

```

#### Return

```json
externalContent external content
```

### Archetype Interface >> getDocumentAtIndex(uint256)


Gets document name at index

```endpoint
CALL getDocumentAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index is out of boundsname
```

### Archetype Interface >> getExecutionProcessDefinition()


Returns the address of the ProcessDefinition that orchestrates the agreement execution.

```endpoint
CALL getExecutionProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### Archetype Interface >> getFormationProcessDefinition()


Returns the address of the ProcessDefinition that orchestrates the agreement formation.

```endpoint
CALL getFormationProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### Archetype Interface >> getJurisdictionAtIndex(uint256)


Retrieves the key for the jurisdiction at the specified index

```endpoint
CALL getJurisdictionAtIndex(uint256)
```

#### Parameters

```solidity
_index // the index position

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index is out of boundsthe key of the jurisdiction or an empty bytes32 if the index was out of bounds
```

### Archetype Interface >> getJurisdictionData(bytes32)


Returns information about the jurisdiction with the specified key

```endpoint
CALL getJurisdictionData(bytes32)
```

#### Parameters

```solidity
_key // the key identifying the jurisdiction

```

#### Return

```json
the country and region identifiers (see IsoCountries), if the jurisdiction exists
```

### Archetype Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### Archetype Interface >> getNumberOfCustomFields()


Gets number of custom fields

```endpoint
CALL getNumberOfCustomFields()
```

#### Return

```json
size number of custom fields
```

### Archetype Interface >> getNumberOfDocuments()


Gets number of documents

```endpoint
CALL getNumberOfDocuments()
```

#### Return

```json
size number of documents
```

### Archetype Interface >> getNumberOfJurisdictions()


Returns the number jurisdictions for this archetype

```endpoint
CALL getNumberOfJurisdictions()
```

#### Return

```json
the number of jurisdictions
```

### Archetype Interface >> isActive()


Returns the active state

```endpoint
CALL isActive()
```

#### Return

```json
true if active, false otherwise
```

### Archetype Interface >> isPrivate()


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
true if private, false otherwise
```

## ArchetypeRegistry Interface


The ArchetypeRegistry Interface contract is found within the agreements bundle.

### ArchetypeRegistry Interface >> activate(address)


Sets active to true for given archetype

```endpoint
CALL activate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### ArchetypeRegistry Interface >> addDocument(address,bytes32,bytes32,bytes32)


Adds Hoard document to the given Archetype

```endpoint
CALL addDocument(address,bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_hoardAddress // hoard address
_name // name
_secretKey // secret key

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() _archetype does not exist, or see DefaultArchetype
```

### ArchetypeRegistry Interface >> addField(address,uint8,bytes32)


Adds the specified custom field to the archetype

```endpoint
CALL addField(address,uint8,bytes32)
```

#### Parameters

```solidity
_customField // customField
_dataType // data type (enum)

```

#### Return

```json
a return code indicating success or failure
```

### ArchetypeRegistry Interface >> addFields(address,uint8[],bytes32[])


Adds the specified custom field to the archetype

```endpoint
CALL addFields(address,uint8[],bytes32[])
```

#### Parameters

```solidity
_customFields // customField
_dataTypes // data type (enum)

```

#### Return

```json
a return code indicating success or failure
```

### ArchetypeRegistry Interface >> addJurisdiction(address,bytes2,bytes32)


Adds the given jurisdiction in the form of a country code and region identifier to this archetype. References codes defined via IsoCountries interface implementations.

```endpoint
CALL addJurisdiction(address,bytes2,bytes32)
```

#### Parameters

```solidity
_country // a ISO- code, e.g. 'US'
_region // a region identifier from a IsoCountries contract

```

#### Return

```json
a return code indicating success or failure
```

### ArchetypeRegistry Interface >> addJurisdictions(address,bytes2[],bytes32[])


Adds the given jurisdictions in the form of a country codes and region identifiers to this archetype. References codes defined via IsoCountries interface implementations.

```endpoint
CALL addJurisdictions(address,bytes2[],bytes32[])
```

#### Parameters

```solidity
_countries // an array of a ISO- code, e.g. 'US'
_regions // an array of region identifiers from a IsoCountries contract

```

#### Return

```json
a return code indicating success or failure
```

### ArchetypeRegistry Interface >> create(bytes32,address,string,bool,address,address)


Creates a archetype with the given parameters

```endpoint
CALL create(bytes32,address,string,bool,address,address)
```

#### Parameters

```solidity
_author // author
_description // description
_executionProcess // the address of a ProcessDefinition that orchestrates the agreement execution
_formationProcess // the address of a ProcessDefinition that orchestrates the agreement formation
_isPrivate // determines if the archetype's documents are encrypted
_name // name

```

#### Return

```json
error - a return code indicating success or failurearchetype - the new archetype's address, if successfully created
```

### ArchetypeRegistry Interface >> deactivate(address)


Sets active to false for given archetype

```endpoint
CALL deactivate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### ArchetypeRegistry Interface >> getArchetypeAtIndex(uint256)


Gets archetype address at given index

```endpoint
CALL getArchetypeAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
the archetype address
```

### ArchetypeRegistry Interface >> getArchetypeData(address)


Returns data about the archetype at the specified address

```endpoint
CALL getArchetypeData(address)
```

#### Parameters

```solidity
_archetype // the archetype's address

```

#### Return

```json
name namedescription descriptionauthor authorformationProcessDefinitionexecutionProcessDefinition
```

### ArchetypeRegistry Interface >> getArchetypesSize()


Gets number of archetypes

```endpoint
CALL getArchetypesSize()
```

#### Return

```json
size size
```

### ArchetypeRegistry Interface >> getDocumentByArchetypeAtIndex(address,uint256)


Gets document name by Archetype At index

```endpoint
CALL getDocumentByArchetypeAtIndex(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype
_index // index

```

#### Return

```json
name name
```

### ArchetypeRegistry Interface >> getDocumentByArchetypeData(address,bytes32)


Returns data about the document given the specified name

```endpoint
CALL getDocumentByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
hoardAddress hoard addresssecretKey secret key
```

### ArchetypeRegistry Interface >> getDocumentsByArchetypeSize(address)


Gets documents size for given Archetype

```endpoint
CALL getDocumentsByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```

### ArchetypeRegistry Interface >> getFieldByArchetypeAtIndex(address,uint256)


Gets field name by Archetype At index

```endpoint
CALL getFieldByArchetypeAtIndex(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype
_index // index

```

#### Return

```json
name name
```

### ArchetypeRegistry Interface >> getFieldByArchetypeData(address,bytes32)


Returns data about the field at with the specified name

```endpoint
CALL getFieldByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
dataType data type
```

### ArchetypeRegistry Interface >> getFieldsByArchetypeSize(address)


Gets fields size for given Archetype

```endpoint
CALL getFieldsByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```

### ArchetypeRegistry Interface >> getJurisdictionAtIndexForArchetype(address,uint256)


Returns the jurisdiction key at the specified index for the given archetype

```endpoint
CALL getJurisdictionAtIndexForArchetype(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype address
_index // the index of the jurisdiction

```

#### Return

```json
the jurisdiction primary key
```

### ArchetypeRegistry Interface >> getJurisdictionDataForArchetype(address,bytes32)


Returns data about the jurisdiction with the specified key in the given archetype

```endpoint
CALL getJurisdictionDataForArchetype(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype address
_key // the jurisdiction key

```

#### Return

```json
country the jurisdiction's countryregion the jurisdiction's region
```

### ArchetypeRegistry Interface >> getNumberOfJurisdictionsForArchetype(address)


Returns the number of jurisdictions for the given Archetype

```endpoint
CALL getNumberOfJurisdictionsForArchetype(address)
```

#### Parameters

```solidity
_archetype // archetype address

```

#### Return

```json
the number of jurisdictions
```

## ArrayUtils Library Interface


The ArrayUtils Library Interface contract is found within the agreements bundle.

### ArrayUtils Library Interface >> contains(address[],address)


Returns whether the specified value is present in the given array

```endpoint
CALL contains(address[],address)
```

#### Parameters

```solidity
_list // the array
_value // the value

```

#### Return

```json
true if the value is found in the array, false otherwise
```

### ArrayUtils Library Interface >> contains(bytes32[],bytes32)


Returns whether the specified value is present in the given array

```endpoint
CALL contains(bytes32[],bytes32)
```

#### Parameters

```solidity
_list // the array
_value // the value

```

#### Return

```json
true if the value is found in the array, false otherwise
```

### ArrayUtils Library Interface >> contains(int256[],int256)


Returns whether the specified value is present in the given array

```endpoint
CALL contains(int256[],int256)
```

#### Parameters

```solidity
_list // the array
_value // the value

```

#### Return

```json
true if the value is found in the array, false otherwise
```

### ArrayUtils Library Interface >> contains(uint256[],uint256)


Returns whether the specified value is present in the given array

```endpoint
CALL contains(uint256[],uint256)
```

#### Parameters

```solidity
_list // the array
_value // the value

```

#### Return

```json
true if the value is found in the array, false otherwise
```

## AuthorizationsManager


The AuthorizationsManager contract is found within the commons-auth bundle.

### AuthorizationsManager >> addRole(bytes32,address,bytes32)


Adds a role to an account in a `AuthorizationsRepository`

```endpoint
CALL addRole(bytes32,address,bytes32)
```

#### Parameters

```solidity
_account // account
_repository // AuthorizationsRepository
_role // role

```

#### Return

```json
error NO_ERROR, RESOURCE_ERROR, or RESOURCE_NOT_FOUND
```

### AuthorizationsManager >> getRepository(bytes32)


Returns the address of the repository with the specified key, if it exists

```endpoint
CALL getRepository(bytes32)
```

#### Parameters

```solidity
_key // the repository identifier

```

#### Return

```json
the address or 0x0, if the repository does not exist
```

### AuthorizationsManager >> hasRole(address,bytes32)


Indicates whether an account has a role in any known `AuthorizationsRepository`

```endpoint
CALL hasRole(address,bytes32)
```

#### Parameters

```solidity
_account // account
_role // role

```

#### Return

```json
true if the role-account association can be found in a registered repository, false otherwise
```

### AuthorizationsManager >> removeRole(bytes32,address,bytes32)


Removes a role from an account in a `AuthorizationsRepository`

```endpoint
CALL removeRole(bytes32,address,bytes32)
```

#### Parameters

```solidity
_account // account
_repository // AuthorizationsRepository
_role // role

```

#### Return

```json
error NO_ERROR, RESOURCE_ERROR, or RESOURCE_NOT_FOUND
```

## AuthorizationsRepository Interface


The AuthorizationsRepository Interface contract is found within the commons-auth bundle.

### AuthorizationsRepository Interface >> addRole(address,bytes32)


This function associates the given address with the specified role in the implementing repository. The function should return an error code indicating success or failure.

```endpoint
CALL addRole(address,bytes32)
```

### AuthorizationsRepository Interface >> hasRole(address,bytes32)


This function allows detection of whether the given address is associated with the specified role in the implementing repository.

```endpoint
CALL hasRole(address,bytes32)
```

### AuthorizationsRepository Interface >> removeRole(address,bytes32)


This function disassociates the given address from the specified role in the implementing repository. The function should return an error code indicating success or failure.

```endpoint
CALL removeRole(address,bytes32)
```





## BpmApi Interface Library


The BpmApi Interface Library contract is found within the bpm-runtime bundle.

### BpmApi Interface Library >> activateAndComplete(BpmRuntime.ActivityInstance storage,ProcessDefinition)


Activates the given ActivityInstance from a suspended state (SUSPENDED or INTERRUPTED) and invokes its application.

```endpoint
CALL activateAndComplete(BpmRuntime.ActivityInstance storage,ProcessDefinition)
```

#### Parameters

```solidity
_activityInstance // the activity instance

```

#### Return

```json
error code indicating success or failure
```

### BpmApi Interface Library >> addActivity(BpmRuntime.ProcessRuntimeInstance storage,bytes32)


Adds an activity with the specified ID to the given process runtime graph.

```endpoint
CALL addActivity(BpmRuntime.ProcessRuntimeInstance storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the activity ID to add

```

### BpmApi Interface Library >> addInputArc(BpmRuntime.ProcessRuntimeInstance storage,bytes32,bytes32)


Adds an input arc to the given process runtime graph to connect from the provided activity to the provided transition.

```endpoint
CALL addInputArc(BpmRuntime.ProcessRuntimeInstance storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity from which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion to which to connect

```

### BpmApi Interface Library >> addOutputArc(BpmRuntime.ProcessRuntimeInstance storage,bytes32,bytes32)


Adds an output arc to the given process runtime graph to connect from the provided transition to the provided activity.

```endpoint
CALL addOutputArc(BpmRuntime.ProcessRuntimeInstance storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity to which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion from which to connect

```

### BpmApi Interface Library >> addTransition(BpmRuntime.ProcessRuntimeInstance storage,bytes32)


Adds a transition with the specified ID to the given process runtime graph.

```endpoint
CALL addTransition(BpmRuntime.ProcessRuntimeInstance storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the transition ID to add

```

### BpmApi Interface Library >> configure(BpmRuntime.ProcessRuntimeInstance storage,ProcessDefinition)


Configures a ProcessRuntimeIntance based on the provided ProcessDefinition. Note: Placing this function in the BpmRuntimeApi library avoids import dependencies of the runtime package by the model.

```endpoint
CALL configure(BpmRuntime.ProcessRuntimeInstance storage,ProcessDefinition)
```

#### Parameters

```solidity
_processDefinition // the process definition
_runtimeInstance // the runtime instance to configure

```

#### Return

```json
an error code indicating success or failure
```

### BpmApi Interface Library >> execute(BpmRuntime.ActivityInstance storage,BpmRuntime.ActivityRuntimeInstance storage,ProcessDefinition)


Executes the given ActivityInstance based on the information in the provided ProcessDefinition.

```endpoint
CALL execute(BpmRuntime.ActivityInstance storage,BpmRuntime.ActivityRuntimeInstance storage,ProcessDefinition)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_processDefinition // a ProcessDefinition containing information how to execute the activity

```

#### Return

```json
an error code indicating success or failure
```

### BpmApi Interface Library >> execute(BpmRuntime.ProcessRuntimeInstance storage)


Executes a single iteration of the given ProcessRuntimeInstance, i.e. it goes over all transitions and attempts to fire them based on the current token state of the graph.

```endpoint
CALL execute(BpmRuntime.ProcessRuntimeInstance storage)
```

#### Parameters

```solidity
_graph // the process runtime graph

```

#### Return

```json
the number of transitions that fired
```

### BpmApi Interface Library >> hasActivatableActivities(BpmRuntime.ProcessRuntimeInstance storage)


Determines whether the given runtime instance has any activities that are waiting to be activated.

```endpoint
CALL hasActivatableActivities(BpmRuntime.ProcessRuntimeInstance storage)
```

#### Parameters

```solidity
_runtimeInstance // the ProcessRuntimeInstance

```

#### Return

```json
true if at least one activatable activity was found, false otherwise
```

### BpmApi Interface Library >> isTransitionEnabled(BpmRuntime.ProcessRuntimeInstance storage,bytes32)


Determines whether the conditions are met to fire the provided transition.

```endpoint
CALL isTransitionEnabled(BpmRuntime.ProcessRuntimeInstance storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph containing the transition
_transitionId // the ID specifying the transition

```

#### Return

```json
true if the transitions can fire, false otherwise
```

## BpmRuntimeDb


The BpmRuntimeDb contract is found within the bpm-runtime bundle.

### BpmRuntimeDb >> addActivityInstance(bytes32)


Adds the given ActivityInstance ID to the registered activity instances. Can only be invoked by an already registered ProcessInstance. The sending ProcessInstance (msg.sender) is recorded as well.

```endpoint
CALL addActivityInstance(bytes32)
```

#### Parameters

```solidity
_id // the globally unique ID of an ActivityInstance

```

### BpmRuntimeDb >> addProcessInstance(address)


Adds the given address to the registered process instances. Can only be invoked by the owner of this BpmRuntimeDb.

```endpoint
CALL addProcessInstance(address)
```

#### Parameters

```solidity
_address // the address of a ProcessInstance

```

### BpmRuntimeDb >> getNumberOfActivityInstances()


Returns the number of registered activity instances.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```

### BpmRuntimeDb >> getNumberOfProcessInstances()


Returns the number of registered process instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the number of process instances
```

### BpmRuntimeDb >> getProcessInstanceAtIndex(uint256)


Returns the process instance address at the specified index

```endpoint
CALL getProcessInstanceAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the process instance address
```

### BpmRuntimeDb >> getProcessInstanceForActivity(bytes32)


Returns the address of the ProcessInstance of the specified ActivityInstance ID

```endpoint
CALL getProcessInstanceForActivity(bytes32)
```

#### Parameters

```solidity
_aiId // the ID of an ActivityInstance

```

#### Return

```json
the ProcessInstance address or 0x0 if it cannot be found
```

### BpmRuntimeDb >> transferSystemOwnership(address)


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```

## BpmService Interface


The BpmService Interface contract is found within the bpm-runtime bundle.

### BpmService Interface >> fireActivityUpdateEvent(address,bytes32)


Fires the UpdateActivities event to update sqlsol with given activity

```endpoint
CALL fireActivityUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_activityId // - the bytes32 Id of the activity
_piAddress // - the address of the process instance to which the activity belongs

```

### BpmService Interface >> getActivityDefinitionDetails(address,bytes32)


Gets the address of the assignee for a given activity Id and process instance address

```endpoint
CALL getActivityDefinitionDetails(address,bytes32)
```

#### Parameters

```solidity
_activityId // the activity Id
_piAddress // process instance address

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### BpmService Interface >> getActivityInstanceAtIndex(address,uint256)


Returns the ActivityInstance ID at the specified index

```endpoint
CALL getActivityInstanceAtIndex(address,uint256)
```

#### Parameters

```solidity
_address // the process instance address
_pos // the activity instance index

```

#### Return

```json
the ActivityInstance ID
```

### BpmService Interface >> getActivityInstanceData(address,bytes32)


Returns ActivityInstance data for given ActivityInstance ID

```endpoint
CALL getActivityInstanceData(address,bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance
_processInstance // the process instance address

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitioncreated - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) state - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```

### BpmService Interface >> getNumberOfActivityInstances(address)


Returns the number of activity instances.

```endpoint
CALL getNumberOfActivityInstances(address)
```

#### Return

```json
the activity instance count as size
```

### BpmService Interface >> getNumberOfProcessData(address)


Returns the number of process data entries.

```endpoint
CALL getNumberOfProcessData(address)
```

#### Return

```json
the process data size
```

### BpmService Interface >> getNumberOfProcessInstances()


Returns the number of Process Instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the process instance count as size
```

### BpmService Interface >> getProcessDataAtIndex(address,uint256)


Returns the process data ID at the specified index

```endpoint
CALL getProcessDataAtIndex(address,uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the data ID
```

### BpmService Interface >> getProcessDataDetails(address,bytes32)


Returns information about the process data entry for the specified process and data ID

```endpoint
CALL getProcessDataDetails(address,bytes32)
```

#### Parameters

```solidity
_address // the process instance
_dataId // the data ID

```

#### Return

```json
(process,id,uintValue,bytes32Value,addressValue,boolValue)
```

### BpmService Interface >> getProcessInstanceAtIndex(uint256)


Returns the process instance address at the specified index

```endpoint
CALL getProcessInstanceAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the process instance address or or BaseErrors.INDEX_OUT_OF_BOUNDS(), 0x0
```

### BpmService Interface >> getProcessInstanceData(address)


Returns information about the process intance with the specified address

```endpoint
CALL getProcessInstanceData(address)
```

#### Parameters

```solidity
_address // the process instance address

```

#### Return

```json
(processId)
```

### BpmService Interface >> getProcessInstanceForActivity(bytes32)


Returns the address of the ProcessInstance of the specified ActivityInstance ID

```endpoint
CALL getProcessInstanceForActivity(bytes32)
```

#### Parameters

```solidity
_aiId // the ID of an ActivityInstance

```

#### Return

```json
the ProcessInstance address or 0x0 if it cannot be found
```

### BpmService Interface >> getProcessModelRepository()


Gets the ProcessModelRepository address for this BpmService

```endpoint
CALL getProcessModelRepository()
```

#### Return

```json
the address of the repository
```

### BpmService Interface >> getRuntimeDb()


Returns a reference to the BpmRuntimeDb currently used by this BpmService

```endpoint
CALL getRuntimeDb()
```

#### Return

```json
the BpmRuntimeDb
```

### BpmService Interface >> getUserTaskDetails(address,bytes32)


Gets the address of the assignee for a given activity Id and process instance address

```endpoint
CALL getUserTaskDetails(address,bytes32)
```

#### Parameters

```solidity
_activityId // the activity Id
_piAddress // process instance address

```

#### Return

```json
assignee the address of the activity's assignee (for interactive activities)processId ID of the process definitionprocessName Name of the process definitionapplication the activity's application
```

### BpmService Interface >> setProcessModelRepository(address)


Sets the ProcessModelRepository for this BpmService

```endpoint
CALL setProcessModelRepository(address)
```

#### Parameters

```solidity
_repository // - the address of the repository

```

### BpmService Interface >> startProcess(bytes32,bytes32)


Registers the specified process and starts its execution.

```endpoint
CALL startProcess(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processId // the process ID

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```

## BusinessAccount Interface


The BusinessAccount Interface contract is found within the bpm-runtime bundle.

### BusinessAccount Interface >> addFunds(uint256)


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
```

#### Parameters

```solidity
_funds // the amount to add

```

### BusinessAccount Interface >> getBalance()


Returns the current balance

```endpoint
CALL getBalance()
```

#### Return

```json
the balance
```

### BusinessAccount Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### BusinessAccount Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### BusinessAccount Interface >> getOrganization()


Returns the address of the organization this business account is associated with.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization address
```

### BusinessAccount Interface >> getOwner()


Returns this account's owner

```endpoint
CALL getOwner()
```

#### Return

```json
the owner address
```

### BusinessAccount Interface >> withdrawFunds(uint256)


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```

#### Parameters

```solidity
_funds // the amount to withdraw

```

## Identifiable Interface


The Identifiable Interface contract is found within the bpm-model bundle.

### Identifiable Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

## Castable


The Castable contract is found within the commons-management bundle.

### Castable >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. 

```

### Castable >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### Castable >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
a bytes32 indicating whether the type is supported. It is recommended to return the input parameter bytes32!
```

## ChainAutorizations


The ChainAutorizations contract is found within the commons-auth bundle.

### ChainAutorizations >> addRole(address,bytes32)


Associates the given account with the specified role

```endpoint
CALL addRole(address,bytes32)
```

#### Parameters

```solidity
_account // account
_role // role

```

#### Return

```json
error NO_ERROR or RUNTIME_ERROR
```

### ChainAutorizations >> hasRole(address,bytes32)


Indicates whether the given account has the specified role

```endpoint
CALL hasRole(address,bytes32)
```

#### Parameters

```solidity
_account // account
_role // role

```

#### Return

```json
true if the account has the role, false otherwise
```

### ChainAutorizations >> removeRole(address,bytes32)


Removes the given account from the specified role

```endpoint
CALL removeRole(address,bytes32)
```

#### Parameters

```solidity
_account // account
_role // role

```

#### Return

```json
error NO_ERROR or RUNTIME_ERROR
```

## Client Registry


The Client Registry contract is found within the commons-auth bundle.

### Client Registry >> addClient(bytes32,bytes32,bytes32)


Adds an client with the specified attributes to the registry.

```endpoint
CALL addClient(bytes32,bytes32,bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_ALREADY_EXISTS
```

### Client Registry >> clear()


Removes all entries stored in the mapping.

```endpoint
CALL clear()
```

#### Return

```json
the number of removed entries
```

### Client Registry >> deleteClient(bytes32)


Deletes client from registry.

```endpoint
CALL deleteClient(bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_NOT_FOUND
```

### Client Registry >> exists(bytes32)


returns true if the map contains a value at the specified key, false otherwise.

```endpoint
CALL exists(bytes32)
```

### Client Registry >> getClient(bytes32)


Gets an client from the mapping.

```endpoint
CALL getClient(bytes32)
```

#### Return

```json
client
```

### Client Registry >> keyAtIndex(uint256)


returns the key at the given index or 0 if the index is out of bounds

```endpoint
CALL keyAtIndex(uint256)
```

### Client Registry >> keyAtIndexHasNext(uint256)


Returns the key at the given index position and the index of the next artifact, if there is one, or 0 otherwise. This method can be used as an iterator: As long as a nextIndex > 0 is returned, there is another key.

```endpoint
CALL keyAtIndexHasNext(uint256)
```

### Client Registry >> keyIndex(bytes32)


returns the index of the given key or -1 if the key does not exist

```endpoint
CALL keyIndex(bytes32)
```

### Client Registry >> size()


returns the size of the mapping, i.e. the number of currently stored entries

```endpoint
CALL size()
```

### Client Registry >> updateClient(bytes32,bytes32)


Updates client information.

```endpoint
CALL updateClient(bytes32,bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_NOT_FOUND
```

## ContractLocator Interface


The ContractLocator Interface contract is found within the commons-management bundle.

### ContractLocator Interface >> addContract(bytes32,address)


Adds the specified contract address to the locator under the given name.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract address
_name // the name to register

```

#### Return

```json
the number of contracts registered at the end of this operation
```

### ContractLocator Interface >> getContract(bytes32)


returns the address of the contract registered under the specified name. TODO can be extended in the future to include version!

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered name

```

#### Return

```json
(errorcode, address) 
```

## ContractLocatorEnabled


The ContractLocatorEnabled contract is found within the commons-management bundle.

### ContractLocatorEnabled >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```

### ContractLocatorEnabled >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### ContractLocatorEnabled >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
the same bytes32 as the input if the type is supported, keccak256("") otherwise.
```

### ContractLocatorEnabled >> setContractLocator(address)


Allows setting the ContractLocator address, if it hadn't been set or if the msg.sender is the currently registered locator.

```endpoint
CALL setContractLocator(address)
```

#### Return

```json
true if successful
```

## DOUG - Decentralized Organization Upgrade Guy


The DOUG - Decentralized Organization Upgrade Guy contract is found within the commons-management bundle.

### DOUG - Decentralized Organization Upgrade Guy >> addChild(address)


Adds the given address as a child of this component

```endpoint
CALL addChild(address)
```

#### Parameters

```solidity
_child // the child to add

```

#### Return

```json
NO_ERROR if successful or INVALID_PARAM_VALUE if the parent-child relationship cannot be established.
```

### DOUG - Decentralized Organization Upgrade Guy >> addContract(bytes32,address)


Adds the specified contract address to the locator under the given name.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract address
_name // the name to register

```

#### Return

```json
the number of contracts registered at the end of this operation
```

### DOUG - Decentralized Organization Upgrade Guy >> addLibrary(bytes32,address)


Registers the given library address under the specified name.

```endpoint
CALL addLibrary(bytes32,address)
```

#### Parameters

```solidity
_address // the library address
_name // the key under which the library should be registered

```

#### Return

```json
the number of registered libraries after this operation
```

### DOUG - Decentralized Organization Upgrade Guy >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DOUG - Decentralized Organization Upgrade Guy >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DOUG - Decentralized Organization Upgrade Guy >> getContract(bytes32)


returns the address of the contract registered under the specified name. TODO can be extended in the future to include version!

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered name

```

#### Return

```json
(errorcode, address) 
```

### DOUG - Decentralized Organization Upgrade Guy >> getLibrary(bytes32)


Returns the address of the library registered under the specified name.

```endpoint
CALL getLibrary(bytes32)
```

#### Parameters

```solidity
_name // the registry key

```

#### Return

```json
the address of the library or 0x0 if it doesn't exist
```

### DOUG - Decentralized Organization Upgrade Guy >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### DOUG - Decentralized Organization Upgrade Guy >> getNumberOfRegistrationContracts()


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```

### DOUG - Decentralized Organization Upgrade Guy >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### DOUG - Decentralized Organization Upgrade Guy >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### DOUG - Decentralized Organization Upgrade Guy >> isDestroyOnUpgrade()


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### DOUG - Decentralized Organization Upgrade Guy >> major()


returns the major version number

```endpoint
CALL major()
```

### DOUG - Decentralized Organization Upgrade Guy >> migrateFrom(address)


Implements the migration of state from the specified predecessor to this contract. This method can be used to 'read' the state of the other contract which is probably easier to achieve.

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
predecessor // the address from which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### DOUG - Decentralized Organization Upgrade Guy >> migrateTo(address)


Implements the migration of state this contract to the specified contract. This method can be used to 'write' the state from this contract to the success. It's probably a little less useful since it requires the successor contract to have appropriate functions to set state.

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
successor // the address to which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### DOUG - Decentralized Organization Upgrade Guy >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### DOUG - Decentralized Organization Upgrade Guy >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### DOUG - Decentralized Organization Upgrade Guy >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### DOUG - Decentralized Organization Upgrade Guy >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### DOUG - Decentralized Organization Upgrade Guy >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### DOUG - Decentralized Organization Upgrade Guy >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## DataStorage Interface


The DataStorage Interface contract is found within the bpm-runtime bundle.

### DataStorage Interface >> getDataIdAtIndex(uint256)


Returns the data id at the given index

```endpoint
CALL getDataIdAtIndex(uint256)
```

#### Parameters

```solidity
_index // the index of the data

```

#### Return

```json
error uint error code id bytes32 id of the data
```

### DataStorage Interface >> getDataType(bytes32)


Returns the data type of the Data object identified by the given id

```endpoint
CALL getDataType(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint8 the DataType
```

### DataStorage Interface >> getDataValueAsAddress(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsAddress(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
address the value of the data
```

### DataStorage Interface >> getDataValueAsAddressArray(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsAddressArray(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
address[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBool(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBool(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bool the bool value of the data
```

### DataStorage Interface >> getDataValueAsBytes(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes32 the value of the data
```

### DataStorage Interface >> getDataValueAsBytes16Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes16Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes16[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes1Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes1Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes1[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes20Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes20Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes20[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes24Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes24Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes24[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes28Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes28Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes28[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes2Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes2Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes2[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes32Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes32Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes32[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes3Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes3Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes3[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes4Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes4Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes4[100] the value of the data
```

### DataStorage Interface >> getDataValueAsBytes8Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsBytes8Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
bytes8[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int the value of the data
```

### DataStorage Interface >> getDataValueAsInt128Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt128Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int128[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt16Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt16Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int16[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt256Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt256Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int256[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt32Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt32Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int32[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt64Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt64Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int64[100] the value of the data
```

### DataStorage Interface >> getDataValueAsInt8Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsInt8Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
int8[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint the value of the data
```

### DataStorage Interface >> getDataValueAsUint128Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint128Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint128[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint16Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint16Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint16[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint256Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint256Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint256[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint32Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint32Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint32[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint64Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint64Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint64[100] the value of the data
```

### DataStorage Interface >> getDataValueAsUint8Array(bytes32)


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsUint8Array(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint8[100] the value of the data
```

### DataStorage Interface >> getSize()


Returns the size of the DataMap

```endpoint
CALL getSize()
```

#### Return

```json
uint the size
```

### DataStorage Interface >> removeData(bytes32)


Removes the Data identified by the id from the DataMap

```endpoint
CALL removeData(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
uint error code
```

### DataStorage Interface >> setDataValueAsAddress(bytes32,address)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddress(bytes32,address)
```

#### Parameters

```solidity
_id // the id of the data
_value // the address value of the data

```

### DataStorage Interface >> setDataValueAsAddressArray(bytes32,address[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddressArray(bytes32,address[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the address[100] value of the data

```

### DataStorage Interface >> setDataValueAsBool(bytes32,bool)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBool(bytes32,bool)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bool value of the data

```

### DataStorage Interface >> setDataValueAsBytes(bytes32,bytes32)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32 value of the data

```

### DataStorage Interface >> setDataValueAsBytes(bytes32,bytes32,uint8)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes(bytes32,bytes32,uint8)
```

#### Parameters

```solidity
_dataType // the uint8 data type of the value denoting the bytes size
_id // the id of the data
_value // the bytes16 value of the data

```

### DataStorage Interface >> setDataValueAsBytes16Array(bytes32,bytes16[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes16Array(bytes32,bytes16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes16[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes1Array(bytes32,bytes1[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes1Array(bytes32,bytes1[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes1[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes20Array(bytes32,bytes20[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes20Array(bytes32,bytes20[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes20[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes24Array(bytes32,bytes24[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes24Array(bytes32,bytes24[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes24[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes28Array(bytes32,bytes28[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes28Array(bytes32,bytes28[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes28[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes2Array(bytes32,bytes2[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes2Array(bytes32,bytes2[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes2[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes32Array(bytes32,bytes32[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32Array(bytes32,bytes32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes3Array(bytes32,bytes3[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes3Array(bytes32,bytes3[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes3[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes4Array(bytes32,bytes4[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes4Array(bytes32,bytes4[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes4[100] value of the data

```

### DataStorage Interface >> setDataValueAsBytes8Array(bytes32,bytes8[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes8Array(bytes32,bytes8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes8[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt(bytes32,int256)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt(bytes32,int256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the int value of the data

```

### DataStorage Interface >> setDataValueAsInt(bytes32,int256,uint8)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt(bytes32,int256,uint8)
```

#### Parameters

```solidity
_dataType // the uint8 DataType denoting the size
_id // the id of the data
_value // the int value of the data

```

### DataStorage Interface >> setDataValueAsInt128Array(bytes32,int128[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt128Array(bytes32,int128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int128[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt16Array(bytes32,int16[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt16Array(bytes32,int16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int16[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt256Array(bytes32,int256[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256Array(bytes32,int256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int256[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt32Array(bytes32,int32[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt32Array(bytes32,int32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int32[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt64Array(bytes32,int64[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt64Array(bytes32,int64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int64[100] value of the data

```

### DataStorage Interface >> setDataValueAsInt8Array(bytes32,int8[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt8Array(bytes32,int8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int8[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint(bytes32,uint256)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint(bytes32,uint256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint value of the data

```

### DataStorage Interface >> setDataValueAsUint(bytes32,uint256,uint8)


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint(bytes32,uint256,uint8)
```

#### Parameters

```solidity
_dataType // the uint8 DataType denoting the size
_id // the id of the data
_value // the uint value of the data

```

### DataStorage Interface >> setDataValueAsUint128Array(bytes32,uint128[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint128Array(bytes32,uint128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint128[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint16Array(bytes32,uint16[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint16Array(bytes32,uint16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint16[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint256Array(bytes32,uint256[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256Array(bytes32,uint256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint256[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint32Array(bytes32,uint32[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint32Array(bytes32,uint32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint32[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint64Array(bytes32,uint64[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint64Array(bytes32,uint64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint64[100] value of the data

```

### DataStorage Interface >> setDataValueAsUint8Array(bytes32,uint8[100])


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint8Array(bytes32,uint8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint8[100] value of the data

```

## DataStorageUtils Library


The DataStorageUtils Library contract is found within the bpm-runtime bundle.

### DataStorageUtils Library >> remove(DataStorageUtils.DataMap storage,bytes32)


Removes the Data registered at the specified key in the provided map. The _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(DataStorageUtils.DataMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```



## DefaultAccountsManager


The DefaultAccountsManager contract is found within the commons-auth bundle.

### DefaultAccountsManager >> addBusinessAccount(address)


Adds the specified BusinessAccount. Returns NO_ERROR, RESOURCE_NOT_FOUND if the organization does not exist, RESOURCE_ALREADY_EXISTS if the business account is already registered

```endpoint
CALL addBusinessAccount(address)
```

### DefaultAccountsManager >> addFunds(address,bytes32,uint256)


Adds the specified fund amount to the specified organization's business account.

```endpoint
CALL addFunds(address,bytes32,uint256)
```

### DefaultAccountsManager >> addUserAccount(address)


Adds the specified UserAccount.

```endpoint
CALL addUserAccount(address)
```

#### Return

```json
NO_ERROR, RESOURCE_NOT_FOUND if the organization does not exist, RESOURCE_ALREADY_EXISTS if the user account is already registered
```

### DefaultAccountsManager >> addUserToOrganization(address,address)


Associates the given user with the specified organization.

```endpoint
CALL addUserToOrganization(address,address)
```

#### Parameters

```solidity
_organization // the organization
_userAccount // the user

```

#### Return

```json
BaseErrors.NULL_PARAM_NOT_ALLOWED if organization not given,
BaseErrors.RESOURCE_NOT_FOUND if the user account is unknown,
BaseErrors.INVALID_STATE if the given user account has the same ID, but different address as an already registered account,
BaseErrors.NO_ERROR if successful
```

### DefaultAccountsManager >> businessAccountExists(address,bytes32)


Indicates whether the specified business account exists for the given organization ID

```endpoint
CALL businessAccountExists(address,bytes32)
```

#### Parameters

```solidity
_name // businessAccount name
_organization // the organization's address

```

#### Return

```json
bool exists
```

### DefaultAccountsManager >> createUserAccount(address,bytes32,bytes32)


Creates and adds a user account

```endpoint
CALL createUserAccount(address,bytes32,bytes32)
```

#### Parameters

```solidity
_id // id (optional)
_owner // owner (optional)
_secret // secret

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RUNTIME_ERROR() if a runtime erroruserAccount user account
```

### DefaultAccountsManager >> getBusinessAccount(address,bytes32)


Returns the business account address for the specified organization ID and business account name.

```endpoint
CALL getBusinessAccount(address,bytes32)
```

#### Parameters

```solidity
_name // businessAccount name
_organization // the organization's address

```

#### Return

```json
(error, address)
```

### DefaultAccountsManager >> getBusinessAccount(bytes32)


Returns the business account address for the specified business account ID.

```endpoint
CALL getBusinessAccount(bytes32)
```

### DefaultAccountsManager >> getBusinessAccountAtIndex(uint256)


Gets business account at the given position.

```endpoint
CALL getBusinessAccountAtIndex(uint256)
```

#### Parameters

```solidity
_pos // position

```

#### Return

```json
businessAccount business account address
```

### DefaultAccountsManager >> getBusinessAccountData(address)


Gets data for the specified business account.

```endpoint
CALL getBusinessAccountData(address)
```

#### Parameters

```solidity
_businessAccount // the business account address

```

#### Return

```json
organizationAddress the organization's addressbusinessAccountId business account IDbusinessAccountName business account nameaccountBalance business account balance
```

### DefaultAccountsManager >> getBusinessAccountsSize()


Gets business accounts size.

```endpoint
CALL getBusinessAccountsSize()
```

#### Return

```json
size size
```

### DefaultAccountsManager >> getUserAccount(bytes32)


Returns the user account address for the specified user account ID.

```endpoint
CALL getUserAccount(bytes32)
```

### DefaultAccountsManager >> getUserAccountAtIndex(uint256)


Gets user account at the given position.

```endpoint
CALL getUserAccountAtIndex(uint256)
```

#### Parameters

```solidity
_pos // position

```

#### Return

```json
userAccount user account address
```

### DefaultAccountsManager >> getUserAccountData(address)


Gets data for the specified user account.

```endpoint
CALL getUserAccountData(address)
```

#### Parameters

```solidity
_userAccount // the user account address

```

#### Return

```json
id user account IDowner user account owner
```

### DefaultAccountsManager >> getUserAccountsSize()


Gets user accounts size.

```endpoint
CALL getUserAccountsSize()
```

#### Return

```json
size size
```

### DefaultAccountsManager >> removeUserFromOrganization(address,address)


Removes (deactivates) the given user from the specified organization.

```endpoint
CALL removeUserFromOrganization(address,address)
```

#### Parameters

```solidity
_organization // the organization
_userAccount // the user

```

#### Return

```json
BaseErrors.NULL_PARAM_NOT_ALLOWED if organization not given,
BaseErrors.RESOURCE_NOT_FOUND if the user account is unknown,
BaseErrors.INVALID_STATE if the given user account has the same ID, but different address as an already registered account,
BaseErrors.NO_ERROR if successful
```

### DefaultAccountsManager >> userAccountExists(bytes32)


Indicates whether the specified user account exists for the given userAccount ID

```endpoint
CALL userAccountExists(bytes32)
```

#### Parameters

```solidity
_id // userAccount ID

```

#### Return

```json
bool exists
```

### DefaultAccountsManager >> withdrawFunds(address,bytes32,uint256)


Subtracts the specified fund amount from the specified organization's business account.

```endpoint
CALL withdrawFunds(address,bytes32,uint256)
```

## DefaultActiveAgreement Interface


The DefaultActiveAgreement Interface contract is found within the agreements bundle.

### DefaultActiveAgreement Interface >> getArchetype()


Returns the archetype

```endpoint
CALL getArchetype()
```

#### Return

```json
the archetype address 
```

### DefaultActiveAgreement Interface >> getCreator()


Returns the creator

```endpoint
CALL getCreator()
```

#### Return

```json
the creator address
```

### DefaultActiveAgreement Interface >> getHoardAddress()


Returns the Hoard Address

```endpoint
CALL getHoardAddress()
```

#### Return

```json
the Hoard Address

```

### DefaultActiveAgreement Interface >> getName()


Gets name

```endpoint
CALL getName()
```

#### Return

```json
name name
```

### DefaultActiveAgreement Interface >> getNumberOfParties()


Gets number of parties

```endpoint
CALL getNumberOfParties()
```

#### Return

```json
size number of parties
```

### DefaultActiveAgreement Interface >> getParty(uint256)


Gets party

```endpoint
CALL getParty(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index out of boundsparty party
```

### DefaultActiveAgreement Interface >> gethoardSecret()


Returns the Hoard Secret

```endpoint
CALL gethoardSecret()
```

#### Return

```json
the Hoard Secret
```

### DefaultActiveAgreement Interface >> isPrivate()


Returns the private flag

```endpoint
CALL isPrivate()
```

#### Return

```json
the private flag 
```

### DefaultActiveAgreement Interface >> setName(bytes32)


Sets name

```endpoint
CALL setName(bytes32)
```

#### Parameters

```solidity
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR()
```

## DefaultActiveAgreementRegistry Interface


The DefaultActiveAgreementRegistry Interface contract is found within the agreements bundle.

### DefaultActiveAgreementRegistry Interface >> create(address,bytes32,address,bytes32,bytes32,bool,address[])


Creates an Active Agreement with the given parameters

```endpoint
CALL create(address,bytes32,address,bytes32,bytes32,bool,address[])
```

#### Parameters

```solidity
_archetype // archetype
_hoardAddress // Address of agreement params in hoard
_hoardSecret // Secret for hoard retrieval
_name // name
_parties // parties

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if _archetype or _name is null, or BaseErrors.RUNTIME_ERROR() if runtime errora return code indicating success or failure and the new activeAgreement's address, if successfully created
```

### DefaultActiveAgreementRegistry Interface >> getActiveAgreementAtIndex(uint256)


Gets activeAgreement address at given index

```endpoint
CALL getActiveAgreementAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
the Active Agreement address
```

### DefaultActiveAgreementRegistry Interface >> getActiveAgreementData(address)


Returns data about the Active Agreement at the specified address

```endpoint
CALL getActiveAgreementData(address)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement

```

#### Return

```json
archetype archetypename namehoardAddress Address of agreement params in hoardhoardSecret Secret for hoard retrieval
```

### DefaultActiveAgreementRegistry Interface >> getActiveAgreementsSize()


Gets number of activeAgreements

```endpoint
CALL getActiveAgreementsSize()
```

#### Return

```json
size size
```

### DefaultActiveAgreementRegistry Interface >> getPartiesByActiveAgreementSize(address)


Gets parties size for given Active Agreement

```endpoint
CALL getPartiesByActiveAgreementSize(address)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement

```

#### Return

```json
size size
```

### DefaultActiveAgreementRegistry Interface >> getPartyByActiveAgreementAtIndex(address,uint256)


Gets getPartyByActiveAgreementAtIndex

```endpoint
CALL getPartyByActiveAgreementAtIndex(address,uint256)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement
_index // index

```

#### Return

```json
party party
```

### DefaultActiveAgreementRegistry Interface >> getPartyByActiveAgreementData(address,address)


Returns data about the party at the specified address. Placeholder function due to SQLSOL requirements.

```endpoint
CALL getPartyByActiveAgreementData(address,address)
```

#### Parameters

```solidity
_activeAgreement // active agreement
_party // party

```

#### Return

```json
placeholder placeholder
```

### DefaultActiveAgreementRegistry Interface >> setName(address,bytes32)


Sets name for given Active Agreement

```endpoint
CALL setName(address,bytes32)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RUNTIME_ERROR() if runtime error
```

## DefaultArchetype


The DefaultArchetype contract is found within the agreements bundle.

### DefaultArchetype >> activate()


Activates this archetype

```endpoint
CALL activate()
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### DefaultArchetype >> addCustomField(uint8,bytes32)


Adds custom field

```endpoint
CALL addCustomField(uint8,bytes32)
```

#### Parameters

```solidity
_customField // customField
_dataType // data type (enum)

```

#### Return

```json
BaseErrors.NO_ERROR() if successful,
BaseErrors.INVALID_PARAM_VALUE() if _dataType is not in the DataTypes enum,
BaseErrors.NULL_PARAM_NOT_ALLOWED() if _customField is empty,
BaseErrors.RESOURCE_ALREADY_EXISTS() if _customField already exists
```

### DefaultArchetype >> addDocument(bytes32,bytes32,bytes32)


Adds document

```endpoint
CALL addDocument(bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_hoardAddress // hoard address
_name // name
_secretKey // secret key

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS() if _name already exists in documentNames
```

### DefaultArchetype >> addJurisdiction(bytes2,bytes32)


Adds the given jurisdiction in the form of a country code and region identifier to this archetype. References codes defined via IsoCountries interface implementations. If the region is empty, the jurisdiction will only reference the country and the regions will be emptied, i.e. any prior regions for that country will be removed.

```endpoint
CALL addJurisdiction(bytes2,bytes32)
```

#### Parameters

```solidity
_country // a ISO- code, e.g. 'US'
_region // a region identifier from a IsoCountries contract

```

#### Return

```json
BaseErrors.NO_ERROR() if successful, and key of jurisdiction just added
BaseErrors.INVALID_PARAM_VALUE() if _country is not in the DataTypes enum,
```

### DefaultArchetype >> deactivate()


Deactivates this archetype

```endpoint
CALL deactivate()
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### DefaultArchetype >> getAuthor()


Gets Author

```endpoint
CALL getAuthor()
```

#### Return

```json
author author
```

### DefaultArchetype >> getCustomFieldAtIndex(uint256)


Gets custom field at index

```endpoint
CALL getCustomFieldAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error error TBDcustomField custom field
```

### DefaultArchetype >> getCustomFieldDataType(bytes32)


Gets custom field data type

```endpoint
CALL getCustomFieldDataType(bytes32)
```

#### Parameters

```solidity
_customField // custom field

```

#### Return

```json
error error TBDdataType data type
```

### DefaultArchetype >> getDescription()


Gets description

```endpoint
CALL getDescription()
```

#### Return

```json
description
```

### DefaultArchetype >> getDocument(bytes32)


Gets document with given name

```endpoint
CALL getDocument(bytes32)
```

#### Parameters

```solidity
_name // document name

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND() if documentsNames does not contain _namehoardAddress hoard addresssecretKey secret key
```

### DefaultArchetype >> getDocumentAtIndex(uint256)


Gets document name at index

```endpoint
CALL getDocumentAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index is out of boundsname
```

### DefaultArchetype >> getExecutionProcessDefinition()


Returns the address of the ProcessDefinition that orchestrates the agreement execution.

```endpoint
CALL getExecutionProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### DefaultArchetype >> getFormationProcessDefinition()


Returns the address of the ProcessDefinition that orchestrates the agreement formation.

```endpoint
CALL getFormationProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### DefaultArchetype >> getJurisdictionAtIndex(uint256)


Retrieves the key for the jurisdiction at the specified index

```endpoint
CALL getJurisdictionAtIndex(uint256)
```

#### Parameters

```solidity
_index // the index position

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS() if index is out of boundsthe key of the jurisdiction or an empty bytes32 if the index was out of bounds
```

### DefaultArchetype >> getJurisdictionData(bytes32)


Returns information about the jurisdiction with the specified key

```endpoint
CALL getJurisdictionData(bytes32)
```

#### Parameters

```solidity
_key // the key identifying the jurisdiction

```

#### Return

```json
the country and region identifiers (see IsoCountries), if the jurisdiction exists
```

### DefaultArchetype >> getName()


Returns the archetype name

```endpoint
CALL getName()
```

#### Return

```json
the name
```

### DefaultArchetype >> getNumberOfCustomFields()


Gets number of custom fields

```endpoint
CALL getNumberOfCustomFields()
```

#### Return

```json
size number of custom fields
```

### DefaultArchetype >> getNumberOfDocuments()


Gets number of documents

```endpoint
CALL getNumberOfDocuments()
```

#### Return

```json
size number of documents
```

### DefaultArchetype >> getNumberOfJurisdictions()


Returns the number jurisdictions for this archetype

```endpoint
CALL getNumberOfJurisdictions()
```

#### Return

```json
the number of jurisdictions
```

### DefaultArchetype >> isActive()


Returns the active state

```endpoint
CALL isActive()
```

#### Return

```json
true if active, false otherwise
```

### DefaultArchetype >> isPrivate()


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
true if private, false otherwise
```

## DefaultArchetypeRegistry


The DefaultArchetypeRegistry contract is found within the agreements bundle.

### DefaultArchetypeRegistry >> activate(address)


Sets active to true for given archetype

```endpoint
CALL activate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### DefaultArchetypeRegistry >> addDocument(address,bytes32,bytes32,bytes32)


Adds Hoard document to the given Archetype

```endpoint
CALL addDocument(address,bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_hoardAddress // hoard address
_name // name
_secretKey // secret key

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() _archetype does not exist, or see DefaultArchetype
```

### DefaultArchetypeRegistry >> addField(address,uint8,bytes32)


Adds custom field to archetype

```endpoint
CALL addField(address,uint8,bytes32)
```

#### Parameters

```solidity
_archetype // the archetype address
_dataType // data type (enum)
_fieldName // the field name

```

#### Return

```json
BaseErrors.NO_ERROR() if successfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundany error returned from the Archetype.addCustomField() function
```

### DefaultArchetypeRegistry >> addFields(address,uint8[],bytes32[])


Adds the specified fields to the archetype. If one of the fields cannot be added, the operation aborts and returns that error code.

```endpoint
CALL addFields(address,uint8[],bytes32[])
```

#### Parameters

```solidity
_archetype // the archetype address
_dataTypes // the data types
_fieldNames // the field names

```

#### Return

```json
BaseErrors.NO_ERROR() if succesfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundBaseErrors.INVALID_PARAM_STATE() if the lengths of the two arrays don't match
```

### DefaultArchetypeRegistry >> addJurisdiction(address,bytes2,bytes32)


Adds the given jurisdiction in the form of a country code and region identifier to this archetype. References codes defined via IsoCountries interface implementations.

```endpoint
CALL addJurisdiction(address,bytes2,bytes32)
```

#### Parameters

```solidity
_country // a ISO-3166-1 code, e.g. 'US'
_region // a region identifier from a IsoCountries contract

```

#### Return

```json
BaseErrors.NO_ERROR() if succesfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundany error returned from the Archetype.addJurisdiction() function
```

### DefaultArchetypeRegistry >> addJurisdictions(address,bytes2[],bytes32[])


Adds the given jurisdictions in the form of a country codes and region identifiers to this archetype. References codes defined via IsoCountries interface implementations.

```endpoint
CALL addJurisdictions(address,bytes2[],bytes32[])
```

#### Parameters

```solidity
_countries // an array of a ISO-3166-1 code, e.g. 'US'
_regions // an array of region identifiers from a IsoCountries contract

```

#### Return

```json
BaseErrors.NO_ERROR() if succesfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundBaseErrors.INVALID_PARAM_STATE() if the lengths of the two arrays don't match
```

### DefaultArchetypeRegistry >> create(bytes32,address,string,bool,address,address)


Creates a new archetype

```endpoint
CALL create(bytes32,address,string,bool,address,address)
```

#### Parameters

```solidity
_author // author
_description // description
_executionProcess // the address of a ProcessDefinition that orchestrates the agreement execution
_formationProcess // the address of a ProcessDefinition that orchestrates the agreement formation
_isPrivate // determines if the archetype's documents are encrypted
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if either _name, _author, _formationProcess, or _executionProcess is nullarchetype - the new archetype's address, if successfully created
```

### DefaultArchetypeRegistry >> deactivate(address)


Sets active to false for given archetype

```endpoint
CALL deactivate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```

### DefaultArchetypeRegistry >> getArchetypeAtIndex(uint256)


Gets archetype address at given index

```endpoint
CALL getArchetypeAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
archetype archetype
```

### DefaultArchetypeRegistry >> getArchetypeData(address)


Returns data about an archetype

```endpoint
CALL getArchetypeData(address)
```

#### Parameters

```solidity
_archetype // the archetype address

```

#### Return

```json
name namedescription descriptionauthor authoractive activeformationProcessDefinitionexecutionProcessDefinition
```

### DefaultArchetypeRegistry >> getArchetypesSize()


Gets number of archetypes

```endpoint
CALL getArchetypesSize()
```

#### Return

```json
size size
```

### DefaultArchetypeRegistry >> getDocumentByArchetypeAtIndex(address,uint256)


Gets document name by Archetype At index

```endpoint
CALL getDocumentByArchetypeAtIndex(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype
_index // index

```

#### Return

```json
name name
```

### DefaultArchetypeRegistry >> getDocumentByArchetypeData(address,bytes32)


Returns data about the document at the specified address

```endpoint
CALL getDocumentByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
_hoardAddress hoard address_secretKey secret key
```

### DefaultArchetypeRegistry >> getDocumentsByArchetypeSize(address)


Gets documents size for given Archetype

```endpoint
CALL getDocumentsByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```

### DefaultArchetypeRegistry >> getFieldByArchetypeAtIndex(address,uint256)


Gets field name by Archetype At index

```endpoint
CALL getFieldByArchetypeAtIndex(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype
_index // index

```

#### Return

```json
name name
```

### DefaultArchetypeRegistry >> getFieldByArchetypeData(address,bytes32)


Returns data about the field at with the specified name

```endpoint
CALL getFieldByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
dataType data type
```

### DefaultArchetypeRegistry >> getFieldsByArchetypeSize(address)


Gets fields size for given Archetype

```endpoint
CALL getFieldsByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```

### DefaultArchetypeRegistry >> getJurisdictionAtIndexForArchetype(address,uint256)


Returns the jurisdiction key at the specified index for the given archetype

```endpoint
CALL getJurisdictionAtIndexForArchetype(address,uint256)
```

#### Parameters

```solidity
_archetype // archetype address
_index // the index of the jurisdiction

```

#### Return

```json
the jurisdiction primary key
```

### DefaultArchetypeRegistry >> getJurisdictionDataForArchetype(address,bytes32)


Returns data about the jurisdiction with the specified key in the given archetype

```endpoint
CALL getJurisdictionDataForArchetype(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype address
_key // the jurisdiction key

```

#### Return

```json
country the jurisdiction's countryregion the jurisdiction's region
```

### DefaultArchetypeRegistry >> getNumberOfJurisdictionsForArchetype(address)


Returns the number of jurisdictions for the given Archetype

```endpoint
CALL getNumberOfJurisdictionsForArchetype(address)
```

#### Parameters

```solidity
_archetype // archetype address

```

#### Return

```json
the number of jurisdictions
```

## DefaultBpmService


The DefaultBpmService contract is found within the bpm-runtime bundle.

### DefaultBpmService >> fireActivityUpdateEvent(address,bytes32)


Fires the UpdateActivities event to update sqlsol with given activity

```endpoint
CALL fireActivityUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_activityId // - the bytes32 Id of the activity
_piAddress // - the address of the process instance to which the activity belongs

```

### DefaultBpmService >> getActivityDefinitionDetails(address,bytes32)


Gets the address of the assignee for a given activity Id and process instance address

```endpoint
CALL getActivityDefinitionDetails(address,bytes32)
```

#### Parameters

```solidity
_activityId // the activity Id
_piAddress // process instance address

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### DefaultBpmService >> getActivityInstanceAtIndex(address,uint256)


Returns the ActivityInstance ID at the specified index

```endpoint
CALL getActivityInstanceAtIndex(address,uint256)
```

#### Parameters

```solidity
_address // the process instance address
_pos // the activity instance index

```

#### Return

```json
the ActivityInstance ID
```

### DefaultBpmService >> getActivityInstanceData(address,bytes32)


Returns ActivityInstance data for given ActivityInstance ID

```endpoint
CALL getActivityInstanceData(address,bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance
_processInstance // the process instance address

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitioncreated - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) state - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```

### DefaultBpmService >> getNumberOfActivityInstances(address)


Returns the number of activity instances.

```endpoint
CALL getNumberOfActivityInstances(address)
```

#### Return

```json
the activity instance count as size
```

### DefaultBpmService >> getNumberOfProcessData(address)


Returns the number of process data entries.

```endpoint
CALL getNumberOfProcessData(address)
```

#### Return

```json
the process data size
```

### DefaultBpmService >> getNumberOfProcessInstances()


Returns the number of Process Instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the process instance count as size
```

### DefaultBpmService >> getProcessDataAtIndex(address,uint256)


Returns the process data ID at the specified index

```endpoint
CALL getProcessDataAtIndex(address,uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the data ID
```

### DefaultBpmService >> getProcessDataDetails(address,bytes32)


Returns information about the process data entry for the specified process and data ID

```endpoint
CALL getProcessDataDetails(address,bytes32)
```

#### Parameters

```solidity
_address // the process instance
_dataId // the data ID

```

#### Return

```json
(process,id,uintValue,bytes32Value,addressValue,boolValue)
```

### DefaultBpmService >> getProcessInstanceAtIndex(uint256)


Returns the process instance address at the specified index

```endpoint
CALL getProcessInstanceAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the process instance address or BaseErrors.INDEX_OUT_OF_BOUNDS(), 0x0
```

### DefaultBpmService >> getProcessInstanceData(address)


Returns information about the process intance with the specified address

```endpoint
CALL getProcessInstanceData(address)
```

#### Parameters

```solidity
_address // the process instance address

```

#### Return

```json
(processId)
```

### DefaultBpmService >> getProcessInstanceForActivity(bytes32)


Returns the address of the ProcessInstance of the specified ActivityInstance ID

```endpoint
CALL getProcessInstanceForActivity(bytes32)
```

#### Parameters

```solidity
_aiId // the ID of an ActivityInstance

```

#### Return

```json
the ProcessInstance address or 0x0 if it cannot be found
```

### DefaultBpmService >> getProcessModelRepository()


Gets the ProcessModelRepository address for this BpmService

```endpoint
CALL getProcessModelRepository()
```

#### Return

```json
the address of the repository
```

### DefaultBpmService >> getRuntimeDb()


Returns a reference to the BpmRuntimeDb currently used by this BpmService

```endpoint
CALL getRuntimeDb()
```

#### Return

```json
the BpmRuntimeDb
```

### DefaultBpmService >> getUserTaskDetails(address,bytes32)


Gets the address of the assignee for a given activity Id and process instance address

```endpoint
CALL getUserTaskDetails(address,bytes32)
```

#### Parameters

```solidity
_activityId // the activity Id
_piAddress // process instance address

```

#### Return

```json
assignee the address of the activity's assignee (for interactive activities)processId ID of the process definitionprocessName Name of the process definitionapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### DefaultBpmService >> setProcessModelRepository(address)


Sets the ProcessModelRepository for this BpmService

```endpoint
CALL setProcessModelRepository(address)
```

#### Parameters

```solidity
_repository // - the address of the repository

```

### DefaultBpmService >> startProcess(bytes32,bytes32)


Registers the specified process and starts it by activating the first activity

```endpoint
CALL startProcess(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processId // the process ID

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if the ProcessBaseErrors.NO_ERROR()the address of a ProcessInstance, if successful
```

## DefaultBusinessAccount


The DefaultBusinessAccount contract is found within the bpm-runtime bundle.

### DefaultBusinessAccount >> addFunds(uint256)


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
```

### DefaultBusinessAccount >> getBalance()


Returns the current balance

```endpoint
CALL getBalance()
```

### DefaultBusinessAccount >> getId()


Returns this account's ID

```endpoint
CALL getId()
```

### DefaultBusinessAccount >> getName()


Returns this account's name

```endpoint
CALL getName()
```

### DefaultBusinessAccount >> getOrganization()


Returns the address of the organization this accounts is associated with.

```endpoint
CALL getOrganization()
```

### DefaultBusinessAccount >> getOwner()


Returns this account's owner

```endpoint
CALL getOwner()
```

### DefaultBusinessAccount >> withdrawFunds(uint256)


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```

## DefaultCastable


The DefaultCastable contract is found within the commons-management bundle.

### DefaultCastable >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```

### DefaultCastable >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### DefaultCastable >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
the same bytes32 as the input if the type is supported, keccak256("") otherwise.
```

## DefaultContractLocator


The DefaultContractLocator contract is found within the commons-management bundle.

### DefaultContractLocator >> addContract(bytes32,address)


Registers the given contract address under the specified name. An existing address at the same name will be overwritten.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract's address to be registered
_name // the registration key

```

#### Return

```json
the number of registered contracts after the specified contract was inserted
```

### DefaultContractLocator >> getContract(bytes32)


Returns the address of a registered contract

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered key

```

#### Return

```json
(error, contractAddress)
```

### DefaultContractLocator >> remove()


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```

### DefaultContractLocator >> removeContract(bytes32)


Removes the contract registered under the specified name.

```endpoint
CALL removeContract(bytes32)
```

#### Parameters

```solidity
_name // the registration key

```

#### Return

```json
BaseErrors.NO_ERROR, if removal successful. If unsuccessful BaseErrors.RESOURCE_NOT_FOUND
```

## DefaultDOUG


The DefaultDOUG contract is found within the commons-management bundle.

### DefaultDOUG >> addChild(address)


Overwrites HierarchyEnabled.addChild()

```endpoint
CALL addChild(address)
```

### DefaultDOUG >> addContract(bytes32,address)


Registers the given contract address under the specified name. An existing address at the same name will be overwritten.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract's address to be registered
_name // the registration key

```

#### Return

```json
the number of registered contracts after the specified contract was inserted
```

### DefaultDOUG >> addLibrary(bytes32,address)


Registers the given library address under the specified name.

```endpoint
CALL addLibrary(bytes32,address)
```

#### Parameters

```solidity
_address // the library address
_name // the key under which the library should be registered

```

#### Return

```json
the number of registered libraries after this operation
```

### DefaultDOUG >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultDOUG >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultDOUG >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```

### DefaultDOUG >> getContract(bytes32)


Returns the address of a registered contract

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered key

```

#### Return

```json
(error, contractAddress)
```

### DefaultDOUG >> getLibrary(bytes32)


Returns the address of the library registered under the specified name.

```endpoint
CALL getLibrary(bytes32)
```

#### Parameters

```solidity
_name // the registry key

```

#### Return

```json
the address of the library or 0x0 if it doesn't exist
```

### DefaultDOUG >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### DefaultDOUG >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### DefaultDOUG >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### DefaultDOUG >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### DefaultDOUG >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
the same bytes32 as the input if the type is supported, keccak256("") otherwise.
```

### DefaultDOUG >> isDestroyOnUpgrade()


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### DefaultDOUG >> major()


returns the major version number

```endpoint
CALL major()
```

### DefaultDOUG >> migrateFrom(address)


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```

### DefaultDOUG >> migrateTo(address)


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

```

### DefaultDOUG >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### DefaultDOUG >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### DefaultDOUG >> remove()


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```

### DefaultDOUG >> removeContract(bytes32)


Removes the contract registered under the specified name.

```endpoint
CALL removeContract(bytes32)
```

#### Parameters

```solidity
_name // the registration key

```

#### Return

```json
BaseErrors.NO_ERROR, if removal successful. If unsuccessful BaseErrors.RESOURCE_NOT_FOUND
```

### DefaultDOUG >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### DefaultDOUG >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### DefaultDOUG >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### DefaultDOUG >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## DefaultDocument


The DefaultDocument contract is found within the documents-commons bundle.

### DefaultDocument >> addVersion(string)


Adds the specified hash as a new version of the document. The msg.sender is registered as owner and the version creation date is set to now.

```endpoint
CALL addVersion(string)
```

#### Parameters

```solidity
_hash // the version hash

```

#### Return

```json
BaseErrors.NO_ERROR, BaseErrors.INSUFFICIENT_PRIVILEGES (as determined by calling canAddVersion(), or BaseErrors.RESOURCE_ALREADY_EXISTS if the version has been added before.
```

### DefaultDocument >> getName()


Returns the document's name

```endpoint
CALL getName()
```

### DefaultDocument >> getNumberOfVersions()


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```

### DefaultDocument >> getVersionCreated(string)


Returns the creation date of the specified version hash.

```endpoint
CALL getVersionCreated(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creation date, or 0 if the version does not exist
```

### DefaultDocument >> getVersionCreator(string)


Returns the address registered as the creator of the specified version hash.

```endpoint
CALL getVersionCreator(string)
```

#### Parameters

```solidity
_hash // the desired version hash

```

#### Return

```json
the creator address, or 0x0 if the version does not exist
```

## DefaultEcosystem


The DefaultEcosystem contract is found within the commons-auth bundle.

### DefaultEcosystem >> addOrganization(address)


Adds the organization at the specified address to this Ecosystem.

```endpoint
CALL addOrganization(address)
```

#### Parameters

```solidity
_address // the Organization contract's address

```

#### Return

```json
BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.RESOURCE_ALREADY_EXISTS() if the organization's ID is already registered, BaseErrors.NO_ERROR() if successful
```

### DefaultEcosystem >> createOrganization(bytes32,bytes32,address[10])


Creates a new Organization with the specified parameters and adds it to this Ecosystem.

```endpoint
CALL createOrganization(bytes32,bytes32,address[10])
```

#### Parameters

```solidity
_approvers // the initial owners. If left empty, the msg.sender will be added as an owner.
_id // the organization's ID
_name // the organization's name

```

#### Return

```json
BaseErrors.INVALID_PARAM_VALUE() if the ID is empty, BaseErrors.RESOURCE_ALREADY_EXISTS() if the organization's ID is already registered, BaseErrors.NO_ERROR() if successfulthe address of the newly created Organization, or 0x0 if not successful
```

### DefaultEcosystem >> eventFired(bytes32,address)


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```

### DefaultEcosystem >> eventFired(bytes32,address,address)


Implementation of the EventListener interface. Can be called by an organization that is registered in this Ecosystem to trigger an UpdateOrganization event.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_event // the event that was fired. Currently supports custom event EVENT_UPDATE_ORGANIZATION_USER
_source // Expected to be a registered Organization

```

### DefaultEcosystem >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultEcosystem >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultEcosystem >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultEcosystem >> getApproverAtIndex(address,uint256)


Returns the approver's address at the given index position of the specified organization.

```endpoint
CALL getApproverAtIndex(address,uint256)
```

#### Parameters

```solidity
_organization // the organization's address
_pos // the index position

```

#### Return

```json
the approver's address, if the position exists
```

### DefaultEcosystem >> getApproverData(address,address)


Function supports SQLsol, but only returns the approver address parameter.

```endpoint
CALL getApproverData(address,address)
```

#### Parameters

```solidity
_approver // the approver's address
_organization // the organization's address

```

#### Return

```json
the approver address
```

### DefaultEcosystem >> getNumberOfApprovers(address)


Returns the number of registered approvers in the specified organization.

```endpoint
CALL getNumberOfApprovers(address)
```

#### Parameters

```solidity
_organization // the organization's address

```

#### Return

```json
the number of approvers
```

### DefaultEcosystem >> getNumberOfOrganizations()


Returns the number of registered organizations.

```endpoint
CALL getNumberOfOrganizations()
```

#### Return

```json
the number of organizations
```

### DefaultEcosystem >> getNumberOfUsers(address)


returns the number of users associated with the specified organization

```endpoint
CALL getNumberOfUsers(address)
```

#### Parameters

```solidity
_organization // the organization's address

```

#### Return

```json
the number of users
```

### DefaultEcosystem >> getOrganization(bytes32)


Returns the address of the organization with the specified ID, if it exists

```endpoint
CALL getOrganization(bytes32)
```

#### Parameters

```solidity
_id // the organization's ID

```

#### Return

```json
the organization's address or 0x0 if it does not exist
```

### DefaultEcosystem >> getOrganizationAtIndex(uint256)


Returns the address of the Organization at the given index.

```endpoint
CALL getOrganizationAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address of the Organization or 0x0 if the index position does not exist
```

### DefaultEcosystem >> getOrganizationData(address)


Returns the public data of the organization at the specified address

```endpoint
CALL getOrganizationData(address)
```

#### Parameters

```solidity
_organization // the address of an organization

```

#### Return

```json
the organization's ID and name
```

### DefaultEcosystem >> getUserAtIndex(address,uint256)


Returns the user's address at the given index position in the specified organization.

```endpoint
CALL getUserAtIndex(address,uint256)
```

#### Parameters

```solidity
_organization // the organization's address
_pos // the index position

```

#### Return

```json
the address or 0x0 if the position does not exist
```

### DefaultEcosystem >> getUserData(address,address)


Returns information about the specified user in the context of the given organization

```endpoint
CALL getUserData(address,address)
```

#### Parameters

```solidity
_organization // the organization's address
_user // the user's address

```

#### Return

```json
active - whether the user is activated in the organization
```

## DefaultEventEmitter


The DefaultEventEmitter contract is found within the bpm-model bundle.

### DefaultEventEmitter >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### DefaultEventEmitter >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### DefaultEventEmitter >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### DefaultEventEmitter >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

## DefaultLifecycleHub


The DefaultLifecycleHub contract is found within the commons-management bundle.

### DefaultLifecycleHub >> addChild(address)


Overwrites HierarchyEnabled.addChild()

```endpoint
CALL addChild(address)
```

### DefaultLifecycleHub >> addContract(bytes32,address)


Registers the given contract address under the specified name. An existing address at the same name will be overwritten.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract's address to be registered
_name // the registration key

```

#### Return

```json
the number of registered contracts after the specified contract was inserted
```

### DefaultLifecycleHub >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultLifecycleHub >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultLifecycleHub >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```

### DefaultLifecycleHub >> getContract(bytes32)


Returns the address of a registered contract

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered key

```

#### Return

```json
(error, contractAddress)
```

### DefaultLifecycleHub >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### DefaultLifecycleHub >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### DefaultLifecycleHub >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### DefaultLifecycleHub >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### DefaultLifecycleHub >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
the same bytes32 as the input if the type is supported, keccak256("") otherwise.
```

### DefaultLifecycleHub >> isDestroyOnUpgrade()


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### DefaultLifecycleHub >> major()


returns the major version number

```endpoint
CALL major()
```

### DefaultLifecycleHub >> migrateFrom(address)


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```

### DefaultLifecycleHub >> migrateTo(address)


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

```

### DefaultLifecycleHub >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### DefaultLifecycleHub >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### DefaultLifecycleHub >> remove()


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```

### DefaultLifecycleHub >> removeContract(bytes32)


Removes the contract registered under the specified name.

```endpoint
CALL removeContract(bytes32)
```

#### Parameters

```solidity
_name // the registration key

```

#### Return

```json
BaseErrors.NO_ERROR, if removal successful. If unsuccessful BaseErrors.RESOURCE_NOT_FOUND
```

### DefaultLifecycleHub >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### DefaultLifecycleHub >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### DefaultLifecycleHub >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### DefaultLifecycleHub >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## DefaultLifecycleModule


The DefaultLifecycleModule contract is found within the commons-management bundle.

### DefaultLifecycleModule >> addChild(address)


Adds the given address as a child of this component

```endpoint
CALL addChild(address)
```

#### Parameters

```solidity
_child // the child to add

```

#### Return

```json
NO_ERROR if successful or INVALID_PARAM_VALUE if the parent-child relationship cannot be established.
```

### DefaultLifecycleModule >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultLifecycleModule >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultLifecycleModule >> declareCastableTo(bytes32)


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```

### DefaultLifecycleModule >> getNumberOfCastTypes()


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```

### DefaultLifecycleModule >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### DefaultLifecycleModule >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### DefaultLifecycleModule >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### DefaultLifecycleModule >> isCastableTo(bytes32)


Checks whether this Castable supports the given type. Note that returning a bytes32 is necessary since a contract that does not implement Castable, but has a fallback function would evaluate to bool 'true' when `isCastableTo(bytes32) returns (bool)` was invoked on it.  

```endpoint
CALL isCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support.

```

#### Return

```json
the same bytes32 as the input if the type is supported, keccak256("") otherwise.
```

### DefaultLifecycleModule >> isDestroyOnUpgrade()


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### DefaultLifecycleModule >> major()


returns the major version number

```endpoint
CALL major()
```

### DefaultLifecycleModule >> migrateFrom(address)


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```

### DefaultLifecycleModule >> migrateTo(address)


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

```

### DefaultLifecycleModule >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### DefaultLifecycleModule >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### DefaultLifecycleModule >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### DefaultLifecycleModule >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### DefaultLifecycleModule >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### DefaultLifecycleModule >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## DefaultOrganization


The DefaultOrganization contract is found within the commons-auth bundle.

### DefaultOrganization >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### DefaultOrganization >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### DefaultOrganization >> addUser(address)


Adds the specified user to this organization as an active user. If the user already exists, the function ensures the account is active.

```endpoint
CALL addUser(address)
```

#### Parameters

```solidity
_userAccount // the user to add

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.INVALID_PARAM_STATE if the UserAccount does not have this organization as its organization.
```

### DefaultOrganization >> getApproverAtIndex(uint256)


Returns the approver's address at the given index position.

```endpoint
CALL getApproverAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address or 0x0 if the position does not exist
```

### DefaultOrganization >> getId()


see NamedElement.getId()

```endpoint
CALL getId()
```

### DefaultOrganization >> getName()


see NamedElement.getName()

```endpoint
CALL getName()
```

### DefaultOrganization >> getNumberOfApprovers()


Returns the number of registered approvers.

```endpoint
CALL getNumberOfApprovers()
```

#### Return

```json
the number of approvers
```

### DefaultOrganization >> getNumberOfUsers()


returns the number of users associated with this organization

```endpoint
CALL getNumberOfUsers()
```

#### Return

```json
the number of users
```

### DefaultOrganization >> getUserAtIndex(uint256)


Returns the user's address at the given index position.

```endpoint
CALL getUserAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address or 0x0 if the position does not exist
```

### DefaultOrganization >> isActiveUser(address)


Returns whether the given user account is valid in this organization

```endpoint
CALL isActiveUser(address)
```

#### Parameters

```solidity
_userAccount // the user account

```

#### Return

```json
true if valid, false otherwise
```

### DefaultOrganization >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### DefaultOrganization >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

### DefaultOrganization >> removeUser(address)


Removes / Deactivates the user in this organization.

```endpoint
CALL removeUser(address)
```

#### Parameters

```solidity
_userAccount // the account to deactivate

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND if the user account does not exist in this organization
```

## DefaultProcessDefinition


The DefaultProcessDefinition contract is found within the bpm-model bundle.

### DefaultProcessDefinition >> addProcessInterfaceImplementation(address,bytes32)


Adds the specified process interface to the list of supported process interfaces of this ProcessDefinition The model address is allowed to be empty in which case this process definition's model will be used.

```endpoint
CALL addProcessInterfaceImplementation(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if the specified interface cannot be located in the modelBaseErrors.NO_ERROR() upon successful creation.
```

### DefaultProcessDefinition >> createActivityDefinition(bytes32,uint8,uint8,address,bool,bytes32)


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,address,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_application // the application handling the execution of the activity
_assignee // the address of an assignee (for interactive activities)
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an activity with the same ID already existsBaseErrors.RESOURCE_NOT_FOUND() if an application is specified, but does not exist in the modelBaseErrors.NO_ERROR() upon successful creation.
```

### DefaultProcessDefinition >> createTransition(bytes32,bytes32)


Creates a transition between the specified source and target activities.

```endpoint
CALL createTransition(bytes32,bytes32)
```

#### Parameters

```solidity
_sourceActivity // the start of the transition
_targetActivity // the end of the transition

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if a transition between the source and target already existsBaseErrors.NO_ERROR() upon successful creation.
```

### DefaultProcessDefinition >> getActivityAtIndex(uint256)


Returns the ID of the ActivityDefinition at the specified index position of the given Process Definition

```endpoint
CALL getActivityAtIndex(uint256)
```

#### Parameters

```solidity
_index // the index position

```

#### Return

```json
bytes32 the ActivityDefinition ID, if it exists
```

### DefaultProcessDefinition >> getActivityData(bytes32)


Returns information about the activity definition with the given ID.

```endpoint
CALL getActivityData(bytes32)
```

#### Parameters

```solidity
_id // the bytes32 id of the activity definition

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### DefaultProcessDefinition >> getActivityInputGateway(bytes32)


Returns the input gateway type of the specified activity.

```endpoint
CALL getActivityInputGateway(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity

```

#### Return

```json
the BpmModel.GatewayType
```

### DefaultProcessDefinition >> getActivityOutputGateway(bytes32)


Returns the output gateway type of the specified activity.

```endpoint
CALL getActivityOutputGateway(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity

```

#### Return

```json
the BpmModel.GatewayType
```

### DefaultProcessDefinition >> getId()


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### DefaultProcessDefinition >> getImplementedProcessInterfaceAtIndex(uint256)


Returns information about the process interface at the given index

```endpoint
CALL getImplementedProcessInterfaceAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
modelAddress the interface's modelinterfaceId the interface ID
```

### DefaultProcessDefinition >> getModel()


Returns the address of the model which contains this process definition

```endpoint
CALL getModel()
```

#### Return

```json
the model address
```

### DefaultProcessDefinition >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### DefaultProcessDefinition >> getNumberOfActivities()


Returns the number of activity definitions in this ProcessDefinition.

```endpoint
CALL getNumberOfActivities()
```

#### Return

```json
the number of activity definitions
```

### DefaultProcessDefinition >> getNumberOfImplementedProcessInterfaces()


Returns the number of implemented process interfaces implemented by this ProcessDefinition

```endpoint
CALL getNumberOfImplementedProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```

### DefaultProcessDefinition >> getStartActivity()


Returns the ID of the start activity of this process definition. This value is set during the validate() function, if the process is valid.

```endpoint
CALL getStartActivity()
```

#### Return

```json
the ID of the identified start activity
```

### DefaultProcessDefinition >> implementsProcessInterface(address,bytes32)


indicates whether this ProcessDefinition implements the specified interface

```endpoint
CALL implementsProcessInterface(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
true if the interface is supported, false otherwise
```

### DefaultProcessDefinition >> isValid()


Returns the current validity state

```endpoint
CALL isValid()
```

#### Return

```json
true if valid, false otherwise
```

### DefaultProcessDefinition >> removeProcessInterfaceImplementation(address,bytes32)


Removes the specified process interface from the list of supported process interfaces of this ProcessDefinition

```endpoint
CALL removeProcessInterfaceImplementation(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
an error code signaling success or failure
```

### DefaultProcessDefinition >> setActivityInputGateway(bytes32,uint8)


Sets the input gateway of the specified activity to the given type.

```endpoint
CALL setActivityInputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```

### DefaultProcessDefinition >> setActivityOutputGateway(bytes32,uint8)


Sets the output gateway of the specified activity to the given type.

```endpoint
CALL setActivityOutputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```

### DefaultProcessDefinition >> validate()


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag. Currently performed validation: 1. There must be exactly one start activity, i.e. one activity with no inputs 2. Activities with more than 1 inputs/outputs must have a supporting input/output gateway type (OR, XOR, AND).

```endpoint
CALL validate()
```

#### Return

```json
valid - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```

## DefaultProcessInstance


The DefaultProcessInstance contract is found within the bpm-runtime bundle.

### DefaultProcessInstance >> completeActivity(bytes32,address)


Completes the specified activity

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the activity instance
_db // the BpmRuntimeDb required for changes to this ProcessInstance after the activity completes

```

#### Return

```json
BaseErrors.NO_ERROR() if successfulBaseErrors.RESOURCE_NOT_FOUND() if the activity instance cannot be locatedBaseErrors.INVALID_STATE() if the activity is not in a state to be completedBaseErrors.INVALID_ACTOR() if the msg.sender or tx.origin is not the assignee of the task
```

### DefaultProcessInstance >> execute(address)


Initiates execution of this ProcessInstance consisting of attempting to activate and process any activities and advance the state of the runtime graph.

```endpoint
CALL execute(address)
```

#### Parameters

```solidity
_db // a reference to the runtime DB in which this ProcessInstance is stored

```

#### Return

```json
error code indicating success or failure
```

### DefaultProcessInstance >> getActivityInstanceAtIndex(uint256)


Returns the globally unique ID of the activity instance at the specified index in the ProcessInstance.

```endpoint
CALL getActivityInstanceAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the bytes32 ID
```

### DefaultProcessInstance >> getActivityInstanceData(bytes32)


Returns information about the activity instance with the specified ID

```endpoint
CALL getActivityInstanceData(bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitionstate - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```

### DefaultProcessInstance >> getNumberOfActivityInstances()


Returns the number of activity instances currently contained in this ProcessInstance. Note that this number is subject to change as long as the process isntance is not completed.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```

### DefaultProcessInstance >> getProcessDefinition()


Returns the process definition on which this instance is based.

```endpoint
CALL getProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### DefaultProcessInstance >> getState()


Returns the state of this process instance

```endpoint
CALL getState()
```

#### Return

```json
the uint8 representation of the BpmRuntime.ProcessInstanceState
```

### DefaultProcessInstance >> initRuntime()


Initiates the runtime graph that handles the state of this ProcessInstance and activates the start activity. The state of this ProcessInstance must be CREATED. If initiation is successful, the state of this ProcessInstance is set to ACTIVE.

```endpoint
CALL initRuntime()
```

#### Return

```json
BaseErrors.INVALID_STATE() if the ProcessInstance is not in state CREATED.an error code if the runtime graph could not be created, e.g. if the process definition is corrupt.BaseErrors.NO_ERROR() otherwise
```

## DefaultProcessModel


The DefaultProcessModel contract is found within the bpm-model bundle.

### DefaultProcessModel >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### DefaultProcessModel >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### DefaultProcessModel >> addProcessInterface(bytes32)


Adds a process interface declaration to this ProcessModel that process definitions can refer to

```endpoint
CALL addProcessInterface(bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an interface with the given ID already exists, BaseErrors.NO_ERROR() otherwise
```

### DefaultProcessModel >> addServiceApplication(bytes32,address,bytes4)


Adds a Service application with the given parameters to this ProcessModel

```endpoint
CALL addServiceApplication(bytes32,address,bytes4)
```

#### Parameters

```solidity
_address // the location of the contract implementing the application
_function // the function to call on the application contract
_id // the ID of the application

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an application with the given ID already exists, BaseErrors.NO_ERROR() otherwise
```

### DefaultProcessModel >> addWebApplication(bytes32,bytes32)


Adds a Web application with the given parameters to this ProcessModel

```endpoint
CALL addWebApplication(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the ID of the application
_webForm // the form identifier (formHash) of the Web application

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an application with the given ID already exists, BaseErrors.NO_ERROR() otherwise
```

### DefaultProcessModel >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultProcessModel >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### DefaultProcessModel >> createProcessDefinition(bytes32,bytes32)


Creates a new process definition with the given parameters in this ProcessModel

```endpoint
CALL createProcessDefinition(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the process ID
_name // the process name

```

#### Return

```json
error - BaseErrors.RESOURCE_ALREADY_EXISTS(), if a process definition with the same ID already exists, BaseErrors.NO_ERROR() otherwisenewAddress - the address of the new ProcessDefinition when successful
```

### DefaultProcessModel >> fireProcessDefinitionUpdateEvent()


To be called by a registered process definition to signal an update. Causes the ProcessModel to emit an update event on behalf of the msg.sender

```endpoint
CALL fireProcessDefinitionUpdateEvent()
```

### DefaultProcessModel >> getApplicationAtIndex(uint256)


Returns the ID of the application at the given index

```endpoint
CALL getApplicationAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the application ID, if it exists
```

### DefaultProcessModel >> getApplicationData(bytes32)


Returns information about the application with the given ID

```endpoint
CALL getApplicationData(bytes32)
```

#### Parameters

```solidity
_id // the application ID

```

#### Return

```json
location the applications contract addressmethod the function signature of the application
```

### DefaultProcessModel >> getId()


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### DefaultProcessModel >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### DefaultProcessModel >> getNumberOfApplications()


Returns the number of applications defined in this ProcessModel

```endpoint
CALL getNumberOfApplications()
```

#### Return

```json
the number of applications
```

### DefaultProcessModel >> getNumberOfProcessDefinitions()


Returns the number of process definitions in this ProcessModel

```endpoint
CALL getNumberOfProcessDefinitions()
```

#### Return

```json
the number of process definitions
```

### DefaultProcessModel >> getNumberOfProcessInterfaces()


Returns the number of process interfaces declared in this ProcessModel

```endpoint
CALL getNumberOfProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```

### DefaultProcessModel >> getProcessDefinition(bytes32)


Returns the address of the ProcessDefinition with the specified ID

```endpoint
CALL getProcessDefinition(bytes32)
```

#### Parameters

```solidity
_id // the process ID

```

#### Return

```json
the address of the process definition, if it exists
```

### DefaultProcessModel >> getProcessDefinitionAtIndex(uint256)


Returns the address for the ProcessDefinition at the given index

```endpoint
CALL getProcessDefinitionAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the address of the ProcessDefinition, if it exists
```

### DefaultProcessModel >> getProcessDefinitionData(address)


Returns information about the ProcessDefinition at the given address

```endpoint
CALL getProcessDefinitionData(address)
```

#### Parameters

```solidity
_processDefinition // the address

```

#### Return

```json
id the process IDname the process nameinterfaceId the first process interface the process definition supports
```

### DefaultProcessModel >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### DefaultProcessModel >> hasApplication(bytes32)


Returns whether an application with the specified ID exists in this ProcessModel

```endpoint
CALL hasApplication(bytes32)
```

#### Parameters

```solidity
_id // the application ID

```

#### Return

```json
true if it exists, false otherwise
```

### DefaultProcessModel >> hasProcessInterface(bytes32)


Returns whether a process interface with the specified ID exists in this ProcessModel

```endpoint
CALL hasProcessInterface(bytes32)
```

#### Parameters

```solidity
_interfaceId // the interface ID

```

#### Return

```json
true if it exists, false otherwise
```

### DefaultProcessModel >> major()


returns the major version number

```endpoint
CALL major()
```

### DefaultProcessModel >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### DefaultProcessModel >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### DefaultProcessModel >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### DefaultProcessModel >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

## DefaultProcessModelRepository


The DefaultProcessModelRepository contract is found within the bpm-model bundle.

### DefaultProcessModelRepository >> activateModel(address)


Activates the given ProcessModel and deactivates any previously activated model version of the same ID

```endpoint
CALL activateModel(address)
```

#### Parameters

```solidity
_model // the ProcessModel to activate

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if the model ID and version is not registered in the repositoryBaseErrors.INVALID_STATE() if the model lookup produces an empty addressBaseErrors.INVALID_STATE_CHANGE() if the model registered model with the same ID and version has a different address than the specified one
```

### DefaultProcessModelRepository >> addModel(address)


Adds the given ProcessModel to this repository.

```endpoint
CALL addModel(address)
```

#### Parameters

```solidity
_model // the ProcessModel to add

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if a model with the same ID and version already existsBaseErrors.NO_ERROR() when added successfully
```

### DefaultProcessModelRepository >> createActivityDefinition(address,bytes32,uint8,uint8,address,bool,bytes32)


Creates a new activity definition on the given process definition with the specified parameters.

```endpoint
CALL createActivityDefinition(address,bytes32,uint8,uint8,address,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_address // process definition address
_application // the application handling the execution of the activity
_assignee // the address of an assignee (for interactive activities)
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
an error code indicating success or failure
```

### DefaultProcessModelRepository >> createProcessDefinition(address,bytes32,bytes32)


Creates a new process definition with the given parameters within the given process model

```endpoint
CALL createProcessDefinition(address,bytes32,bytes32)
```

#### Parameters

```solidity
_address // the process model
_id // the process ID
_name // the process name

```

#### Return

```json
error - BaseErrors.RESOURCE_ALREADY_EXISTS(), if a process definition with the same ID already exists, BaseErrors.NO_ERROR() otherwisenewAddress - the address of the new ProcessDefinition when successful
```

### DefaultProcessModelRepository >> createProcessModel(bytes32,bytes32,uint8[3])


Factory function to instantiate a ProcessModel. The model is automatically added to this repository.

```endpoint
CALL createProcessModel(bytes32,bytes32,uint8[3])
```

#### Parameters

```solidity
_id // the model ID
_name // the model name
_version // the model version

```

### DefaultProcessModelRepository >> createTransition(address,bytes32,bytes32)


Creates a transition between the specified source and target activities within the given process definition.

```endpoint
CALL createTransition(address,bytes32,bytes32)
```

#### Parameters

```solidity
_address // process definition address	 
_sourceActivity // the start of the transition
_targetActivity // the end of the transition

```

#### Return

```json
an error code indicating success or failure
```

### DefaultProcessModelRepository >> eventFired(bytes32,address)


Overwrites AbstractEventListener.eventFired to receive UPDATE_PROCESS_MODEL  and UPDATE_PROCESS_DEFINITION events from registered models.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the event source (process model)

```

### DefaultProcessModelRepository >> eventFired(bytes32,address,address)


Invoked by an EventEmitter for a named event with an additional address payload.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultProcessModelRepository >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultProcessModelRepository >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultProcessModelRepository >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### DefaultProcessModelRepository >> getActivityAtIndex(address,address,uint256)


Returns the ID of the ActivityDefinition at the specified index position of the given Process Definition

```endpoint
CALL getActivityAtIndex(address,address,uint256)
```

#### Parameters

```solidity
_index // the index position
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
bytes32 the ActivityDefinition ID, if it exists
```

### DefaultProcessModelRepository >> getActivityData(address,address,bytes32)


Returns information about the activity definition with the given ID.

```endpoint
CALL getActivityData(address,address,bytes32)
```

#### Parameters

```solidity
_id // the bytes32 id of the activity definition
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### DefaultProcessModelRepository >> getModel(bytes32)


Returns the address of the activated model with the given ID

```endpoint
CALL getModel(bytes32)
```

#### Parameters

```solidity
_id // the model ID

```

#### Return

```json
the model address, if it exists and has an active version
```

### DefaultProcessModelRepository >> getModelAtIndex(uint256)


Returns the address of the ProcessModel at the given index position, if it exists

```endpoint
CALL getModelAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the model address
```

### DefaultProcessModelRepository >> getModelByVersion(bytes32,uint8[3])


Returns the address of the model with the given ID and version

```endpoint
CALL getModelByVersion(bytes32,uint8[3])
```

#### Parameters

```solidity
_id // the model ID
_version // the model version

```

#### Return

```json
the model address, if found
```

### DefaultProcessModelRepository >> getModelData(address)


Returns information about the ProcessModel at the given address

```endpoint
CALL getModelData(address)
```

#### Parameters

```solidity
_model // the ProcessModel address

```

#### Return

```json
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch version
```

### DefaultProcessModelRepository >> getNumberOfActivities(address,address)


Returns the number of Activity Definitions in the specified Process Definition

```endpoint
CALL getNumberOfActivities(address,address)
```

#### Parameters

```solidity
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
uint - the number of Activity Definitions
```

### DefaultProcessModelRepository >> getNumberOfModels()


Returns the number of models in this repository.

```endpoint
CALL getNumberOfModels()
```

#### Return

```json
size - the number of models
```

### DefaultProcessModelRepository >> getNumberOfProcessDefinitions(address)


Returns the number of process definitions in the specified model

```endpoint
CALL getNumberOfProcessDefinitions(address)
```

#### Parameters

```solidity
_model // a ProcessModel address

```

#### Return

```json
size - the number of process definitions
```

### DefaultProcessModelRepository >> getProcessDefinition(bytes32,bytes32)


Returns the process definition address when the model ID and process definition ID are provided

```endpoint
CALL getProcessDefinition(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // - the ProcessModel ID

```

#### Return

```json
_processId - the ProcessDefinition IDaddress - the ProcessDefinition address
```

### DefaultProcessModelRepository >> getProcessDefinitionAtIndex(address,uint256)


Returns the address of the ProcessDefinition at the specified index position of the given model

```endpoint
CALL getProcessDefinitionAtIndex(address,uint256)
```

#### Parameters

```solidity
_idx // the index position
_model // a ProcessModel address

```

#### Return

```json
the ProcessDefinition address, if it exists
```

### DefaultProcessModelRepository >> getProcessDefinitionData(address,address)


Returns data about the specified ProcessDefinition in the specified ProcessModel

```endpoint
CALL getProcessDefinitionData(address,address)
```

#### Parameters

```solidity
_model // a ProcessModel address
_processDefinition // a ProcessDefinition address

```

#### Return

```json
id - the ProcessDefinition IDname - the ProcessDefinition nameinterfaceId - the ProcessDefinition's first interface ID
```

### DefaultProcessModelRepository >> validateProcessDefinition(bytes32,bytes32)


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag. Currently performed validation: 1. There must be exactly one start activity, i.e. one activity with no inputs 2. Activities with more than 1 inputs/outputs must have a supporting input/output gateway type (OR, XOR, AND).

```endpoint
CALL validateProcessDefinition(bytes32,bytes32)
```

#### Return

```json
valid - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```

## DefaultUserAccount


The DefaultUserAccount contract is found within the commons-auth bundle.

### DefaultUserAccount >> getId()


Returns this account's ID

```endpoint
CALL getId()
```

### DefaultUserAccount >> getOrganization()


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```

### DefaultUserAccount >> getOwner()


Returns this account's owner

```endpoint
CALL getOwner()
```

### DefaultUserAccount >> secretIsValid(bytes32)


Validates secret

```endpoint
CALL secretIsValid(bytes32)
```

#### Parameters

```solidity
_secret // _secret

```

#### Return

```json
whether _secret is valid
```

### DefaultUserAccount >> setOrganization(address)


Sets the organization of this user account

```endpoint
CALL setOrganization(address)
```

#### Parameters

```solidity
_organization // the organization's address with which to associate this user account

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.OVERWRITE_NOT_ALLOWED() if the organization is already set
```

## Destructible


The Destructible contract is found within the commons-base bundle.

### Destructible >> destroy()


Transfers this contract's value to the owner and frees up storage

```endpoint
CALL destroy()
```

### Destructible >> isDestructible()


Function that can be actively checked to detect if the contract is a destructible contract.

```endpoint
CALL isDestructible()
```

## Document Interface


The Document Interface contract is found within the documents-commons bundle.

### Document Interface >> addVersion(string)


Registers a new document version

```endpoint
CALL addVersion(string)
```

#### Parameters

```solidity
_hash // the hash representing the version being added

```

#### Return

```json
an error code in case of problems
```

### Document Interface >> getName()


Returns the document's name

```endpoint
CALL getName()
```

#### Return

```json
the name
```

### Document Interface >> getNumberOfVersions()


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```

### Document Interface >> getVersionCreated(string)


Returns the creation date of the specified version hash

```endpoint
CALL getVersionCreated(string)
```

#### Parameters

```solidity
_hash // the desired version

```

#### Return

```json
the creation date, if the version exists
```

### Document Interface >> getVersionCreator(string)


Returns the account of the entity that created the specified version hash

```endpoint
CALL getVersionCreator(string)
```

#### Parameters

```solidity
_hash // the desired version

```

#### Return

```json
the creator's address, if the version exists
```

## Ecosystem Interface


The Ecosystem Interface contract is found within the commons-auth bundle.

### Ecosystem Interface >> addOrganization(address)


Adds the organization at the specified address to this Ecosystem.

```endpoint
CALL addOrganization(address)
```

#### Parameters

```solidity
_address // the Organization contract's address

```

#### Return

```json
error code
```

### Ecosystem Interface >> createOrganization(bytes32,bytes32,address[10])


Creates a new Organization with the specified parameters and adds it to this Ecosystem.

```endpoint
CALL createOrganization(bytes32,bytes32,address[10])
```

#### Parameters

```solidity
_approvers // the initial owners.
_id // the organization's ID
_name // the organization's name

```

#### Return

```json
error code and the address of the newly created organization, if successful
```

### Ecosystem Interface >> eventFired(bytes32,address)


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```

### Ecosystem Interface >> eventFired(bytes32,address,address)


Invoked by an EventEmitter for a named event with an additional address payload.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### Ecosystem Interface >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### Ecosystem Interface >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### Ecosystem Interface >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### Ecosystem Interface >> getApproverAtIndex(address,uint256)


Returns the approver's address at the given index position of the specified organization.

```endpoint
CALL getApproverAtIndex(address,uint256)
```

#### Parameters

```solidity
_organization // the organization's address
_pos // the index position

```

#### Return

```json
the approver's address, if the position exists
```

### Ecosystem Interface >> getApproverData(address,address)


Function supports SQLsol, but only returns the approver address parameter.

```endpoint
CALL getApproverData(address,address)
```

#### Parameters

```solidity
_approver // the approver's address
_organization // the organization's address

```

### Ecosystem Interface >> getNumberOfApprovers(address)


Returns the number of registered approvers in the specified organization.

```endpoint
CALL getNumberOfApprovers(address)
```

#### Parameters

```solidity
_organization // the organization's address

```

#### Return

```json
the number of approvers
```

### Ecosystem Interface >> getNumberOfOrganizations()


Returns the number of registered organizations.

```endpoint
CALL getNumberOfOrganizations()
```

#### Return

```json
the number of organizations
```

### Ecosystem Interface >> getNumberOfUsers(address)


returns the number of users associated with the specified organization

```endpoint
CALL getNumberOfUsers(address)
```

#### Parameters

```solidity
_organization // the organization's address

```

#### Return

```json
the number of users
```

### Ecosystem Interface >> getOrganization(bytes32)


Returns the address of the organization with the specified ID, if it exists

```endpoint
CALL getOrganization(bytes32)
```

#### Parameters

```solidity
_id // the organization's ID

```

#### Return

```json
the organization's address, if it exists
```

### Ecosystem Interface >> getOrganizationAtIndex(uint256)


Returns the organization at the specified index.

```endpoint
CALL getOrganizationAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address of the organization
```

### Ecosystem Interface >> getOrganizationData(address)


Returns the public data of the organization at the specified address

```endpoint
CALL getOrganizationData(address)
```

#### Parameters

```solidity
_organization // the address of an organization

```

#### Return

```json
the organization's ID and name
```

### Ecosystem Interface >> getUserAtIndex(address,uint256)


Returns the user's address at the given index position in the specified organization.

```endpoint
CALL getUserAtIndex(address,uint256)
```

#### Parameters

```solidity
_organization // the organization's address
_pos // the index position

```

#### Return

```json
the address or 0x0 if the position does not exist
```

### Ecosystem Interface >> getUserData(address,address)


Returns information about the specified user in the context of the given organization

```endpoint
CALL getUserData(address,address)
```

#### Parameters

```solidity
_organization // the organization's address
_user // the user's address

```

#### Return

```json
active - whether the user is activated in the organization
```

## EventEmitter Interface


The EventEmitter Interface contract is found within the bpm-model bundle.

### EventEmitter Interface >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### EventEmitter Interface >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### EventEmitter Interface >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### EventEmitter Interface >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

## EventListener


The EventListener contract is found within the bpm-model bundle.

### EventListener >> eventFired(bytes32,address)


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```

### EventListener >> eventFired(bytes32,address,address)


Invoked by an EventEmitter for a named event with an additional address payload.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### EventListener >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### EventListener >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### EventListener >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```


## HierarchyEnabled


The HierarchyEnabled contract is found within the commons-management bundle.

### HierarchyEnabled >> addChild(address)


Adds the given address as a child of this component

```endpoint
CALL addChild(address)
```

#### Parameters

```solidity
_child // the child to add

```

#### Return

```json
NO_ERROR if successful or INVALID_PARAM_VALUE if the parent-child relationship cannot be established.
```

### HierarchyEnabled >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### HierarchyEnabled >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### HierarchyEnabled >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### HierarchyEnabled >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

## IsoCountries Interface


The IsoCountries Interface contract is found within the commons-standards bundle.

### IsoCountries Interface >> appendNewVersion(address)


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```

### IsoCountries Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCountries Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCountries Interface >> getTargetVersion(uint8[3])


Retrieves the specified version

```endpoint
CALL getTargetVersion(uint8[3])
```

#### Parameters

```solidity
_targetVer // - the version to retrieve

```

#### Return

```json
targetAddr - address of the version to retrieve, 0x0 if not found
```

### IsoCountries Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### IsoCountries Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### IsoCountries Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### IsoCountries Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### IsoCountries Interface >> setLatest(address)


Sets the latest version, and recursively sets latest for preceeding links

```endpoint
CALL setLatest(address)
```

#### Parameters

```solidity
_latest // - the latest version

```

#### Return

```json
success - representing whether latest was successfully set for all links
```

### IsoCountries Interface >> setPredecessor()


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```

## IsoCountries100 Interface


The IsoCountries100 Interface contract is found within the commons-standards bundle.

### IsoCountries100 Interface >> appendNewVersion(address)


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```

### IsoCountries100 Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCountries100 Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCountries100 Interface >> getTargetVersion(uint8[3])


Retrieves the specified version

```endpoint
CALL getTargetVersion(uint8[3])
```

#### Parameters

```solidity
_targetVer // - the version to retrieve

```

#### Return

```json
targetAddr - address of the version to retrieve, 0x0 if not found
```

### IsoCountries100 Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### IsoCountries100 Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### IsoCountries100 Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### IsoCountries100 Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### IsoCountries100 Interface >> setLatest(address)


Sets the latest version, and recursively sets latest for preceeding links

```endpoint
CALL setLatest(address)
```

#### Parameters

```solidity
_latest // - the latest version

```

#### Return

```json
success - representing whether latest was successfully set for all links
```

### IsoCountries100 Interface >> setPredecessor()


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```

## IsoCurrencies Interface


The IsoCurrencies Interface contract is found within the commons-standards bundle.

### IsoCurrencies Interface >> appendNewVersion(address)


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```

### IsoCurrencies Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCurrencies Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCurrencies Interface >> getTargetVersion(uint8[3])


Retrieves the specified version

```endpoint
CALL getTargetVersion(uint8[3])
```

#### Parameters

```solidity
_targetVer // - the version to retrieve

```

#### Return

```json
targetAddr - address of the version to retrieve, 0x0 if not found
```

### IsoCurrencies Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### IsoCurrencies Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### IsoCurrencies Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### IsoCurrencies Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### IsoCurrencies Interface >> setLatest(address)


Sets the latest version, and recursively sets latest for preceeding links

```endpoint
CALL setLatest(address)
```

#### Parameters

```solidity
_latest // - the latest version

```

#### Return

```json
success - representing whether latest was successfully set for all links
```

### IsoCurrencies Interface >> setPredecessor()


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```

## IsoCurrencies100 Interface


The IsoCurrencies100 Interface contract is found within the commons-standards bundle.

### IsoCurrencies100 Interface >> appendNewVersion(address)


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```

### IsoCurrencies100 Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCurrencies100 Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### IsoCurrencies100 Interface >> getTargetVersion(uint8[3])


Retrieves the specified version

```endpoint
CALL getTargetVersion(uint8[3])
```

#### Parameters

```solidity
_targetVer // - the version to retrieve

```

#### Return

```json
targetAddr - address of the version to retrieve, 0x0 if not found
```

### IsoCurrencies100 Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### IsoCurrencies100 Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### IsoCurrencies100 Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### IsoCurrencies100 Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### IsoCurrencies100 Interface >> setLatest(address)


Sets the latest version, and recursively sets latest for preceeding links

```endpoint
CALL setLatest(address)
```

#### Parameters

```solidity
_latest // - the latest version

```

#### Return

```json
success - representing whether latest was successfully set for all links
```

### IsoCurrencies100 Interface >> setPredecessor()


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```

## LifecycleEnabled


The LifecycleEnabled contract is found within the commons-management bundle.

### LifecycleEnabled >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

## LifecycleHub


The LifecycleHub contract is found within the commons-management bundle.

### LifecycleHub >> addChild(address)


Adds the given address as a child of this component

```endpoint
CALL addChild(address)
```

#### Parameters

```solidity
_child // the child to add

```

#### Return

```json
NO_ERROR if successful or INVALID_PARAM_VALUE if the parent-child relationship cannot be established.
```

### LifecycleHub >> addContract(bytes32,address)


Adds the specified contract address to the locator under the given name.

```endpoint
CALL addContract(bytes32,address)
```

#### Parameters

```solidity
_address // the contract address
_name // the name to register

```

#### Return

```json
the number of contracts registered at the end of this operation
```

### LifecycleHub >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### LifecycleHub >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### LifecycleHub >> getContract(bytes32)


returns the address of the contract registered under the specified name. TODO can be extended in the future to include version!

```endpoint
CALL getContract(bytes32)
```

#### Parameters

```solidity
_name // the registered name

```

#### Return

```json
(errorcode, address) 
```

### LifecycleHub >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### LifecycleHub >> getNumberOfRegistrationContracts()


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```

### LifecycleHub >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### LifecycleHub >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### LifecycleHub >> isDestroyOnUpgrade()


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### LifecycleHub >> major()


returns the major version number

```endpoint
CALL major()
```

### LifecycleHub >> migrateFrom(address)


Implements the migration of state from the specified predecessor to this contract. This method can be used to 'read' the state of the other contract which is probably easier to achieve.

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
predecessor // the address from which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### LifecycleHub >> migrateTo(address)


Implements the migration of state this contract to the specified contract. This method can be used to 'write' the state from this contract to the success. It's probably a little less useful since it requires the successor contract to have appropriate functions to set state.

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
successor // the address to which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### LifecycleHub >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### LifecycleHub >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### LifecycleHub >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### LifecycleHub >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### LifecycleHub >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### LifecycleHub >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## LifecycleModule


The LifecycleModule contract is found within the commons-management bundle.

### LifecycleModule >> addChild(address)


Adds the given address as a child of this component

```endpoint
CALL addChild(address)
```

#### Parameters

```solidity
_child // the child to add

```

#### Return

```json
NO_ERROR if successful or INVALID_PARAM_VALUE if the parent-child relationship cannot be established.
```

### LifecycleModule >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### LifecycleModule >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### LifecycleModule >> getNumberOfChildren()


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```

### LifecycleModule >> getNumberOfRegistrationContracts()


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```

### LifecycleModule >> getParent()


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```

### LifecycleModule >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### LifecycleModule >> isDestroyOnUpgrade()


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### LifecycleModule >> major()


returns the major version number

```endpoint
CALL major()
```

### LifecycleModule >> migrateFrom(address)


Implements the migration of state from the specified predecessor to this contract. This method can be used to 'read' the state of the other contract which is probably easier to achieve.

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
predecessor // the address from which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### LifecycleModule >> migrateTo(address)


Implements the migration of state this contract to the specified contract. This method can be used to 'write' the state from this contract to the success. It's probably a little less useful since it requires the successor contract to have appropriate functions to set state.

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
successor // the address to which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### LifecycleModule >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### LifecycleModule >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### LifecycleModule >> setLifecycleOwner(address)


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```

### LifecycleModule >> setParent(address)


Sets the parent of this component

```endpoint
CALL setParent(address)
```

#### Parameters

```solidity
_parent // the parent

```

#### Return

```json
NO_ERROR if successful or OVERWRITE_NOT_ALLOWED if this module's parent had already been set.
```

### LifecycleModule >> setRoot(address)


Sets the hierarchy root to the given address, if it had not been set before and is not empty (0x0) If the root had already been set, only the root as msg.sender can change it to a new value.

```endpoint
CALL setRoot(address)
```

#### Parameters

```solidity
_address // the hierarchy root

```

#### Return

```json
BaseErrors.NO_ERROR() when successful, BaseErrors.INVALID_PARAM_VALUE() if address is empty, BaseErrors.OVERWRITE_NOT_ALLOWED() if already set and caller is not the current root
```

### LifecycleModule >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


## Mappings Library Public API Contract


The Mappings Library Public API Contract contract is found within the agreements bundle.

### Mappings Library Public API Contract >> addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter specifies whether duplicate values in the array are allowed.

```endpoint
CALL addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings Library Public API Contract >> addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter specifies whether duplicate values in the array are allowed.

```endpoint
CALL addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings Library Public API Contract >> addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter specifies whether duplicate values in the array are allowed.

```endpoint
CALL addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings Library Public API Contract >> addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter specifies whether duplicate values in the array are allowed.

```endpoint
CALL addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings Library Public API Contract >> addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter specifies whether duplicate values in the array are allowed.

```endpoint
CALL addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings Library Public API Contract >> clear(Mappings.AddressAddressArrayMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.AddressAddressArrayMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.AddressAddressMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.AddressAddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.AddressBytes32ArrayMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.AddressBytes32ArrayMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.AddressBytes32Map storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.AddressBytes32Map storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.Bytes32AddressArrayMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.Bytes32AddressArrayMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.Bytes32AddressMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.Bytes32AddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.Bytes32Bytes32Map storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.Bytes32Bytes32Map storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.Bytes32UintMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.Bytes32UintMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.UintAddressArrayMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.UintAddressArrayMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.UintAddressMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.UintAddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> clear(Mappings.UintBytes32ArrayMap storage)


Removes all entries stored in the given map.

```endpoint
CALL clear(Mappings.UintBytes32ArrayMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings Library Public API Contract >> exists(Mappings.AddressAddressArrayMap storage,address)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.AddressAddressMap storage,address)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.AddressAddressMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.AddressBytes32ArrayMap storage,address)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.AddressBytes32Map storage,address)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.AddressBytes32Map storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.Bytes32AddressArrayMap storage,bytes32)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.Bytes32AddressMap storage,bytes32)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.Bytes32Bytes32Map storage,bytes32)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.Bytes32UintMap storage,bytes32)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.Bytes32UintMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.UintAddressArrayMap storage,uint256)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.UintAddressMap storage,uint256)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> exists(Mappings.UintBytes32ArrayMap storage,uint256)


Checks whether the specified key exists in the given map.

```endpoint
CALL exists(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings Library Public API Contract >> get(Mappings.AddressAddressArrayMap storage,address)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.AddressAddressMap storage,address)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.AddressAddressMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.AddressBytes32ArrayMap storage,address)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.AddressBytes32Map storage,address)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.AddressBytes32Map storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.Bytes32AddressArrayMap storage,bytes32)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.Bytes32AddressMap storage,bytes32)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.Bytes32Bytes32Map storage,bytes32)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.Bytes32UintMap storage,bytes32)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.Bytes32UintMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.UintAddressArrayMap storage,uint256)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.UintAddressMap storage,uint256)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> get(Mappings.UintBytes32ArrayMap storage,uint256)


Returns the value registered at the specified key in the given map. 

```endpoint
CALL get(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the value
```

### Mappings Library Public API Contract >> insert(Mappings.AddressAddressArrayMap storage,address,address[])


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.AddressAddressArrayMap storage,address,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.AddressAddressMap storage,address,address)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.AddressAddressMap storage,address,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.AddressBytes32Map storage,address,bytes32)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.AddressBytes32Map storage,address,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.Bytes32AddressMap storage,bytes32,address)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.Bytes32AddressMap storage,bytes32,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.Bytes32UintMap storage,bytes32,uint256)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.Bytes32UintMap storage,bytes32,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.UintAddressArrayMap storage,uint256,address[])


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.UintAddressArrayMap storage,uint256,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.UintAddressMap storage,uint256,address)


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.UintAddressMap storage,uint256,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


Inserts the given value at the specified key in the provided map.

```endpoint
CALL insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.AddressAddressMap storage,address,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressAddressMap storage,address,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.AddressAddressMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.AddressBytes32Map storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.Bytes32UintMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codekey at _index
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.UintAddressMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the key at the given index.

```endpoint
CALL keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error codethe key
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorkeynextindex the next index, if there is one
```

### Mappings Library Public API Contract >> keyIndex(Mappings.AddressAddressArrayMap storage,address)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.AddressAddressMap storage,address)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.AddressAddressMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.AddressBytes32ArrayMap storage,address)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.AddressBytes32Map storage,address)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.AddressBytes32Map storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.Bytes32AddressMap storage,bytes32)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.Bytes32UintMap storage,bytes32)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.Bytes32UintMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.UintAddressArrayMap storage,uint256)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.UintAddressMap storage,uint256)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)


Returns the index of the given key.

```endpoint
CALL keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index
```

### Mappings Library Public API Contract >> remove(Mappings.AddressAddressArrayMap storage,address)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.AddressAddressMap storage,address)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.AddressAddressMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.AddressBytes32ArrayMap storage,address)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.AddressBytes32Map storage,address)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.AddressBytes32Map storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.Bytes32AddressArrayMap storage,bytes32)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.Bytes32AddressMap storage,bytes32)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.Bytes32Bytes32Map storage,bytes32)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.Bytes32UintMap storage,bytes32)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.Bytes32UintMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.UintAddressArrayMap storage,uint256)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.UintAddressMap storage,uint256)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> remove(Mappings.UintBytes32ArrayMap storage,uint256)


Removes the entry registered at the specified key in the provided map.

```endpoint
CALL remove(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
error code
```

### Mappings Library Public API Contract >> removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


Removes the specified value from the inner array in the given map structure. The bool parameter specifies whether 'all' occurences of the value should be deleted.

```endpoint
CALL removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)
```

#### Parameters

```solidity
_all // if true, all occurences of the value should be deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings Library Public API Contract >> removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


Removes the specified value from the inner array in the given map structure. The bool parameter specifies whether 'all' occurences of the value should be deleted.

```endpoint
CALL removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)
```

#### Parameters

```solidity
_all // if true, all occurences of the value should be deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings Library Public API Contract >> removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


Removes the specified value from the inner array in the given map structure. The bool parameter specifies whether 'all' occurences of the value should be deleted.

```endpoint
CALL removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)
```

#### Parameters

```solidity
_all // if true, all occurences of the value should be deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings Library Public API Contract >> removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


Removes the specified value from the inner array in the given map structure. The bool parameter specifies whether 'all' occurences of the value should be deleted.

```endpoint
CALL removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)
```

#### Parameters

```solidity
_all // if true, all occurences of the value should be deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings Library Public API Contract >> removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


Removes the specified value from the inner array in the given map structure. The bool parameter specifies whether 'all' occurences of the value should be deleted.

```endpoint
CALL removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)
```

#### Parameters

```solidity
_all // if true, all occurences of the value should be deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

### Mappings Library Public API Contract >> valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
errorvaluenextIndex the next index, if there is one
```

## Mappings API Library


The Mappings API Library contract is found within the commons-collections bundle.

### Mappings API Library >> addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter can be used to avoid duplicate values in the array.Note that the array will be automatically initiated even if there was no prior entry at the specified key. If you want to make sure the key is valid, use exists(key).

```endpoint
CALL addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings API Library >> addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter can be used to avoid duplicate values in the array.Note that the array will be automatically initiated even if there was no prior entry at the specified key. If you want to make sure the key is valid, use exists(key).

```endpoint
CALL addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings API Library >> addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter can be used to avoid duplicate values in the array.Note that the array will be automatically initiated even if there was no prior entry at the specified key. If you want to make sure the key is valid, use exists(key).

```endpoint
CALL addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings API Library >> addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter can be used to avoid duplicate values in the array.Note that the array will be automatically initiated even if there was no prior entry at the specified key. If you want to make sure the key is valid, use exists(key).

```endpoint
CALL addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings API Library >> addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


Adds the specified value to the array that is stored in the map under the given key. The boolean parameter can be used to avoid duplicate values in the array.Note that the array will be automatically initiated even if there was no prior entry at the specified key. If you want to make sure the key is valid, use exists(key).

```endpoint
CALL addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)
```

#### Parameters

```solidity
_key // the key for the array
_map // the map
_unique // set to true if the value should only be added if it does not already exist in the array
_value // the value to store in the array

```

#### Return

```json
the length of the array after the operation
```

### Mappings API Library >> clear(Mappings.AddressAddressArrayMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.AddressAddressArrayMap storage)
```

#### Parameters

```solidity
_map // the AddressArrayMap

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.AddressAddressMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.AddressAddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.AddressBytes32ArrayMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.AddressBytes32ArrayMap storage)
```

#### Parameters

```solidity
_map // the AddressBytes32ArrayMap

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.AddressBytes32Map storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.AddressBytes32Map storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.Bytes32AddressArrayMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.Bytes32AddressArrayMap storage)
```

#### Parameters

```solidity
_map // the AddressArrayMap

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.Bytes32AddressMap storage)


Removes all entries stored in the map.

```endpoint
CALL clear(Mappings.Bytes32AddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.Bytes32Bytes32Map storage)


Removes all entries stored in the map.

```endpoint
CALL clear(Mappings.Bytes32Bytes32Map storage)
```

#### Parameters

```solidity
_map // the Bytes32Bytes32Map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.Bytes32UintMap storage)


Removes all entries stored in the map.

```endpoint
CALL clear(Mappings.Bytes32UintMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.UintAddressArrayMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.UintAddressArrayMap storage)
```

#### Parameters

```solidity
_map // the AddressArrayMap

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.UintAddressMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.UintAddressMap storage)
```

#### Parameters

```solidity
_map // the map

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> clear(Mappings.UintBytes32ArrayMap storage)


Removes all entries stored in the mapping.

```endpoint
CALL clear(Mappings.UintBytes32ArrayMap storage)
```

#### Parameters

```solidity
_map // the AddressArrayMap

```

#### Return

```json
the number of removed entries
```

### Mappings API Library >> exists(Mappings.AddressAddressArrayMap storage,address)

```endpoint
CALL exists(Mappings.AddressAddressArrayMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.AddressAddressMap storage,address)

```endpoint
CALL exists(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.AddressBytes32ArrayMap storage,address)

```endpoint
CALL exists(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.AddressBytes32Map storage,address)

```endpoint
CALL exists(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.Bytes32AddressArrayMap storage,bytes32)

```endpoint
CALL exists(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.Bytes32AddressMap storage,bytes32)


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.Bytes32Bytes32Map storage,bytes32)


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.Bytes32UintMap storage,bytes32)


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.UintAddressArrayMap storage,uint256)

```endpoint
CALL exists(Mappings.UintAddressArrayMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.UintAddressMap storage,uint256)

```endpoint
CALL exists(Mappings.UintAddressMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> exists(Mappings.UintBytes32ArrayMap storage,uint256)

```endpoint
CALL exists(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```

### Mappings API Library >> get(Mappings.AddressAddressArrayMap storage,address)


Retrieves the address array in the map at the specified key.

```endpoint
CALL get(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the addresses array value registered at the specified key, or empty address[] if it doesn't exist
```

### Mappings API Library >> get(Mappings.AddressAddressMap storage,address)

```endpoint
CALL get(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```

### Mappings API Library >> get(Mappings.AddressBytes32ArrayMap storage,address)


Retrieves the bytes32 array in the map at the specified key.

```endpoint
CALL get(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressBytes32ArrayMap

```

#### Return

```json
the addresses array value registered at the specified key, or empty bytes32[] if it doesn't exist
```

### Mappings API Library >> get(Mappings.AddressBytes32Map storage,address)

```endpoint
CALL get(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
the value registered at the specified key, or an empty bytes32 if it doesn't exist
```

### Mappings API Library >> get(Mappings.Bytes32AddressArrayMap storage,bytes32)


Retrieves the address array in the map at the specified key.

```endpoint
CALL get(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the addresses array value registered at the specified key, or empty address[] if it doesn't exist
```

### Mappings API Library >> get(Mappings.Bytes32AddressMap storage,bytes32)

```endpoint
CALL get(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```

### Mappings API Library >> get(Mappings.Bytes32Bytes32Map storage,bytes32)

```endpoint
CALL get(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```

### Mappings API Library >> get(Mappings.Bytes32UintMap storage,bytes32)

```endpoint
CALL get(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
the value registered at the specified key
```

### Mappings API Library >> get(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the address array in the map at the specified key.

```endpoint
CALL get(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the addresses array value registered at the specified key, or empty address[] if it doesn't exist
```

### Mappings API Library >> get(Mappings.UintAddressMap storage,uint256)

```endpoint
CALL get(Mappings.UintAddressMap storage,uint256)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```

### Mappings API Library >> get(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the address array in the map at the specified key.

```endpoint
CALL get(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the addresses array value registered at the specified key, or empty bytes32[] if it doesn't exist
```

### Mappings API Library >> insert(Mappings.AddressAddressArrayMap storage,address,address[])


Inserts the given address array value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.AddressAddressArrayMap storage,address,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS()
```

### Mappings API Library >> insert(Mappings.AddressAddressMap storage,address,address)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.AddressAddressMap storage,address,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


Inserts the given bytes32 array value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS()
```

### Mappings API Library >> insert(Mappings.AddressBytes32Map storage,address,bytes32)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.AddressBytes32Map storage,address,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


Inserts the given address array value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS()
```

### Mappings API Library >> insert(Mappings.Bytes32AddressMap storage,bytes32,address)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.Bytes32AddressMap storage,bytes32,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressMap
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the Bytes32Bytes32Map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.Bytes32UintMap storage,bytes32,uint256)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.Bytes32UintMap storage,bytes32,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the Uint Map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.UintAddressArrayMap storage,uint256,address[])


Inserts the given address array value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.UintAddressArrayMap storage,uint256,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS()
```

### Mappings API Library >> insert(Mappings.UintAddressMap storage,uint256,address)


Inserts the given value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.UintAddressMap storage,uint256,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_ALREADY_EXISTS
```

### Mappings API Library >> insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


Inserts the given bytes32 array value at the specified key in the provided map, but only if the key does not exist, yet. The `insert` function essentially behaves like a database insert in that it avoids entering duplicate keys. In most cases you'd want to use `insertOrUpdate(...)`

```endpoint
CALL insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_ALREADY_EXISTS()
```

### Mappings API Library >> insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])


Inserts or updates the given address array value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.AddressAddressMap storage,address,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressAddressMap storage,address,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


Inserts or updates the given address array value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


Inserts or updates the given address array value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressMap
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the Bytes32Bytes32Map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the Uint Map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])


Inserts or updates the given address array value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)


Inserts or updates the given value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


Inserts or updates the given address array value at the specified key in the provided map.

```endpoint
CALL insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])
```

#### Parameters

```solidity
_key // the key
_map // the map
_value // the value

```

#### Return

```json
the size of the map after the operation
```

### Mappings API Library >> keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.AddressAddressMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), 0x0)
```

### Mappings API Library >> keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressBytes32ArrayMap

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.AddressBytes32Map storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), 0x0)
```

### Mappings API Library >> keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the Bytes32Bytes32Map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.Bytes32UintMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndex(Mappings.UintAddressMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), uint(-1))
```

### Mappings API Library >> keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the key at the given index, if it exists.

```endpoint
CALL keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
(BaseErrors.NO_ERROR(), key) or (BaseErrors.INDEX_OUT_OF_BOUNDS(), "")
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or 0x0nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or 0x0nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or uint(-1)nextIndex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or 0x0nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or ""nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or ""nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the Bytes32Bytes32Map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or ""nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or ""nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or uint(-1)nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or uint(-1)nextindex the next index if there is one or 0
```

### Mappings API Library >> keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the key at the given index position and the index of the next artifact.

```endpoint
CALL keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS()key the key or uint(-1)nextindex the next index if there is one or 0
```

### Mappings API Library >> keyIndex(Mappings.AddressAddressArrayMap storage,address)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.AddressAddressMap storage,address)

```endpoint
CALL keyIndex(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.AddressBytes32ArrayMap storage,address)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressBytes32ArrayMap

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.AddressBytes32Map storage,address)

```endpoint
CALL keyIndex(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.Bytes32AddressMap storage,bytes32)

```endpoint
CALL keyIndex(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)

```endpoint
CALL keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.Bytes32UintMap storage,bytes32)

```endpoint
CALL keyIndex(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.UintAddressMap storage,uint256)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the index of the specified key.

```endpoint
CALL keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```

### Mappings API Library >> remove(Mappings.AddressAddressArrayMap storage,address)


Removes the address array registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.AddressAddressArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND().
```

### Mappings API Library >> remove(Mappings.AddressAddressMap storage,address)


Removes the entry registered at the specified key in the provided map.the _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.AddressAddressMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.AddressBytes32ArrayMap storage,address)


Removes the bytes32 array registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND().
```

### Mappings API Library >> remove(Mappings.AddressBytes32Map storage,address)


Removes the entry registered at the specified key in the provided map.the _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.AddressBytes32Map storage,address)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.Bytes32AddressArrayMap storage,bytes32)


Removes the address array registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND().
```

### Mappings API Library >> remove(Mappings.Bytes32AddressMap storage,bytes32)


Removes the entry registered at the specified key in the provided map.the _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the AddressMap

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.Bytes32Bytes32Map storage,bytes32)


Removes the entry registered at the specified key in the provided map.the _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the Bytes32Bytes32Map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.Bytes32UintMap storage,bytes32)


Removes the entry registered at the specified key in the provided map.the _map.keys array may get re-ordered by this operation: unless the removed entry was the last element in the map's keys, the last key will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.Bytes32UintMap storage,bytes32)
```

#### Parameters

```solidity
_key // the key
_map // the Uint Map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.UintAddressArrayMap storage,uint256)


Removes the address array registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND().
```

### Mappings API Library >> remove(Mappings.UintAddressMap storage,uint256)


Removes the entry registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR or BaseErrors.RESOURCE_NOT_FOUND.
```

### Mappings API Library >> remove(Mappings.UintBytes32ArrayMap storage,uint256)


Removes the address array registered at the specified key in the provided map.the _map.keys array might get re-ordered by this operation: if the removed entry was not the last element in the map's keys, the last element will be moved into the void position created by the removal.

```endpoint
CALL remove(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_key // the key
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.RESOURCE_NOT_FOUND().
```

### Mappings API Library >> removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


Removes the given value from the inner array in the given map structure. The bool parameter controls if 'all' occurences of the value should be deleted.Searching for the value to be deleted starts at the end of the array, but LIFO is not guaranteed, because entries can be moved around as part of this function, i.e. when the deletion does not happen to be at the end of the array, the last entry is swapped into position of the deleted item and the array is truncated at the end.

```endpoint
CALL removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)
```

#### Parameters

```solidity
_all // if true, the entire array will be traversed and all occurences deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings API Library >> removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


Removes the given value from the inner array in the given map structure. The bool parameter controls if 'all' occurences of the value should be deleted.Searching for the value to be deleted starts at the end of the array, but LIFO is not guaranteed, because entries can be moved around as part of this function, i.e. when the deletion does not happen to be at the end of the array, the last entry is swapped into position of the deleted item and the array is truncated at the end.

```endpoint
CALL removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)
```

#### Parameters

```solidity
_all // if true, the entire array will be traversed and all occurences deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings API Library >> removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


Removes the given value from the inner array in the given map structure. The bool parameter controls if 'all' occurences of the value should be deleted.Searching for the value to be deleted starts at the end of the array, but LIFO is not guaranteed, because entries can be moved around as part of this function, i.e. when the deletion does not happen to be at the end of the array, the last entry is swapped into position of the deleted item and the array is truncated at the end.

```endpoint
CALL removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)
```

#### Parameters

```solidity
_all // if true, the entire array will be traversed and all occurences deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings API Library >> removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


Removes the given value from the inner array in the given map structure. The bool parameter controls if 'all' occurences of the value should be deleted.Searching for the value to be deleted starts at the end of the array, but LIFO is not guaranteed, because entries can be moved around as part of this function, i.e. when the deletion does not happen to be at the end of the array, the last entry is swapped into position of the deleted item and the array is truncated at the end.

```endpoint
CALL removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)
```

#### Parameters

```solidity
_all // if true, the entire array will be traversed and all occurences deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings API Library >> removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


Removes the given value from the inner array in the given map structure. The bool parameter controls if 'all' occurences of the value should be deleted.Searching for the value to be deleted starts at the end of the array, but LIFO is not guaranteed, because entries can be moved around as part of this function, i.e. when the deletion does not happen to be at the end of the array, the last entry is swapped into position of the deleted item and the array is truncated at the end.

```endpoint
CALL removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)
```

#### Parameters

```solidity
_all // if true, the entire array will be traversed and all occurences deleted, if false only the first encountered one
_key // the key for the array
_map // the map
_value // the value to be deleted in the array

```

#### Return

```json
the resulting array length
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


Retrieves the array at the given index position and the index of the next array.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value or address[], and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


Retrieves the array at the given index position and the index of the next array.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value or bytes32[], and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


Retrieves the array at the given index position and the index of the next array.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value or address[], and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


Retrieves the value at the given index position and the index of the next address.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the Bytes32Bytes32Map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


Retrieves the value at the given index position and the index of the next value.

```endpoint
CALL valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


Retrieves the array at the given index position and the index of the next array.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value or address[], and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


Retrieves the value at the given index position and the index of the next address.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the map

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value, and nextIndex
```

### Mappings API Library >> valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


Retrieves the array at the given index position and the index of the next array.Internal function to retrieve the value and nextIndex from a given Map

```endpoint
CALL valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Parameters

```solidity
_index // the index
_map // the AddressArrayMap

```

#### Return

```json
BaseErrors.NO_ERROR() or BaseErrors.INDEX_OUT_OF_BOUNDS(), value or bytes32[], and nextIndex
```

## Migratable Interface


The Migratable Interface contract is found within the commons-management bundle.

### Migratable Interface >> migrateFrom(address)


Implements the migration of state from the specified predecessor to this contract. This method can be used to 'read' the state of the other contract which is probably easier to achieve.

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
predecessor // the address from which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### Migratable Interface >> migrateTo(address)


Implements the migration of state this contract to the specified contract. This method can be used to 'write' the state from this contract to the success. It's probably a little less useful since it requires the successor contract to have appropriate functions to set state.

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
successor // the address to which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

## Named Interface


The Named Interface contract is found within the agreements bundle.

### Named Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

## NamedElement Interface


The NamedElement Interface contract is found within the bpm-model bundle.

### NamedElement Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### NamedElement Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

## Organization Interface


The Organization Interface contract is found within the commons-auth bundle.

### Organization Interface >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### Organization Interface >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### Organization Interface >> addUser(address)


Adds the specified user to this organization

```endpoint
CALL addUser(address)
```

#### Parameters

```solidity
_userAccount // the user to add

```

#### Return

```json
error code indicating success or failure
```

### Organization Interface >> getApproverAtIndex(uint256)


Returns the approver's address at the given index position.

```endpoint
CALL getApproverAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address, if the position exists
```

### Organization Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### Organization Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### Organization Interface >> getNumberOfApprovers()


Returns the number of registered approvers.

```endpoint
CALL getNumberOfApprovers()
```

#### Return

```json
the number of approvers
```

### Organization Interface >> getNumberOfUsers()


returns the number of users associated with this organization

```endpoint
CALL getNumberOfUsers()
```

#### Return

```json
the number of users
```

### Organization Interface >> getUserAtIndex(uint256)


Returns the user's address at the given index position.

```endpoint
CALL getUserAtIndex(uint256)
```

#### Parameters

```solidity
_pos // the index position

```

#### Return

```json
the address or 0x0 if the position does not exist
```

### Organization Interface >> isActiveUser(address)


Returns whether the given user account is active in this organization

```endpoint
CALL isActiveUser(address)
```

#### Parameters

```solidity
_userAccount // the user account

```

#### Return

```json
true if valid, false otherwise
```

### Organization Interface >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### Organization Interface >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

### Organization Interface >> removeUser(address)


Removes / Deactivates the user in this organization.

```endpoint
CALL removeUser(address)
```

#### Parameters

```solidity
_userAccount // the account to deactivate

```

#### Return

```json
error code indicating success or failure
```



## ProcessDefinition Interface


The ProcessDefinition Interface contract is found within the bpm-model bundle.

### ProcessDefinition Interface >> addProcessInterfaceImplementation(address,bytes32)


Adds the specified process interface to the list of supported process interfaces of this ProcessDefinition

```endpoint
CALL addProcessInterfaceImplementation(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
an error code signaling success or failure
```

### ProcessDefinition Interface >> createActivityDefinition(bytes32,uint8,uint8,address,bool,bytes32)


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,address,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_application // the application handling the execution of the activity
_assignee // the address of an assignee (for interactive activities)
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
an error code indicating success or failure
```

### ProcessDefinition Interface >> createTransition(bytes32,bytes32)


Creates a transition between the specified source and target activities.

```endpoint
CALL createTransition(bytes32,bytes32)
```

#### Parameters

```solidity
_sourceActivity // the start of the transition
_targetActivity // the end of the transition

```

#### Return

```json
an error code indicating success or failure
```

### ProcessDefinition Interface >> getActivityAtIndex(uint256)


Returns the ID of the ActivityDefinition at the specified index position of the given Process Definition

```endpoint
CALL getActivityAtIndex(uint256)
```

#### Parameters

```solidity
_index // the index position

```

#### Return

```json
bytes32 the ActivityDefinition ID, if it exists
```

### ProcessDefinition Interface >> getActivityData(bytes32)


Returns information about the activity definition with the given ID.

```endpoint
CALL getActivityData(bytes32)
```

#### Parameters

```solidity
_id // the bytes32 id of the activity definition

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### ProcessDefinition Interface >> getActivityInputGateway(bytes32)


Returns the input gateway type of the specified activity.

```endpoint
CALL getActivityInputGateway(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity

```

#### Return

```json
the BpmModel.GatewayType
```

### ProcessDefinition Interface >> getActivityOutputGateway(bytes32)


Returns the output gateway type of the specified activity.

```endpoint
CALL getActivityOutputGateway(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity

```

#### Return

```json
the BpmModel.GatewayType
```

### ProcessDefinition Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### ProcessDefinition Interface >> getImplementedProcessInterfaceAtIndex(uint256)


Returns information about the process interface at the given index

```endpoint
CALL getImplementedProcessInterfaceAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
modelAddress the interface's modelinterfaceId the interface ID
```

### ProcessDefinition Interface >> getModel()


Returns the address of the model which contains this process definition

```endpoint
CALL getModel()
```

#### Return

```json
the model address
```

### ProcessDefinition Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### ProcessDefinition Interface >> getNumberOfActivities()


Returns the number of activity definitions in this ProcessDefinition.

```endpoint
CALL getNumberOfActivities()
```

#### Return

```json
the number of activity definitions
```

### ProcessDefinition Interface >> getNumberOfImplementedProcessInterfaces()


Returns the number of implemented process interfaces implemented by this ProcessDefinition

```endpoint
CALL getNumberOfImplementedProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```

### ProcessDefinition Interface >> getStartActivity()


Returns the ID of the start activity of this process definition. If the process is valid, this value must be set.

```endpoint
CALL getStartActivity()
```

#### Return

```json
the ID of the identified start activity
```

### ProcessDefinition Interface >> implementsProcessInterface(address,bytes32)


indicates whether this ProcessDefinition implements the specified interface

```endpoint
CALL implementsProcessInterface(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
true if the interface is supported, false otherwise
```

### ProcessDefinition Interface >> isValid()


Returns the current validity state

```endpoint
CALL isValid()
```

#### Return

```json
true if valid, false otherwise
```

### ProcessDefinition Interface >> removeProcessInterfaceImplementation(address,bytes32)


Removes the specified process interface from the list of supported process interfaces of this ProcessDefinition

```endpoint
CALL removeProcessInterfaceImplementation(address,bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface
_model // the model defining the interface

```

#### Return

```json
an error code signaling success or failure
```

### ProcessDefinition Interface >> setActivityInputGateway(bytes32,uint8)


Sets the input gateway of the specified activity to the given type.

```endpoint
CALL setActivityInputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```

### ProcessDefinition Interface >> setActivityOutputGateway(bytes32,uint8)


Sets the output gateway of the specified activity to the given type.

```endpoint
CALL setActivityOutputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```

### ProcessDefinition Interface >> validate()


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag.

```endpoint
CALL validate()
```

#### Return

```json
valid - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```

## ProcessInstance Interface


The ProcessInstance Interface contract is found within the bpm-runtime bundle.

### ProcessInstance Interface >> completeActivity(bytes32,address)


Completes the specified activity

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the activity instance
_db // the BpmRuntimeDb required for changes to this ProcessInstance after the activity completes

```

#### Return

```json
an error code indicating success or failure
```

### ProcessInstance Interface >> execute(address)


Initiates execution of this ProcessInstance consisting of attempting to activate and process any activities and advance the state of the runtime graph.

```endpoint
CALL execute(address)
```

#### Parameters

```solidity
_db // a reference to the runtime DB in which this ProcessInstance is stored

```

#### Return

```json
error code indicating success or failure
```

### ProcessInstance Interface >> getActivityInstanceAtIndex(uint256)


Returns the globally unique ID of the activity instance at the specified index in the ProcessInstance.

```endpoint
CALL getActivityInstanceAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the bytes32 ID
```

### ProcessInstance Interface >> getActivityInstanceData(bytes32)


Returns information about the activity instance with the specified ID

```endpoint
CALL getActivityInstanceData(bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitionstate - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```

### ProcessInstance Interface >> getNumberOfActivityInstances()


Returns the number of activity instances currently contained in this ProcessInstance. Note that this number is subject to change as long as the process isntance is not completed.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```

### ProcessInstance Interface >> getProcessDefinition()


Returns the process definition on which this instance is based.

```endpoint
CALL getProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```

### ProcessInstance Interface >> getState()


Returns the state of this process instance

```endpoint
CALL getState()
```

#### Return

```json
the uint representation of the BpmRuntime.ProcessInstanceState
```

### ProcessInstance Interface >> initRuntime()


Initiates and populates the runtime graph that will handle the state of this ProcessInstance

```endpoint
CALL initRuntime()
```

#### Return

```json
error code indicating success or failure
```

## ProcessModel Interface


The ProcessModel Interface contract is found within the bpm-model bundle.

### ProcessModel Interface >> addEventListener(bytes32)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```

### ProcessModel Interface >> addEventListener(bytes32,address)


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```

### ProcessModel Interface >> addProcessInterface(bytes32)


Adds a process interface declaration to this ProcessModel that process definitions can refer to

```endpoint
CALL addProcessInterface(bytes32)
```

#### Parameters

```solidity
_interfaceId // the ID of the interface

```

#### Return

```json
an error code indicating success of failure
```

### ProcessModel Interface >> addServiceApplication(bytes32,address,bytes4)


Adds a Service application with the given parameters to this ProcessModel

```endpoint
CALL addServiceApplication(bytes32,address,bytes4)
```

#### Parameters

```solidity
_address // the location of the contract implementing the application
_function // the function to call on the application contract
_id // the ID of the application

```

#### Return

```json
an error code indicating success or failure
```

### ProcessModel Interface >> addWebApplication(bytes32,bytes32)


Adds a Web application with the given parameters to this ProcessModel

```endpoint
CALL addWebApplication(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the ID of the application
_webForm // the form identifier (formHash) of the Web application

```

#### Return

```json
an error code indicating success or failure
```

### ProcessModel Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### ProcessModel Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### ProcessModel Interface >> createProcessDefinition(bytes32,bytes32)


Creates a new process definition with the given parameters in this ProcessModel

```endpoint
CALL createProcessDefinition(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the process ID
_name // the process name

```

#### Return

```json
an error code indicating success or failurethe address of the new ProcessDefinition when successful
```

### ProcessModel Interface >> fireProcessDefinitionUpdateEvent()


To be called by a registered process definition to signal an update.

```endpoint
CALL fireProcessDefinitionUpdateEvent()
```

### ProcessModel Interface >> getApplicationAtIndex(uint256)


Returns the ID of the application at the given index

```endpoint
CALL getApplicationAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the application ID, if it exists
```

### ProcessModel Interface >> getApplicationData(bytes32)


Returns information about the application with the given ID

```endpoint
CALL getApplicationData(bytes32)
```

#### Parameters

```solidity
_id // the application ID

```

#### Return

```json
location the applications contract address, only available for a service applicationmethod the function signature of the application, only available for a service applicationwebForm the form identifier (formHash) of the web application, only available for a web application
```

### ProcessModel Interface >> getId()


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### ProcessModel Interface >> getName()


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```

### ProcessModel Interface >> getNumberOfApplications()


Returns the number of applications defined in this ProcessModel

```endpoint
CALL getNumberOfApplications()
```

#### Return

```json
the number of applications
```

### ProcessModel Interface >> getNumberOfProcessDefinitions()


Returns the number of process definitions in this ProcessModel

```endpoint
CALL getNumberOfProcessDefinitions()
```

#### Return

```json
the number of process definitions
```

### ProcessModel Interface >> getNumberOfProcessInterfaces()


Returns the number of process interfaces declared in this ProcessModel

```endpoint
CALL getNumberOfProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```

### ProcessModel Interface >> getProcessDefinition(bytes32)


Returns the address of the ProcessDefinition with the specified ID

```endpoint
CALL getProcessDefinition(bytes32)
```

#### Parameters

```solidity
_id // the process ID

```

#### Return

```json
the address of the process definition, if it exists
```

### ProcessModel Interface >> getProcessDefinitionAtIndex(uint256)


Returns the address for the ProcessDefinition at the given index

```endpoint
CALL getProcessDefinitionAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the address of the ProcessDefinition, if it exists
```

### ProcessModel Interface >> getProcessDefinitionData(address)


Returns information about the ProcessDefinition at the given address

```endpoint
CALL getProcessDefinitionData(address)
```

#### Parameters

```solidity
_processDefinition // the address

```

#### Return

```json
id the process IDname the process nameinterfaceId the first process interface the process definition supports
```

### ProcessModel Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### ProcessModel Interface >> hasApplication(bytes32)


Returns whether an application with the specified ID exists in this ProcessModel

```endpoint
CALL hasApplication(bytes32)
```

#### Parameters

```solidity
_id // the application ID

```

#### Return

```json
true if it exists, false otherwise
```

### ProcessModel Interface >> hasProcessInterface(bytes32)


Returns whether a process interface with the specified ID exists in this ProcessModel

```endpoint
CALL hasProcessInterface(bytes32)
```

#### Parameters

```solidity
_interfaceId // the interface ID

```

#### Return

```json
true if it exists, false otherwise
```

### ProcessModel Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### ProcessModel Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### ProcessModel Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### ProcessModel Interface >> removeEventListener(bytes32)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```

### ProcessModel Interface >> removeEventListener(bytes32,address)


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```

## ProcessModelRepository Interface


The ProcessModelRepository Interface contract is found within the bpm-model bundle.

### ProcessModelRepository Interface >> activateModel(address)


Activates the given ProcessModel and deactivates any previously activated model version of the same ID

```endpoint
CALL activateModel(address)
```

#### Parameters

```solidity
_model // the ProcessModel to activate

```

#### Return

```json
an error indicating success or failure
```

### ProcessModelRepository Interface >> addModel(address)


Adds the given ProcessModel to this repository.

```endpoint
CALL addModel(address)
```

#### Parameters

```solidity
_model // the ProcessModel to add

```

#### Return

```json
an error indicating success or failure
```

### ProcessModelRepository Interface >> createActivityDefinition(address,bytes32,uint8,uint8,address,bool,bytes32)


Creates a new activity definition on the given process definition with the specified parameters.

```endpoint
CALL createActivityDefinition(address,bytes32,uint8,uint8,address,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_address // process definition address
_application // the application handling the execution of the activity
_assignee // the address of an assignee (for interactive activities)
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
an error code indicating success or failure
```

### ProcessModelRepository Interface >> createProcessDefinition(address,bytes32,bytes32)


Creates a new process definition with the given parameters within the given process model

```endpoint
CALL createProcessDefinition(address,bytes32,bytes32)
```

#### Parameters

```solidity
_address // the process model
_id // the process ID
_name // the process name

```

#### Return

```json
error - BaseErrors.RESOURCE_ALREADY_EXISTS(), if a process definition with the same ID already exists, BaseErrors.NO_ERROR() otherwisenewAddress - the address of the new ProcessDefinition when successful
```

### ProcessModelRepository Interface >> createProcessModel(bytes32,bytes32,uint8[3])


Factory function to instantiate a ProcessModel.

```endpoint
CALL createProcessModel(bytes32,bytes32,uint8[3])
```

#### Parameters

```solidity
_id // the model ID
_name // the model name
_version // the model version

```

### ProcessModelRepository Interface >> createTransition(address,bytes32,bytes32)


Creates a transition between the specified source and target activities within the given process definition.

```endpoint
CALL createTransition(address,bytes32,bytes32)
```

#### Parameters

```solidity
_address // process definition address	 
_sourceActivity // the start of the transition
_targetActivity // the end of the transition

```

#### Return

```json
an error code indicating success or failure
```

### ProcessModelRepository Interface >> eventFired(bytes32,address)


Overwrites AbstractEventListener.eventFired to receive UPDATE_PROCESS_MODEL  and UPDATE_PROCESS_DEFINITION events from registered models.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the event source (process model)

```

### ProcessModelRepository Interface >> eventFired(bytes32,address,address)


Invoked by an EventEmitter for a named event with an additional address payload.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### ProcessModelRepository Interface >> eventFired(bytes32,address,bytes32)


Invoked by an EventEmitter for a named event with an additional bytes32 payload.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### ProcessModelRepository Interface >> eventFired(bytes32,address,string)


Invoked by an EventEmitter for a named event with an additional string payload.

```endpoint
CALL eventFired(bytes32,address,string)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### ProcessModelRepository Interface >> eventFired(bytes32,address,uint256)


Invoked by an EventEmitter for a named event with an additional uint payload.

```endpoint
CALL eventFired(bytes32,address,uint256)
```

#### Parameters

```solidity
_data // the payload
_event // the event name
_source // the source of the event

```

### ProcessModelRepository Interface >> getActivityAtIndex(address,address,uint256)


Returns the ID of the ActivityDefinition at the specified index position of the given Process Definition

```endpoint
CALL getActivityAtIndex(address,address,uint256)
```

#### Parameters

```solidity
_index // the index position
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
bytes32 the ActivityDefinition ID, if it exists
```

### ProcessModelRepository Interface >> getActivityData(address,address,bytes32)


Returns information about the activity definition with the given ID.

```endpoint
CALL getActivityData(address,address,bytes32)
```

#### Parameters

```solidity
_id // the bytes32 id of the activity definition
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the address of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
```

### ProcessModelRepository Interface >> getModel(bytes32)


Returns the address of the activated model with the given ID, if it exists and is activated

```endpoint
CALL getModel(bytes32)
```

#### Parameters

```solidity
_id // the model ID

```

#### Return

```json
the model address, if found
```

### ProcessModelRepository Interface >> getModelAtIndex(uint256)


Returns the address of the ProcessModel at the given index position, if it exists

```endpoint
CALL getModelAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the model address
```

### ProcessModelRepository Interface >> getModelByVersion(bytes32,uint8[3])


Returns the address of the model with the given ID and version

```endpoint
CALL getModelByVersion(bytes32,uint8[3])
```

#### Parameters

```solidity
_id // the model ID
_version // the model version

```

#### Return

```json
the model address, if found
```

### ProcessModelRepository Interface >> getModelData(address)


Returns information about the ProcessModel at the given address

```endpoint
CALL getModelData(address)
```

#### Parameters

```solidity
_model // the ProcessModel address

```

#### Return

```json
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch version
```

### ProcessModelRepository Interface >> getNumberOfActivities(address,address)


Returns the number of Activity Definitions in the specified Process 

```endpoint
CALL getNumberOfActivities(address,address)
```

#### Parameters

```solidity
_model // the model address
_processDefinition // a Process Definition address

```

#### Return

```json
uint - the number of Activity Definitions
```

### ProcessModelRepository Interface >> getNumberOfModels()


Returns the number of models in this repository.

```endpoint
CALL getNumberOfModels()
```

#### Return

```json
size - the number of models
```

### ProcessModelRepository Interface >> getNumberOfProcessDefinitions(address)


Returns the number of process definitions in the specified model

```endpoint
CALL getNumberOfProcessDefinitions(address)
```

#### Parameters

```solidity
_model // a ProcessModel address

```

#### Return

```json
size - the number of process definitions
```

### ProcessModelRepository Interface >> getProcessDefinition(bytes32,bytes32)


Returns the process definition address when the model ID and process definition ID are provided

```endpoint
CALL getProcessDefinition(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // - the ProcessModel ID

```

#### Return

```json
_processId - the ProcessDefinition IDaddress - the ProcessDefinition address
```

### ProcessModelRepository Interface >> getProcessDefinitionAtIndex(address,uint256)


Returns the address of the ProcessDefinition at the specified index position of the given model

```endpoint
CALL getProcessDefinitionAtIndex(address,uint256)
```

#### Parameters

```solidity
_idx // the index position
_model // a ProcessModel address

```

#### Return

```json
the ProcessDefinition address, if it exists
```

### ProcessModelRepository Interface >> getProcessDefinitionData(address,address)


Returns data about the specified ProcessDefinition in the specified ProcessModel

```endpoint
CALL getProcessDefinitionData(address,address)
```

#### Parameters

```solidity
_model // a ProcessModel address
_processDefinition // a ProcessDefinition address

```

#### Return

```json
id - the ProcessDefinition IDname - the ProcessDefinition nameinterfaceId - the ProcessDefinition's first interface ID
```

### ProcessModelRepository Interface >> validateProcessDefinition(bytes32,bytes32)


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag. Currently performed validation: 1. There must be exactly one start activity, i.e. one activity with no inputs 2. Activities with more than 1 inputs/outputs must have a supporting input/output gateway type (OR, XOR, AND).

```endpoint
CALL validateProcessDefinition(bytes32,bytes32)
```

#### Return

```json
valid - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```

## SecureNativeAuthorizations Interface


The SecureNativeAuthorizations Interface contract is found within the commons-auth bundle.

### SecureNativeAuthorizations Interface >> addRole(address,bytes32)


Adds a role to an account

```endpoint
CALL addRole(address,bytes32)
```

#### Parameters

```solidity
_account // account address
_role // role name

```

#### Return

```json
result whether role was added
```

### SecureNativeAuthorizations Interface >> hasBase(address,uint64)


Indicates whether an account has a subset of permissions set

```endpoint
CALL hasBase(address,uint64)
```

#### Parameters

```solidity
_account // account address
_permission // the permissions flags (mask) to check whether enabled against base permissions for the account

```

#### Return

```json
result whether account has the passed permissions flags set
```

### SecureNativeAuthorizations Interface >> hasRole(address,bytes32)


Indicates whether an account has a role

```endpoint
CALL hasRole(address,bytes32)
```

#### Parameters

```solidity
_account // account address
_role // role name

```

#### Return

```json
result whether account has role
```

### SecureNativeAuthorizations Interface >> removeRole(address,bytes32)


Removes a role from an account

```endpoint
CALL removeRole(address,bytes32)
```

#### Parameters

```solidity
_account // account address
_role // role name

```

#### Return

```json
result whether role was removed
```

### SecureNativeAuthorizations Interface >> setBase(address,uint64,bool)


Sets the permission flags for an account. Makes them explicitly set (on or off).

```endpoint
CALL setBase(address,uint64,bool)
```

#### Parameters

```solidity
_account // account address
_permission // the base permissions flags to set for the account
_set // whether to set or unset the permissions flags at the account level

```

#### Return

```json
result the effective permissions flags on the account after the call
```

### SecureNativeAuthorizations Interface >> setGlobal(uint64,bool)


Sets the global (default) permissions flags for the entire chain

```endpoint
CALL setGlobal(uint64,bool)
```

#### Parameters

```solidity
_permission // the permissions flags to set
_set // whether to set (or unset) the permissions flags

```

#### Return

```json
result the global permissions flags after the call
```

### SecureNativeAuthorizations Interface >> unsetBase(address,uint64)


Unsets the permissions flags for an account. Causes permissions being unset to fall through to global permissions.

```endpoint
CALL unsetBase(address,uint64)
```

#### Parameters

```solidity
_account // account address
_permission // the permissions flags to unset for the account

```

#### Return

```json
result the effective permissions flags on the account after the call
```

## Signable


The Signable contract is found within the documents-commons bundle.

### Signable >> sign(address)


Applies a signature. The implementing function has the provided address, the msg.sender, or the tx.origin at their disposal.

```endpoint
CALL sign(address)
```

#### Parameters

```solidity
_address // the address to use as signature

```

#### Return

```json
a return code indicating success or type of failure
```

## SystemOwned


The SystemOwned contract is found within the bpm-runtime bundle.

### SystemOwned >> transferSystemOwnership(address)


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```

## TypeUtils Library Interface


The TypeUtils Library Interface contract is found within the agreements bundle.

### TypeUtils Library Interface >> contentLength(bytes32)


Returns the length of the alphanumeric content of the bytes32, i.e. the number of non-empty bytes

```endpoint
CALL contentLength(bytes32)
```

#### Parameters

```solidity
self // bytes32

```

#### Return

```json
the length
```

### TypeUtils Library Interface >> isEmpty(bytes32)


Checks if the given bytes32 is empty.

```endpoint
CALL isEmpty(bytes32)
```

#### Parameters

```solidity
_value // the value to check

```

#### Return

```json
true if empty, false otherwise
```

### TypeUtils Library Interface >> toBytes32(string)


Converts the given string to bytes32. If the string is longer than 32 byte-sized characters (depends on encoding and character-set), it will be truncated.

```endpoint
CALL toBytes32(string)
```

#### Parameters

```solidity
s // a string

```

#### Return

```json
the bytes32 representation
```

### TypeUtils Library Interface >> toBytes32(uint256)


Converts an unsigned integer to its string representation.

```endpoint
CALL toBytes32(uint256)
```

#### Parameters

```solidity
v // The number to be converted.

```

#### Return

```json
the bytes32 representation
```

## Upgradeable


The Upgradeable contract is found within the commons-management bundle.

### Upgradeable >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### Upgradeable >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### Upgradeable >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### Upgradeable >> isDestroyOnUpgrade()


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

### Upgradeable >> major()


returns the major version number

```endpoint
CALL major()
```

### Upgradeable >> migrateFrom(address)


Implements the migration of state from the specified predecessor to this contract. This method can be used to 'read' the state of the other contract which is probably easier to achieve.

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
predecessor // the address from which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### Upgradeable >> migrateTo(address)


Implements the migration of state this contract to the specified contract. This method can be used to 'write' the state from this contract to the success. It's probably a little less useful since it requires the successor contract to have appropriate functions to set state.

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
successor // the address to which the state is migrated

```

#### Return

```json
result the result of the operation, e.g. a constant from commons-base/BaseErrors.sol
```

### Upgradeable >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### Upgradeable >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### Upgradeable >> upgrade(address)


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```

## UserAccount Interface


The UserAccount Interface contract is found within the commons-auth bundle.

### UserAccount Interface >> getId()


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```

### UserAccount Interface >> getOrganization()


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```

### UserAccount Interface >> getOwner()


Returns this account's owner

```endpoint
CALL getOwner()
```

#### Return

```json
the owner address
```

### UserAccount Interface >> secretIsValid(bytes32)


Validates secret

```endpoint
CALL secretIsValid(bytes32)
```

#### Parameters

```solidity
_secret // _secret

```

#### Return

```json
whether _secret is valid
```

### UserAccount Interface >> setOrganization(address)


Sets the organization of this user account

```endpoint
CALL setOrganization(address)
```

#### Parameters

```solidity
_organization // the organization's address with which to associate this user account

```

#### Return

```json
error code indicating success or failure
```

## VersionLinked


The VersionLinked contract is found within the commons-management bundle.

### VersionLinked >> acceptVersionLink(address)


Adds the given VersionLinked contract into the linked version list or returns an error, if the operation is not possible

```endpoint
CALL acceptVersionLink(address)
```

#### Parameters

```solidity
_link // a new VersionedLink contract.

```

#### Return

```json
BaseErrors.NO_ERROR() if the given VersionLinked instance was successfully placed into the linked version list.
BaseErrors.NULL_PARAM_NOT_ALLOWED() if the _newPredecessor is empty (null address).
BaseErrors.INVALID_STATE() if the given VersionLinked instance has a different owner than this contract.
BaseErrors.INVALID_PARAM_VALUE() if the given VersionLinked instance has the same version or address as this contract.
```

### VersionLinked >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### VersionLinked >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### VersionLinked >> getOwner()


Returns the owner

```endpoint
CALL getOwner()
```

#### Return

```json
the address of the owner
```

### VersionLinked >> getPredecessor()


Returns the predecessor version

```endpoint
CALL getPredecessor()
```

#### Return

```json
the address of the predecessor or 0x0 if not set
```

### VersionLinked >> getSuccessor()


Returns the successor version

```endpoint
CALL getSuccessor()
```

#### Return

```json
the address of the successor or 0x0 if not set
```

### VersionLinked >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### VersionLinked >> major()


returns the major version number

```endpoint
CALL major()
```

### VersionLinked >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### VersionLinked >> patch()


returns the patch version number

```endpoint
CALL patch()
```

## VersionLinkedAppendOnly Interface


The VersionLinkedAppendOnly Interface contract is found within the commons-management bundle.

### VersionLinkedAppendOnly Interface >> appendNewVersion(address)


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```

### VersionLinkedAppendOnly Interface >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### VersionLinkedAppendOnly Interface >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### VersionLinkedAppendOnly Interface >> getTargetVersion(uint8[3])


Retrieves the specified version

```endpoint
CALL getTargetVersion(uint8[3])
```

#### Parameters

```solidity
_targetVer // - the version to retrieve

```

#### Return

```json
targetAddr - address of the version to retrieve, 0x0 if not found
```

### VersionLinkedAppendOnly Interface >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### VersionLinkedAppendOnly Interface >> major()


returns the major version number

```endpoint
CALL major()
```

### VersionLinkedAppendOnly Interface >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### VersionLinkedAppendOnly Interface >> patch()


returns the patch version number

```endpoint
CALL patch()
```

### VersionLinkedAppendOnly Interface >> setLatest(address)


Sets the latest version, and recursively sets latest for preceeding links

```endpoint
CALL setLatest(address)
```

#### Parameters

```solidity
_latest // - the latest version

```

#### Return

```json
success - representing whether latest was successfully set for all links
```

### VersionLinkedAppendOnly Interface >> setPredecessor()


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```

## Versioned


The Versioned contract is found within the bpm-model bundle.

### Versioned >> compareVersion(address)


Compares this contract's version to the version of the contract at the specified address.

```endpoint
CALL compareVersion(address)
```

#### Parameters

```solidity
_other // the address to which this contract is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### Versioned >> compareVersion(uint8[3])


Compares this contract's version to the specified version.

```endpoint
CALL compareVersion(uint8[3])
```

#### Parameters

```solidity
_version // the version to which this contract's version is compared

```

#### Return

```json
0 (equal), -1 (the other version is lower), or 1 (the other version is higher).
```

### Versioned >> getVersion()


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```

### Versioned >> major()


returns the major version number

```endpoint
CALL major()
```

### Versioned >> minor()


returns the minor version number

```endpoint
CALL minor()
```

### Versioned >> patch()


returns the patch version number

```endpoint
CALL patch()
```

## WorkflowBusinessAccount


The WorkflowBusinessAccount contract is found within the bpm-runtime bundle.

### WorkflowBusinessAccount >> addFunds(uint256)


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
```

### WorkflowBusinessAccount >> completeActivity(bytes32,address)


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService requried for lookup and access to the BpmRuntimeDb

```

#### Return

```json
error code if the completion failed
```

### WorkflowBusinessAccount >> getBalance()


Returns the current balance

```endpoint
CALL getBalance()
```

### WorkflowBusinessAccount >> getId()


Returns this account's ID

```endpoint
CALL getId()
```

### WorkflowBusinessAccount >> getName()


Returns this account's name

```endpoint
CALL getName()
```

### WorkflowBusinessAccount >> getOrganization()


Returns the address of the organization this accounts is associated with.

```endpoint
CALL getOrganization()
```

### WorkflowBusinessAccount >> getOwner()


Returns this account's owner

```endpoint
CALL getOwner()
```

### WorkflowBusinessAccount >> withdrawFunds(uint256)


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```

## WorkflowProxy


The WorkflowProxy contract is found within the bpm-runtime bundle.

### WorkflowProxy >> completeActivity(bytes32,address)


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService requried for lookup and access to the BpmRuntimeDb

```

#### Return

```json
error code if the completion failed
```
