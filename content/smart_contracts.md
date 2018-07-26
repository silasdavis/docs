## Agreements Network Contracts


The Agreements Network suite of smart contracts are solidity based and provide a near no-code solution for most of the users of the Network.


Below you will find the specifics on how to interact with the smart contracts via solidity based CALLS. These calls can be managed in a variety of ways, from other smart contracts or from various non-blockchain clients.

## agreements

### AbstractDataStorage


The AbstractDataStorage contract is found within the agreements bundle.

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Returns the number of non-default entries in the specified array-type DataStorage field

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if false the function will return as soon as a default value (0 for int/uint, 0x0 for address, "" for bytes32, etc.) is encountered, if true the array will be scanned to its end
_id // the key under which to find the array-type value

```

#### Return

```json
the number of non-default entries in the array
```


---

### DbUpgradeable


The DbUpgradeable contract is found within the agreements bundle.

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### AbstractEventListener


The AbstractEventListener contract is found within the agreements bundle.

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


See EventListener.eventFired(bytes32,address)

```endpoint
CALL eventFired(bytes32,address)
```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


See EventListener.eventFired(bytes32,address,address)

```endpoint
CALL eventFired(bytes32,address,address)
```


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


See EventListener.eventFired(bytes32,address,bytes32)

```endpoint
CALL eventFired(bytes32,address,bytes32)
```


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


See EventListener.eventFired(bytes32,address,string)

```endpoint
CALL eventFired(bytes32,address,string)
```


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


See EventListener.eventFired(bytes32,address,uint)

```endpoint
CALL eventFired(bytes32,address,uint256)
```


---

### AbstractNamedElement


The AbstractNamedElement contract is found within the agreements bundle.

#### getId()


**getId()**


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

### AccountsManager Interface


The AccountsManager Interface contract is found within the agreements bundle.

#### addBusinessAccount(address)


**addBusinessAccount(address)**


Adds the specified BusinessAccount

```endpoint
CALL addBusinessAccount(address)
```

#### Return

```json
an error code
```


---

#### addFunds(address,bytes32,uint256)


**addFunds(address,bytes32,uint256)**


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


---

#### addUserAccount(address)


**addUserAccount(address)**


Adds the specified UserAccount

```endpoint
CALL addUserAccount(address)
```

#### Return

```json
an error code
```


---

#### addUserToOrganization(address,address)


**addUserToOrganization(address,address)**


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


---

#### businessAccountExists(address,bytes32)


**businessAccountExists(address,bytes32)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createUserAccount(address,bytes32)


**createUserAccount(address,bytes32)**


Creates and adds a user account

```endpoint
CALL createUserAccount(address,bytes32)
```

#### Parameters

```solidity
_id // id (optional)
_owner // owner (optional)

```

#### Return

```json
error BaseErrors.NO_ERROR() or BaseErrors.RUNTIME_ERROR() if a runtime erroruserAccount user account
```


---

#### getBusinessAccount(address,bytes32)


**getBusinessAccount(address,bytes32)**


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


---

#### getBusinessAccount(bytes32)


**getBusinessAccount(bytes32)**


Returns the business account address for the specified business account ID.

```endpoint
CALL getBusinessAccount(bytes32)
```


---

#### getUserAccount(bytes32)


**getUserAccount(bytes32)**


Returns the user account address for the specified user account ID.

```endpoint
CALL getUserAccount(bytes32)
```


---

#### getUserAccountDataById(bytes32)


**getUserAccountDataById(bytes32)**


Gets hashed user account ID and user account address for the specified user account ID.

```endpoint
CALL getUserAccountDataById(bytes32)
```

#### Parameters

```solidity
_id // the user account ID

```

#### Return

```json
error RESOURCE_NOT_FOUND or NO_ERRORaddr user account addresshashedId hashed user account ID
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### removeUserFromOrganization(address,address)


**removeUserFromOrganization(address,address)**


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


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

#### userAccountExists(bytes32)


**userAccountExists(bytes32)**


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


---

#### withdrawFunds(address,bytes32,uint256)


**withdrawFunds(address,bytes32,uint256)**


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


---

### ActiveAgreement Interface


The ActiveAgreement Interface contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### cancel()


**cancel()**


Registers the msg.sender as having cancelled the agreement. During formation (legal states DRAFT and FORMULATED), the agreement can cancelled unilaterally by one of the parties to the agreement. During execution (legal state EXECUTED), the agreement can only be canceled if all parties agree to do so by invoking this function.

```endpoint
CALL cancel()
```

#### Return

```json
BaseErrors.INVALID_ACTOR() if the msg.sender is not a party on this agreement, BaseErrors.NO_ERROR() otherwise.
```


---

#### getArchetype()


**getArchetype()**


Returns the archetype

```endpoint
CALL getArchetype()
```

#### Return

```json
the archetype address
```


---

#### getCreator()


**getCreator()**


Returns the creator

```endpoint
CALL getCreator()
```

#### Return

```json
the creator

```


---

#### getDataIdAtIndex(uint256)


**getDataIdAtIndex(uint256)**


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


---

#### getDataType(bytes32)


**getDataType(bytes32)**


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


---

#### getDataValueAsAddress(bytes32)


**getDataValueAsAddress(bytes32)**


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


---

#### getDataValueAsAddressArray(bytes32)


**getDataValueAsAddressArray(bytes32)**


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


---

#### getDataValueAsBool(bytes32)


**getDataValueAsBool(bytes32)**


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


---

#### getDataValueAsBytes(bytes32)


**getDataValueAsBytes(bytes32)**


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


---

#### getDataValueAsBytes16Array(bytes32)


**getDataValueAsBytes16Array(bytes32)**


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


---

#### getDataValueAsBytes1Array(bytes32)


**getDataValueAsBytes1Array(bytes32)**


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


---

#### getDataValueAsBytes20Array(bytes32)


**getDataValueAsBytes20Array(bytes32)**


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


---

#### getDataValueAsBytes24Array(bytes32)


**getDataValueAsBytes24Array(bytes32)**


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


---

#### getDataValueAsBytes28Array(bytes32)


**getDataValueAsBytes28Array(bytes32)**


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


---

#### getDataValueAsBytes2Array(bytes32)


**getDataValueAsBytes2Array(bytes32)**


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


---

#### getDataValueAsBytes32Array(bytes32)


**getDataValueAsBytes32Array(bytes32)**


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


---

#### getDataValueAsBytes3Array(bytes32)


**getDataValueAsBytes3Array(bytes32)**


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


---

#### getDataValueAsBytes4Array(bytes32)


**getDataValueAsBytes4Array(bytes32)**


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


---

#### getDataValueAsBytes8Array(bytes32)


**getDataValueAsBytes8Array(bytes32)**


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


---

#### getDataValueAsInt(bytes32)


**getDataValueAsInt(bytes32)**


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


---

#### getDataValueAsInt128Array(bytes32)


**getDataValueAsInt128Array(bytes32)**


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


---

#### getDataValueAsInt16Array(bytes32)


**getDataValueAsInt16Array(bytes32)**


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


---

#### getDataValueAsInt256Array(bytes32)


**getDataValueAsInt256Array(bytes32)**


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


---

#### getDataValueAsInt32Array(bytes32)


**getDataValueAsInt32Array(bytes32)**


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


---

#### getDataValueAsInt64Array(bytes32)


**getDataValueAsInt64Array(bytes32)**


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


---

#### getDataValueAsInt8Array(bytes32)


**getDataValueAsInt8Array(bytes32)**


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


---

#### getDataValueAsString(bytes32)


**getDataValueAsString(bytes32)**


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsString(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
string the value of the data
```


---

#### getDataValueAsUint(bytes32)


**getDataValueAsUint(bytes32)**


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


---

#### getDataValueAsUint128Array(bytes32)


**getDataValueAsUint128Array(bytes32)**


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


---

#### getDataValueAsUint16Array(bytes32)


**getDataValueAsUint16Array(bytes32)**


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


---

#### getDataValueAsUint256Array(bytes32)


**getDataValueAsUint256Array(bytes32)**


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


---

#### getDataValueAsUint32Array(bytes32)


**getDataValueAsUint32Array(bytes32)**


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


---

#### getDataValueAsUint64Array(bytes32)


**getDataValueAsUint64Array(bytes32)**


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


---

#### getDataValueAsUint8Array(bytes32)


**getDataValueAsUint8Array(bytes32)**


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


---

#### getEventLogReference()


**getEventLogReference()**


Returns the Hoard Address and Hoard Secret for the Event Log

```endpoint
CALL getEventLogReference()
```

#### Return

```json
the Hoard Address and Hoard Secret for the Event Log
```


---

#### getHoardAddress()


**getHoardAddress()**


Returns the Hoard Address

```endpoint
CALL getHoardAddress()
```

#### Return

```json
the Hoard Address

```


---

#### getLegalState()


**getLegalState()**


Returns the legal state of this agreement

```endpoint
CALL getLegalState()
```

#### Return

```json
the Agreements.LegalState as a uint
```


---

#### getMaxNumberOfEvents()


**getMaxNumberOfEvents()**


Returns the max number of events for the event log

```endpoint
CALL getMaxNumberOfEvents()
```

#### Return

```json
the max number of events for the event log
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Returns the number of non-default entries in the specified array-type DataStorage field

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if false the function will return as soon as a default value (0 for int/uint, 0x0 for address, "" for bytes32, etc.) is encountered, if true the array will be scanned to its end
_key // the key for the array-type value

```

#### Return

```json
the number of non-default entries in the array
```


---

#### getNumberOfParties()


**getNumberOfParties()**


Gets number of parties

```endpoint
CALL getNumberOfParties()
```

#### Return

```json
size number of parties
```


---

#### getParty(uint256)


**getParty(uint256)**


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


---

#### getSignatureDetails(address)


**getSignatureDetails(address)**


Returns the timestamp of the signature of the given party.

```endpoint
CALL getSignatureDetails(address)
```

#### Parameters

```solidity
_party // the signing party

```

#### Return

```json
the address of the signee (if the party authorized a signee other than itself)the time of signing or 0 if the address is not a party to this agreement or has not signed yet
```


---

#### getSize()


**getSize()**


Returns the size of the DataMap

```endpoint
CALL getSize()
```

#### Return

```json
uint the size
```


---

#### gethoardSecret()


**gethoardSecret()**


Returns the Hoard Secret

```endpoint
CALL gethoardSecret()
```

#### Return

```json
the Hoard Secret
```


---

#### isPrivate()


**isPrivate()**


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
the private flag 
```


---

#### isSignedBy(address)


**isSignedBy(address)**


Returns whether the given account's signature is on the agreement.

```endpoint
CALL isSignedBy(address)
```

#### Parameters

```solidity
_signee // The account to check

```

#### Return

```json
true if the provided address is a recorded signature on the agreement, false otherwise
```


---

#### removeData(bytes32)


**removeData(bytes32)**


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


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

#### setDataValueAsAddress(bytes32,address)


**setDataValueAsAddress(bytes32,address)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddress(bytes32,address)
```

#### Parameters

```solidity
_id // the id of the data
_value // the address value of the data

```


---

#### setDataValueAsAddressArray(bytes32,address[100])


**setDataValueAsAddressArray(bytes32,address[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddressArray(bytes32,address[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the address[100] value of the data

```


---

#### setDataValueAsBool(bytes32,bool)


**setDataValueAsBool(bytes32,bool)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBool(bytes32,bool)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bool value of the data

```


---

#### setDataValueAsBytes(bytes32,bytes32,uint8)


**setDataValueAsBytes(bytes32,bytes32,uint8)**


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


---

#### setDataValueAsBytes16Array(bytes32,bytes16[100])


**setDataValueAsBytes16Array(bytes32,bytes16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes16Array(bytes32,bytes16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes16[100] value of the data

```


---

#### setDataValueAsBytes1Array(bytes32,bytes1[100])


**setDataValueAsBytes1Array(bytes32,bytes1[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes1Array(bytes32,bytes1[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes1[100] value of the data

```


---

#### setDataValueAsBytes20Array(bytes32,bytes20[100])


**setDataValueAsBytes20Array(bytes32,bytes20[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes20Array(bytes32,bytes20[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes20[100] value of the data

```


---

#### setDataValueAsBytes24Array(bytes32,bytes24[100])


**setDataValueAsBytes24Array(bytes32,bytes24[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes24Array(bytes32,bytes24[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes24[100] value of the data

```


---

#### setDataValueAsBytes28Array(bytes32,bytes28[100])


**setDataValueAsBytes28Array(bytes32,bytes28[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes28Array(bytes32,bytes28[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes28[100] value of the data

```


---

#### setDataValueAsBytes2Array(bytes32,bytes2[100])


**setDataValueAsBytes2Array(bytes32,bytes2[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes2Array(bytes32,bytes2[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes2[100] value of the data

```


---

#### setDataValueAsBytes32(bytes32,bytes32)


**setDataValueAsBytes32(bytes32,bytes32)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32 value of the data

```


---

#### setDataValueAsBytes32Array(bytes32,bytes32[100])


**setDataValueAsBytes32Array(bytes32,bytes32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32Array(bytes32,bytes32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32[100] value of the data

```


---

#### setDataValueAsBytes3Array(bytes32,bytes3[100])


**setDataValueAsBytes3Array(bytes32,bytes3[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes3Array(bytes32,bytes3[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes3[100] value of the data

```


---

#### setDataValueAsBytes4Array(bytes32,bytes4[100])


**setDataValueAsBytes4Array(bytes32,bytes4[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes4Array(bytes32,bytes4[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes4[100] value of the data

```


---

#### setDataValueAsBytes8Array(bytes32,bytes8[100])


**setDataValueAsBytes8Array(bytes32,bytes8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes8Array(bytes32,bytes8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes8[100] value of the data

```


---

#### setDataValueAsInt(bytes32,int256,uint8)


**setDataValueAsInt(bytes32,int256,uint8)**


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


---

#### setDataValueAsInt128Array(bytes32,int128[100])


**setDataValueAsInt128Array(bytes32,int128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt128Array(bytes32,int128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int128[100] value of the data

```


---

#### setDataValueAsInt16Array(bytes32,int16[100])


**setDataValueAsInt16Array(bytes32,int16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt16Array(bytes32,int16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int16[100] value of the data

```


---

#### setDataValueAsInt256(bytes32,int256)


**setDataValueAsInt256(bytes32,int256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256(bytes32,int256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the int value of the data

```


---

#### setDataValueAsInt256Array(bytes32,int256[100])


**setDataValueAsInt256Array(bytes32,int256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256Array(bytes32,int256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int256[100] value of the data

```


---

#### setDataValueAsInt32Array(bytes32,int32[100])


**setDataValueAsInt32Array(bytes32,int32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt32Array(bytes32,int32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int32[100] value of the data

```


---

#### setDataValueAsInt64Array(bytes32,int64[100])


**setDataValueAsInt64Array(bytes32,int64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt64Array(bytes32,int64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int64[100] value of the data

```


---

#### setDataValueAsInt8Array(bytes32,int8[100])


**setDataValueAsInt8Array(bytes32,int8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt8Array(bytes32,int8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int8[100] value of the data

```


---

#### setDataValueAsString(bytes32,string)


**setDataValueAsString(bytes32,string)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsString(bytes32,string)
```

#### Parameters

```solidity
_id // the id of the data
_value // the string value of the data

```


---

#### setDataValueAsUint(bytes32,uint256,uint8)


**setDataValueAsUint(bytes32,uint256,uint8)**


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


---

#### setDataValueAsUint128Array(bytes32,uint128[100])


**setDataValueAsUint128Array(bytes32,uint128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint128Array(bytes32,uint128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint128[100] value of the data

```


---

#### setDataValueAsUint16Array(bytes32,uint16[100])


**setDataValueAsUint16Array(bytes32,uint16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint16Array(bytes32,uint16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint16[100] value of the data

```


---

#### setDataValueAsUint256(bytes32,uint256)


**setDataValueAsUint256(bytes32,uint256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256(bytes32,uint256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint value of the data

```


---

#### setDataValueAsUint256Array(bytes32,uint256[100])


**setDataValueAsUint256Array(bytes32,uint256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256Array(bytes32,uint256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint256[100] value of the data

```


---

#### setDataValueAsUint32Array(bytes32,uint32[100])


**setDataValueAsUint32Array(bytes32,uint32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint32Array(bytes32,uint32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint32[100] value of the data

```


---

#### setDataValueAsUint64Array(bytes32,uint64[100])


**setDataValueAsUint64Array(bytes32,uint64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint64Array(bytes32,uint64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint64[100] value of the data

```


---

#### setDataValueAsUint8Array(bytes32,uint8[100])


**setDataValueAsUint8Array(bytes32,uint8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint8Array(bytes32,uint8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint8[100] value of the data

```


---

#### setEventLogReference(bytes32,bytes32)


**setEventLogReference(bytes32,bytes32)**


Sets the Hoard Address and Hoard Secret for the Event Log

```endpoint
CALL setEventLogReference(bytes32,bytes32)
```


---

#### setFulfilled()


**setFulfilled()**


Sets the legal state of this agreement to Agreements.LegalState.FULFILLED. Note: All other legal states are set by internal logic.

```endpoint
CALL setFulfilled()
```


---

#### sign()


**sign()**


Applies the msg.sender signature

```endpoint
CALL sign()
```

#### Return

```json
an error code indicating success or failure
```


---

### ActiveAgreementRegistry Interface


The ActiveAgreementRegistry Interface contract is found within the agreements bundle.

#### addAgreementToCollection(bytes32,address)


**addAgreementToCollection(bytes32,address)**


Adds an agreement to given collection

```endpoint
CALL addAgreementToCollection(bytes32,address)
```

#### Parameters

```solidity
_agreement // agreement address
_collectionId // the bytes32 collection id

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() collection by given id does not exist
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)


**createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)**


Creates an Active Agreement with the given parameters

```endpoint
CALL createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_collectionId // id of agreement collection (optional)
_hoardAddress // Address of agreement params in hoard
_hoardSecret // Secret for hoard retrieval
_name // name
_parties // parties

```

#### Return

```json
error - BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if _archetype or _name is nullactiveAgreement - the new ActiveAgreement's address, if successfully created, 0x0 otherwise
```


---

#### createAgreementCollection(string,address,uint8,bytes32)


**createAgreementCollection(string,address,uint8,bytes32)**


Creates a new agreement collection

```endpoint
CALL createAgreementCollection(string,address,uint8,bytes32)
```

#### Parameters

```solidity
_author // address of author
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED(), BaseErrors.RESOURCE_ALREADY_EXISTS()id bytes32 id of package
```


---

#### createUserAccount(address,address,bytes32)


**createUserAccount(address,address,bytes32)**


Creates a AgreementPartyAccount with the specified parameters and adds it to the AccountsManager

```endpoint
CALL createUserAccount(address,address,bytes32)
```

#### Parameters

```solidity
_accountsManager // the AccountsManager address
_id // id (optional)
_owner // owner (optional)

```

#### Return

```json
error BaseErrors.RESOURCE_ALREADY_EXISTS() or BaseErrors.NO_ERROR()userAccount user account address, or 0x0 if not successful
```


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


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


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


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


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


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


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


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


---

#### getActiveAgreementAtIndex(uint256)


**getActiveAgreementAtIndex(uint256)**


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


---

#### getActiveAgreementData(address)


**getActiveAgreementData(address)**


Returns data about the ActiveAgreement at the specified address

```endpoint
CALL getActiveAgreementData(address)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement

```

#### Return

```json
archetype - the agreement's archetype adressname - the name of the agreementcreator - the creator of the agreementhoardAddress - address of the agreement parameters in hoard (only used when agreement is private)hoardSecret - secret for retrieval of hoard parameterseventLogHoardAddress - address of the agreement's event log in hoardeventLogHoardSecret - secret for retrieval of the hoard event log filemaxNumberOfEvents - the maximum number of events allowed to be stored for this agreementisPrivate - whether the agreement's parameters are private, i.e. stored off-chain in hoardlegalState - the agreement's Agreement.LegalState as uint8formationProcessInstance - the address of the process instance representing the formation of this agreementexecutionProcessInstance - the address of the process instance representing the execution of this agreement
```


---

#### getActiveAgreementsSize()


**getActiveAgreementsSize()**


Gets number of activeAgreements

```endpoint
CALL getActiveAgreementsSize()
```

#### Return

```json
size size
```


---

#### getAgreementAtIndexInCollection(bytes32,uint256)


**getAgreementAtIndexInCollection(bytes32,uint256)**


Gets agreement address at index in colelction

```endpoint
CALL getAgreementAtIndexInCollection(bytes32,uint256)
```

#### Parameters

```solidity
_id // id of the collection
_index // uint index

```

#### Return

```json
agreement address of archetype
```


---

#### getAgreementCollectionAtIndex(uint256)


**getAgreementCollectionAtIndex(uint256)**


Gets collection id at index

```endpoint
CALL getAgreementCollectionAtIndex(uint256)
```

#### Parameters

```solidity
_index // uint index

```

#### Return

```json
id bytes32 id
```


---

#### getAgreementCollectionData(bytes32)


**getAgreementCollectionData(bytes32)**


Gets collection data by id

```endpoint
CALL getAgreementCollectionData(bytes32)
```

#### Parameters

```solidity
_id // bytes32 collection id

```

#### Return

```json
name stringauthor addresscollectionType type of collectionpackageId id of the archetype package
```


---

#### getAgreementDataInCollection(bytes32,address)


**getAgreementDataInCollection(bytes32,address)**


Get agreement data by collection id and agreement address

```endpoint
CALL getAgreementDataInCollection(bytes32,address)
```

#### Parameters

```solidity
_agreement // address of agreement
_id // id of the collection

```

#### Return

```json
agreementName name of agreementarchetype address of archetype
```


---

#### getAgreementParameterAtIndex(address,uint256)


**getAgreementParameterAtIndex(address,uint256)**


Returns the process data ID at the specified index

```endpoint
CALL getAgreementParameterAtIndex(address,uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the data ID
```


---

#### getAgreementParameterDetails(address,bytes32)


**getAgreementParameterDetails(address,bytes32)**


Returns information about the process data entry for the specified process and data ID

```endpoint
CALL getAgreementParameterDetails(address,bytes32)
```

#### Parameters

```solidity
_address // the active agreement
_dataId // the data ID

```

#### Return

```json
(process,id,uintValue,bytes32Value,addressValue,boolValue)
```


---

#### getArchetypeRegistry()


**getArchetypeRegistry()**


Returns the ArchetypeRegistry address

```endpoint
CALL getArchetypeRegistry()
```

#### Return

```json
address the ArchetypeRegistry
```


---

#### getBpmService()


**getBpmService()**


Returns the BpmService address

```endpoint
CALL getBpmService()
```

#### Return

```json
address the BpmService
```


---

#### getNumberOfAgreementCollections()


**getNumberOfAgreementCollections()**


Gets number of agreement collections

```endpoint
CALL getNumberOfAgreementCollections()
```

#### Return

```json
size size
```


---

#### getNumberOfAgreementParameters(address)


**getNumberOfAgreementParameters(address)**


Returns the number of agreement parameter entries.

```endpoint
CALL getNumberOfAgreementParameters(address)
```

#### Return

```json
the number of parameters
```


---

#### getNumberOfAgreementsInCollection(bytes32)


**getNumberOfAgreementsInCollection(bytes32)**


Gets number of agreements in given collection

```endpoint
CALL getNumberOfAgreementsInCollection(bytes32)
```

#### Parameters

```solidity
_id // id of the collection

```

#### Return

```json
size agreement count
```


---

#### getPartiesByActiveAgreementSize(address)


**getPartiesByActiveAgreementSize(address)**


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


---

#### getPartyByActiveAgreementAtIndex(address,uint256)


**getPartyByActiveAgreementAtIndex(address,uint256)**


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


---

#### getPartyByActiveAgreementData(address,address)


**getPartyByActiveAgreementData(address,address)**


Returns data about the given party's signature on the specified agreement.

```endpoint
CALL getPartyByActiveAgreementData(address,address)
```

#### Parameters

```solidity
_activeAgreement // the ActiveAgreement
_party // the signing party

```

#### Return

```json
signedBy the actual signature authorized by the partysignatureTimestamp the timestamp when the party has signed, or 0 if not signed yet
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### processStateChanged(address)


**processStateChanged(address)**


Invoked by a ProcessStateChangeEventEmitter to notify of process state change

```endpoint
CALL processStateChanged(address)
```

#### Parameters

```solidity
_pi // the process instance whose state changed

```


---

#### setArchetypeRegistry(address)


**setArchetypeRegistry(address)**


Sets the ArchetypeRegistry reference

```endpoint
CALL setArchetypeRegistry(address)
```

#### Parameters

```solidity
_archetypeRegistry // the ArchetypeRegistry

```


---

#### setBpmService(address)


**setBpmService(address)**


Sets the BpmService reference to use for controlling the agreement workflows.

```endpoint
CALL setBpmService(address)
```

#### Parameters

```solidity
_service // the BpmService

```


---

#### setEventLogReference(address,bytes32,bytes32)


**setEventLogReference(address,bytes32,bytes32)**


Updates the hoard address and secret for the event log of the specified agreement

```endpoint
CALL setEventLogReference(address,bytes32,bytes32)
```

#### Parameters

```solidity
_activeAgreement // Address of active agreement
_eventLogHoardAddress // New hoard address of event log for agreement
_eventLogHoardSecret // New hoard secret key of event log for agreement

```


---

#### startFormation(address)


**startFormation(address)**


Creates a starts a ProcessInstance to handle the formation workflow as defined by the given agreement's archetype.

```endpoint
CALL startFormation(address)
```

#### Parameters

```solidity
_agreement // an ActiveAgreement

```

#### Return

```json
error - an error code indicating success or failurethe address of the ProcessInstance, if successful
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### ActiveAgreementRegistryDb Interface


The ActiveAgreementRegistryDb Interface contract is found within the agreements bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### AgreementPartyAccount


The AgreementPartyAccount contract is found within the agreements bundle.

#### cancelAgreement(address)


**cancelAgreement(address)**


Signs the provided ActiveAgreement contract

```endpoint
CALL cancelAgreement(address)
```

#### Parameters

```solidity
_agreement // the address of a ActiveAgreement

```

#### Return

```json
error code if the signing failed
```


---

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService required for lookup and access to the BpmServiceDb

```

#### Return

```json
error code if the completion failed
```


---

#### getId()


**getId()**


Returns this account's ID

```endpoint
CALL getId()
```


---

#### getOrganization()


**getOrganization()**


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```


---

#### setOrganization(address)


**setOrganization(address)**


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


---

#### signAgreement(address)


**signAgreement(address)**


Signs the provided ActiveAgreement contract

```endpoint
CALL signAgreement(address)
```

#### Parameters

```solidity
_agreement // the address of a ActiveAgreement

```

#### Return

```json
error code if the signing failed
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### AgreementPartyProxy


The AgreementPartyProxy contract is found within the agreements bundle.

#### cancelAgreement(address)


**cancelAgreement(address)**


Signs the provided ActiveAgreement contract

```endpoint
CALL cancelAgreement(address)
```

#### Parameters

```solidity
_agreement // the address of a ActiveAgreement

```

#### Return

```json
error code if the signing failed
```


---

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService required for lookup and access to the BpmServiceDb

```

#### Return

```json
error code if the completion failed
```


---

#### signAgreement(address)


**signAgreement(address)**


Signs the provided ActiveAgreement contract

```endpoint
CALL signAgreement(address)
```

#### Parameters

```solidity
_agreement // the address of a ActiveAgreement

```

#### Return

```json
error code if the signing failed
```


---

### AgreementSignatureCheck Interface


The AgreementSignatureCheck Interface contract is found within the agreements bundle.

#### complete(address,bytes32,bytes32,address)


**complete(address,bytes32,bytes32,address)**


Treats the provided DataStorage as the agreement and checks if the TX performer has applied a signature. The function will throw if the presence of the signature could not be established. NOTE: Not used parameters 

```endpoint
CALL complete(address,bytes32,bytes32,address)
```

#### Parameters

```solidity
_dataStorage // the Agreement
_txPerformer // the address performing the transaction

```


---


### AgreementsAPI


The AgreementsAPI contract is found within the agreements bundle.

#### authorizePartyActor(ActiveAgreement)


**authorizePartyActor(ActiveAgreement)**


Evaluates the msg.sender and tx.origin against the given agreement to determine if there is an authorized party/actor relationship.

```endpoint
CALL authorizePartyActor(ActiveAgreement)
```

#### Parameters

```solidity
_agreement // an ActiveAgreement

```

#### Return

```json
actor - the address of either msg.sender or tx.origin depending on which one was authorized; 0x0 if authorization failedparty - the agreement party associated with the identified actor. This is typically the same as the actor, but can also contain an Organization address if an Organization was registered as a party. 0x0 if authorization failed
```


---

#### isFullyExecuted(ActiveAgreement)


**isFullyExecuted(ActiveAgreement)**


Checks whether the given agreement is fully executed.

```endpoint
CALL isFullyExecuted(ActiveAgreement)
```

#### Parameters

```solidity
_agreement // an ActiveAgreement

```

#### Return

```json
true if all parties have signed, false otherwise
```


---


### ApplicationRegistry Interface


The ApplicationRegistry Interface contract is found within the agreements bundle.

#### addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)


**addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)**


Adds an application with the given parameters to this ProcessModel

```endpoint
CALL addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)
```

#### Parameters

```solidity
_eventName // the ID of an event to fire (only for event application)
_function // the signature of the completion function
_id // the ID of the application
_location // the location of the contract implementing the application
_type // the BpmModel.ApplicationType
_webForm // the hash of a web form (only for web applications)

```

#### Return

```json
an error code indicating success or failure
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getApplicationAccessPathAtIndex(bytes32,uint256,uint8)


**getApplicationAccessPathAtIndex(bytes32,uint256,uint8)**


Returns information about the specified I/O access path of an application

```endpoint
CALL getApplicationAccessPathAtIndex(bytes32,uint256,uint8)
```

#### Parameters

```solidity
_direction // BpmModel.Direction.[IN|OUT]
_id // the ID of the application
_idx // the index of the input/output parameter

```

#### Return

```json
the ID of the input/outputthe uint8 representation of the DataTypes value
```


---

#### getApplicationAtIndex(uint256)


**getApplicationAtIndex(uint256)**


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


---

#### getApplicationData(bytes32)


**getApplicationData(bytes32)**


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
applicationType the BpmModel.ApplicationType as uint8location the applications contract addressmethod the function signature of the application's completion functionwebForm the form identifier (hash) of the web application (only for a web application)eventName the identifier for an event to emit (only for event application)inputs the number of inputsoutputs the number of outputs
```


---

#### getNumberOfApplications()


**getNumberOfApplications()**


Returns the number of applications defined in this ProcessModel

```endpoint
CALL getNumberOfApplications()
```

#### Return

```json
the number of applications
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setApplicationAccessPath(bytes32,bytes32,uint8,uint8)


**setApplicationAccessPath(bytes32,bytes32,uint8,uint8)**


Adds an input or output declaration to the application identified by the activity ID.

```endpoint
CALL setApplicationAccessPath(bytes32,bytes32,uint8,uint8)
```

#### Parameters

```solidity
_dataType // a DataTypes code
_direction // the BpmModel.Direction (IN/OUT) of the data flow
_id // the ID of the application to which to add the declaration
_pathId // the ID of the data path

```

#### Return

```json
an error code indicating success or failure
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### Archetype Interface


The Archetype Interface contract is found within the agreements bundle.

#### activate()


**activate()**


Activates this archetype

```endpoint
CALL activate()
```

#### Return

```json
error code indicating success or failure
```


---

#### addDocument(bytes32,bytes32,bytes32)


**addDocument(bytes32,bytes32,bytes32)**


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


---

#### addJurisdiction(bytes2,bytes32)


**addJurisdiction(bytes2,bytes32)**


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


---

#### addParameter(uint8,bytes32)


**addParameter(uint8,bytes32)**


Adds a parameter with the specified type and name to the archetype

```endpoint
CALL addParameter(uint8,bytes32)
```

#### Parameters

```solidity
_parameter // parameter
_parameterType // parameter type (enum)

```

#### Return

```json
error code indicating success or failure
```


---

#### deactivate()


**deactivate()**


Deactivates this archetype

```endpoint
CALL deactivate()
```

#### Return

```json
error code indicating success or failure
```


---

#### getAuthor()


**getAuthor()**


Gets Author

```endpoint
CALL getAuthor()
```

#### Return

```json
author author
```


---

#### getDescription()


**getDescription()**


Gets description

```endpoint
CALL getDescription()
```

#### Return

```json
description
```


---

#### getDocument(bytes32)


**getDocument(bytes32)**


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


---

#### getDocumentAtIndex(uint256)


**getDocumentAtIndex(uint256)**


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


---

#### getExecutionProcessDefinition()


**getExecutionProcessDefinition()**


Returns the address of the ProcessDefinition that orchestrates the agreement execution.

```endpoint
CALL getExecutionProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getFormationProcessDefinition()


**getFormationProcessDefinition()**


Returns the address of the ProcessDefinition that orchestrates the agreement formation.

```endpoint
CALL getFormationProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getJurisdictionAtIndex(uint256)


**getJurisdictionAtIndex(uint256)**


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


---

#### getJurisdictionData(bytes32)


**getJurisdictionData(bytes32)**


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


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfDocuments()


**getNumberOfDocuments()**


Gets number of documents

```endpoint
CALL getNumberOfDocuments()
```

#### Return

```json
size number of documents
```


---

#### getNumberOfJurisdictions()


**getNumberOfJurisdictions()**


Returns the number jurisdictions for this archetype

```endpoint
CALL getNumberOfJurisdictions()
```

#### Return

```json
the number of jurisdictions
```


---

#### getNumberOfParameters()


**getNumberOfParameters()**


Gets number of parameters

```endpoint
CALL getNumberOfParameters()
```

#### Return

```json
size number of parameters
```


---

#### getParameterAtIndex(uint256)


**getParameterAtIndex(uint256)**


Gets parameter at index

```endpoint
CALL getParameterAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error error TBDcustomField parameter
```


---

#### getParameterType(bytes32)


**getParameterType(bytes32)**


Gets parameter data type

```endpoint
CALL getParameterType(bytes32)
```

#### Parameters

```solidity
_parameter // parameter

```

#### Return

```json
error error TBDparameterType parameter type
```


---

#### isActive()


**isActive()**


Returns the active state

```endpoint
CALL isActive()
```

#### Return

```json
true if active, false otherwise
```


---

#### isPrivate()


**isPrivate()**


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
true if private, false otherwise
```


---

### ArchetypeRegistry Interface


The ArchetypeRegistry Interface contract is found within the agreements bundle.

#### activate(address)


**activate(address)**


Sets active to true for given archetype

```endpoint
CALL activate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### addArchetypeToPackage(bytes32,address)


**addArchetypeToPackage(bytes32,address)**


Adds archetype to package

```endpoint
CALL addArchetypeToPackage(bytes32,address)
```

#### Parameters

```solidity
_archetype // the archetype address
_packageId // the bytes32 package id

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() package by given id does not exist
```


---

#### addDocument(address,bytes32,bytes32,bytes32)


**addDocument(address,bytes32,bytes32,bytes32)**


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


---

#### addJurisdiction(address,bytes2,bytes32)


**addJurisdiction(address,bytes2,bytes32)**


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


---

#### addJurisdictions(address,bytes2[],bytes32[])


**addJurisdictions(address,bytes2[],bytes32[])**


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


---

#### addParameter(address,uint8,bytes32)


**addParameter(address,uint8,bytes32)**


Adds the specified parameter to the archetype

```endpoint
CALL addParameter(address,uint8,bytes32)
```

#### Parameters

```solidity
_parameterName // parameter name
_parameterType // parameter type (enum)

```

#### Return

```json
a return code indicating success or failure
```


---

#### addParameters(address,uint8[],bytes32[])


**addParameters(address,uint8[],bytes32[])**


Adds the specified parameters to the archetype

```endpoint
CALL addParameters(address,uint8[],bytes32[])
```

#### Parameters

```solidity
_parameterNames // parameter names array
_parameterTypes // parameter type (enum) array

```

#### Return

```json
a return code indicating success or failure
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createArchetype(bytes32,address,string,bool,address,address,bytes32)


**createArchetype(bytes32,address,string,bool,address,address,bytes32)**


Creates a archetype with the given parameters

```endpoint
CALL createArchetype(bytes32,address,string,bool,address,address,bytes32)
```

#### Parameters

```solidity
_author // author
_description // description
_executionProcess // the address of a ProcessDefinition that orchestrates the agreement execution
_formationProcess // the address of a ProcessDefinition that orchestrates the agreement formation
_isPrivate // determines if the archetype's documents are encrypted
_name // name
_packageId // id of package this archetype is part of (optional)

```

#### Return

```json
error - a return code indicating success or failurearchetype - the new archetype's address, if successfully created
```


---

#### createArchetypePackage(string,string,address,bool)


**createArchetypePackage(string,string,address,bool)**


Adds a new archetype package

```endpoint
CALL createArchetypePackage(string,string,address,bool)
```

#### Parameters

```solidity
_author // address of author (user account of organization)
_description // description
_isPrivate // makes it a private package visible to only the author
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED(), BaseErrors.RESOURCE_ALREADY_EXISTS()id bytes32 id of package
```


---

#### deactivate(address)


**deactivate(address)**


Sets active to false for given archetype

```endpoint
CALL deactivate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### getArchetypeAtIndex(uint256)


**getArchetypeAtIndex(uint256)**


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


---

#### getArchetypeAtIndexInPackage(bytes32,uint256)


**getArchetypeAtIndexInPackage(bytes32,uint256)**


Gets archetype address at index in package

```endpoint
CALL getArchetypeAtIndexInPackage(bytes32,uint256)
```

#### Parameters

```solidity
_id // id of the package
_index // uint index

```

#### Return

```json
archetype address of archetype
```


---

#### getArchetypeData(address)


**getArchetypeData(address)**


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


---

#### getArchetypeDataInPackage(bytes32,address)


**getArchetypeDataInPackage(bytes32,address)**


Get archetype data by package id and archetype address

```endpoint
CALL getArchetypeDataInPackage(bytes32,address)
```

#### Parameters

```solidity
_archetype // address of archetype
_id // id of the package

```

#### Return

```json
archetypeName name of archetype
```


---

#### getArchetypePackageAtIndex(uint256)


**getArchetypePackageAtIndex(uint256)**


Gets package id at index

```endpoint
CALL getArchetypePackageAtIndex(uint256)
```

#### Parameters

```solidity
_index // uint index

```

#### Return

```json
id bytes32 id
```


---

#### getArchetypePackageData(bytes32)


**getArchetypePackageData(bytes32)**


Gets package data by id

```endpoint
CALL getArchetypePackageData(bytes32)
```

#### Parameters

```solidity
_id // bytes32 package id

```

#### Return

```json
name stringdescription stringauthor addressisPrivate bool
```


---

#### getArchetypesSize()


**getArchetypesSize()**


Gets number of archetypes

```endpoint
CALL getArchetypesSize()
```

#### Return

```json
size size
```


---

#### getDocumentByArchetypeAtIndex(address,uint256)


**getDocumentByArchetypeAtIndex(address,uint256)**


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


---

#### getDocumentByArchetypeData(address,bytes32)


**getDocumentByArchetypeData(address,bytes32)**


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


---

#### getDocumentsByArchetypeSize(address)


**getDocumentsByArchetypeSize(address)**


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


---

#### getJurisdictionAtIndexForArchetype(address,uint256)


**getJurisdictionAtIndexForArchetype(address,uint256)**


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


---

#### getJurisdictionDataForArchetype(address,bytes32)


**getJurisdictionDataForArchetype(address,bytes32)**


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


---

#### getNumberOfArchetypePackages()


**getNumberOfArchetypePackages()**


Gets number of archetype packages

```endpoint
CALL getNumberOfArchetypePackages()
```

#### Return

```json
size size
```


---

#### getNumberOfArchetypesInPackage(bytes32)


**getNumberOfArchetypesInPackage(bytes32)**


Gets number of archetypes in given package

```endpoint
CALL getNumberOfArchetypesInPackage(bytes32)
```

#### Parameters

```solidity
_id // id of the package

```

#### Return

```json
size archetype count
```


---

#### getNumberOfJurisdictionsForArchetype(address)


**getNumberOfJurisdictionsForArchetype(address)**


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


---

#### getParameterByArchetypeAtIndex(address,uint256)


**getParameterByArchetypeAtIndex(address,uint256)**


Gets parameter name by Archetype At index

```endpoint
CALL getParameterByArchetypeAtIndex(address,uint256)
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


---

#### getParameterByArchetypeData(address,bytes32)


**getParameterByArchetypeData(address,bytes32)**


Returns data about the parameter at with the specified name

```endpoint
CALL getParameterByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
parameterType parameter type
```


---

#### getParametersByArchetypeSize(address)


**getParametersByArchetypeSize(address)**


Gets parameters size for given Archetype

```endpoint
CALL getParametersByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### packageHasArchetype(bytes32,address)


**packageHasArchetype(bytes32,address)**


Determines whether given archetype address is in the package identified by the packageId

```endpoint
CALL packageHasArchetype(bytes32,address)
```

#### Parameters

```solidity
_archetype // address of archetype
_packageId // id of the package

```

#### Return

```json
hasArchetype bool representing if archetype is in package
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### ArchetypeRegistryDb Interface


The ArchetypeRegistryDb Interface contract is found within the agreements bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### ArrayUtils Library Interface


The ArrayUtils Library Interface contract is found within the agreements bundle.

#### contains(address[],address)


**contains(address[],address)**


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


---

#### contains(bytes32[],bytes32)


**contains(bytes32[],bytes32)**


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


---

#### contains(int256[],int256)


**contains(int256[],int256)**


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


---

#### contains(uint256[],uint256)


**contains(uint256[],uint256)**


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


---




### BpmService Interface


The BpmService Interface contract is found within the agreements bundle.

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createDefaultProcessInstance(address,address,bytes32)


**createDefaultProcessInstance(address,address,bytes32)**


Creates a new ProcessInstance initiated with the provided parameters. This ProcessInstance can be further customized and then submitted to the #startProcessInstance(ProcessInstance) function for execution.

```endpoint
CALL createDefaultProcessInstance(address,address,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_processDefinition // the address of a ProcessDefinition
_startedBy // the address of an account that regarded as the starting user

```


---

#### fireActivityUpdateEvent(address,bytes32)


**fireActivityUpdateEvent(address,bytes32)**


Fires the UpdateActivities event to update sqlsol with given activity

```endpoint
CALL fireActivityUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_activityId // - the bytes32 Id of the activity
_piAddress // - the address of the process instance to which the activity belongs

```


---

#### fireProcessDataUpdateEvent(address,bytes32)


**fireProcessDataUpdateEvent(address,bytes32)**


Fires the UpdateProcessData event to update sqlsol with given information

```endpoint
CALL fireProcessDataUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_dataId // - the ID of the data entry
_piAddress // - the address of the process instance to which the activity belongs

```


---

#### getActivityInstanceAtIndex(address,uint256)


**getActivityInstanceAtIndex(address,uint256)**


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


---

#### getActivityInstanceData(address,bytes32)


**getActivityInstanceData(address,bytes32)**


Returns ActivityInstance data for the given ActivityInstance ID

```endpoint
CALL getActivityInstanceData(address,bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance
_processInstance // the process instance address to which the ActivityInstance belongs

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitioncreated - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) state - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```


---

#### getApplicationRegistry()


**getApplicationRegistry()**


Returns a reference to the ApplicationRegistry currently used by this BpmService

```endpoint
CALL getApplicationRegistry()
```

#### Return

```json
the ApplicationRegistry
```


---

#### getBpmServiceDb()


**getBpmServiceDb()**


Returns a reference to the BpmServiceDb currently used by this BpmService

```endpoint
CALL getBpmServiceDb()
```

#### Return

```json
the BpmServiceDb
```


---

#### getNumberOfActivityInstances(address)


**getNumberOfActivityInstances(address)**


Returns the number of activity instances.

```endpoint
CALL getNumberOfActivityInstances(address)
```

#### Return

```json
the activity instance count as size
```


---

#### getNumberOfProcessData(address)


**getNumberOfProcessData(address)**


Returns the number of process data entries.

```endpoint
CALL getNumberOfProcessData(address)
```

#### Return

```json
the process data size
```


---

#### getNumberOfProcessInstances()


**getNumberOfProcessInstances()**


Returns the number of Process Instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the process instance count as size
```


---

#### getProcessDataAtIndex(address,uint256)


**getProcessDataAtIndex(address,uint256)**


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


---

#### getProcessDataDetails(address,bytes32)


**getProcessDataDetails(address,bytes32)**


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


---

#### getProcessInstanceAtIndex(uint256)


**getProcessInstanceAtIndex(uint256)**


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


---

#### getProcessInstanceData(address)


**getProcessInstanceData(address)**


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
processDefinition the address of the ProcessDefinitionstate the BpmRuntime.ProcessInstanceState as uint8startedBy the address of the account who started the process
```


---

#### getProcessInstanceForActivity(bytes32)


**getProcessInstanceForActivity(bytes32)**


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


---

#### getProcessModelRepository()


**getProcessModelRepository()**


Gets the ProcessModelRepository address for this BpmService

```endpoint
CALL getProcessModelRepository()
```

#### Return

```json
the address of the repository
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setApplicationRegistry(address)


**setApplicationRegistry(address)**


Sets the ApplicationRegistry for this BpmService

```endpoint
CALL setApplicationRegistry(address)
```

#### Parameters

```solidity
_registry // - the address of the application registry

```


---

#### setProcessModelRepository(address)


**setProcessModelRepository(address)**


Sets the ProcessModelRepository for this BpmService

```endpoint
CALL setProcessModelRepository(address)
```

#### Parameters

```solidity
_repository // - the address of the model repository

```


---

#### startProcess(address,bytes32)


**startProcess(address,bytes32)**


Creates a new ProcessInstance based on the specified ProcessDefinition and starts its execution

```endpoint
CALL startProcess(address,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

#### startProcessFromRepository(bytes32,bytes32,bytes32)


**startProcessFromRepository(bytes32,bytes32,bytes32)**


Creates a new ProcessInstance based on the specified IDs of a ProcessModel and ProcessDefinition and starts its execution

```endpoint
CALL startProcessFromRepository(bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processDefinitionId // the ID of the process definition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

#### startProcessInstance(address)


**startProcessInstance(address)**


Initializes, registers, and executes a given ProcessInstance

```endpoint
CALL startProcessInstance(address)
```

#### Parameters

```solidity
_pi // the ProcessInstance

```

#### Return

```json
BaseErrors.NO_ERROR() if successful or an error code from initializing or executing the ProcessInstance
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### BpmServiceDb


The BpmServiceDb contract is found within the agreements bundle.

#### addActivityInstance(bytes32)


**addActivityInstance(bytes32)**


Adds the given ActivityInstance ID to the registered activity instances. Can only be invoked by an already registered ProcessInstance. The sending ProcessInstance (msg.sender) is recorded as well.

```endpoint
CALL addActivityInstance(bytes32)
```

#### Parameters

```solidity
_id // the globally unique ID of an ActivityInstance

```


---

#### addProcessInstance(address)


**addProcessInstance(address)**


Adds the given address to the registered process instances. Can only be invoked by the owner of this BpmServiceDb.

```endpoint
CALL addProcessInstance(address)
```

#### Parameters

```solidity
_address // the address of a ProcessInstance

```


---

#### getNumberOfActivityInstances()


**getNumberOfActivityInstances()**


Returns the number of registered activity instances.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```


---

#### getNumberOfProcessInstances()


**getNumberOfProcessInstances()**


Returns the number of registered process instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the number of process instances
```


---

#### getProcessInstanceAtIndex(uint256)


**getProcessInstanceAtIndex(uint256)**


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


---

#### getProcessInstanceForActivity(bytes32)


**getProcessInstanceForActivity(bytes32)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### Identifiable Interface


The Identifiable Interface contract is found within the agreements bundle.

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

### DataStorage Interface


The DataStorage Interface contract is found within the agreements bundle.

#### getDataIdAtIndex(uint256)


**getDataIdAtIndex(uint256)**


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


---

#### getDataType(bytes32)


**getDataType(bytes32)**


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


---

#### getDataValueAsAddress(bytes32)


**getDataValueAsAddress(bytes32)**


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


---

#### getDataValueAsAddressArray(bytes32)


**getDataValueAsAddressArray(bytes32)**


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


---

#### getDataValueAsBool(bytes32)


**getDataValueAsBool(bytes32)**


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


---

#### getDataValueAsBytes(bytes32)


**getDataValueAsBytes(bytes32)**


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


---

#### getDataValueAsBytes16Array(bytes32)


**getDataValueAsBytes16Array(bytes32)**


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


---

#### getDataValueAsBytes1Array(bytes32)


**getDataValueAsBytes1Array(bytes32)**


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


---

#### getDataValueAsBytes20Array(bytes32)


**getDataValueAsBytes20Array(bytes32)**


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


---

#### getDataValueAsBytes24Array(bytes32)


**getDataValueAsBytes24Array(bytes32)**


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


---

#### getDataValueAsBytes28Array(bytes32)


**getDataValueAsBytes28Array(bytes32)**


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


---

#### getDataValueAsBytes2Array(bytes32)


**getDataValueAsBytes2Array(bytes32)**


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


---

#### getDataValueAsBytes32Array(bytes32)


**getDataValueAsBytes32Array(bytes32)**


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


---

#### getDataValueAsBytes3Array(bytes32)


**getDataValueAsBytes3Array(bytes32)**


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


---

#### getDataValueAsBytes4Array(bytes32)


**getDataValueAsBytes4Array(bytes32)**


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


---

#### getDataValueAsBytes8Array(bytes32)


**getDataValueAsBytes8Array(bytes32)**


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


---

#### getDataValueAsInt(bytes32)


**getDataValueAsInt(bytes32)**


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


---

#### getDataValueAsInt128Array(bytes32)


**getDataValueAsInt128Array(bytes32)**


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


---

#### getDataValueAsInt16Array(bytes32)


**getDataValueAsInt16Array(bytes32)**


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


---

#### getDataValueAsInt256Array(bytes32)


**getDataValueAsInt256Array(bytes32)**


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


---

#### getDataValueAsInt32Array(bytes32)


**getDataValueAsInt32Array(bytes32)**


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


---

#### getDataValueAsInt64Array(bytes32)


**getDataValueAsInt64Array(bytes32)**


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


---

#### getDataValueAsInt8Array(bytes32)


**getDataValueAsInt8Array(bytes32)**


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


---

#### getDataValueAsString(bytes32)


**getDataValueAsString(bytes32)**


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsString(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
string the value of the data
```


---

#### getDataValueAsUint(bytes32)


**getDataValueAsUint(bytes32)**


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


---

#### getDataValueAsUint128Array(bytes32)


**getDataValueAsUint128Array(bytes32)**


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


---

#### getDataValueAsUint16Array(bytes32)


**getDataValueAsUint16Array(bytes32)**


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


---

#### getDataValueAsUint256Array(bytes32)


**getDataValueAsUint256Array(bytes32)**


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


---

#### getDataValueAsUint32Array(bytes32)


**getDataValueAsUint32Array(bytes32)**


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


---

#### getDataValueAsUint64Array(bytes32)


**getDataValueAsUint64Array(bytes32)**


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


---

#### getDataValueAsUint8Array(bytes32)


**getDataValueAsUint8Array(bytes32)**


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


---

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Returns the number of non-default entries in the specified array-type DataStorage field

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if false the function will return as soon as a default value (0 for int/uint, 0x0 for address, "" for bytes32, etc.) is encountered, if true the array will be scanned to its end
_key // the key for the array-type value

```

#### Return

```json
the number of non-default entries in the array
```


---

#### getSize()


**getSize()**


Returns the size of the DataMap

```endpoint
CALL getSize()
```

#### Return

```json
uint the size
```


---

#### removeData(bytes32)


**removeData(bytes32)**


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


---

#### setDataValueAsAddress(bytes32,address)


**setDataValueAsAddress(bytes32,address)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddress(bytes32,address)
```

#### Parameters

```solidity
_id // the id of the data
_value // the address value of the data

```


---

#### setDataValueAsAddressArray(bytes32,address[100])


**setDataValueAsAddressArray(bytes32,address[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddressArray(bytes32,address[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the address[100] value of the data

```


---

#### setDataValueAsBool(bytes32,bool)


**setDataValueAsBool(bytes32,bool)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBool(bytes32,bool)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bool value of the data

```


---

#### setDataValueAsBytes(bytes32,bytes32,uint8)


**setDataValueAsBytes(bytes32,bytes32,uint8)**


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


---

#### setDataValueAsBytes16Array(bytes32,bytes16[100])


**setDataValueAsBytes16Array(bytes32,bytes16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes16Array(bytes32,bytes16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes16[100] value of the data

```


---

#### setDataValueAsBytes1Array(bytes32,bytes1[100])


**setDataValueAsBytes1Array(bytes32,bytes1[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes1Array(bytes32,bytes1[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes1[100] value of the data

```


---

#### setDataValueAsBytes20Array(bytes32,bytes20[100])


**setDataValueAsBytes20Array(bytes32,bytes20[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes20Array(bytes32,bytes20[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes20[100] value of the data

```


---

#### setDataValueAsBytes24Array(bytes32,bytes24[100])


**setDataValueAsBytes24Array(bytes32,bytes24[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes24Array(bytes32,bytes24[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes24[100] value of the data

```


---

#### setDataValueAsBytes28Array(bytes32,bytes28[100])


**setDataValueAsBytes28Array(bytes32,bytes28[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes28Array(bytes32,bytes28[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes28[100] value of the data

```


---

#### setDataValueAsBytes2Array(bytes32,bytes2[100])


**setDataValueAsBytes2Array(bytes32,bytes2[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes2Array(bytes32,bytes2[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes2[100] value of the data

```


---

#### setDataValueAsBytes32(bytes32,bytes32)


**setDataValueAsBytes32(bytes32,bytes32)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32 value of the data

```


---

#### setDataValueAsBytes32Array(bytes32,bytes32[100])


**setDataValueAsBytes32Array(bytes32,bytes32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32Array(bytes32,bytes32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32[100] value of the data

```


---

#### setDataValueAsBytes3Array(bytes32,bytes3[100])


**setDataValueAsBytes3Array(bytes32,bytes3[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes3Array(bytes32,bytes3[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes3[100] value of the data

```


---

#### setDataValueAsBytes4Array(bytes32,bytes4[100])


**setDataValueAsBytes4Array(bytes32,bytes4[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes4Array(bytes32,bytes4[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes4[100] value of the data

```


---

#### setDataValueAsBytes8Array(bytes32,bytes8[100])


**setDataValueAsBytes8Array(bytes32,bytes8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes8Array(bytes32,bytes8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes8[100] value of the data

```


---

#### setDataValueAsInt(bytes32,int256,uint8)


**setDataValueAsInt(bytes32,int256,uint8)**


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


---

#### setDataValueAsInt128Array(bytes32,int128[100])


**setDataValueAsInt128Array(bytes32,int128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt128Array(bytes32,int128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int128[100] value of the data

```


---

#### setDataValueAsInt16Array(bytes32,int16[100])


**setDataValueAsInt16Array(bytes32,int16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt16Array(bytes32,int16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int16[100] value of the data

```


---

#### setDataValueAsInt256(bytes32,int256)


**setDataValueAsInt256(bytes32,int256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256(bytes32,int256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the int value of the data

```


---

#### setDataValueAsInt256Array(bytes32,int256[100])


**setDataValueAsInt256Array(bytes32,int256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256Array(bytes32,int256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int256[100] value of the data

```


---

#### setDataValueAsInt32Array(bytes32,int32[100])


**setDataValueAsInt32Array(bytes32,int32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt32Array(bytes32,int32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int32[100] value of the data

```


---

#### setDataValueAsInt64Array(bytes32,int64[100])


**setDataValueAsInt64Array(bytes32,int64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt64Array(bytes32,int64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int64[100] value of the data

```


---

#### setDataValueAsInt8Array(bytes32,int8[100])


**setDataValueAsInt8Array(bytes32,int8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt8Array(bytes32,int8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int8[100] value of the data

```


---

#### setDataValueAsString(bytes32,string)


**setDataValueAsString(bytes32,string)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsString(bytes32,string)
```

#### Parameters

```solidity
_id // the id of the data
_value // the string value of the data

```


---

#### setDataValueAsUint(bytes32,uint256,uint8)


**setDataValueAsUint(bytes32,uint256,uint8)**


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


---

#### setDataValueAsUint128Array(bytes32,uint128[100])


**setDataValueAsUint128Array(bytes32,uint128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint128Array(bytes32,uint128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint128[100] value of the data

```


---

#### setDataValueAsUint16Array(bytes32,uint16[100])


**setDataValueAsUint16Array(bytes32,uint16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint16Array(bytes32,uint16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint16[100] value of the data

```


---

#### setDataValueAsUint256(bytes32,uint256)


**setDataValueAsUint256(bytes32,uint256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256(bytes32,uint256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint value of the data

```


---

#### setDataValueAsUint256Array(bytes32,uint256[100])


**setDataValueAsUint256Array(bytes32,uint256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256Array(bytes32,uint256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint256[100] value of the data

```


---

#### setDataValueAsUint32Array(bytes32,uint32[100])


**setDataValueAsUint32Array(bytes32,uint32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint32Array(bytes32,uint32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint32[100] value of the data

```


---

#### setDataValueAsUint64Array(bytes32,uint64[100])


**setDataValueAsUint64Array(bytes32,uint64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint64Array(bytes32,uint64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint64[100] value of the data

```


---

#### setDataValueAsUint8Array(bytes32,uint8[100])


**setDataValueAsUint8Array(bytes32,uint8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint8Array(bytes32,uint8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint8[100] value of the data

```


---

### DataStorageUtils Library


The DataStorageUtils Library contract is found within the agreements bundle.

#### getNumberOfArrayEntries(DataStorageUtils.DataMap storage,bytes32,bool)


**getNumberOfArrayEntries(DataStorageUtils.DataMap storage,bytes32,bool)**


Returns the number of non-default entries in the array-type field specified in the given DataMap. Empty values are: 0 for int/uint, 0x0 for address, "" for bytes32, etc.) Currently only DataTypes.ADDRESSARRAY() and DataTypes.BYTES32ARRAY() are supported by this function

```endpoint
CALL getNumberOfArrayEntries(DataStorageUtils.DataMap storage,bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if true the array will be scanned to its end, otherwise the function returns on the first encountered default value
_key // a key pointing to a supported array-type field
_map // the DataMap

```

#### Return

```json
the number of non-default entries
```


---

#### getNumberOfEntries(address[100],bool)


**getNumberOfEntries(address[100],bool)**


Returns the number of non-default entries in the given array.

```endpoint
CALL getNumberOfEntries(address[100],bool)
```

#### Parameters

```solidity
_array // the array to scan
_fullscan // whether to keep scanning to the end even if default values are encountered

```

#### Return

```json
the number of non-empty entries in the array
```


---

#### getNumberOfEntries(bytes32[100],bool)


**getNumberOfEntries(bytes32[100],bool)**


Returns the number of non-default entries in the given array.

```endpoint
CALL getNumberOfEntries(bytes32[100],bool)
```

#### Parameters

```solidity
_array // the array to scan
_fullscan // whether to keep scanning to the end even if default values are encountered

```

#### Return

```json
the number of non-empty entries in the array
```


---

#### keyAtIndex(DataStorageUtils.DataMap storage,uint256)


**keyAtIndex(DataStorageUtils.DataMap storage,uint256)**


Returns the ID of the Data at the specified index in the given map

```endpoint
CALL keyAtIndex(DataStorageUtils.DataMap storage,uint256)
```


---

#### remove(DataStorageUtils.DataMap storage,bytes32)


**remove(DataStorageUtils.DataMap storage,bytes32)**


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


---


### DefaultActiveAgreement Interface


The DefaultActiveAgreement Interface contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### cancel()


**cancel()**


Registers the msg.sender as having canceled the agreement. During formation (legal states DRAFT and FORMULATED), the agreement can canceled unilaterally by one of the parties to the agreement. During execution (legal state EXECUTED), the agreement can only be canceled if all parties agree to do so by invoking this function.

```endpoint
CALL cancel()
```

#### Return

```json
BaseErrors.INVALID_ACTOR() if the msg.sender is not a party on this agreement, BaseErrors.NO_ERROR() otherwise.
```


---

#### getArchetype()


**getArchetype()**


Returns the archetype

```endpoint
CALL getArchetype()
```

#### Return

```json
the archetype address 
```


---

#### getCreator()


**getCreator()**


Returns the creator

```endpoint
CALL getCreator()
```

#### Return

```json
the creator address
```


---

#### getDataValueAsAddressArray(bytes32)


**getDataValueAsAddressArray(bytes32)**


Overriden method of DataStorage to return the agreement parties for special ID DATA_FIELD_AGREEMENT_PARTIES.

```endpoint
CALL getDataValueAsAddressArray(bytes32)
```

#### Parameters

```solidity
_id // the bytes32 ID of an address array

```

#### Return

```json
the address array
```


---

#### getEventLogReference()


**getEventLogReference()**


Returns the Hoard Address and Hoard Secret for the Event Log

```endpoint
CALL getEventLogReference()
```

#### Return

```json
the Hoard Address and Hoard Secret for the Event Log
```


---

#### getHoardAddress()


**getHoardAddress()**


Returns the Hoard Address

```endpoint
CALL getHoardAddress()
```

#### Return

```json
the Hoard Address

```


---

#### getLegalState()


**getLegalState()**


Returns the legal state of this agreement

```endpoint
CALL getLegalState()
```

#### Return

```json
the Agreements.LegalState as a uint
```


---

#### getMaxNumberOfEvents()


**getMaxNumberOfEvents()**


Returns the max number of events for the event log

```endpoint
CALL getMaxNumberOfEvents()
```

#### Return

```json
the max number of events for the event log
```


---

#### getName()


**getName()**


Gets name

```endpoint
CALL getName()
```

#### Return

```json
name name
```


---

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Overridden method of DataStorage to return the number of parties for special ID DATA_FIELD_AGREEMENT_PARTIES.

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // whether to scan beyond non-default values
_id // the ID of the data field

```

#### Return

```json
the size of the specified array
```


---

#### getNumberOfParties()


**getNumberOfParties()**


Gets number of parties

```endpoint
CALL getNumberOfParties()
```

#### Return

```json
size number of parties
```


---

#### getParty(uint256)


**getParty(uint256)**


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


---

#### getSignatureDetails(address)


**getSignatureDetails(address)**


Returns the signee and timestamp of the signature of the given party.

```endpoint
CALL getSignatureDetails(address)
```

#### Parameters

```solidity
_party // the signing party

```

#### Return

```json
the address of the signee (if the party authorized a signee other than itself)the time of signing or 0 if the address is not a party to this agreement or has not signed yet
```


---

#### gethoardSecret()


**gethoardSecret()**


Returns the Hoard Secret

```endpoint
CALL gethoardSecret()
```

#### Return

```json
the Hoard Secret
```


---

#### isPrivate()


**isPrivate()**


Returns the private flag

```endpoint
CALL isPrivate()
```

#### Return

```json
the private flag 
```


---

#### isSignedBy(address)


**isSignedBy(address)**


Returns whether the given account's signature is on the agreement.

```endpoint
CALL isSignedBy(address)
```

#### Parameters

```solidity
_signee // The account to check

```

#### Return

```json
true if the provided address is a recorded signature on the agreement, false otherwise
```


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

#### setEventLogReference(bytes32,bytes32)


**setEventLogReference(bytes32,bytes32)**


Sets the Hoard Address and Hoard Secret for the Event Log

```endpoint
CALL setEventLogReference(bytes32,bytes32)
```


---

#### setFulfilled()


**setFulfilled()**


Sets the legal state of this agreement to Agreements.LegalState.FULFILLED. Note: All other legal states are set by internal logic.

```endpoint
CALL setFulfilled()
```


---

#### sign()


**sign()**


Applies the msg.sender or tx.origin as a signature to this agreement, if the it can be authorized as a valid signee. The timestamp of an already existing signature is not overwritten!

```endpoint
CALL sign()
```

#### Return

```json
an error code indicating success or failure
```


---

### DefaultActiveAgreementRegistry Interface


The DefaultActiveAgreementRegistry Interface contract is found within the agreements bundle.

#### addAgreementToCollection(bytes32,address)


**addAgreementToCollection(bytes32,address)**


Adds an agreement to given collection

```endpoint
CALL addAgreementToCollection(bytes32,address)
```

#### Parameters

```solidity
_agreement // agreement address
_collectionId // the bytes32 collection id

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() collection by given id does not exist
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)


**createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)**


Creates an Active Agreement with the given parameters

```endpoint
CALL createAgreement(address,bytes32,address,bytes32,bytes32,bytes32,bytes32,uint256,bool,address[],bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_collectionId // id of agreement collection (optional)
_hoardAddress // Address of agreement params in hoard
_hoardSecret // Secret for hoard retrieval
_name // name
_parties // parties

```

#### Return

```json
error - BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if _archetype or _name is nullactiveAgreement - the new ActiveAgreement's address, if successfully created, 0x0 otherwise
```


---

#### createAgreementCollection(string,address,uint8,bytes32)


**createAgreementCollection(string,address,uint8,bytes32)**


Creates a new agreement collection

```endpoint
CALL createAgreementCollection(string,address,uint8,bytes32)
```

#### Parameters

```solidity
_author // address of author
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED(), BaseErrors.RESOURCE_ALREADY_EXISTS()id bytes32 id of package
```


---

#### createUserAccount(address,address,bytes32)


**createUserAccount(address,address,bytes32)**


Creates an AgreementPartyAccount with the specified parameters and adds it to the AccountsManager

```endpoint
CALL createUserAccount(address,address,bytes32)
```

#### Parameters

```solidity
_accountsManager // the AccountsManager address
_id // id (optional)
_owner // owner (optional)

```

#### Return

```json
error BaseErrors.RESOURCE_ALREADY_EXISTS() or BaseErrors.NO_ERROR()userAccount user account address, or 0x0 if not successful
```


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Overwrites AbstractEventListener function to receive updates from ActiveAgreements that are registered in this registry. Currently supports AGREEMENT_STATE_CHANGED and EVENT_LOG_UPDATED

```endpoint
CALL eventFired(bytes32,address)
```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


Overwrites AbstractEventListener function to receive updates from ActiveAgreements that are registered in this registry. Currently supports AGREEMENT_SIGNATURE_ADDED

```endpoint
CALL eventFired(bytes32,address,address)
```


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


See EventListener.eventFired(bytes32,address,bytes32)

```endpoint
CALL eventFired(bytes32,address,bytes32)
```


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


See EventListener.eventFired(bytes32,address,string)

```endpoint
CALL eventFired(bytes32,address,string)
```


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


See EventListener.eventFired(bytes32,address,uint)

```endpoint
CALL eventFired(bytes32,address,uint256)
```


---

#### getActiveAgreementAtIndex(uint256)


**getActiveAgreementAtIndex(uint256)**


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


---

#### getActiveAgreementData(address)


**getActiveAgreementData(address)**


Returns data about the ActiveAgreement at the specified address

```endpoint
CALL getActiveAgreementData(address)
```

#### Parameters

```solidity
_activeAgreement // Active Agreement

```

#### Return

```json
archetype - the agreement's archetype adressname - the name of the agreementcreator - the creator of the agreementhoardAddress - address of the agreement parameters in hoard (only used when agreement is private)hoardSecret - secret for retrieval of hoard parameterseventLogHoardAddress - address of the agreement's event log in hoardeventLogHoardSecret - secret for retrieval of the hoard event log filemaxNumberOfEvents - the maximum number of events allowed to be stored for this agreementisPrivate - whether the agreement's parameters are private, i.e. stored off-chain in hoardlegalState - the agreement's Agreement.LegalState as uint8formationProcessInstance - the address of the process instance representing the formation of this agreementexecutionProcessInstance - the address of the process instance representing the execution of this agreement
```


---

#### getActiveAgreementsSize()


**getActiveAgreementsSize()**


Gets number of activeAgreements

```endpoint
CALL getActiveAgreementsSize()
```

#### Return

```json
size size
```


---

#### getAgreementAtIndexInCollection(bytes32,uint256)


**getAgreementAtIndexInCollection(bytes32,uint256)**


Gets agreement address at index in colelction

```endpoint
CALL getAgreementAtIndexInCollection(bytes32,uint256)
```

#### Parameters

```solidity
_id // id of the collection
_index // uint index

```

#### Return

```json
agreement address of archetype
```


---

#### getAgreementCollectionAtIndex(uint256)


**getAgreementCollectionAtIndex(uint256)**


Gets collection id at index

```endpoint
CALL getAgreementCollectionAtIndex(uint256)
```

#### Parameters

```solidity
_index // uint index

```

#### Return

```json
id bytes32 id
```


---

#### getAgreementCollectionData(bytes32)


**getAgreementCollectionData(bytes32)**


Gets collection data by id

```endpoint
CALL getAgreementCollectionData(bytes32)
```

#### Parameters

```solidity
_id // bytes32 collection id

```

#### Return

```json
name stringauthor addresscollectionType type of collectionpackageId id of the archetype package
```


---

#### getAgreementDataInCollection(bytes32,address)


**getAgreementDataInCollection(bytes32,address)**


Get agreement data by collection id and agreement address

```endpoint
CALL getAgreementDataInCollection(bytes32,address)
```

#### Parameters

```solidity
_agreement // address of agreement
_id // id of the collection

```

#### Return

```json
agreementName name of agreementarchetype address of archetype
```


---

#### getAgreementParameterAtIndex(address,uint256)


**getAgreementParameterAtIndex(address,uint256)**


Returns the ID of the agreement parameter value at the given index.

```endpoint
CALL getAgreementParameterAtIndex(address,uint256)
```

#### Parameters

```solidity
_pos // the index

```

#### Return

```json
the parameter ID
```


---

#### getAgreementParameterDetails(address,bytes32)


**getAgreementParameterDetails(address,bytes32)**


Returns information about the process data entry for the specified process and data ID

```endpoint
CALL getAgreementParameterDetails(address,bytes32)
```

#### Parameters

```solidity
_address // the active agreement
_dataId // the parameter ID

```

#### Return

```json
(process,id,uintValue,bytes32Value,addressValue,boolValue)
```


---

#### getArchetypeRegistry()


**getArchetypeRegistry()**


Returns the ArchetypeRegistry address

```endpoint
CALL getArchetypeRegistry()
```

#### Return

```json
address the ArchetypeRegistry
```


---

#### getBpmService()


**getBpmService()**


Returns the BpmService address

```endpoint
CALL getBpmService()
```

#### Return

```json
address the BpmService
```


---

#### getNumberOfAgreementCollections()


**getNumberOfAgreementCollections()**


Gets number of agreement collections

```endpoint
CALL getNumberOfAgreementCollections()
```

#### Return

```json
size size
```


---

#### getNumberOfAgreementParameters(address)


**getNumberOfAgreementParameters(address)**


Returns the number of agreement parameter values.

```endpoint
CALL getNumberOfAgreementParameters(address)
```

#### Return

```json
the number of parameters
```


---

#### getNumberOfAgreementsInCollection(bytes32)


**getNumberOfAgreementsInCollection(bytes32)**


Gets number of agreements in given collection

```endpoint
CALL getNumberOfAgreementsInCollection(bytes32)
```

#### Parameters

```solidity
_id // id of the collection

```

#### Return

```json
size agreement count
```


---

#### getPartiesByActiveAgreementSize(address)


**getPartiesByActiveAgreementSize(address)**


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


---

#### getPartyByActiveAgreementAtIndex(address,uint256)


**getPartyByActiveAgreementAtIndex(address,uint256)**


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


---

#### getPartyByActiveAgreementData(address,address)


**getPartyByActiveAgreementData(address,address)**


Returns data about the given party's signature on the specified agreement.

```endpoint
CALL getPartyByActiveAgreementData(address,address)
```

#### Parameters

```solidity
_activeAgreement // the ActiveAgreement
_party // the signing party

```

#### Return

```json
signedBy the actual signature authorized by the partysignatureTimestamp the timestamp when the party has signed, or 0 if not signed yet
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### processStateChanged(address)


**processStateChanged(address)**

```endpoint
CALL processStateChanged(address)
```

#### Parameters

```solidity
_processInstance // the process instance whose state has changed

```


---

#### setArchetypeRegistry(address)


**setArchetypeRegistry(address)**


Sets the ArchetypeRegistry reference used to find archetypes in packages

```endpoint
CALL setArchetypeRegistry(address)
```

#### Parameters

```solidity
_archetypeRegistry // the ArchetypeRegistry

```


---

#### setBpmService(address)


**setBpmService(address)**


Sets the BpmService reference to use for controlling the agreement workflows.

```endpoint
CALL setBpmService(address)
```

#### Parameters

```solidity
_service // the BpmService

```


---

#### setEventLogReference(address,bytes32,bytes32)


**setEventLogReference(address,bytes32,bytes32)**


Updates the hoard address and secret for the event log of the specified agreement

```endpoint
CALL setEventLogReference(address,bytes32,bytes32)
```

#### Parameters

```solidity
_activeAgreement // Address of active agreement
_eventLogHoardAddress // New hoard address of event log for agreement
_eventLogHoardSecret // New hoard secret key of event log for agreement

```


---

#### startFormation(address)


**startFormation(address)**


Creates a starts a ProcessInstance to handle the formation workflow as defined by the given agreement's archetype.

```endpoint
CALL startFormation(address)
```

#### Parameters

```solidity
_agreement // an ActiveAgreement

```

#### Return

```json
error - BaseErrors.INVALID_PARAM_STATE() if the agreement is not in legal state FORMULATEDerror - BaseErrors.OVERWRITE_NOT_ALLOWED() if there is an ongoing formation process for the agreementerror - BaseErrors.NO_ERROR() if the formation process was started successfully, or a different error code if there were problems in the processthe address of the ProcessInstance, if successful
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultArchetype


The DefaultArchetype contract is found within the agreements bundle.

#### activate()


**activate()**


Activates this archetype

```endpoint
CALL activate()
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### addDocument(bytes32,bytes32,bytes32)


**addDocument(bytes32,bytes32,bytes32)**


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


---

#### addJurisdiction(bytes2,bytes32)


**addJurisdiction(bytes2,bytes32)**


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


---

#### addParameter(uint8,bytes32)


**addParameter(uint8,bytes32)**


Adds parameter

```endpoint
CALL addParameter(uint8,bytes32)
```

#### Parameters

```solidity
_parameterName // parameter name
_parameterType // parameter type (enum)

```

#### Return

```json
BaseErrors.NO_ERROR() if successful,
BaseErrors.NULL_PARAM_NOT_ALLOWED() if _parameter is empty,
BaseErrors.RESOURCE_ALREADY_EXISTS() if _parameter already exists
```


---

#### deactivate()


**deactivate()**


Deactivates this archetype

```endpoint
CALL deactivate()
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### getAuthor()


**getAuthor()**


Gets Author

```endpoint
CALL getAuthor()
```

#### Return

```json
author author
```


---

#### getDescription()


**getDescription()**


Gets description

```endpoint
CALL getDescription()
```

#### Return

```json
description
```


---

#### getDocument(bytes32)


**getDocument(bytes32)**


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


---

#### getDocumentAtIndex(uint256)


**getDocumentAtIndex(uint256)**


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


---

#### getExecutionProcessDefinition()


**getExecutionProcessDefinition()**


Returns the address of the ProcessDefinition that orchestrates the agreement execution.

```endpoint
CALL getExecutionProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getFormationProcessDefinition()


**getFormationProcessDefinition()**


Returns the address of the ProcessDefinition that orchestrates the agreement formation.

```endpoint
CALL getFormationProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getJurisdictionAtIndex(uint256)


**getJurisdictionAtIndex(uint256)**


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


---

#### getJurisdictionData(bytes32)


**getJurisdictionData(bytes32)**


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


---

#### getName()


**getName()**


Returns the archetype name

```endpoint
CALL getName()
```

#### Return

```json
the name
```


---

#### getNumberOfDocuments()


**getNumberOfDocuments()**


Gets number of documents

```endpoint
CALL getNumberOfDocuments()
```

#### Return

```json
size number of documents
```


---

#### getNumberOfJurisdictions()


**getNumberOfJurisdictions()**


Returns the number jurisdictions for this archetype

```endpoint
CALL getNumberOfJurisdictions()
```

#### Return

```json
the number of jurisdictions
```


---

#### getNumberOfParameters()


**getNumberOfParameters()**


Gets number of parameters

```endpoint
CALL getNumberOfParameters()
```

#### Return

```json
size number of parameters
```


---

#### getParameterAtIndex(uint256)


**getParameterAtIndex(uint256)**


Gets parameter at index

```endpoint
CALL getParameterAtIndex(uint256)
```

#### Parameters

```solidity
_index // index

```

#### Return

```json
error error TBDparameter parameter
```


---

#### getParameterType(bytes32)


**getParameterType(bytes32)**


Gets parameter data type

```endpoint
CALL getParameterType(bytes32)
```

#### Parameters

```solidity
_parameter // parameter

```

#### Return

```json
error error TBDparameterType parameter type
```


---

#### isActive()


**isActive()**


Returns the active state

```endpoint
CALL isActive()
```

#### Return

```json
true if active, false otherwise
```


---

#### isPrivate()


**isPrivate()**


Returns the private state

```endpoint
CALL isPrivate()
```

#### Return

```json
true if private, false otherwise
```


---

### DefaultArchetypeRegistry


The DefaultArchetypeRegistry contract is found within the agreements bundle.

#### activate(address)


**activate(address)**


Sets active to true for given archetype

```endpoint
CALL activate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### addArchetypeToPackage(bytes32,address)


**addArchetypeToPackage(bytes32,address)**


Adds archetype to package

```endpoint
CALL addArchetypeToPackage(bytes32,address)
```

#### Parameters

```solidity
_archetype // the archetype address
_packageId // the bytes32 package id

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.RESOURCE_NOT_FOUND() package by given id does not exist
```


---

#### addDocument(address,bytes32,bytes32,bytes32)


**addDocument(address,bytes32,bytes32,bytes32)**


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


---

#### addJurisdiction(address,bytes2,bytes32)


**addJurisdiction(address,bytes2,bytes32)**


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


---

#### addJurisdictions(address,bytes2[],bytes32[])


**addJurisdictions(address,bytes2[],bytes32[])**


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


---

#### addParameter(address,uint8,bytes32)


**addParameter(address,uint8,bytes32)**


Adds parameter to archetype

```endpoint
CALL addParameter(address,uint8,bytes32)
```

#### Parameters

```solidity
_archetype // the archetype address
_parameterName // the parameter name
_parameterType // data type (enum)

```

#### Return

```json
BaseErrors.NO_ERROR() if successfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundany error returned from the Archetype.addParameter() function
```


---

#### addParameters(address,uint8[],bytes32[])


**addParameters(address,uint8[],bytes32[])**


Adds the specified parameters to the archetype. If one of the parameters cannot be added, the operation aborts and returns that error code.

```endpoint
CALL addParameters(address,uint8[],bytes32[])
```

#### Parameters

```solidity
_archetype // the archetype address
_parameterNames // the parameter names
_parameterTypes // the parameter types

```

#### Return

```json
BaseErrors.NO_ERROR() if succesfulBaseErrors.RESOURCE_NOT_FOUND() if archetype is not foundBaseErrors.INVALID_PARAM_STATE() if the lengths of the two arrays don't match
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createArchetype(bytes32,address,string,bool,address,address,bytes32)


**createArchetype(bytes32,address,string,bool,address,address,bytes32)**


Creates a new archetype

```endpoint
CALL createArchetype(bytes32,address,string,bool,address,address,bytes32)
```

#### Parameters

```solidity
_author // author
_description // description
_executionProcess // the address of a ProcessDefinition that orchestrates the agreement execution
_formationProcess // the address of a ProcessDefinition that orchestrates the agreement formation
_isPrivate // determines if the archetype's documents are encrypted
_name // name
_packageId // id of package this archetype is part of (optional)

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED() if either _name, _author, _formationProcess, or _executionProcess is nullarchetype - the new archetype's address, if successfully created
```


---

#### createArchetypePackage(string,string,address,bool)


**createArchetypePackage(string,string,address,bool)**


Adds a new archetype package

```endpoint
CALL createArchetypePackage(string,string,address,bool)
```

#### Parameters

```solidity
_author // address of author (user account of organization)
_description // description
_isPrivate // makes it a private package visible to only the author
_name // name

```

#### Return

```json
error BaseErrors.NO_ERROR(), BaseErrors.NULL_PARAM_NOT_ALLOWED(), BaseErrors.RESOURCE_ALREADY_EXISTS()id bytes32 id of package
```


---

#### deactivate(address)


**deactivate(address)**


Sets active to false for given archetype

```endpoint
CALL deactivate(address)
```

#### Return

```json
error BaseErrors.NO_ERROR()
```


---

#### getArchetypeAtIndex(uint256)


**getArchetypeAtIndex(uint256)**


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


---

#### getArchetypeAtIndexInPackage(bytes32,uint256)


**getArchetypeAtIndexInPackage(bytes32,uint256)**


Gets archetype address at index in package

```endpoint
CALL getArchetypeAtIndexInPackage(bytes32,uint256)
```

#### Parameters

```solidity
_id // id of the package
_index // uint index

```

#### Return

```json
archetype address of archetype
```


---

#### getArchetypeData(address)


**getArchetypeData(address)**


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


---

#### getArchetypeDataInPackage(bytes32,address)


**getArchetypeDataInPackage(bytes32,address)**


Get archetype data by package id and archetype address

```endpoint
CALL getArchetypeDataInPackage(bytes32,address)
```

#### Parameters

```solidity
_archetype // address of archetype
_id // id of the package

```

#### Return

```json
archetypeName name of archetype
```


---

#### getArchetypePackageAtIndex(uint256)


**getArchetypePackageAtIndex(uint256)**


Gets package id at index

```endpoint
CALL getArchetypePackageAtIndex(uint256)
```

#### Parameters

```solidity
_index // uint index

```

#### Return

```json
id bytes32 id
```


---

#### getArchetypePackageData(bytes32)


**getArchetypePackageData(bytes32)**


Gets package data by id

```endpoint
CALL getArchetypePackageData(bytes32)
```

#### Parameters

```solidity
_id // bytes32 package id

```

#### Return

```json
name stringdescription stringauthor addressisPrivate bool
```


---

#### getArchetypesSize()


**getArchetypesSize()**


Gets number of archetypes

```endpoint
CALL getArchetypesSize()
```

#### Return

```json
size size
```


---

#### getDocumentByArchetypeAtIndex(address,uint256)


**getDocumentByArchetypeAtIndex(address,uint256)**


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


---

#### getDocumentByArchetypeData(address,bytes32)


**getDocumentByArchetypeData(address,bytes32)**


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


---

#### getDocumentsByArchetypeSize(address)


**getDocumentsByArchetypeSize(address)**


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


---

#### getJurisdictionAtIndexForArchetype(address,uint256)


**getJurisdictionAtIndexForArchetype(address,uint256)**


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


---

#### getJurisdictionDataForArchetype(address,bytes32)


**getJurisdictionDataForArchetype(address,bytes32)**


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


---

#### getNumberOfArchetypePackages()


**getNumberOfArchetypePackages()**


Gets number of archetype packages

```endpoint
CALL getNumberOfArchetypePackages()
```

#### Return

```json
size size
```


---

#### getNumberOfArchetypesInPackage(bytes32)


**getNumberOfArchetypesInPackage(bytes32)**


Gets number of archetypes in given package

```endpoint
CALL getNumberOfArchetypesInPackage(bytes32)
```

#### Parameters

```solidity
_id // id of the package

```

#### Return

```json
size archetype count
```


---

#### getNumberOfJurisdictionsForArchetype(address)


**getNumberOfJurisdictionsForArchetype(address)**


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


---

#### getParameterByArchetypeAtIndex(address,uint256)


**getParameterByArchetypeAtIndex(address,uint256)**


Gets parameter name by Archetype At index

```endpoint
CALL getParameterByArchetypeAtIndex(address,uint256)
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


---

#### getParameterByArchetypeData(address,bytes32)


**getParameterByArchetypeData(address,bytes32)**


Returns data about the parameter at with the specified name

```endpoint
CALL getParameterByArchetypeData(address,bytes32)
```

#### Parameters

```solidity
_archetype // archetype
_name // name

```

#### Return

```json
parameterType parameter type
```


---

#### getParametersByArchetypeSize(address)


**getParametersByArchetypeSize(address)**


Gets parameter count for given Archetype

```endpoint
CALL getParametersByArchetypeSize(address)
```

#### Parameters

```solidity
_archetype // archetype

```

#### Return

```json
size size
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### packageHasArchetype(bytes32,address)


**packageHasArchetype(bytes32,address)**


Determines whether given archetype address is in the package identified by the packageId

```endpoint
CALL packageHasArchetype(bytes32,address)
```

#### Parameters

```solidity
_archetype // address of archetype
_packageId // id of the package

```

#### Return

```json
hasArchetype bool representing if archetype is in package
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultEventEmitter


The DefaultEventEmitter contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

### DefaultUserAccount


The DefaultUserAccount contract is found within the agreements bundle.

#### getId()


**getId()**


Returns this account's ID

```endpoint
CALL getId()
```


---

#### getOrganization()


**getOrganization()**


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```


---

#### setOrganization(address)


**setOrganization(address)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---


### ERC165 Interface


The ERC165 Interface contract is found within the agreements bundle.

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Interface identification is specified in ERC-165. This function  uses less than 30,000 gas.

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
interfaceID // The interface identifier, as specified in ERC-165

```

#### Return

```json
`true` if the contract implements `interfaceID` and
`interfaceID` is not 0xffffffff, `false` otherwise
```


---

### ERC165Utils


The ERC165Utils contract is found within the agreements bundle.

#### implementsInterface(address,bytes4)


**implementsInterface(address,bytes4)**


Detects whether the given contract implements the specified ERC165 interface signature. This is a modified implementation of the example in EIP 881 to avoid the use of the "staticcall" opcode. This function performs two invocations: 1. A "call" to the 0x01ffc9a7 function signature to test if it can be invoked 2. If step 1 returns 'true', the contract is cast to ERC165 and the supportsInterface(bytes4) function is invoked

```endpoint
CALL implementsInterface(address,bytes4)
```

#### Parameters

```solidity
_contract // the contract to be examined
_interfaceId // the signature of the interface for which to test

```

#### Return

```json
true if the contract implements the interface, false otherwise
```


---

### EventEmitter Interface


The EventEmitter Interface contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

### EventListener


The EventListener contract is found within the agreements bundle.

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


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


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


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


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


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


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


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


---



### Mappings Library Public API Contract


The Mappings Library Public API Contract contract is found within the agreements bundle.

#### addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


**addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)**


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


---

#### addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


**addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)**


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


---

#### addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


**addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)**


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


---

#### addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


**addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)**


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


---

#### addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


**addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)**


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


---

#### clear(Mappings.AddressAddressArrayMap storage)


**clear(Mappings.AddressAddressArrayMap storage)**


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


---

#### clear(Mappings.AddressAddressMap storage)


**clear(Mappings.AddressAddressMap storage)**


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


---

#### clear(Mappings.AddressBytes32ArrayMap storage)


**clear(Mappings.AddressBytes32ArrayMap storage)**


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


---

#### clear(Mappings.AddressBytes32Map storage)


**clear(Mappings.AddressBytes32Map storage)**


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


---

#### clear(Mappings.Bytes32AddressArrayMap storage)


**clear(Mappings.Bytes32AddressArrayMap storage)**


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


---

#### clear(Mappings.Bytes32AddressMap storage)


**clear(Mappings.Bytes32AddressMap storage)**


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


---

#### clear(Mappings.Bytes32Bytes32Map storage)


**clear(Mappings.Bytes32Bytes32Map storage)**


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


---

#### clear(Mappings.Bytes32UintMap storage)


**clear(Mappings.Bytes32UintMap storage)**


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


---

#### clear(Mappings.UintAddressArrayMap storage)


**clear(Mappings.UintAddressArrayMap storage)**


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


---

#### clear(Mappings.UintAddressMap storage)


**clear(Mappings.UintAddressMap storage)**


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


---

#### clear(Mappings.UintBytes32ArrayMap storage)


**clear(Mappings.UintBytes32ArrayMap storage)**


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


---

#### exists(Mappings.AddressAddressArrayMap storage,address)


**exists(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### exists(Mappings.AddressAddressMap storage,address)


**exists(Mappings.AddressAddressMap storage,address)**


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


---

#### exists(Mappings.AddressBytes32ArrayMap storage,address)


**exists(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### exists(Mappings.AddressBytes32Map storage,address)


**exists(Mappings.AddressBytes32Map storage,address)**


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


---

#### exists(Mappings.Bytes32AddressArrayMap storage,bytes32)


**exists(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### exists(Mappings.Bytes32AddressMap storage,bytes32)


**exists(Mappings.Bytes32AddressMap storage,bytes32)**


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


---

#### exists(Mappings.Bytes32Bytes32Map storage,bytes32)


**exists(Mappings.Bytes32Bytes32Map storage,bytes32)**


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


---

#### exists(Mappings.Bytes32UintMap storage,bytes32)


**exists(Mappings.Bytes32UintMap storage,bytes32)**


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


---

#### exists(Mappings.UintAddressArrayMap storage,uint256)


**exists(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### exists(Mappings.UintAddressMap storage,uint256)


**exists(Mappings.UintAddressMap storage,uint256)**


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


---

#### exists(Mappings.UintBytes32ArrayMap storage,uint256)


**exists(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### get(Mappings.AddressAddressArrayMap storage,address)


**get(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### get(Mappings.AddressAddressMap storage,address)


**get(Mappings.AddressAddressMap storage,address)**


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


---

#### get(Mappings.AddressBytes32ArrayMap storage,address)


**get(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### get(Mappings.AddressBytes32Map storage,address)


**get(Mappings.AddressBytes32Map storage,address)**


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


---

#### get(Mappings.Bytes32AddressArrayMap storage,bytes32)


**get(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### get(Mappings.Bytes32AddressMap storage,bytes32)


**get(Mappings.Bytes32AddressMap storage,bytes32)**


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


---

#### get(Mappings.Bytes32Bytes32Map storage,bytes32)


**get(Mappings.Bytes32Bytes32Map storage,bytes32)**


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


---

#### get(Mappings.Bytes32UintMap storage,bytes32)


**get(Mappings.Bytes32UintMap storage,bytes32)**


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


---

#### get(Mappings.UintAddressArrayMap storage,uint256)


**get(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### get(Mappings.UintAddressMap storage,uint256)


**get(Mappings.UintAddressMap storage,uint256)**


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


---

#### get(Mappings.UintBytes32ArrayMap storage,uint256)


**get(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### insert(Mappings.AddressAddressArrayMap storage,address,address[])


**insert(Mappings.AddressAddressArrayMap storage,address,address[])**


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


---

#### insert(Mappings.AddressAddressMap storage,address,address)


**insert(Mappings.AddressAddressMap storage,address,address)**


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


---

#### insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


**insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])**


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


---

#### insert(Mappings.AddressBytes32Map storage,address,bytes32)


**insert(Mappings.AddressBytes32Map storage,address,bytes32)**


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


---

#### insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


**insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])**


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


---

#### insert(Mappings.Bytes32AddressMap storage,bytes32,address)


**insert(Mappings.Bytes32AddressMap storage,bytes32,address)**


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


---

#### insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


**insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)**


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


---

#### insert(Mappings.Bytes32UintMap storage,bytes32,uint256)


**insert(Mappings.Bytes32UintMap storage,bytes32,uint256)**


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


---

#### insert(Mappings.UintAddressArrayMap storage,uint256,address[])


**insert(Mappings.UintAddressArrayMap storage,uint256,address[])**


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


---

#### insert(Mappings.UintAddressMap storage,uint256,address)


**insert(Mappings.UintAddressMap storage,uint256,address)**


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


---

#### insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


**insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])**


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


---

#### insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])


**insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])**


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


---

#### insertOrUpdate(Mappings.AddressAddressMap storage,address,address)


**insertOrUpdate(Mappings.AddressAddressMap storage,address,address)**


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


---

#### insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


**insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])**


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


---

#### insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)


**insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)**


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


---

#### insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


**insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])**


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


---

#### insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)


**insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)**


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


---

#### insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


**insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)**


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


---

#### insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)


**insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)**


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


---

#### insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])


**insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])**


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


---

#### insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)


**insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)**


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


---

#### insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


**insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])**


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


---

#### keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)


**keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressAddressMap storage,uint256)


**keyAtIndex(Mappings.AddressAddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)


**keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressBytes32Map storage,uint256)


**keyAtIndex(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)


**keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)


**keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)


**keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32UintMap storage,uint256)


**keyAtIndex(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)


**keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintAddressMap storage,uint256)


**keyAtIndex(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)


**keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


**keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### keyIndex(Mappings.AddressAddressArrayMap storage,address)


**keyIndex(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### keyIndex(Mappings.AddressAddressMap storage,address)


**keyIndex(Mappings.AddressAddressMap storage,address)**


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


---

#### keyIndex(Mappings.AddressBytes32ArrayMap storage,address)


**keyIndex(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### keyIndex(Mappings.AddressBytes32Map storage,address)


**keyIndex(Mappings.AddressBytes32Map storage,address)**


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


---

#### keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)


**keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### keyIndex(Mappings.Bytes32AddressMap storage,bytes32)


**keyIndex(Mappings.Bytes32AddressMap storage,bytes32)**


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


---

#### keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)


**keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)**


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


---

#### keyIndex(Mappings.Bytes32UintMap storage,bytes32)


**keyIndex(Mappings.Bytes32UintMap storage,bytes32)**


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


---

#### keyIndex(Mappings.UintAddressArrayMap storage,uint256)


**keyIndex(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyIndex(Mappings.UintAddressMap storage,uint256)


**keyIndex(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)


**keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### remove(Mappings.AddressAddressArrayMap storage,address)


**remove(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### remove(Mappings.AddressAddressMap storage,address)


**remove(Mappings.AddressAddressMap storage,address)**


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


---

#### remove(Mappings.AddressBytes32ArrayMap storage,address)


**remove(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### remove(Mappings.AddressBytes32Map storage,address)


**remove(Mappings.AddressBytes32Map storage,address)**


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


---

#### remove(Mappings.Bytes32AddressArrayMap storage,bytes32)


**remove(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### remove(Mappings.Bytes32AddressMap storage,bytes32)


**remove(Mappings.Bytes32AddressMap storage,bytes32)**


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


---

#### remove(Mappings.Bytes32Bytes32Map storage,bytes32)


**remove(Mappings.Bytes32Bytes32Map storage,bytes32)**


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


---

#### remove(Mappings.Bytes32UintMap storage,bytes32)


**remove(Mappings.Bytes32UintMap storage,bytes32)**


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


---

#### remove(Mappings.UintAddressArrayMap storage,uint256)


**remove(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### remove(Mappings.UintAddressMap storage,uint256)


**remove(Mappings.UintAddressMap storage,uint256)**


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


---

#### remove(Mappings.UintBytes32ArrayMap storage,uint256)


**remove(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


**removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)**


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


---

#### removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


**removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)**


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


---

#### removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


**removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)**


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


---

#### removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


**removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)**


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


---

#### removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


**removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)**


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


---

#### valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


**valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

### Migratable Interface


The Migratable Interface contract is found within the agreements bundle.

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

### Named Interface


The Named Interface contract is found within the agreements bundle.

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

### NamedElement Interface


The NamedElement Interface contract is found within the agreements bundle.

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

### Organization Interface


The Organization Interface contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### addUser(address)


**addUser(address)**


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


---

#### getApproverAtIndex(uint256)


**getApproverAtIndex(uint256)**


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


---

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfApprovers()


**getNumberOfApprovers()**


Returns the number of registered approvers.

```endpoint
CALL getNumberOfApprovers()
```

#### Return

```json
the number of approvers
```


---

#### getNumberOfUsers()


**getNumberOfUsers()**


returns the number of users associated with this organization

```endpoint
CALL getNumberOfUsers()
```

#### Return

```json
the number of users
```


---

#### getUserAtIndex(uint256)


**getUserAtIndex(uint256)**


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


---

#### isActiveUser(address)


**isActiveUser(address)**


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


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

#### removeUser(address)


**removeUser(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Interface identification is specified in ERC-165. This function  uses less than 30,000 gas.

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
interfaceID // The interface identifier, as specified in ERC-165

```

#### Return

```json
`true` if the contract implements `interfaceID` and
`interfaceID` is not 0xffffffff, `false` otherwise
```


---

### Owned


The Owned contract is found within the agreements bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### OwnerTransferable


The OwnerTransferable contract is found within the agreements bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---


### ProcessDefinition Interface


The ProcessDefinition Interface contract is found within the agreements bundle.

#### addProcessInterfaceImplementation(address,bytes32)


**addProcessInterfaceImplementation(address,bytes32)**


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


---

#### createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)


**createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)**


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType [TASK|SUBPROCESS]
_application // the application handling the execution of the activity
_assignee // the ID of the participant performing the activity (for USER tasks only)
_behavior // the BpmModel.TaskBehavior [SEND|SENDRECEIVE|RECEIVE]
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_subProcessDefinitionId // references a subprocess definition (only for SUBPROCESS ActivityType)
_subProcessModelId // references the model containg a subprocess definition (only for SUBPROCESS ActivityType)
_taskType // the BpmModel.TaskType [DUMMY|USER|SERVICE|EVENT]

```

#### Return

```json
an error code indicating success or failure
```


---

#### createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)


**createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)**


Create a data mapping for the specified activity and direction.

```endpoint
CALL createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)
```

#### Parameters

```solidity
_accessPath // the access path offered by the application
_activityId // the ID of the activity in this ProcessDefinition
_dataPath // a data path (key) to use for data lookup on a DataStorage.
_dataStorage // an optional address of a DataStorage as basis for the data path other than the default one
_dataStorageId // an optional key to identify a DataStorage as basis for the data path other than the default one
_direction // the BpmModel.Direction [IN|OUT]

```


---

#### createTransition(bytes32,bytes32)


**createTransition(bytes32,bytes32)**


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


---

#### getActivityAtIndex(uint256)


**getActivityAtIndex(uint256)**


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


---

#### getActivityData(bytes32)


**getActivityData(bytes32)**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8taskBehavior the BpmModel.TaskBehavior as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationsubProcessModelId the ID of a process model (for subprocess activities)subProcessDefinitionId the ID of a process definition (for subprocess activities)
```


---

#### getActivityInputGateway(bytes32)


**getActivityInputGateway(bytes32)**


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


---

#### getActivityOutputGateway(bytes32)


**getActivityOutputGateway(bytes32)**


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


---

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getImplementedProcessInterfaceAtIndex(uint256)


**getImplementedProcessInterfaceAtIndex(uint256)**


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


---

#### getInDataMappingAtIndex(bytes32,uint256)


**getInDataMappingAtIndex(bytes32,uint256)**


Returns information about the IN data mapping of the specified activity at the given index

```endpoint
CALL getInDataMappingAtIndex(bytes32,uint256)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition
_idx // the index position

```

#### Return

```json
accessPath the access path on the applicationdataPath a data path (key) to use for identifying the data location in a DataStorage contractdataStorageId a key to identify a secondary DataStorage as basis for the data path other than the default onedataStorage an address of a DataStorage as basis for the data path other than the default one
```


---

#### getModel()


**getModel()**


Returns the address of the model which contains this process definition

```endpoint
CALL getModel()
```

#### Return

```json
the model address
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfActivities()


**getNumberOfActivities()**


Returns the number of activity definitions in this ProcessDefinition.

```endpoint
CALL getNumberOfActivities()
```

#### Return

```json
the number of activity definitions
```


---

#### getNumberOfImplementedProcessInterfaces()


**getNumberOfImplementedProcessInterfaces()**


Returns the number of implemented process interfaces implemented by this ProcessDefinition

```endpoint
CALL getNumberOfImplementedProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```


---

#### getNumberOfInDataMappings(bytes32)


**getNumberOfInDataMappings(bytes32)**


Returns the number of IN data mappings for the specified activity.

```endpoint
CALL getNumberOfInDataMappings(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition

```

#### Return

```json
the number of IN data mappings
```


---

#### getNumberOfOutDataMappings(bytes32)


**getNumberOfOutDataMappings(bytes32)**


Returns the number of OUT data mappings for the specified activity.

```endpoint
CALL getNumberOfOutDataMappings(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition

```

#### Return

```json
the number of OUT data mappings
```


---

#### getOutDataMappingAtIndex(bytes32,uint256)


**getOutDataMappingAtIndex(bytes32,uint256)**


Returns information about the OUT data mapping of the specified activity at the given index

```endpoint
CALL getOutDataMappingAtIndex(bytes32,uint256)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition
_idx // the index position

```

#### Return

```json
accessPath the access path on the applicationdataPath a data path (key) to use for identifying the data location in a DataStorage contractdataStorageId a key to identify a secondary DataStorage as basis for the data path other than the default onedataStorage an address of a DataStorage as basis for the data path other than the default one
```


---

#### getStartActivity()


**getStartActivity()**


Returns the ID of the start activity of this process definition. If the process is valid, this value must be set.

```endpoint
CALL getStartActivity()
```

#### Return

```json
the ID of the identified start activity
```


---

#### implementsProcessInterface(address,bytes32)


**implementsProcessInterface(address,bytes32)**


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


---

#### isValid()


**isValid()**


Returns the current validity state

```endpoint
CALL isValid()
```

#### Return

```json
true if valid, false otherwise
```


---

#### setActivityInputGateway(bytes32,uint8)


**setActivityInputGateway(bytes32,uint8)**


Sets the input gateway of the specified activity to the given type.

```endpoint
CALL setActivityInputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```


---

#### setActivityOutputGateway(bytes32,uint8)


**setActivityOutputGateway(bytes32,uint8)**


Sets the output gateway of the specified activity to the given type.

```endpoint
CALL setActivityOutputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```


---

#### validate()


**validate()**


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag.

```endpoint
CALL validate()
```

#### Return

```json
valid - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```


---

### ProcessInstance Interface


The ProcessInstance Interface contract is found within the agreements bundle.

#### abort(address)


**abort(address)**


Aborts this ProcessInstance and halts any ongoing activities. After the abort the ProcessInstance cannot be resurrected.

```endpoint
CALL abort(address)
```

#### Parameters

```solidity
_service // the BpmService to emit update events for ActivityInstances

```


---

#### addProcessStateChangeListener(address)


**addProcessStateChangeListener(address)**


Adds a ProcessStateChangeListener to listeners collection

```endpoint
CALL addProcessStateChangeListener(address)
```

#### Parameters

```solidity
_listener // the ProcessStateChangeListener to add

```


---

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the activity instance
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance after the activity completes)

```

#### Return

```json
an error code indicating success or failure
```


---

#### execute(address)


**execute(address)**


Initiates execution of this ProcessInstance consisting of attempting to activate and process any activities and advance the state of the runtime graph.

```endpoint
CALL execute(address)
```

#### Parameters

```solidity
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance and access to the BpmServiceDb)

```

#### Return

```json
error code indicating success or failure
```


---

#### getActivityInstanceAtIndex(uint256)


**getActivityInstanceAtIndex(uint256)**


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


---

#### getActivityInstanceData(bytes32)


**getActivityInstanceData(bytes32)**


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
activityId - the ID of the activity as defined by the process definitioncreated - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) state - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```


---

#### getDataIdAtIndex(uint256)


**getDataIdAtIndex(uint256)**


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


---

#### getDataType(bytes32)


**getDataType(bytes32)**


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


---

#### getDataValueAsAddress(bytes32)


**getDataValueAsAddress(bytes32)**


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


---

#### getDataValueAsAddressArray(bytes32)


**getDataValueAsAddressArray(bytes32)**


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


---

#### getDataValueAsBool(bytes32)


**getDataValueAsBool(bytes32)**


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


---

#### getDataValueAsBytes(bytes32)


**getDataValueAsBytes(bytes32)**


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


---

#### getDataValueAsBytes16Array(bytes32)


**getDataValueAsBytes16Array(bytes32)**


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


---

#### getDataValueAsBytes1Array(bytes32)


**getDataValueAsBytes1Array(bytes32)**


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


---

#### getDataValueAsBytes20Array(bytes32)


**getDataValueAsBytes20Array(bytes32)**


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


---

#### getDataValueAsBytes24Array(bytes32)


**getDataValueAsBytes24Array(bytes32)**


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


---

#### getDataValueAsBytes28Array(bytes32)


**getDataValueAsBytes28Array(bytes32)**


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


---

#### getDataValueAsBytes2Array(bytes32)


**getDataValueAsBytes2Array(bytes32)**


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


---

#### getDataValueAsBytes32Array(bytes32)


**getDataValueAsBytes32Array(bytes32)**


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


---

#### getDataValueAsBytes3Array(bytes32)


**getDataValueAsBytes3Array(bytes32)**


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


---

#### getDataValueAsBytes4Array(bytes32)


**getDataValueAsBytes4Array(bytes32)**


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


---

#### getDataValueAsBytes8Array(bytes32)


**getDataValueAsBytes8Array(bytes32)**


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


---

#### getDataValueAsInt(bytes32)


**getDataValueAsInt(bytes32)**


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


---

#### getDataValueAsInt128Array(bytes32)


**getDataValueAsInt128Array(bytes32)**


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


---

#### getDataValueAsInt16Array(bytes32)


**getDataValueAsInt16Array(bytes32)**


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


---

#### getDataValueAsInt256Array(bytes32)


**getDataValueAsInt256Array(bytes32)**


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


---

#### getDataValueAsInt32Array(bytes32)


**getDataValueAsInt32Array(bytes32)**


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


---

#### getDataValueAsInt64Array(bytes32)


**getDataValueAsInt64Array(bytes32)**


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


---

#### getDataValueAsInt8Array(bytes32)


**getDataValueAsInt8Array(bytes32)**


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


---

#### getDataValueAsString(bytes32)


**getDataValueAsString(bytes32)**


Gets the value of the Data object identified by the given id

```endpoint
CALL getDataValueAsString(bytes32)
```

#### Parameters

```solidity
_id // the id of the data

```

#### Return

```json
string the value of the data
```


---

#### getDataValueAsUint(bytes32)


**getDataValueAsUint(bytes32)**


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


---

#### getDataValueAsUint128Array(bytes32)


**getDataValueAsUint128Array(bytes32)**


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


---

#### getDataValueAsUint16Array(bytes32)


**getDataValueAsUint16Array(bytes32)**


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


---

#### getDataValueAsUint256Array(bytes32)


**getDataValueAsUint256Array(bytes32)**


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


---

#### getDataValueAsUint32Array(bytes32)


**getDataValueAsUint32Array(bytes32)**


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


---

#### getDataValueAsUint64Array(bytes32)


**getDataValueAsUint64Array(bytes32)**


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


---

#### getDataValueAsUint8Array(bytes32)


**getDataValueAsUint8Array(bytes32)**


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


---

#### getNumberOfActivityInstances()


**getNumberOfActivityInstances()**


Returns the number of activity instances currently contained in this ProcessInstance. Note that this number is subject to change as long as the process isntance is not completed.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```


---

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Returns the number of non-default entries in the specified array-type DataStorage field

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if false the function will return as soon as a default value (0 for int/uint, 0x0 for address, "" for bytes32, etc.) is encountered, if true the array will be scanned to its end
_key // the key for the array-type value

```

#### Return

```json
the number of non-default entries in the array
```


---

#### getProcessDefinition()


**getProcessDefinition()**


Returns the process definition on which this instance is based.

```endpoint
CALL getProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getSize()


**getSize()**


Returns the size of the DataMap

```endpoint
CALL getSize()
```

#### Return

```json
uint the size
```


---

#### getStartedBy()


**getStartedBy()**


Returns the account that started this process instance

```endpoint
CALL getStartedBy()
```

#### Return

```json
the address registered when creating the process instance
```


---

#### getState()


**getState()**


Returns the state of this process instance

```endpoint
CALL getState()
```

#### Return

```json
the uint representation of the BpmRuntime.ProcessInstanceState
```


---

#### initRuntime()


**initRuntime()**


Initiates and populates the runtime graph that will handle the state of this ProcessInstance

```endpoint
CALL initRuntime()
```

#### Return

```json
error code indicating success or failure
```


---

#### notifyProcessStateChange()


**notifyProcessStateChange()**


Notifies listeners about a process state change

```endpoint
CALL notifyProcessStateChange()
```


---

#### removeData(bytes32)


**removeData(bytes32)**


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


---

#### setDataValueAsAddress(bytes32,address)


**setDataValueAsAddress(bytes32,address)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddress(bytes32,address)
```

#### Parameters

```solidity
_id // the id of the data
_value // the address value of the data

```


---

#### setDataValueAsAddressArray(bytes32,address[100])


**setDataValueAsAddressArray(bytes32,address[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsAddressArray(bytes32,address[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the address[100] value of the data

```


---

#### setDataValueAsBool(bytes32,bool)


**setDataValueAsBool(bytes32,bool)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBool(bytes32,bool)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bool value of the data

```


---

#### setDataValueAsBytes(bytes32,bytes32,uint8)


**setDataValueAsBytes(bytes32,bytes32,uint8)**


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


---

#### setDataValueAsBytes16Array(bytes32,bytes16[100])


**setDataValueAsBytes16Array(bytes32,bytes16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes16Array(bytes32,bytes16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes16[100] value of the data

```


---

#### setDataValueAsBytes1Array(bytes32,bytes1[100])


**setDataValueAsBytes1Array(bytes32,bytes1[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes1Array(bytes32,bytes1[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes1[100] value of the data

```


---

#### setDataValueAsBytes20Array(bytes32,bytes20[100])


**setDataValueAsBytes20Array(bytes32,bytes20[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes20Array(bytes32,bytes20[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes20[100] value of the data

```


---

#### setDataValueAsBytes24Array(bytes32,bytes24[100])


**setDataValueAsBytes24Array(bytes32,bytes24[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes24Array(bytes32,bytes24[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes24[100] value of the data

```


---

#### setDataValueAsBytes28Array(bytes32,bytes28[100])


**setDataValueAsBytes28Array(bytes32,bytes28[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes28Array(bytes32,bytes28[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes28[100] value of the data

```


---

#### setDataValueAsBytes2Array(bytes32,bytes2[100])


**setDataValueAsBytes2Array(bytes32,bytes2[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes2Array(bytes32,bytes2[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes2[100] value of the data

```


---

#### setDataValueAsBytes32(bytes32,bytes32)


**setDataValueAsBytes32(bytes32,bytes32)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32(bytes32,bytes32)
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32 value of the data

```


---

#### setDataValueAsBytes32Array(bytes32,bytes32[100])


**setDataValueAsBytes32Array(bytes32,bytes32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes32Array(bytes32,bytes32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes32[100] value of the data

```


---

#### setDataValueAsBytes3Array(bytes32,bytes3[100])


**setDataValueAsBytes3Array(bytes32,bytes3[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes3Array(bytes32,bytes3[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes3[100] value of the data

```


---

#### setDataValueAsBytes4Array(bytes32,bytes4[100])


**setDataValueAsBytes4Array(bytes32,bytes4[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes4Array(bytes32,bytes4[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes4[100] value of the data

```


---

#### setDataValueAsBytes8Array(bytes32,bytes8[100])


**setDataValueAsBytes8Array(bytes32,bytes8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsBytes8Array(bytes32,bytes8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the bytes8[100] value of the data

```


---

#### setDataValueAsInt(bytes32,int256,uint8)


**setDataValueAsInt(bytes32,int256,uint8)**


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


---

#### setDataValueAsInt128Array(bytes32,int128[100])


**setDataValueAsInt128Array(bytes32,int128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt128Array(bytes32,int128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int128[100] value of the data

```


---

#### setDataValueAsInt16Array(bytes32,int16[100])


**setDataValueAsInt16Array(bytes32,int16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt16Array(bytes32,int16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int16[100] value of the data

```


---

#### setDataValueAsInt256(bytes32,int256)


**setDataValueAsInt256(bytes32,int256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256(bytes32,int256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the int value of the data

```


---

#### setDataValueAsInt256Array(bytes32,int256[100])


**setDataValueAsInt256Array(bytes32,int256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt256Array(bytes32,int256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int256[100] value of the data

```


---

#### setDataValueAsInt32Array(bytes32,int32[100])


**setDataValueAsInt32Array(bytes32,int32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt32Array(bytes32,int32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int32[100] value of the data

```


---

#### setDataValueAsInt64Array(bytes32,int64[100])


**setDataValueAsInt64Array(bytes32,int64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt64Array(bytes32,int64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int64[100] value of the data

```


---

#### setDataValueAsInt8Array(bytes32,int8[100])


**setDataValueAsInt8Array(bytes32,int8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsInt8Array(bytes32,int8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the int8[100] value of the data

```


---

#### setDataValueAsString(bytes32,string)


**setDataValueAsString(bytes32,string)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsString(bytes32,string)
```

#### Parameters

```solidity
_id // the id of the data
_value // the string value of the data

```


---

#### setDataValueAsUint(bytes32,uint256,uint8)


**setDataValueAsUint(bytes32,uint256,uint8)**


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


---

#### setDataValueAsUint128Array(bytes32,uint128[100])


**setDataValueAsUint128Array(bytes32,uint128[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint128Array(bytes32,uint128[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint128[100] value of the data

```


---

#### setDataValueAsUint16Array(bytes32,uint16[100])


**setDataValueAsUint16Array(bytes32,uint16[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint16Array(bytes32,uint16[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint16[100] value of the data

```


---

#### setDataValueAsUint256(bytes32,uint256)


**setDataValueAsUint256(bytes32,uint256)**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256(bytes32,uint256)
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint value of the data

```


---

#### setDataValueAsUint256Array(bytes32,uint256[100])


**setDataValueAsUint256Array(bytes32,uint256[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint256Array(bytes32,uint256[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint256[100] value of the data

```


---

#### setDataValueAsUint32Array(bytes32,uint32[100])


**setDataValueAsUint32Array(bytes32,uint32[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint32Array(bytes32,uint32[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint32[100] value of the data

```


---

#### setDataValueAsUint64Array(bytes32,uint64[100])


**setDataValueAsUint64Array(bytes32,uint64[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint64Array(bytes32,uint64[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint64[100] value of the data

```


---

#### setDataValueAsUint8Array(bytes32,uint8[100])


**setDataValueAsUint8Array(bytes32,uint8[100])**


Creates a Data object with the given value and inserts it into the DataMap

```endpoint
CALL setDataValueAsUint8Array(bytes32,uint8[100])
```

#### Parameters

```solidity
_id // the id of the data
_value // the uint8[100] value of the data

```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### ProcessModel Interface


The ProcessModel Interface contract is found within the agreements bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### addParticipant(bytes32,address,bytes32,bytes32,address)


**addParticipant(bytes32,address,bytes32,bytes32,address)**


Adds a participant with the specified ID and attributes to this ProcessModel

```endpoint
CALL addParticipant(bytes32,address,bytes32,bytes32,address)
```

#### Parameters

```solidity
_account // the address of a participant account
_dataPath // the field key under which to locate the conditional participant
_dataStorage // the address of a DataStorage contract to find a conditional participant
_dataStorageId // a field key in a known DataStorage containing an address of another DataStorage contract
_id // the participant ID

```

#### Return

```json
an error code indicating success or failure
```


---

#### addProcessInterface(bytes32)


**addProcessInterface(bytes32)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createProcessDefinition(bytes32,bytes32)


**createProcessDefinition(bytes32,bytes32)**


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


---

#### fireActivityDefinitionUpdateEvent(bytes32)


**fireActivityDefinitionUpdateEvent(bytes32)**


To be called by a registered process definition to signal an update.

```endpoint
CALL fireActivityDefinitionUpdateEvent(bytes32)
```


---

#### fireProcessDefinitionUpdateEvent()


**fireProcessDefinitionUpdateEvent()**


To be called by a registered process definition to signal an update.

```endpoint
CALL fireProcessDefinitionUpdateEvent()
```


---

#### getDiagram()


**getDiagram()**


Returns the HOARD file information of the model's diagram

```endpoint
CALL getDiagram()
```

#### Return

```json
location - the HOARD addresssecret - the HOARD secret
```


---

#### getId()


**getId()**


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfParticipants()


**getNumberOfParticipants()**


Returns the number of participants defined in this ProcessModel

```endpoint
CALL getNumberOfParticipants()
```

#### Return

```json
the number of participants
```


---

#### getNumberOfProcessDefinitions()


**getNumberOfProcessDefinitions()**


Returns the number of process definitions in this ProcessModel

```endpoint
CALL getNumberOfProcessDefinitions()
```

#### Return

```json
the number of process definitions
```


---

#### getNumberOfProcessInterfaces()


**getNumberOfProcessInterfaces()**


Returns the number of process interfaces declared in this ProcessModel

```endpoint
CALL getNumberOfProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```


---

#### getParticipantAtIndex(uint256)


**getParticipantAtIndex(uint256)**


Returns the ID of the participant at the given index

```endpoint
CALL getParticipantAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the participant ID, if it exists
```


---

#### getParticipantData(bytes32)


**getParticipantData(bytes32)**


Returns information about the participant with the given ID

```endpoint
CALL getParticipantData(bytes32)
```

#### Parameters

```solidity
_id // the participant ID

```

#### Return

```json
location the applications contract address, only available for a service participantmethod the function signature of the participant, only available for a service participantwebForm the form identifier (formHash) of the web participant, only available for a web participant
```


---

#### getProcessDefinition(bytes32)


**getProcessDefinition(bytes32)**


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


---

#### getProcessDefinitionAtIndex(uint256)


**getProcessDefinitionAtIndex(uint256)**


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


---

#### getProcessDefinitionData(address)


**getProcessDefinitionData(address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### hasParticipant(bytes32)


**hasParticipant(bytes32)**


Returns whether a participant with the specified ID exists in this ProcessModel

```endpoint
CALL hasParticipant(bytes32)
```

#### Parameters

```solidity
_id // the participant ID

```

#### Return

```json
true if it exists, false otherwise
```


---

#### hasProcessInterface(bytes32)


**hasProcessInterface(bytes32)**


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


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

### ProcessModelRepository Interface


The ProcessModelRepository Interface contract is found within the agreements bundle.

#### activateModel(address)


**activateModel(address)**


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


---

#### addModel(address)


**addModel(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)


**createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)**


Factory function to instantiate a ProcessModel.

```endpoint
CALL createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)
```

#### Parameters

```solidity
_hoardAddress // the HOARD address of the model file
_hoardSecret // the HOARD secret of the model file
_id // the model ID
_name // the model name
_version // the model version

```


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


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


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


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


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


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


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


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


---

#### getActivityAtIndex(address,address,uint256)


**getActivityAtIndex(address,address,uint256)**


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


---

#### getActivityData(address,address,bytes32)


**getActivityData(address,address,bytes32)**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8taskBehavior the BpmModel.TaskBehavior as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationsubProcessModelId the ID of a process model (for subprocess activities)subProcessDefinitionId the ID of a process definition (for subprocess activities)
```


---

#### getModel(bytes32)


**getModel(bytes32)**


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


---

#### getModelAtIndex(uint256)


**getModelAtIndex(uint256)**


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


---

#### getModelByVersion(bytes32,uint8[3])


**getModelByVersion(bytes32,uint8[3])**


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


---

#### getModelData(address)


**getModelData(address)**


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
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch versionactive - whether the model is activediagramAddress - the HOARD address of the model diagram filediagramSecret - the HOARD secret of the model diagram file
```


---

#### getNumberOfActivities(address,address)


**getNumberOfActivities(address,address)**


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


---

#### getNumberOfModels()


**getNumberOfModels()**


Returns the number of models in this repository.

```endpoint
CALL getNumberOfModels()
```

#### Return

```json
size - the number of models
```


---

#### getNumberOfProcessDefinitions(address)


**getNumberOfProcessDefinitions(address)**


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


---

#### getProcessDefinition(bytes32,bytes32)


**getProcessDefinition(bytes32,bytes32)**


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


---

#### getProcessDefinitionAtIndex(address,uint256)


**getProcessDefinitionAtIndex(address,uint256)**


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


---

#### getProcessDefinitionData(address,address)


**getProcessDefinitionData(address,address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### ProcessStateChangeEmitter


The ProcessStateChangeEmitter contract is found within the agreements bundle.

#### addProcessStateChangeListener(address)


**addProcessStateChangeListener(address)**


Adds a ProcessStateChangeListener to listeners collection

```endpoint
CALL addProcessStateChangeListener(address)
```

#### Parameters

```solidity
_listener // the ProcessStateChangeListener to add

```


---

#### notifyProcessStateChange()


**notifyProcessStateChange()**


Notifies listeners about a process state change

```endpoint
CALL notifyProcessStateChange()
```


---

### ProcessStateChangeListener


The ProcessStateChangeListener contract is found within the agreements bundle.

#### processStateChanged(address)


**processStateChanged(address)**


Invoked by a ProcessStateChangeEventEmitter to notify of process state change

```endpoint
CALL processStateChanged(address)
```

#### Parameters

```solidity
_pi // the process instance whose state changed

```


---

### Signable


The Signable contract is found within the agreements bundle.

#### sign()


**sign()**


Applies a signature. The implementing contract has the msg.sender, or the tx.origin at its disposal to use as signature. This function is therefore intended to be called directly from the account that is attempting to sign.

```endpoint
CALL sign()
```

#### Return

```json
a return code indicating success or type of failure
```


---

### SystemOwned


The SystemOwned contract is found within the agreements bundle.

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### SystemOwnerTransferable


The SystemOwnerTransferable contract is found within the agreements bundle.

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### TypeUtils Library Interface


The TypeUtils Library Interface contract is found within the agreements bundle.

#### contentLength(bytes32)


**contentLength(bytes32)**


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


---

#### isEmpty(bytes32)


**isEmpty(bytes32)**


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


---

#### toBytes32(string)


**toBytes32(string)**


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


---

#### toBytes32(uint256)


**toBytes32(uint256)**


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


---

### Upgradeable


The Upgradeable contract is found within the agreements bundle.

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### UserAccount Interface


The UserAccount Interface contract is found within the agreements bundle.

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getOrganization()


**getOrganization()**


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```

#### Return

```json
the owner address
```


---

#### setOrganization(address)


**setOrganization(address)**


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


---

### Versioned


The Versioned contract is found within the agreements bundle.

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

### WorkflowProxy


The WorkflowProxy contract is found within the agreements bundle.

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService required for lookup and access to the BpmServiceDb

```

#### Return

```json
error code if the completion failed
```


---

### WorkflowUserAccount


The WorkflowUserAccount contract is found within the agreements bundle.

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService required for lookup and access to the BpmServiceDb

```

#### Return

```json
error code if the completion failed
```


---

#### getId()


**getId()**


Returns this account's ID

```endpoint
CALL getId()
```


---

#### getOrganization()


**getOrganization()**


Returns this user account's organization, if it is associated with one.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization's address or 0x0
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```


---

#### setOrganization(address)


**setOrganization(address)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

## bpm-model


### DefaultProcessDefinition


The DefaultProcessDefinition contract is found within the bpm-model bundle.

#### addProcessInterfaceImplementation(address,bytes32)


**addProcessInterfaceImplementation(address,bytes32)**


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


---

#### createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)


**createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)**


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,uint8,bytes32,bool,bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType [TASK|SUBPROCESS]
_application // the application handling the execution of the activity
_assignee // the ID of the participant performing the activity (for USER tasks only)
_behavior // the BpmModel.TaskBehavior [SEND|SENDRECEIVE|RECEIVE]
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_subProcessDefinitionId // references a subprocess definition (only for SUBPROCESS ActivityType)
_subProcessModelId // references the model containg a subprocess definition (only for SUBPROCESS ActivityType)
_taskType // the BpmModel.TaskType [DUMMY|USER|SERVICE|EVENT]

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an activity with the same ID already existsBaseErrors.INVALID_PARAM_VALUE() if an assignee is specified, but the BpmModel.TaskType is not USERBaseErrors.NULL_PARAM_NOT_ALLOWED() if BpmModel.TaskType is USER, but no assignee was specifiedBaseErrors.RESOURCE_NOT_FOUND() if an assignee is specified that does not exist in the modelBaseErrors.NO_ERROR() upon successful creation.
```


---

#### createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)


**createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)**


Create a data mapping for the specified activity and direction.

```endpoint
CALL createDataMapping(bytes32,uint8,bytes32,bytes32,bytes32,address)
```

#### Parameters

```solidity
_accessPath // the access path offered by the application
_activityId // the ID of the activity in this ProcessDefinition
_dataPath // a data path (key) to use for data lookup on a DataStorage.
_dataStorage // an optional address of a DataStorage as basis for the data path other than the default one
_dataStorageId // an optional key to identify a DataStorage as basis for the data path other than the default one
_direction // the BpmModel.Direction [IN|OUT]

```


---

#### createTransition(bytes32,bytes32)


**createTransition(bytes32,bytes32)**


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
BaseErrors.RESOURCE_NOT_FOUND() if either the source or target activity does not existBaseErrors.RESOURCE_ALREADY_EXISTS() if a transition between the source and target already existsBaseErrors.NO_ERROR() upon successful creation.
```


---

#### getActivityAtIndex(uint256)


**getActivityAtIndex(uint256)**


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


---

#### getActivityData(bytes32)


**getActivityData(bytes32)**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8taskBehavior the BpmModel.TaskBehavior as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationsubProcessModelId the ID of a process model (for subprocess activities)subProcessDefinitionId the ID of a process definition (for subprocess activities)
```


---

#### getActivityInputGateway(bytes32)


**getActivityInputGateway(bytes32)**


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


---

#### getActivityOutputGateway(bytes32)


**getActivityOutputGateway(bytes32)**


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


---

#### getId()


**getId()**


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getImplementedProcessInterfaceAtIndex(uint256)


**getImplementedProcessInterfaceAtIndex(uint256)**


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


---

#### getInDataMappingAtIndex(bytes32,uint256)


**getInDataMappingAtIndex(bytes32,uint256)**


Returns information about the IN data mapping of the specified activity at the given index

```endpoint
CALL getInDataMappingAtIndex(bytes32,uint256)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition
_idx // the index position

```

#### Return

```json
accessPath the access path on the applicationdataPath a data path (key) to use for identifying the data location in a DataStorage contractdataStorageId a key to identify a secondary DataStorage as basis for the data path other than the default onedataStorage an address of a DataStorage as basis for the data path other than the default one
```


---

#### getModel()


**getModel()**


Returns the address of the model which contains this process definition

```endpoint
CALL getModel()
```

#### Return

```json
the model address
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfActivities()


**getNumberOfActivities()**


Returns the number of activity definitions in this ProcessDefinition.

```endpoint
CALL getNumberOfActivities()
```

#### Return

```json
the number of activity definitions
```


---

#### getNumberOfImplementedProcessInterfaces()


**getNumberOfImplementedProcessInterfaces()**


Returns the number of implemented process interfaces implemented by this ProcessDefinition

```endpoint
CALL getNumberOfImplementedProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```


---

#### getNumberOfInDataMappings(bytes32)


**getNumberOfInDataMappings(bytes32)**


Returns the number of IN data mappings for the specified activity.

```endpoint
CALL getNumberOfInDataMappings(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition

```

#### Return

```json
the number of IN data mappings
```


---

#### getNumberOfOutDataMappings(bytes32)


**getNumberOfOutDataMappings(bytes32)**


Returns the number of OUT data mappings for the specified activity.

```endpoint
CALL getNumberOfOutDataMappings(bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition

```

#### Return

```json
the number of OUT data mappings
```


---

#### getOutDataMappingAtIndex(bytes32,uint256)


**getOutDataMappingAtIndex(bytes32,uint256)**


Returns information about the OUT data mapping of the specified activity at the given index

```endpoint
CALL getOutDataMappingAtIndex(bytes32,uint256)
```

#### Parameters

```solidity
_activityId // the ID of the activity in this ProcessDefinition
_idx // the index position

```

#### Return

```json
accessPath the access path on the applicationdataPath a data path (key) to use for identifying the data location in a DataStorage contractdataStorageId a key to identify a secondary DataStorage as basis for the data path other than the default onedataStorage an address of a DataStorage as basis for the data path other than the default one
```


---

#### getStartActivity()


**getStartActivity()**


Returns the ID of the start activity of this process definition. This value is set during the validate() function, if the process is valid.

```endpoint
CALL getStartActivity()
```

#### Return

```json
the ID of the identified start activity
```


---

#### implementsProcessInterface(address,bytes32)


**implementsProcessInterface(address,bytes32)**


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


---

#### isValid()


**isValid()**


Returns the current validity state

```endpoint
CALL isValid()
```

#### Return

```json
true if valid, false otherwise
```


---

#### setActivityInputGateway(bytes32,uint8)


**setActivityInputGateway(bytes32,uint8)**


Sets the input gateway of the specified activity to the given type.

```endpoint
CALL setActivityInputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```


---

#### setActivityOutputGateway(bytes32,uint8)


**setActivityOutputGateway(bytes32,uint8)**


Sets the output gateway of the specified activity to the given type.

```endpoint
CALL setActivityOutputGateway(bytes32,uint8)
```

#### Parameters

```solidity
_activityId // the ID of the activity
_type // the gateway type

```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### validate()


**validate()**


Validates the coherence of the process definition in terms of the diagram and its configuration and sets the valid flag. Currently performed validation: 1. There must be exactly one start activity, i.e. one activity with no inputs 2. Activities with more than 1 inputs/outputs must have a supporting input/output gateway type (OR, XOR, AND). 3. User task activities must have an assignee or conditional assignee configuration

```endpoint
CALL validate()
```

#### Return

```json
result - boolean indicating validityerrorMessage - empty string if valid, otherwise contains a hint what failed
```


---

### DefaultProcessModel


The DefaultProcessModel contract is found within the bpm-model bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### addParticipant(bytes32,address,bytes32,bytes32,address)


**addParticipant(bytes32,address,bytes32,bytes32,address)**


Adds a participant with the specified ID and attributes to this ProcessModel

```endpoint
CALL addParticipant(bytes32,address,bytes32,bytes32,address)
```

#### Parameters

```solidity
_account // the address of a participant account
_dataPath // the field key under which to locate the conditional participant
_dataStorage // the address of a DataStorage contract to find a conditional participant
_dataStorageId // a field key in a known DataStorage containing an address of another DataStorage contract
_id // the participant ID

```

#### Return

```json
BaseErrors.INVALID_PARAM_VALUE() if both participant and conditional participant are being attempted to be set or if the config for a conditional participant is missing the _dataPathBaseErrors.NO_ERROR() if successful
```


---

#### addProcessInterface(bytes32)


**addProcessInterface(bytes32)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createProcessDefinition(bytes32,bytes32)


**createProcessDefinition(bytes32,bytes32)**


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


---

#### fireActivityDefinitionUpdateEvent(bytes32)


**fireActivityDefinitionUpdateEvent(bytes32)**


To be called by a registered process definition to signal an update. Causes the ProcessModel to emit an update event on behalf of the msg.sender

```endpoint
CALL fireActivityDefinitionUpdateEvent(bytes32)
```


---

#### fireProcessDefinitionUpdateEvent()


**fireProcessDefinitionUpdateEvent()**


To be called by a registered process definition to signal an update. Causes the ProcessModel to emit an update event on behalf of the msg.sender

```endpoint
CALL fireProcessDefinitionUpdateEvent()
```


---

#### getDiagram()


**getDiagram()**


Returns the HOARD file information of the model's diagram

```endpoint
CALL getDiagram()
```

#### Return

```json
location - the HOARD addresssecret - the HOARD secret
```


---

#### getId()


**getId()**


Returns the ID of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getNumberOfParticipants()


**getNumberOfParticipants()**


Returns the number of participants defined in this ProcessModel

```endpoint
CALL getNumberOfParticipants()
```

#### Return

```json
the number of participants
```


---

#### getNumberOfProcessDefinitions()


**getNumberOfProcessDefinitions()**


Returns the number of process definitions in this ProcessModel

```endpoint
CALL getNumberOfProcessDefinitions()
```

#### Return

```json
the number of process definitions
```


---

#### getNumberOfProcessInterfaces()


**getNumberOfProcessInterfaces()**


Returns the number of process interfaces declared in this ProcessModel

```endpoint
CALL getNumberOfProcessInterfaces()
```

#### Return

```json
the number of process interfaces
```


---

#### getParticipantAtIndex(uint256)


**getParticipantAtIndex(uint256)**


Returns the ID of the participant at the given index

```endpoint
CALL getParticipantAtIndex(uint256)
```

#### Parameters

```solidity
_idx // the index position

```

#### Return

```json
the participant ID, if it exists
```


---

#### getParticipantData(bytes32)


**getParticipantData(bytes32)**


Returns information about the participant with the given ID

```endpoint
CALL getParticipantData(bytes32)
```

#### Parameters

```solidity
_id // the participant ID

```

#### Return

```json
location the applications contract address, only available for a service participantmethod the function signature of the participant, only available for a service participantwebForm the form identifier (formHash) of the web participant, only available for a web participant
```


---

#### getProcessDefinition(bytes32)


**getProcessDefinition(bytes32)**


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


---

#### getProcessDefinitionAtIndex(uint256)


**getProcessDefinitionAtIndex(uint256)**


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


---

#### getProcessDefinitionData(address)


**getProcessDefinitionData(address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### hasParticipant(bytes32)


**hasParticipant(bytes32)**


Returns whether a participant with the specified ID exists in this ProcessModel

```endpoint
CALL hasParticipant(bytes32)
```

#### Parameters

```solidity
_id // the participant ID

```

#### Return

```json
true if it exists, false otherwise
```


---

#### hasProcessInterface(bytes32)


**hasProcessInterface(bytes32)**


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


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

### DefaultProcessModelRepository


The DefaultProcessModelRepository contract is found within the bpm-model bundle.

#### activateModel(address)


**activateModel(address)**


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


---

#### addModel(address)


**addModel(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)


**createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)**


Factory function to instantiate a ProcessModel. The model is automatically added to this repository.

```endpoint
CALL createProcessModel(bytes32,bytes32,uint8[3],bytes32,bytes32)
```

#### Parameters

```solidity
_hoardAddress // the HOARD address of the model file
_hoardSecret // the HOARD secret of the model file
_id // the model ID
_name // the model name
_version // the model version

```


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Overwrites AbstractEventListener.eventFired to receive UPDATE_PROCESS_MODEL  and UPDATE_PROCESS_DEFINITION events from registered models.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the event source (process model)

```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


See EventListener.eventFired(bytes32,address,address)

```endpoint
CALL eventFired(bytes32,address,address)
```


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


Overwrites AbstractEventListener.eventFired to receive UPDATE_ACTIVITY_DEFINITION  events from registered models.

```endpoint
CALL eventFired(bytes32,address,bytes32)
```

#### Parameters

```solidity
_activityId // the activityId
_event // the event name
_source // the event source (process model)

```


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


See EventListener.eventFired(bytes32,address,string)

```endpoint
CALL eventFired(bytes32,address,string)
```


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


See EventListener.eventFired(bytes32,address,uint)

```endpoint
CALL eventFired(bytes32,address,uint256)
```


---

#### getActivityAtIndex(address,address,uint256)


**getActivityAtIndex(address,address,uint256)**


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


---

#### getActivityData(address,address,bytes32)


**getActivityData(address,address,bytes32)**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8taskBehavior the BpmModel.TaskBehavior as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationsubProcessModelId the ID of a process model (for subprocess activities)subProcessDefinitionId the ID of a process definition (for subprocess activities)
```


---

#### getModel(bytes32)


**getModel(bytes32)**


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


---

#### getModelAtIndex(uint256)


**getModelAtIndex(uint256)**


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


---

#### getModelByVersion(bytes32,uint8[3])


**getModelByVersion(bytes32,uint8[3])**


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


---

#### getModelData(address)


**getModelData(address)**


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
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch versionactive - whether the model is activediagramAddress - the HOARD address of the model diagram filediagramSecret - the HOARD secret of the model diagram file
```


---

#### getNumberOfActivities(address,address)


**getNumberOfActivities(address,address)**


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


---

#### getNumberOfModels()


**getNumberOfModels()**


Returns the number of models in this repository.

```endpoint
CALL getNumberOfModels()
```

#### Return

```json
size - the number of models
```


---

#### getNumberOfProcessDefinitions(address)


**getNumberOfProcessDefinitions(address)**


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


---

#### getProcessDefinition(bytes32,bytes32)


**getProcessDefinition(bytes32,bytes32)**


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


---

#### getProcessDefinitionAtIndex(address,uint256)


**getProcessDefinitionAtIndex(address,uint256)**


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


---

#### getProcessDefinitionData(address,address)


**getProcessDefinitionData(address,address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### ProcessModelRepositoryDb Interface


The ProcessModelRepositoryDb Interface contract is found within the bpm-model bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

## bpm-runtime

### AbstractProcessStateChangeEmitter


The AbstractProcessStateChangeEmitter contract is found within the bpm-runtime bundle.

#### addProcessStateChangeListener(address)


**addProcessStateChangeListener(address)**


Adds a ProcessStateChangeListener to listeners collection

```endpoint
CALL addProcessStateChangeListener(address)
```

#### Parameters

```solidity
_listener // the ProcessStateChangeListener to add

```


---

#### notifyProcessStateChange()


**notifyProcessStateChange()**


Notifies listeners about a process state change

```endpoint
CALL notifyProcessStateChange()
```


---


### ApplicationRegistryDb Interface


The ApplicationRegistryDb Interface contract is found within the bpm-runtime bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### BpmApi Interface Library


The BpmApi Interface Library contract is found within the bpm-runtime bundle.

#### abort(BpmRuntime.ProcessInstance storage,BpmService)


**abort(BpmRuntime.ProcessInstance storage,BpmService)**


Aborts the given ProcessInstance and all of its activities

```endpoint
CALL abort(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the process instance to abort

```


---

#### addActivity(BpmRuntime.ProcessGraph storage,bytes32)


**addActivity(BpmRuntime.ProcessGraph storage,bytes32)**


Adds an activity with the specified ID to the given process runtime graph.

```endpoint
CALL addActivity(BpmRuntime.ProcessGraph storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the activity ID to add

```


---

#### addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)


**addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)**


Adds an input arc to the given process runtime graph to connect from the provided activity to the provided transition.

```endpoint
CALL addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity from which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion to which to connect

```


---

#### addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)


**addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)**


Adds an output arc to the given process runtime graph to connect from the provided transition to the provided activity.

```endpoint
CALL addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity to which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion from which to connect

```


---

#### addTransition(BpmRuntime.ProcessGraph storage,bytes32)


**addTransition(BpmRuntime.ProcessGraph storage,bytes32)**


Adds a transition with the specified ID to the given process runtime graph.

```endpoint
CALL addTransition(BpmRuntime.ProcessGraph storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the transition ID to add

```


---

#### configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)


**configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)**


Configures a ProcessRuntimeIntance based on the provided ProcessDefinition.

```endpoint
CALL configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)
```

#### Parameters

```solidity
_graph // the runtime instance to configure
_processDefinition // the process definition

```

#### Return

```json
an error code indicating success or failure
```


---

#### continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)


**continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)**


Checks the given ProcessInstance for completeness and open activities. If activatable activities are detected, recursive execution is entered via execute(ProcessInstance). If the ProcessInstance is complete, its state is set to COMPLETED. Otherwise the function returns BaseErrors.NO_ERROR().

```endpoint
CALL continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the BpmRuntime.ProcessInstance

```

#### Return

```json
BaseErrors.NO_ERROR() if no errors were encountered during processing or no processing happenedany error code from entering into a recursive execute(ProcessInstance) and continuing to execute the process
```


---

#### execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)


**execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)**


Executes the given ActivityInstance based on the information in the provided ProcessDefinition.

```endpoint
CALL execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_processDefinition // a ProcessDefinition containing information how to execute the activity
_rootDataStorage // a DataStorage that can be used to resolve process data (typically this is the ProcessInstance itself)
_service // the BpmService to use for communicating

```

#### Return

```json
an error code indicating success or failure
```


---

#### execute(BpmRuntime.ProcessGraph storage)


**execute(BpmRuntime.ProcessGraph storage)**


Executes a single iteration of the given ProcessGraph, i.e. it goes over all transitions and attempts to fire them based on the current token state of the graph.

```endpoint
CALL execute(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the process runtime graph

```

#### Return

```json
the number of transitions that fired
```


---

#### execute(BpmRuntime.ProcessInstance storage,BpmService)


**execute(BpmRuntime.ProcessInstance storage,BpmService)**


Executes the given ProcessInstance leveraging the given BpmService reference by looking for activities that are "ready" to be executed. Execution continues along the process graph until no more activities can be executed. This function implements a single transaction of all activities in a process flow until an asynchronous point in the flow is reached or the process has ended.

```endpoint
CALL execute(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the ProcessInstance to execute
_service // the BpmService managing the ProcessInstance (used to register changes to the ProcessInstance and fire events)

```

#### Return

```json
an error code signaling success or failure
```


---

#### hasActivatableActivities(BpmRuntime.ProcessGraph storage)


**hasActivatableActivities(BpmRuntime.ProcessGraph storage)**


Determines whether the given runtime instance has any activities that are waiting to be activated.

```endpoint
CALL hasActivatableActivities(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the ProcessGraph

```

#### Return

```json
true if at least one activatable activity was found, false otherwise
```


---

#### invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)


**invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)**


Performs a call on the given application ID defined in the provided ApplicationRegistry

```endpoint
CALL invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_application // the application ID
_applicationRegistry // the registry where information about an application can be retrieved
_processDefinition // the process definition
_rootDataStorage // a DataStorage that is used as the root or default for resolving data references
_txPerformer // the account that initiated the current transaction (optional)

```

#### Return

```json
BaseErrors.RUNTIME_ERROR if there was an exception in calling the defined appliationBaseErrors.NO_ERROR() if successful
```


---

#### isCompleted(BpmRuntime.ProcessGraph storage)


**isCompleted(BpmRuntime.ProcessGraph storage)**


Executes the given ProcessGraph and reports back on completeness and open activities. The following scenarios are possible: (completed, !readyActivities): the process is done, there are no more activities to process (!completed, readyActivities): the process is still active and there are activities ready for processing (!completed, !readyActivities): the process is still active, but no activities are ready to be processed (which means there must be instances waiting for asynchronous events)

```endpoint
CALL isCompleted(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the BpmRuntime.ProcessGraph

```

#### Return

```json
completed - if true, the graph cannot be executed any furtherreadyActivities - if true there are activities ready for processing, false otherwise
```


---

#### isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)


**isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)**


Determines whether the conditions are met to fire the provided transition.

```endpoint
CALL isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)
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


---

#### resolveParticipant(ProcessModel,DataStorage,bytes32)


**resolveParticipant(ProcessModel,DataStorage,bytes32)**


Provides runtime resolution capabilities to determine the account address or lookup location of an account for a participant in a given ProcessModel. This function supports dealing with concrete participants as well as conditional performers. Examples: Return value (FE80A3F6CDFEF73D4FACA7DBA1DFCF215299279D, "") => The address is a concrete (user) account and can be used directly Return value (AA194B34D18F710058C0B14CFDAD4FF0150856EA, "accountant") => The address is a DataStorage contract and the (user) account to use can be located using DataStorage(AA194B34D18F710058C0B14CFDAD4FF0150856EA).getDataValueAsAddress("accountant")

```endpoint
CALL resolveParticipant(ProcessModel,DataStorage,bytes32)
```

#### Parameters

```solidity
_dataStorage // a concrete DataStorage instance supporting the lookup
_participant // the ID of a participant in the given model
_processModel // a ProcessModel

```

#### Return

```json
target - either the address of an account or the address of another DataStorage where the account can be founddataPath - empty bytes32 in case the returned target is already an identified account or a key where to retrieve the account if the target is another DataStorage
```


---

### BpmRuntimeImpl Implementation Library


The BpmRuntimeImpl Implementation Library contract is found within the bpm-runtime bundle.

#### abort(BpmRuntime.ProcessInstance storage,BpmService)


**abort(BpmRuntime.ProcessInstance storage,BpmService)**


Aborts the given ProcessInstance and all of its activities

```endpoint
CALL abort(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the process instance to abort

```


---

#### addActivity(BpmRuntime.ProcessGraph storage,bytes32)


**addActivity(BpmRuntime.ProcessGraph storage,bytes32)**


Adds an activity with the specified ID to the given process runtime graph.

```endpoint
CALL addActivity(BpmRuntime.ProcessGraph storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the activity ID to add

```


---

#### addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)


**addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)**


Adds an input arc to the given process runtime graph to connect from the provided activity to the provided transition.

```endpoint
CALL addInputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity from which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion to which to connect

```


---

#### addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)


**addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)**


Adds an output arc to the given process runtime graph to connect from the provided transition to the provided activity.

```endpoint
CALL addOutputArc(BpmRuntime.ProcessGraph storage,bytes32,bytes32)
```

#### Parameters

```solidity
_activityId // the ID of the activity to which to connect
_graph // the process runtime graph
_transitionId // the ID of the transtion from which to connect

```


---

#### addTransition(BpmRuntime.ProcessGraph storage,bytes32)


**addTransition(BpmRuntime.ProcessGraph storage,bytes32)**


Adds a transition with the specified ID to the given process runtime graph.

```endpoint
CALL addTransition(BpmRuntime.ProcessGraph storage,bytes32)
```

#### Parameters

```solidity
_graph // the process runtime graph
_id // the transition ID to add

```


---

#### configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)


**configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)**


Configures a ProcessRuntimeIntance based on the provided ProcessDefinition. Note: Placing this function in the BpmRuntimeApi library avoids import dependencies of the runtime package by the model.

```endpoint
CALL configure(BpmRuntime.ProcessGraph storage,ProcessDefinition)
```

#### Parameters

```solidity
_processDefinition // the process definition
_runtime // the runtime instance

```

#### Return

```json
an error code indicating success or failure
```


---

#### continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)


**continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)**


Checks the given ProcessInstance for completeness and open activities. If activatable activities are detected, recursive execution is entered via execute(ProcessInstance). If the ProcessInstance is complete, its state is set to COMPLETED. Otherwise the function returns BaseErrors.NO_ERROR().

```endpoint
CALL continueTransaction(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the BpmRuntime.ProcessInstance

```

#### Return

```json
BaseErrors.NO_ERROR() if no errors were encountered during processing or no processing happenedany error code from entering into a recursive execute(ProcessInstance) and continuing to execute the process
```


---

#### createActivityInstance(BpmRuntime.ProcessInstance storage,bytes32,uint256)


**createActivityInstance(BpmRuntime.ProcessInstance storage,bytes32,uint256)**


Creates a new BpmRuntime.ActivityInstance with the specified parameters and adds it to the given ProcessInstance

```endpoint
CALL createActivityInstance(BpmRuntime.ProcessInstance storage,bytes32,uint256)
```

#### Parameters

```solidity
_activityId // the ID of the activity as defined in the ProcessDefinition
_index // indicates the position of the ActivityInstance when used in a multi-instance context
_processInstance // the ProcessInstance to which the ActivityInstance is added

```

#### Return

```json
the unique global ID of the activity instance
```


---

#### execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)


**execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)**


Executes the given ActivityInstance based on the information in the provided ProcessDefinition.

```endpoint
CALL execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,BpmService)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_processDefinition // a ProcessDefinition containing information how to execute the activity
_rootDataStorage // a DataStorage that can be used to resolve process data (typically this is the ProcessInstance itself)
_service // the BpmService to use for communicating

```

#### Return

```json
BaseErrors.INVALID_PARAM_STATE() if the ActivityInstance's state is not CREATED, SUSPENDED, or INTERRUPTEDBaseErrors.INVALID_ACTOR() if the ActivityInstance is of TaskType.USER, but neither the msg.sender nor the tx.origin is the assignee of the task.BaseErrors.NO_ERROR() if successful
```


---

#### execute(BpmRuntime.ProcessGraph storage)


**execute(BpmRuntime.ProcessGraph storage)**


Executes a single iteration of the given ProcessGraph, i.e. it goes over all transitions and attempts to fire them based on the current marker state of the network graph. If after this iteration the new marker state would result in more transitions being fired, this function should be invoked again.

```endpoint
CALL execute(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the process runtime graph

```

#### Return

```json
the number of transitions that fired
```


---

#### execute(BpmRuntime.ProcessInstance storage,BpmService)


**execute(BpmRuntime.ProcessInstance storage,BpmService)**


Executes the given ProcessInstance leveraging the given BpmService reference by looking for activities that are "ready" to be executed. Execution continues along the process graph until no more activities can be executed. This function implements a single transaction of all activities in a process flow until an asynchronous point in the flow is reached or the process has ended.

```endpoint
CALL execute(BpmRuntime.ProcessInstance storage,BpmService)
```

#### Parameters

```solidity
_processInstance // the ProcessInstance to execute
_service // the BpmService managing the ProcessInstance (used to register changes to the ProcessInstance and fire events)

```

#### Return

```json
BaseErrors.INVALID_STATE() if the ProcessInstance is not ACTIVEBaseErrors.NO_ERROR() if successful
```


---

#### hasActivatableActivities(BpmRuntime.ProcessGraph storage)


**hasActivatableActivities(BpmRuntime.ProcessGraph storage)**


Determines whether the given runtime instance has any activities that are waiting to be activated.

```endpoint
CALL hasActivatableActivities(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the ProcessGraph

```

#### Return

```json
true if at least one activatable activity was found, false otherwise
```


---

#### invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)


**invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)**


Performs a call on the given application ID defined in the provided ApplicationRegistry

```endpoint
CALL invokeApplication(BpmRuntime.ActivityInstance storage,address,bytes32,address,ProcessDefinition,ApplicationRegistry)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_application // the application ID
_applicationRegistry // the registry where information about an application can be retrieved
_processDefinition // the process definition
_rootDataStorage // a DataStorage that is used as the root or default for resolving data references
_txPerformer // the account that initiated the current transaction (optional)

```

#### Return

```json
BaseErrors.RUNTIME_ERROR if there was an exception in calling the defined appliationBaseErrors.NO_ERROR() if successful
```


---

#### isCompleted(BpmRuntime.ProcessGraph storage)


**isCompleted(BpmRuntime.ProcessGraph storage)**


Executes the given ProcessGraph and reports back on completeness and open activities. The following scenarios are possible: (completed, !readyActivities): the process is done, there are no more activities to process (!completed, readyActivities): the process is still active and there are activities ready for processing (!completed, !readyActivities): the process is still active, but no activities are ready to be processed (which means there must be instances waiting for asynchronous events)

```endpoint
CALL isCompleted(BpmRuntime.ProcessGraph storage)
```

#### Parameters

```solidity
_graph // the BpmRuntime.ProcessGraph

```

#### Return

```json
completed - if true, the graph cannot be executed any furtherreadyActivities - if true there are activities ready for processing, false otherwise
```


---

#### isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)


**isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)**


Determines whether the conditions are met to fire the provided transition.

```endpoint
CALL isTransitionEnabled(BpmRuntime.ProcessGraph storage,bytes32)
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


---

#### resolveParticipant(ProcessModel,DataStorage,bytes32)


**resolveParticipant(ProcessModel,DataStorage,bytes32)**


Provides runtime resolution capabilities to determine the account address or lookup location of an account for a participant in a given ProcessModel. This function supports dealing with concrete participants as well as conditional performers. Examples: Return value (FE80A3F6CDFEF73D4FACA7DBA1DFCF215299279D, "") => The address is a concrete (user) account and can be used directly Return value (AA194B34D18F710058C0B14CFDAD4FF0150856EA, "accountant") => The address is a DataStorage contract and the (user) account to use can be located using DataStorage(AA194B34D18F710058C0B14CFDAD4FF0150856EA).getDataValueAsAddress("accountant")

```endpoint
CALL resolveParticipant(ProcessModel,DataStorage,bytes32)
```

#### Parameters

```solidity
_dataStorage // a concrete DataStorage instance supporting the lookup
_participant // the ID of a participant in the given model
_processModel // a ProcessModel

```

#### Return

```json
target - either the address of an account or the address of another DataStorage where the account can be founddataPath - empty bytes32 in case the returned target is already an identified account or a key where to retrieve the account if the target is another DataStorage
```


---

### ApplicationRegistry


The ApplicationRegistry contract is found within the bpm-runtime bundle.

#### addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)


**addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)**


Adds a Service application with the given parameters to this ProcessModel

```endpoint
CALL addApplication(bytes32,uint8,address,bytes4,bytes32,bytes32)
```

#### Parameters

```solidity
_eventName // the ID of an event to fire (only for event application)
_function // the signature of the completion function
_id // the ID of the application
_location // the location of the contract implementing the application
_type // the BpmModel.ApplicationType
_webForm // the hash of a web form (only for web applications)

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an application with the given ID already exists, BaseErrors.NO_ERROR() otherwise
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getApplicationAccessPathAtIndex(bytes32,uint256,uint8)


**getApplicationAccessPathAtIndex(bytes32,uint256,uint8)**


Returns information about the specified I/O access path of an application

```endpoint
CALL getApplicationAccessPathAtIndex(bytes32,uint256,uint8)
```

#### Parameters

```solidity
_direction // BpmModel.Direction.[IN|OUT]
_id // the ID of the application
_idx // the index of the input/output parameter

```

#### Return

```json
the ID of the input/outputthe uint8 representation of the DataTypes value
```


---

#### getApplicationAtIndex(uint256)


**getApplicationAtIndex(uint256)**


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


---

#### getApplicationData(bytes32)


**getApplicationData(bytes32)**


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
applicationType the BpmModel.ApplicationType as uint8location the applications contract addressmethod the function signature of the application's completion functionwebForm the form identifier (hash) of the web application (only for a web application)eventName the identifier for an event to emit (only for event application)inputs the number of inputsoutputs the number of outputs
```


---

#### getNumberOfApplications()


**getNumberOfApplications()**


Returns the number of applications defined in this ProcessModel

```endpoint
CALL getNumberOfApplications()
```

#### Return

```json
the number of applications
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setApplicationAccessPath(bytes32,bytes32,uint8,uint8)


**setApplicationAccessPath(bytes32,bytes32,uint8,uint8)**


Adds an input or output declaration to the application identified by the activity ID. Overwrites any previously recorded 

```endpoint
CALL setApplicationAccessPath(bytes32,bytes32,uint8,uint8)
```

#### Parameters

```solidity
_dataType // a DataTypes code
_direction // the BpmModel.Direction (IN/OUT) of the data flow
_id // the ID of the application to which to add the declaration
_pathId // the ID of the data path

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if the application does not exist, BaseErrors.NO_ERROR() otherwise
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultBpmService


The DefaultBpmService contract is found within the bpm-runtime bundle.

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createDefaultProcessInstance(address,address,bytes32)


**createDefaultProcessInstance(address,address,bytes32)**


Creates a new ProcessInstance initiated with the provided parameters. This ProcessInstance can be further customized and then submitted to the #startProcessInstance(ProcessInstance) function for execution. The ownership of the created ProcessInstance is transfered to the msg.sender, i.e. the caller of this function will be the owner of the ProcessInstance.

```endpoint
CALL createDefaultProcessInstance(address,address,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_processDefinition // the address of a ProcessDefinition
_startedBy // the address of an account that regarded as the starting user. If empty, the msg.sender is used.

```


---

#### fireActivityUpdateEvent(address,bytes32)


**fireActivityUpdateEvent(address,bytes32)**


Fires the UpdateActivities event to update sqlsol with given activity

```endpoint
CALL fireActivityUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_activityId // - the bytes32 Id of the activity
_piAddress // - the address of the process instance to which the activity belongs

```


---

#### fireProcessDataUpdateEvent(address,bytes32)


**fireProcessDataUpdateEvent(address,bytes32)**


Fires the UpdateProcessData event to update sqlsol with given information

```endpoint
CALL fireProcessDataUpdateEvent(address,bytes32)
```

#### Parameters

```solidity
_dataId // - the ID of the data entry
_piAddress // - the address of the process instance to which the activity belongs

```


---

#### getActivityInstanceAtIndex(address,uint256)


**getActivityInstanceAtIndex(address,uint256)**


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


---

#### getActivityInstanceData(address,bytes32)


**getActivityInstanceData(address,bytes32)**


Returns ActivityInstance data for given the ActivityInstance ID

```endpoint
CALL getActivityInstanceData(address,bytes32)
```

#### Parameters

```solidity
_id // the global ID of the activity instance
_processInstance // the process instance address to which the ActivityInstance belongs

```

#### Return

```json
activityId - the ID of the activity as defined by the process definitioncreated - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) state - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```


---

#### getApplicationRegistry()


**getApplicationRegistry()**


Returns a reference to the ApplicationRegistry currently used by this BpmService

```endpoint
CALL getApplicationRegistry()
```

#### Return

```json
the ApplicationRegistry
```


---

#### getBpmServiceDb()


**getBpmServiceDb()**


Returns a reference to the BpmServiceDb currently used by this BpmService

```endpoint
CALL getBpmServiceDb()
```

#### Return

```json
the BpmServiceDb
```


---

#### getNumberOfActivityInstances(address)


**getNumberOfActivityInstances(address)**


Returns the number of activity instances.

```endpoint
CALL getNumberOfActivityInstances(address)
```

#### Return

```json
the activity instance count as size
```


---

#### getNumberOfProcessData(address)


**getNumberOfProcessData(address)**


Returns the number of process data entries.

```endpoint
CALL getNumberOfProcessData(address)
```

#### Return

```json
the process data size
```


---

#### getNumberOfProcessInstances()


**getNumberOfProcessInstances()**


Returns the number of Process Instances.

```endpoint
CALL getNumberOfProcessInstances()
```

#### Return

```json
the process instance count as size
```


---

#### getProcessDataAtIndex(address,uint256)


**getProcessDataAtIndex(address,uint256)**


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


---

#### getProcessDataDetails(address,bytes32)


**getProcessDataDetails(address,bytes32)**


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


---

#### getProcessInstanceAtIndex(uint256)


**getProcessInstanceAtIndex(uint256)**


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


---

#### getProcessInstanceData(address)


**getProcessInstanceData(address)**


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
processDefinition the address of the ProcessDefinitionstate the BpmRuntime.ProcessInstanceState as uint8startedBy the address of the account who started the process
```


---

#### getProcessInstanceForActivity(bytes32)


**getProcessInstanceForActivity(bytes32)**


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


---

#### getProcessModelRepository()


**getProcessModelRepository()**


Gets the ProcessModelRepository address for this BpmService

```endpoint
CALL getProcessModelRepository()
```

#### Return

```json
the address of the repository
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setApplicationRegistry(address)


**setApplicationRegistry(address)**


Sets the ApplicationRegistry for this BpmService

```endpoint
CALL setApplicationRegistry(address)
```

#### Parameters

```solidity
_registry // - the address of the application registry

```


---

#### setProcessModelRepository(address)


**setProcessModelRepository(address)**


Sets the ProcessModelRepository for this BpmService

```endpoint
CALL setProcessModelRepository(address)
```

#### Parameters

```solidity
_repository // - the address of the model repository

```


---

#### startProcess(address,bytes32)


**startProcess(address,bytes32)**


Creates a new ProcessInstance based on the specified ProcessDefinition and starts its execution

```endpoint
CALL startProcess(address,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
any error resulting from ProcessInstance.execute() or ProcessBaseErrors.NO_ERROR(), if successfulthe address of a ProcessInstance, if successful
```


---

#### startProcessFromRepository(bytes32,bytes32,bytes32)


**startProcessFromRepository(bytes32,bytes32,bytes32)**


Creates a new ProcessInstance based on the specified IDs of a ProcessModel and ProcessDefinition and starts its execution

```endpoint
CALL startProcessFromRepository(bytes32,bytes32,bytes32)
```

#### Parameters

```solidity
_activityInstanceId // the ID of a subprocess activity instance that initiated this ProcessInstance (optional)
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processDefinitionId // the ID of the process definition

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if ProcessDefinition cannot be located in the ProcessModelRepositoryany error resulting from ProcessInstance.execute() or ProcessBaseErrors.NO_ERROR(), if successfulthe address of a ProcessInstance, if successful //TODO this function should be called startProcess(bytes32, bytes32), but our JS libs have a problem with polymorphism: AN-301
```


---

#### startProcessInstance(address)


**startProcessInstance(address)**


Initializes, registers, and executes a given ProcessInstance

```endpoint
CALL startProcessInstance(address)
```

#### Parameters

```solidity
_pi // the ProcessInstance

```

#### Return

```json
BaseErrors.NO_ERROR() if successful or an error code from initializing or executing the ProcessInstance
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultProcessInstance


The DefaultProcessInstance contract is found within the bpm-runtime bundle.

#### abort(address)


**abort(address)**


Aborts this ProcessInstance and halts any ongoing activities. After the abort the ProcessInstance cannot be resurrected.

```endpoint
CALL abort(address)
```

#### Parameters

```solidity
_service // the BpmService to emit update events for ActivityInstances

```


---

#### addProcessStateChangeListener(address)


**addProcessStateChangeListener(address)**


Adds a ProcessStateChangeListener to listeners collection

```endpoint
CALL addProcessStateChangeListener(address)
```

#### Parameters

```solidity
_listener // the ProcessStateChangeListener to add

```


---

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the activity instance
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance after the activity completes)

```

#### Return

```json
BaseErrors.NO_ERROR() if successfulBaseErrors.RESOURCE_NOT_FOUND() if the activity instance cannot be locatedBaseErrors.INVALID_STATE() if the activity is not in a state to be completed (SUSPENDED or INTERRUPTED)BaseErrors.INVALID_ACTOR() if the msg.sender or tx.origin is not the assignee of the task
```


---

#### execute(address)


**execute(address)**


Initiates execution of this ProcessInstance consisting of attempting to activate and process any activities and advance the state of the runtime graph.

```endpoint
CALL execute(address)
```

#### Parameters

```solidity
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance and access to the BpmServiceDb)

```

#### Return

```json
error code indicating success or failure
```


---

#### getActivityInstanceAtIndex(uint256)


**getActivityInstanceAtIndex(uint256)**


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


---

#### getActivityInstanceData(bytes32)


**getActivityInstanceData(bytes32)**


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
created - the creation timestampcompleted - the completion timestampperformer - the account who is performing the activity (for interactive activities only)completedBy - the account who completed the activity (for interactive activities only) activityId - the ID of the activity as defined by the process definitionstate - the uint8 representation of the BpmRuntime.ActivityInstanceState of this activity instance
```


---

#### getNumberOfActivityInstances()


**getNumberOfActivityInstances()**


Returns the number of activity instances currently contained in this ProcessInstance. Note that this number is subject to change as long as the process isntance is not completed.

```endpoint
CALL getNumberOfActivityInstances()
```

#### Return

```json
the number of activity instances
```


---

#### getNumberOfArrayEntries(bytes32,bool)


**getNumberOfArrayEntries(bytes32,bool)**


Returns the number of non-default entries in the specified array-type DataStorage field

```endpoint
CALL getNumberOfArrayEntries(bytes32,bool)
```

#### Parameters

```solidity
_fullscan // if false the function will return as soon as a default value (0 for int/uint, 0x0 for address, "" for bytes32, etc.) is encountered, if true the array will be scanned to its end
_id // the key under which to find the array-type value

```

#### Return

```json
the number of non-default entries in the array
```


---

#### getProcessDefinition()


**getProcessDefinition()**


Returns the process definition on which this instance is based.

```endpoint
CALL getProcessDefinition()
```

#### Return

```json
the address of a ProcessDefinition
```


---

#### getStartedBy()


**getStartedBy()**


Returns the account that started this process instance

```endpoint
CALL getStartedBy()
```

#### Return

```json
the address registered when creating the process instance
```


---

#### getState()


**getState()**


Returns the state of this process instance

```endpoint
CALL getState()
```

#### Return

```json
the uint8 representation of the BpmRuntime.ProcessInstanceState
```


---

#### initRuntime()


**initRuntime()**


Initiates the runtime graph that handles the state of this ProcessInstance and activates the start activity. The state of this ProcessInstance must be CREATED. If initiation is successful, the state of this ProcessInstance is set to ACTIVE.

```endpoint
CALL initRuntime()
```

#### Return

```json
BaseErrors.INVALID_STATE() if the ProcessInstance is not in state CREATED.an error code if the runtime graph could not be created, e.g. if the process definition is corrupt.BaseErrors.NO_ERROR() otherwise
```


---

#### notifyProcessStateChange()


**notifyProcessStateChange()**


Notifies listeners about a process state change

```endpoint
CALL notifyProcessStateChange()
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### Ecosystem Interface


The Ecosystem Interface contract is found within the bpm-runtime bundle.

#### addOrganization(address)


**addOrganization(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createOrganization(bytes32,bytes32,address[10])


**createOrganization(bytes32,bytes32,address[10])**


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


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


Invoked by an EventEmitter for a named event without any additional data.

```endpoint
CALL eventFired(bytes32,address)
```

#### Parameters

```solidity
_event // the event name
_source // the source of the event

```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


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


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


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


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


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


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


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


---

#### getApproverAtIndex(address,uint256)


**getApproverAtIndex(address,uint256)**


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


---

#### getApproverData(address,address)


**getApproverData(address,address)**


Function supports SQLsol, but only returns the approver address parameter.

```endpoint
CALL getApproverData(address,address)
```

#### Parameters

```solidity
_approver // the approver's address
_organization // the organization's address

```


---

#### getNumberOfApprovers(address)


**getNumberOfApprovers(address)**


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


---

#### getNumberOfOrganizations()


**getNumberOfOrganizations()**


Returns the number of registered organizations.

```endpoint
CALL getNumberOfOrganizations()
```

#### Return

```json
the number of organizations
```


---

#### getNumberOfUsers(address)


**getNumberOfUsers(address)**


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


---

#### getOrganization(bytes32)


**getOrganization(bytes32)**


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


---

#### getOrganizationAtIndex(uint256)


**getOrganizationAtIndex(uint256)**


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


---

#### getOrganizationData(address)


**getOrganizationData(address)**


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


---

#### getUserAtIndex(address,uint256)


**getUserAtIndex(address,uint256)**


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


---

#### getUserData(address,address)


**getUserData(address,address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### organizationExists(bytes32)


**organizationExists(bytes32)**


Indicates whether the specified organization exists for the given organization id

```endpoint
CALL organizationExists(bytes32)
```

#### Parameters

```solidity
_id // organization ID

```

#### Return

```json
bool exists
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

## commons-auth

### AbstractERC165


The AbstractERC165 contract is found within the commons-auth bundle.

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

### AccountsManagerDb Interface


The AccountsManagerDb Interface contract is found within the commons-auth bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### AuthorizationsManager


The AuthorizationsManager contract is found within the commons-auth bundle.

#### addRole(bytes32,address,bytes32)


**addRole(bytes32,address,bytes32)**


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


---

#### getRepository(bytes32)


**getRepository(bytes32)**


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


---

#### hasRole(address,bytes32)


**hasRole(address,bytes32)**


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


---

#### removeRole(bytes32,address,bytes32)


**removeRole(bytes32,address,bytes32)**


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


---

### AuthorizationsRepository Interface


The AuthorizationsRepository Interface contract is found within the commons-auth bundle.

#### addRole(address,bytes32)


**addRole(address,bytes32)**


This function associates the given address with the specified role in the implementing repository. The function should return an error code indicating success or failure.

```endpoint
CALL addRole(address,bytes32)
```


---

#### hasRole(address,bytes32)


**hasRole(address,bytes32)**


This function allows detection of whether the given address is associated with the specified role in the implementing repository.

```endpoint
CALL hasRole(address,bytes32)
```


---

#### removeRole(address,bytes32)


**removeRole(address,bytes32)**


This function disassociates the given address from the specified role in the implementing repository. The function should return an error code indicating success or failure.

```endpoint
CALL removeRole(address,bytes32)
```


---

### BusinessAccount Interface


The BusinessAccount Interface contract is found within the commons-auth bundle.

#### addFunds(uint256)


**addFunds(uint256)**


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
```

#### Parameters

```solidity
_funds // the amount to add

```


---

#### getBalance()


**getBalance()**


Returns the current balance

```endpoint
CALL getBalance()
```

#### Return

```json
the balance
```


---

#### getId()


**getId()**


Returns the identifier of this contract.

```endpoint
CALL getId()
```

#### Return

```json
the bytes32 ID
```


---

#### getName()


**getName()**


Returns the name of this contract.

```endpoint
CALL getName()
```

#### Return

```json
the bytes32 name
```


---

#### getOrganization()


**getOrganization()**


Returns the address of the organization this business account is associated with.

```endpoint
CALL getOrganization()
```

#### Return

```json
the organization address
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```

#### Return

```json
the owner address
```


---

#### withdrawFunds(uint256)


**withdrawFunds(uint256)**


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```

#### Parameters

```solidity
_funds // the amount to withdraw

```


---

### ChainAutorizations


The ChainAutorizations contract is found within the commons-auth bundle.

#### addRole(address,bytes32)


**addRole(address,bytes32)**


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


---

#### hasRole(address,bytes32)


**hasRole(address,bytes32)**


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


---

#### removeRole(address,bytes32)


**removeRole(address,bytes32)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### Client Registry


The Client Registry contract is found within the commons-auth bundle.

#### addClient(bytes32,bytes32,bytes32)


**addClient(bytes32,bytes32,bytes32)**


Adds an client with the specified attributes to the registry.

```endpoint
CALL addClient(bytes32,bytes32,bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_ALREADY_EXISTS
```


---

#### clear()


**clear()**


Removes all entries stored in the mapping.

```endpoint
CALL clear()
```

#### Return

```json
the number of removed entries
```


---

#### deleteClient(bytes32)


**deleteClient(bytes32)**


Deletes client from registry.

```endpoint
CALL deleteClient(bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_NOT_FOUND
```


---

#### exists(bytes32)


**exists(bytes32)**


returns true if the map contains a value at the specified key, false otherwise.

```endpoint
CALL exists(bytes32)
```


---

#### getClient(bytes32)


**getClient(bytes32)**


Gets an client from the mapping.

```endpoint
CALL getClient(bytes32)
```

#### Return

```json
client
```


---

#### keyAtIndex(uint256)


**keyAtIndex(uint256)**


returns the key at the given index or 0 if the index is out of bounds

```endpoint
CALL keyAtIndex(uint256)
```


---

#### keyAtIndexHasNext(uint256)


**keyAtIndexHasNext(uint256)**


Returns the key at the given index position and the index of the next artifact, if there is one, or 0 otherwise. This method can be used as an iterator: As long as a nextIndex > 0 is returned, there is another key.

```endpoint
CALL keyAtIndexHasNext(uint256)
```


---

#### keyIndex(bytes32)


**keyIndex(bytes32)**


returns the index of the given key or -1 if the key does not exist

```endpoint
CALL keyIndex(bytes32)
```


---

#### size()


**size()**


returns the size of the mapping, i.e. the number of currently stored entries

```endpoint
CALL size()
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### updateClient(bytes32,bytes32)


**updateClient(bytes32,bytes32)**


Updates client information.

```endpoint
CALL updateClient(bytes32,bytes32)
```

#### Return

```json
NO_ERROR or RESOURCE_NOT_FOUND
```


---

### DefaultAccountsManager


The DefaultAccountsManager contract is found within the commons-auth bundle.

#### addBusinessAccount(address)


**addBusinessAccount(address)**


Adds the specified BusinessAccount. Returns NO_ERROR, RESOURCE_NOT_FOUND if the organization does not exist, RESOURCE_ALREADY_EXISTS if the business account is already registered

```endpoint
CALL addBusinessAccount(address)
```


---

#### addFunds(address,bytes32,uint256)


**addFunds(address,bytes32,uint256)**


Adds the specified fund amount to the specified organization's business account.

```endpoint
CALL addFunds(address,bytes32,uint256)
```


---

#### addUserAccount(address)


**addUserAccount(address)**


Adds the specified UserAccount.

```endpoint
CALL addUserAccount(address)
```

#### Return

```json
NO_ERROR, RESOURCE_ALREADY_EXISTS if the user account ID is already registered
```


---

#### addUserToOrganization(address,address)


**addUserToOrganization(address,address)**


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


---

#### businessAccountExists(address,bytes32)


**businessAccountExists(address,bytes32)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createUserAccount(address,bytes32)


**createUserAccount(address,bytes32)**


Creates and adds a user account

```endpoint
CALL createUserAccount(address,bytes32)
```

#### Parameters

```solidity
_id // id (required)
_owner // owner (optional)

```

#### Return

```json
error BaseErrors.NO_ERROR() or RESOURCE_ALREADY_EXISTS if the user account ID is already registereduserAccount user account
```


---

#### getBusinessAccount(address,bytes32)


**getBusinessAccount(address,bytes32)**


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


---

#### getBusinessAccount(bytes32)


**getBusinessAccount(bytes32)**


Returns the business account address for the specified business account ID.

```endpoint
CALL getBusinessAccount(bytes32)
```


---

#### getBusinessAccountAtIndex(uint256)


**getBusinessAccountAtIndex(uint256)**


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


---

#### getBusinessAccountData(address)


**getBusinessAccountData(address)**


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


---

#### getBusinessAccountsSize()


**getBusinessAccountsSize()**


Gets business accounts size.

```endpoint
CALL getBusinessAccountsSize()
```

#### Return

```json
size size
```


---

#### getUserAccount(bytes32)


**getUserAccount(bytes32)**


Returns the user account address for the specified user account ID.

```endpoint
CALL getUserAccount(bytes32)
```


---

#### getUserAccountAtIndex(uint256)


**getUserAccountAtIndex(uint256)**


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


---

#### getUserAccountData(address)


**getUserAccountData(address)**


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


---

#### getUserAccountDataById(bytes32)


**getUserAccountDataById(bytes32)**


Gets hashed user account ID and user account address for the specified user account ID.

```endpoint
CALL getUserAccountDataById(bytes32)
```

#### Parameters

```solidity
_id // the user account ID

```

#### Return

```json
error RESOURCE_NOT_FOUND or NO_ERRORaddr user account addresshashedId hashed user account ID
```


---

#### getUserAccountsSize()


**getUserAccountsSize()**


Gets user accounts size.

```endpoint
CALL getUserAccountsSize()
```

#### Return

```json
size size
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### removeUserFromOrganization(address,address)


**removeUserFromOrganization(address,address)**


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


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

#### userAccountExists(bytes32)


**userAccountExists(bytes32)**


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


---

#### withdrawFunds(address,bytes32,uint256)


**withdrawFunds(address,bytes32,uint256)**


Subtracts the specified fund amount from the specified organization's business account.

```endpoint
CALL withdrawFunds(address,bytes32,uint256)
```


---

### DefaultBusinessAccount


The DefaultBusinessAccount contract is found within the commons-auth bundle.

#### addFunds(uint256)


**addFunds(uint256)**


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
```


---

#### getBalance()


**getBalance()**


Returns the current balance

```endpoint
CALL getBalance()
```


---

#### getId()


**getId()**


Returns this account's ID

```endpoint
CALL getId()
```


---

#### getName()


**getName()**


Returns this account's name

```endpoint
CALL getName()
```


---

#### getOrganization()


**getOrganization()**


Returns the address of the organization this accounts is associated with.

```endpoint
CALL getOrganization()
```


---

#### getOwner()


**getOwner()**


Returns this account's owner

```endpoint
CALL getOwner()
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### withdrawFunds(uint256)


**withdrawFunds(uint256)**


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```


---

### DefaultEcosystem


The DefaultEcosystem contract is found within the commons-auth bundle.

#### addOrganization(address)


**addOrganization(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### createOrganization(bytes32,bytes32,address[10])


**createOrganization(bytes32,bytes32,address[10])**


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


---

#### eventFired(bytes32,address)


**eventFired(bytes32,address)**


See EventListener.eventFired(bytes32,address)

```endpoint
CALL eventFired(bytes32,address)
```


---

#### eventFired(bytes32,address,address)


**eventFired(bytes32,address,address)**


Implementation of the EventListener interface. Can be called by an organization that is registered in this Ecosystem to trigger an UpdateOrganization event.

```endpoint
CALL eventFired(bytes32,address,address)
```

#### Parameters

```solidity
_event // the event that was fired. Currently supports custom event EVENT_UPDATE_ORGANIZATION_USER
_source // Expected to be a registered Organization

```


---

#### eventFired(bytes32,address,bytes32)


**eventFired(bytes32,address,bytes32)**


See EventListener.eventFired(bytes32,address,bytes32)

```endpoint
CALL eventFired(bytes32,address,bytes32)
```


---

#### eventFired(bytes32,address,string)


**eventFired(bytes32,address,string)**


See EventListener.eventFired(bytes32,address,string)

```endpoint
CALL eventFired(bytes32,address,string)
```


---

#### eventFired(bytes32,address,uint256)


**eventFired(bytes32,address,uint256)**


See EventListener.eventFired(bytes32,address,uint)

```endpoint
CALL eventFired(bytes32,address,uint256)
```


---

#### getApproverAtIndex(address,uint256)


**getApproverAtIndex(address,uint256)**


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


---

#### getApproverData(address,address)


**getApproverData(address,address)**


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


---

#### getNumberOfApprovers(address)


**getNumberOfApprovers(address)**


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


---

#### getNumberOfOrganizations()


**getNumberOfOrganizations()**


Returns the number of registered organizations.

```endpoint
CALL getNumberOfOrganizations()
```

#### Return

```json
the number of organizations
```


---

#### getNumberOfUsers(address)


**getNumberOfUsers(address)**


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


---

#### getOrganization(bytes32)


**getOrganization(bytes32)**


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


---

#### getOrganizationAtIndex(uint256)


**getOrganizationAtIndex(uint256)**


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


---

#### getOrganizationData(address)


**getOrganizationData(address)**


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


---

#### getUserAtIndex(address,uint256)


**getUserAtIndex(address,uint256)**


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


---

#### getUserData(address,address)


**getUserData(address,address)**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### organizationExists(bytes32)


**organizationExists(bytes32)**


Indicates whether the specified organization exists for the given organization id

```endpoint
CALL organizationExists(bytes32)
```

#### Parameters

```solidity
_id // organization ID

```

#### Return

```json
bool exists
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### transferSystemOwnership(address)


**transferSystemOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferSystemOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultOrganization


The DefaultOrganization contract is found within the commons-auth bundle.

#### addEventListener(bytes32)


**addEventListener(bytes32)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to subscribe to

```


---

#### addEventListener(bytes32,address)


**addEventListener(bytes32,address)**


Adds the msg.sender as listener for the specified event.

```endpoint
CALL addEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to subscribe to
_listener // the address of an EventListener

```


---

#### addUser(address)


**addUser(address)**


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
BaseErrors.INVALID_PARAM_STATE if the UserAccount does not have this organization as its organization.BaseErrors.NO_ERROR if successful
```


---

#### getApproverAtIndex(uint256)


**getApproverAtIndex(uint256)**


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


---

#### getId()


**getId()**


see NamedElement.getId()

```endpoint
CALL getId()
```


---

#### getName()


**getName()**


see NamedElement.getName()

```endpoint
CALL getName()
```


---

#### getNumberOfApprovers()


**getNumberOfApprovers()**


Returns the number of registered approvers.

```endpoint
CALL getNumberOfApprovers()
```

#### Return

```json
the number of approvers
```


---

#### getNumberOfUsers()


**getNumberOfUsers()**


returns the number of users associated with this organization

```endpoint
CALL getNumberOfUsers()
```

#### Return

```json
the number of users
```


---

#### getUserAtIndex(uint256)


**getUserAtIndex(uint256)**


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


---

#### isActiveUser(address)


**isActiveUser(address)**


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


---

#### removeEventListener(bytes32)


**removeEventListener(bytes32)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32)
```

#### Parameters

```solidity
_event // the event to unsubscribe from

```


---

#### removeEventListener(bytes32,address)


**removeEventListener(bytes32,address)**


Removes the msg.sender from the list of listeners for the specified event.

```endpoint
CALL removeEventListener(bytes32,address)
```

#### Parameters

```solidity
_event // the event to unsubscribe from
_listener // the address of an EventListener

```


---

#### removeUser(address)


**removeUser(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

### EcosystemDb Interface


The EcosystemDb Interface contract is found within the commons-auth bundle.

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### SecureNativeAuthorizations Interface


The SecureNativeAuthorizations Interface contract is found within the commons-auth bundle.

#### addRole(address,bytes32)


**addRole(address,bytes32)**


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


---

#### hasBase(address,uint64)


**hasBase(address,uint64)**


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


---

#### hasRole(address,bytes32)


**hasRole(address,bytes32)**


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


---

#### removeRole(address,bytes32)


**removeRole(address,bytes32)**


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


---

#### setBase(address,uint64,bool)


**setBase(address,uint64,bool)**


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


---

#### setGlobal(uint64,bool)


**setGlobal(uint64,bool)**


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


---

#### unsetBase(address,uint64)


**unsetBase(address,uint64)**


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


---

## commons-base

### Destructible


The Destructible contract is found within the commons-base bundle.

#### destroy()


**destroy()**


Transfers this contract's value to the owner and frees up storage

```endpoint
CALL destroy()
```


---

#### isDestructible()


**isDestructible()**


Function that can be actively checked to detect if the contract is a destructible contract.

```endpoint
CALL isDestructible()
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

## commons-collections

### Mappings API Library


The Mappings API Library contract is found within the commons-collections bundle.

#### addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


**addToArray(Mappings.AddressAddressArrayMap storage,address,address,bool)**


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


---

#### addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


**addToArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)**


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


---

#### addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


**addToArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)**


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


---

#### addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


**addToArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)**


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


---

#### addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


**addToArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)**


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


---

#### clear(Mappings.AddressAddressArrayMap storage)


**clear(Mappings.AddressAddressArrayMap storage)**


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


---

#### clear(Mappings.AddressAddressMap storage)


**clear(Mappings.AddressAddressMap storage)**


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


---

#### clear(Mappings.AddressBytes32ArrayMap storage)


**clear(Mappings.AddressBytes32ArrayMap storage)**


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


---

#### clear(Mappings.AddressBytes32Map storage)


**clear(Mappings.AddressBytes32Map storage)**


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


---

#### clear(Mappings.Bytes32AddressArrayMap storage)


**clear(Mappings.Bytes32AddressArrayMap storage)**


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


---

#### clear(Mappings.Bytes32AddressMap storage)


**clear(Mappings.Bytes32AddressMap storage)**


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


---

#### clear(Mappings.Bytes32Bytes32Map storage)


**clear(Mappings.Bytes32Bytes32Map storage)**


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


---

#### clear(Mappings.Bytes32UintMap storage)


**clear(Mappings.Bytes32UintMap storage)**


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


---

#### clear(Mappings.UintAddressArrayMap storage)


**clear(Mappings.UintAddressArrayMap storage)**


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


---

#### clear(Mappings.UintAddressMap storage)


**clear(Mappings.UintAddressMap storage)**


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


---

#### clear(Mappings.UintBytes32ArrayMap storage)


**clear(Mappings.UintBytes32ArrayMap storage)**


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


---

#### exists(Mappings.AddressAddressArrayMap storage,address)


**exists(Mappings.AddressAddressArrayMap storage,address)**

```endpoint
CALL exists(Mappings.AddressAddressArrayMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.AddressAddressMap storage,address)


**exists(Mappings.AddressAddressMap storage,address)**

```endpoint
CALL exists(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.AddressBytes32ArrayMap storage,address)


**exists(Mappings.AddressBytes32ArrayMap storage,address)**

```endpoint
CALL exists(Mappings.AddressBytes32ArrayMap storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.AddressBytes32Map storage,address)


**exists(Mappings.AddressBytes32Map storage,address)**

```endpoint
CALL exists(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.Bytes32AddressArrayMap storage,bytes32)


**exists(Mappings.Bytes32AddressArrayMap storage,bytes32)**

```endpoint
CALL exists(Mappings.Bytes32AddressArrayMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.Bytes32AddressMap storage,bytes32)


**exists(Mappings.Bytes32AddressMap storage,bytes32)**


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.Bytes32Bytes32Map storage,bytes32)


**exists(Mappings.Bytes32Bytes32Map storage,bytes32)**


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.Bytes32UintMap storage,bytes32)


**exists(Mappings.Bytes32UintMap storage,bytes32)**


Convenience function to return the row[_key].exists value.

```endpoint
CALL exists(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.UintAddressArrayMap storage,uint256)


**exists(Mappings.UintAddressArrayMap storage,uint256)**

```endpoint
CALL exists(Mappings.UintAddressArrayMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.UintAddressMap storage,uint256)


**exists(Mappings.UintAddressMap storage,uint256)**

```endpoint
CALL exists(Mappings.UintAddressMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### exists(Mappings.UintBytes32ArrayMap storage,uint256)


**exists(Mappings.UintBytes32ArrayMap storage,uint256)**

```endpoint
CALL exists(Mappings.UintBytes32ArrayMap storage,uint256)
```

#### Return

```json
true if the map contains valid values at the specified key, false otherwise.
```


---

#### get(Mappings.AddressAddressArrayMap storage,address)


**get(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### get(Mappings.AddressAddressMap storage,address)


**get(Mappings.AddressAddressMap storage,address)**

```endpoint
CALL get(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```


---

#### get(Mappings.AddressBytes32ArrayMap storage,address)


**get(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### get(Mappings.AddressBytes32Map storage,address)


**get(Mappings.AddressBytes32Map storage,address)**

```endpoint
CALL get(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
the value registered at the specified key, or an empty bytes32 if it doesn't exist
```


---

#### get(Mappings.Bytes32AddressArrayMap storage,bytes32)


**get(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### get(Mappings.Bytes32AddressMap storage,bytes32)


**get(Mappings.Bytes32AddressMap storage,bytes32)**

```endpoint
CALL get(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```


---

#### get(Mappings.Bytes32Bytes32Map storage,bytes32)


**get(Mappings.Bytes32Bytes32Map storage,bytes32)**

```endpoint
CALL get(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```


---

#### get(Mappings.Bytes32UintMap storage,bytes32)


**get(Mappings.Bytes32UintMap storage,bytes32)**

```endpoint
CALL get(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
the value registered at the specified key
```


---

#### get(Mappings.UintAddressArrayMap storage,uint256)


**get(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### get(Mappings.UintAddressMap storage,uint256)


**get(Mappings.UintAddressMap storage,uint256)**

```endpoint
CALL get(Mappings.UintAddressMap storage,uint256)
```

#### Return

```json
the value registered at the specified key, or 0x0 if it doesn't exist
```


---

#### get(Mappings.UintBytes32ArrayMap storage,uint256)


**get(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### insert(Mappings.AddressAddressArrayMap storage,address,address[])


**insert(Mappings.AddressAddressArrayMap storage,address,address[])**


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


---

#### insert(Mappings.AddressAddressMap storage,address,address)


**insert(Mappings.AddressAddressMap storage,address,address)**


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


---

#### insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


**insert(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])**


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


---

#### insert(Mappings.AddressBytes32Map storage,address,bytes32)


**insert(Mappings.AddressBytes32Map storage,address,bytes32)**


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


---

#### insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


**insert(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])**


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


---

#### insert(Mappings.Bytes32AddressMap storage,bytes32,address)


**insert(Mappings.Bytes32AddressMap storage,bytes32,address)**


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


---

#### insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


**insert(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)**


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


---

#### insert(Mappings.Bytes32UintMap storage,bytes32,uint256)


**insert(Mappings.Bytes32UintMap storage,bytes32,uint256)**


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


---

#### insert(Mappings.UintAddressArrayMap storage,uint256,address[])


**insert(Mappings.UintAddressArrayMap storage,uint256,address[])**


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


---

#### insert(Mappings.UintAddressMap storage,uint256,address)


**insert(Mappings.UintAddressMap storage,uint256,address)**


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


---

#### insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


**insert(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])**


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


---

#### insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])


**insertOrUpdate(Mappings.AddressAddressArrayMap storage,address,address[])**


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


---

#### insertOrUpdate(Mappings.AddressAddressMap storage,address,address)


**insertOrUpdate(Mappings.AddressAddressMap storage,address,address)**


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


---

#### insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])


**insertOrUpdate(Mappings.AddressBytes32ArrayMap storage,address,bytes32[])**


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


---

#### insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)


**insertOrUpdate(Mappings.AddressBytes32Map storage,address,bytes32)**


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


---

#### insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])


**insertOrUpdate(Mappings.Bytes32AddressArrayMap storage,bytes32,address[])**


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


---

#### insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)


**insertOrUpdate(Mappings.Bytes32AddressMap storage,bytes32,address)**


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


---

#### insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)


**insertOrUpdate(Mappings.Bytes32Bytes32Map storage,bytes32,bytes32)**


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


---

#### insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)


**insertOrUpdate(Mappings.Bytes32UintMap storage,bytes32,uint256)**


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


---

#### insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])


**insertOrUpdate(Mappings.UintAddressArrayMap storage,uint256,address[])**


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


---

#### insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)


**insertOrUpdate(Mappings.UintAddressMap storage,uint256,address)**


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


---

#### insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])


**insertOrUpdate(Mappings.UintBytes32ArrayMap storage,uint256,bytes32[])**


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


---

#### keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)


**keyAtIndex(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressAddressMap storage,uint256)


**keyAtIndex(Mappings.AddressAddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)


**keyAtIndex(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.AddressBytes32Map storage,uint256)


**keyAtIndex(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)


**keyAtIndex(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)


**keyAtIndex(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)


**keyAtIndex(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### keyAtIndex(Mappings.Bytes32UintMap storage,uint256)


**keyAtIndex(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)


**keyAtIndex(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintAddressMap storage,uint256)


**keyAtIndex(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)


**keyAtIndex(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


**keyAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


**keyAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


**keyAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### keyIndex(Mappings.AddressAddressArrayMap storage,address)


**keyIndex(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### keyIndex(Mappings.AddressAddressMap storage,address)


**keyIndex(Mappings.AddressAddressMap storage,address)**

```endpoint
CALL keyIndex(Mappings.AddressAddressMap storage,address)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```


---

#### keyIndex(Mappings.AddressBytes32ArrayMap storage,address)


**keyIndex(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### keyIndex(Mappings.AddressBytes32Map storage,address)


**keyIndex(Mappings.AddressBytes32Map storage,address)**

```endpoint
CALL keyIndex(Mappings.AddressBytes32Map storage,address)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```


---

#### keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)


**keyIndex(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### keyIndex(Mappings.Bytes32AddressMap storage,bytes32)


**keyIndex(Mappings.Bytes32AddressMap storage,bytes32)**

```endpoint
CALL keyIndex(Mappings.Bytes32AddressMap storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```


---

#### keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)


**keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)**

```endpoint
CALL keyIndex(Mappings.Bytes32Bytes32Map storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```


---

#### keyIndex(Mappings.Bytes32UintMap storage,bytes32)


**keyIndex(Mappings.Bytes32UintMap storage,bytes32)**

```endpoint
CALL keyIndex(Mappings.Bytes32UintMap storage,bytes32)
```

#### Return

```json
the index of the given key or int_constant uint(-1) if the key does not exist
```


---

#### keyIndex(Mappings.UintAddressArrayMap storage,uint256)


**keyIndex(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### keyIndex(Mappings.UintAddressMap storage,uint256)


**keyIndex(Mappings.UintAddressMap storage,uint256)**


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


---

#### keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)


**keyIndex(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### remove(Mappings.AddressAddressArrayMap storage,address)


**remove(Mappings.AddressAddressArrayMap storage,address)**


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


---

#### remove(Mappings.AddressAddressMap storage,address)


**remove(Mappings.AddressAddressMap storage,address)**


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


---

#### remove(Mappings.AddressBytes32ArrayMap storage,address)


**remove(Mappings.AddressBytes32ArrayMap storage,address)**


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


---

#### remove(Mappings.AddressBytes32Map storage,address)


**remove(Mappings.AddressBytes32Map storage,address)**


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


---

#### remove(Mappings.Bytes32AddressArrayMap storage,bytes32)


**remove(Mappings.Bytes32AddressArrayMap storage,bytes32)**


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


---

#### remove(Mappings.Bytes32AddressMap storage,bytes32)


**remove(Mappings.Bytes32AddressMap storage,bytes32)**


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


---

#### remove(Mappings.Bytes32Bytes32Map storage,bytes32)


**remove(Mappings.Bytes32Bytes32Map storage,bytes32)**


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


---

#### remove(Mappings.Bytes32UintMap storage,bytes32)


**remove(Mappings.Bytes32UintMap storage,bytes32)**


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


---

#### remove(Mappings.UintAddressArrayMap storage,uint256)


**remove(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### remove(Mappings.UintAddressMap storage,uint256)


**remove(Mappings.UintAddressMap storage,uint256)**


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


---

#### remove(Mappings.UintBytes32ArrayMap storage,uint256)


**remove(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

#### removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)


**removeFromArray(Mappings.AddressAddressArrayMap storage,address,address,bool)**


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


---

#### removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)


**removeFromArray(Mappings.AddressBytes32ArrayMap storage,address,bytes32,bool)**


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


---

#### removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)


**removeFromArray(Mappings.Bytes32AddressArrayMap storage,bytes32,address,bool)**


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


---

#### removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)


**removeFromArray(Mappings.UintAddressArrayMap storage,uint256,address,bool)**


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


---

#### removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)


**removeFromArray(Mappings.UintBytes32ArrayMap storage,uint256,bytes32,bool)**


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


---

#### valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressAddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressAddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.AddressBytes32ArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)


**valueAtIndexHasNext(Mappings.AddressBytes32Map storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32AddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32AddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32Bytes32Map storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)


**valueAtIndexHasNext(Mappings.Bytes32UintMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintAddressArrayMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintAddressMap storage,uint256)**


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


---

#### valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)


**valueAtIndexHasNext(Mappings.UintBytes32ArrayMap storage,uint256)**


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


---

### VersionLinked


The VersionLinked contract is found within the commons-collections bundle.

#### acceptVersionLink(address)


**acceptVersionLink(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getOwner()


**getOwner()**


Returns the owner

```endpoint
CALL getOwner()
```

#### Return

```json
the address of the owner
```


---

#### getPredecessor()


**getPredecessor()**


Returns the predecessor version

```endpoint
CALL getPredecessor()
```

#### Return

```json
the address of the predecessor or 0x0 if not set
```


---

#### getSuccessor()


**getSuccessor()**


Returns the successor version

```endpoint
CALL getSuccessor()
```

#### Return

```json
the address of the successor or 0x0 if not set
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### VersionLinkedAppendOnly Interface


The VersionLinkedAppendOnly Interface contract is found within the commons-collections bundle.

#### appendNewVersion(address)


**appendNewVersion(address)**


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getTargetVersion(uint8[3])


**getTargetVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLatest(address)


**setLatest(address)**


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


---

#### setPredecessor()


**setPredecessor()**


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

## commons-management

### ContractLocator Interface


The ContractLocator Interface contract is found within the commons-management bundle.

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

### ContractLocatorEnabled


The ContractLocatorEnabled contract is found within the commons-management bundle.

#### setContractLocator(address)


**setContractLocator(address)**


Allows setting the ContractLocator address, if it hadn't been set or if the msg.sender is the currently registered locator.

```endpoint
CALL setContractLocator(address)
```

#### Return

```json
true if successful, false otherwise
```


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

### DOUG - Decentralized Organization Upgrade Guy


The DOUG - Decentralized Organization Upgrade Guy contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


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


---

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### addLibrary(bytes32,address)


**addLibrary(bytes32,address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

#### getLibrary(bytes32)


**getLibrary(bytes32)**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index.

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
the registered name and address as (bytes32,address)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Interface identification is specified in ERC-165. This function  uses less than 30,000 gas.

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
interfaceID // The interface identifier, as specified in ERC-165

```

#### Return

```json
`true` if the contract implements `interfaceID` and
`interfaceID` is not 0xffffffff, `false` otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultContractLocator


The DefaultContractLocator contract is found within the commons-management bundle.

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

#### remove()


**remove()**


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```


---

#### removeContract(bytes32)


**removeContract(bytes32)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### DefaultDOUG


The DefaultDOUG contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


Overwrites HierarchyEnabled.addChild()

```endpoint
CALL addChild(address)
```

#### Return

```json
BaseErrors.INVALID_TYPE() if the address is not a LifecycleModuleBaseErrors.NO_ERROR() if sucessfull
```


---

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### addLibrary(bytes32,address)


**addLibrary(bytes32,address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

#### getLibrary(bytes32)


**getLibrary(bytes32)**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Returns the number of contracts registered in this module

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
0
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
("", 0x0)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

#### Return

```json
false
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


Default implementation of Upgradeable.migrateFrom(address).

```endpoint
CALL migrateFrom(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### migrateTo(address)


**migrateTo(address)**


Default implementation of Upgradeable.migrateTo(address).

```endpoint
CALL migrateTo(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### remove()


**remove()**


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```


---

#### removeContract(bytes32)


**removeContract(bytes32)**


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


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultLifecycleHub


The DefaultLifecycleHub contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


Overwrites HierarchyEnabled.addChild()

```endpoint
CALL addChild(address)
```

#### Return

```json
BaseErrors.INVALID_TYPE() if the address is not a LifecycleModuleBaseErrors.NO_ERROR() if sucessfull
```


---

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Returns the number of contracts registered in this module

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
0
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
("", 0x0)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

#### Return

```json
false
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


Default implementation of Upgradeable.migrateFrom(address).

```endpoint
CALL migrateFrom(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### migrateTo(address)


**migrateTo(address)**


Default implementation of Upgradeable.migrateTo(address).

```endpoint
CALL migrateTo(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### remove()


**remove()**


Clears the registry and selfdestructs this contract.

```endpoint
CALL remove()
```


---

#### removeContract(bytes32)


**removeContract(bytes32)**


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


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultLifecycleModule


The DefaultLifecycleModule contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Returns the number of contracts registered in this module

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
0
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
("", 0x0)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```

#### Return

```json
false
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


Default implementation of Upgradeable.migrateFrom(address).

```endpoint
CALL migrateFrom(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### migrateTo(address)


**migrateTo(address)**


Default implementation of Upgradeable.migrateTo(address).

```endpoint
CALL migrateTo(address)
```

#### Return

```json
BaseErrors.UNSUPPORTED_OPERATION()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Returns whether the declared interface signature is supported by this contract

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
_interfaceId // the signature of the ERC165 interface

```

#### Return

```json
true if supported, false otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### HierarchyEnabled


The HierarchyEnabled contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

### LifecycleEnabled


The LifecycleEnabled contract is found within the commons-management bundle.

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

### LifecycleHub


The LifecycleHub contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


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


---

#### addContract(bytes32,address)


**addContract(bytes32,address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getContract(bytes32)


**getContract(bytes32)**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index.

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
the registered name and address as (bytes32,address)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Interface identification is specified in ERC-165. This function  uses less than 30,000 gas.

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
interfaceID // The interface identifier, as specified in ERC-165

```

#### Return

```json
`true` if the contract implements `interfaceID` and
`interfaceID` is not 0xffffffff, `false` otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### LifecycleModule


The LifecycleModule contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


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


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getNumberOfChildren()


**getNumberOfChildren()**


returns the number of child sub-modules

```endpoint
CALL getNumberOfChildren()
```

#### Return

```json
the number of children
```


---

#### getNumberOfRegistrationContracts()


**getNumberOfRegistrationContracts()**


Is called when this module is being added to a ContractLocator, e.g. a LifecycleHub or DOUG to give the module the chance to register contracts contained in this module.

```endpoint
CALL getNumberOfRegistrationContracts()
```

#### Return

```json
the number of contracts
```


---

#### getParent()


**getParent()**


Returns the parent address

```endpoint
CALL getParent()
```

#### Return

```json
the parent or 0x0, if this is the root of the hierarchy
```


---

#### getRegistrationContract(uint256)


**getRegistrationContract(uint256)**


Returns information about the contract registered at the specified index.

```endpoint
CALL getRegistrationContract(uint256)
```

#### Return

```json
the registered name and address as (bytes32,address)
```


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


To be implemented to signal whether this contract should be destroyed after a successful upgrade.

```endpoint
CALL isDestroyOnUpgrade()
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### migrateFrom(address)


**migrateFrom(address)**


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


---

#### migrateTo(address)


**migrateTo(address)**


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


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLifecycleOwner(address)


**setLifecycleOwner(address)**


Sets the lifecycle owner to the given address

```endpoint
CALL setLifecycleOwner(address)
```

#### Parameters

```solidity
_address // the new owner

```


---

#### setParent(address)


**setParent(address)**


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


---

#### setRoot(address)


**setRoot(address)**


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


---

#### supportsInterface(bytes4)


**supportsInterface(bytes4)**


Interface identification is specified in ERC-165. This function  uses less than 30,000 gas.

```endpoint
CALL supportsInterface(bytes4)
```

#### Parameters

```solidity
interfaceID // The interface identifier, as specified in ERC-165

```

#### Return

```json
`true` if the contract implements `interfaceID` and
`interfaceID` is not 0xffffffff, `false` otherwise
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

## commons-standards

### IsoCountries Interface


The IsoCountries Interface contract is found within the commons-standards bundle.

#### appendNewVersion(address)


**appendNewVersion(address)**


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getTargetVersion(uint8[3])


**getTargetVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLatest(address)


**setLatest(address)**


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


---

#### setPredecessor()


**setPredecessor()**


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### IsoCountries100 Interface


The IsoCountries100 Interface contract is found within the commons-standards bundle.

#### appendNewVersion(address)


**appendNewVersion(address)**


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getTargetVersion(uint8[3])


**getTargetVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLatest(address)


**setLatest(address)**


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


---

#### setPredecessor()


**setPredecessor()**


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### IsoCurrencies Interface


The IsoCurrencies Interface contract is found within the commons-standards bundle.

#### appendNewVersion(address)


**appendNewVersion(address)**


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getTargetVersion(uint8[3])


**getTargetVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLatest(address)


**setLatest(address)**


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


---

#### setPredecessor()


**setPredecessor()**


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### IsoCurrencies100 Interface


The IsoCurrencies100 Interface contract is found within the commons-standards bundle.

#### appendNewVersion(address)


**appendNewVersion(address)**


Appends the given version as the latest in version linked list

```endpoint
CALL appendNewVersion(address)
```

#### Return

```json
error - failure to append due to various reasons
```


---

#### compareVersion(address)


**compareVersion(address)**


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


---

#### compareVersion(uint8[3])


**compareVersion(uint8[3])**


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


---

#### getTargetVersion(uint8[3])


**getTargetVersion(uint8[3])**


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


---

#### getVersion()


**getVersion()**


Returns the version as 3-digit array

```endpoint
CALL getVersion()
```

#### Return

```json
the version as unit8[3]
```


---

#### major()


**major()**


returns the major version number

```endpoint
CALL major()
```


---

#### minor()


**minor()**


returns the minor version number

```endpoint
CALL minor()
```


---

#### patch()


**patch()**


returns the patch version number

```endpoint
CALL patch()
```


---

#### setLatest(address)


**setLatest(address)**


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


---

#### setPredecessor()


**setPredecessor()**


Sets the predecessor to msg.sender who should also have the same owner

```endpoint
CALL setPredecessor()
```

#### Return

```json
error - if a predecessor is already set (i.e. no overwriting allowed), or if there is a owner mismatch
```


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

## commons-utils


## documents-commons

### AbstractDocument


The AbstractDocument contract is found within the documents-commons bundle.

#### addVersion(string)


**addVersion(string)**


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


---

#### getName()


**getName()**


Returns the document's name

```endpoint
CALL getName()
```


---

#### getNumberOfVersions()


**getNumberOfVersions()**


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```


---

#### getVersionCreated(string)


**getVersionCreated(string)**


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


---

#### getVersionCreator(string)


**getVersionCreator(string)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### Agreement


The Agreement contract is found within the documents-commons bundle.

#### addSignatories(address[])


**addSignatories(address[])**


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


---

#### addSignatory(address)


**addSignatory(address)**


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


---

#### addVersion(string)


**addVersion(string)**


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


---

#### confirmExecutionVersion(string)


**confirmExecutionVersion(string)**


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


---

#### getConfirmedVersion()


**getConfirmedVersion()**


Returns the confirmed version of this agreement, if it has been set.

```endpoint
CALL getConfirmedVersion()
```


---

#### getEndorsedVersion(address)


**getEndorsedVersion(address)**


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


---

#### getName()


**getName()**


Returns the document's name

```endpoint
CALL getName()
```


---

#### getNumberOfVersions()


**getNumberOfVersions()**


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```


---

#### getSignatoriesSize()


**getSignatoriesSize()**


Returns the number of signatories of this agreement.

```endpoint
CALL getSignatoriesSize()
```

#### Return

```json
the number of signatories
```


---

#### getVersionCreated(string)


**getVersionCreated(string)**


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


---

#### getVersionCreator(string)


**getVersionCreator(string)**


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


---

#### isConfirmedVersion(string)


**isConfirmedVersion(string)**


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


---

#### isEffective()


**isEffective()**


Returns whether this agreement is effective or not

```endpoint
CALL isEffective()
```


---

#### isFullyConfirmed(string)


**isFullyConfirmed(string)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### DefaultDocument


The DefaultDocument contract is found within the documents-commons bundle.

#### addVersion(string)


**addVersion(string)**


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


---

#### getName()


**getName()**


Returns the document's name

```endpoint
CALL getName()
```


---

#### getNumberOfVersions()


**getNumberOfVersions()**


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```


---

#### getVersionCreated(string)


**getVersionCreated(string)**


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


---

#### getVersionCreator(string)


**getVersionCreator(string)**


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


---

#### transferOwnership(address)


**transferOwnership(address)**


Allows the current owner to transfer control of the contract to a new owner.

```endpoint
CALL transferOwnership(address)
```

#### Parameters

```solidity
_newOwner // The address to transfer ownership to.

```


---

### Document Interface


The Document Interface contract is found within the documents-commons bundle.

#### addVersion(string)


**addVersion(string)**


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


---

#### getName()


**getName()**


Returns the document's name

```endpoint
CALL getName()
```

#### Return

```json
the name
```


---

#### getNumberOfVersions()


**getNumberOfVersions()**


Returns the number of versions of this document

```endpoint
CALL getNumberOfVersions()
```

#### Return

```json
the number of versions
```


---

#### getVersionCreated(string)


**getVersionCreated(string)**


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


---

#### getVersionCreator(string)


**getVersionCreator(string)**


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


---

