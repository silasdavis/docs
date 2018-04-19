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

### ActiveAgreement Interface


The ActiveAgreement Interface contract is found within the agreements bundle.

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

#### setName(bytes32)


**setName(bytes32)**


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


---

### ActiveAgreementRegistry Interface


The ActiveAgreementRegistry Interface contract is found within the agreements bundle.

#### create(address,bytes32,address,bytes32,bytes32,bool,address[])


**create(address,bytes32,address,bytes32,bytes32,bool,address[])**


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


---

#### setName(address,bytes32)


**setName(address,bytes32)**


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

#### addCustomField(uint8,bytes32)


**addCustomField(uint8,bytes32)**


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

#### getCustomFieldAtIndex(uint256)


**getCustomFieldAtIndex(uint256)**


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


---

#### getCustomFieldDataType(bytes32)


**getCustomFieldDataType(bytes32)**


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

#### getNumberOfCustomFields()


**getNumberOfCustomFields()**


Gets number of custom fields

```endpoint
CALL getNumberOfCustomFields()
```

#### Return

```json
size number of custom fields
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

#### addField(address,uint8,bytes32)


**addField(address,uint8,bytes32)**


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


---

#### addFields(address,uint8[],bytes32[])


**addFields(address,uint8[],bytes32[])**


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

#### create(bytes32,address,string,bool,address,address)


**create(bytes32,address,string,bool,address,address)**


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

#### getFieldByArchetypeAtIndex(address,uint256)


**getFieldByArchetypeAtIndex(address,uint256)**


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


---

#### getFieldByArchetypeData(address,bytes32)


**getFieldByArchetypeData(address,bytes32)**


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


---

#### getFieldsByArchetypeSize(address)


**getFieldsByArchetypeSize(address)**


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


Overriden method to get Address Array value from Data Storage

```endpoint
CALL getDataValueAsAddressArray(bytes32)
```

#### Parameters

```solidity
_id // the bytes32 id of the address array

```

#### Return

```json
the address array
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

#### setName(bytes32)


**setName(bytes32)**


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


---

### DefaultActiveAgreementRegistry Interface


The DefaultActiveAgreementRegistry Interface contract is found within the agreements bundle.

#### create(address,bytes32,address,bytes32,bytes32,bool,address[])


**create(address,bytes32,address,bytes32,bytes32,bool,address[])**


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


---

#### setName(address,bytes32)


**setName(address,bytes32)**


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

#### addCustomField(uint8,bytes32)


**addCustomField(uint8,bytes32)**


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

#### getCustomFieldAtIndex(uint256)


**getCustomFieldAtIndex(uint256)**


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


---

#### getCustomFieldDataType(bytes32)


**getCustomFieldDataType(bytes32)**


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

#### getNumberOfCustomFields()


**getNumberOfCustomFields()**


Gets number of custom fields

```endpoint
CALL getNumberOfCustomFields()
```

#### Return

```json
size number of custom fields
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

#### addField(address,uint8,bytes32)


**addField(address,uint8,bytes32)**


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


---

#### addFields(address,uint8[],bytes32[])


**addFields(address,uint8[],bytes32[])**


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

#### create(bytes32,address,string,bool,address,address)


**create(bytes32,address,string,bool,address,address)**


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

#### getFieldByArchetypeAtIndex(address,uint256)


**getFieldByArchetypeAtIndex(address,uint256)**


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


---

#### getFieldByArchetypeData(address,bytes32)


**getFieldByArchetypeData(address,bytes32)**


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


---

#### getFieldsByArchetypeSize(address)


**getFieldsByArchetypeSize(address)**


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

## bpm-model

### AbstractEventListener


The AbstractEventListener contract is found within the bpm-model bundle.

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

### AbstractNamedElement


The AbstractNamedElement contract is found within the bpm-model bundle.

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



### Identifiable Interface


The Identifiable Interface contract is found within the bpm-model bundle.

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

### DefaultEventEmitter


The DefaultEventEmitter contract is found within the bpm-model bundle.

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

#### createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)


**createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)**


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_application // the application handling the execution of the activity
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
BaseErrors.RESOURCE_ALREADY_EXISTS() if an activity with the same ID already existsBaseErrors.INVALID_PARAM_VALUE() if an assignee is specified, but the BpmModel.TaskType is not USERBaseErrors.NULL_PARAM_NOT_ALLOWED() if BpmModel.TaskType is USER, but no assignee was specifiedBaseErrors.RESOURCE_NOT_FOUND() if an application or an assignee is specified that does not exist in the modelBaseErrors.NO_ERROR() upon successful creation.
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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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

#### removeProcessInterfaceImplementation(address,bytes32)


**removeProcessInterfaceImplementation(address,bytes32)**


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

#### addServiceApplication(bytes32,address,bytes4)


**addServiceApplication(bytes32,address,bytes4)**


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


---

#### addWebApplication(bytes32,bytes32)


**addWebApplication(bytes32,bytes32)**


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

#### fireProcessDefinitionUpdateEvent()


**fireProcessDefinitionUpdateEvent()**


To be called by a registered process definition to signal an update. Causes the ProcessModel to emit an update event on behalf of the msg.sender

```endpoint
CALL fireProcessDefinitionUpdateEvent()
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
applicationType the BpmModel.ApplicationType as uint8location the applications contract address, only available for a service applicationmethod the function signature of the application, only available for a service applicationwebForm the form identifier (formHash) of the web application, only available for a web application
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

#### hasApplication(bytes32)


**hasApplication(bytes32)**


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

#### createProcessModel(bytes32,bytes32,uint8[3])


**createProcessModel(bytes32,bytes32,uint8[3])**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch version
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

### EventEmitter Interface


The EventEmitter Interface contract is found within the bpm-model bundle.

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


The EventListener contract is found within the bpm-model bundle.

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

### NamedElement Interface


The NamedElement Interface contract is found within the bpm-model bundle.

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


### ProcessDefinition Interface


The ProcessDefinition Interface contract is found within the bpm-model bundle.

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

#### createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)


**createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)**


Creates a new activity definition with the specified parameters.

```endpoint
CALL createActivityDefinition(bytes32,uint8,uint8,bytes32,bool,bytes32)
```

#### Parameters

```solidity
_activityType // the BpmModel.ActivityType
_application // the application handling the execution of the activity
_assignee // the ID of the participant performing the activity (for USER tasks only)
_id // the activity ID
_multiInstance // whether the activity represents multiple instances
_taskType // the BpmModel.TaskType

```

#### Return

```json
an error code indicating success or failure
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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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

#### removeProcessInterfaceImplementation(address,bytes32)


**removeProcessInterfaceImplementation(address,bytes32)**


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

### ProcessModel Interface


The ProcessModel Interface contract is found within the bpm-model bundle.

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

#### addServiceApplication(bytes32,address,bytes4)


**addServiceApplication(bytes32,address,bytes4)**


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


---

#### addWebApplication(bytes32,bytes32)


**addWebApplication(bytes32,bytes32)**


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

#### fireProcessDefinitionUpdateEvent()


**fireProcessDefinitionUpdateEvent()**


To be called by a registered process definition to signal an update.

```endpoint
CALL fireProcessDefinitionUpdateEvent()
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
applicationType the BpmModel.ApplicationType as uint8location the applications contract address, only available for a service applicationmethod the function signature of the application, only available for a service applicationwebForm the form identifier (formHash) of the web application, only available for a web application
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

#### hasApplication(bytes32)


**hasApplication(bytes32)**


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


The ProcessModelRepository Interface contract is found within the bpm-model bundle.

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

#### createProcessModel(bytes32,bytes32,uint8[3])


**createProcessModel(bytes32,bytes32,uint8[3])**


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
activityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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
id - the model IDname - the model nameversionMajor - the model's major versionversionMinor - the model's minor versionversionPatch - the model's patch version
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

### Versioned


The Versioned contract is found within the bpm-model bundle.

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

## bpm-runtime


### BpmApi Interface Library


The BpmApi Interface Library contract is found within the bpm-runtime bundle.

#### activateAndComplete(BpmRuntime.ActivityInstance storage,ProcessDefinition)


**activateAndComplete(BpmRuntime.ActivityInstance storage,ProcessDefinition)**


Activates the given ActivityInstance from a suspended state (SUSPENDED or INTERRUPTED) and invokes its application.

```endpoint
CALL activateAndComplete(BpmRuntime.ActivityInstance storage,ProcessDefinition)
```

#### Parameters

```solidity
_activityInstance // the activity instance
_processDefinition // a ProcessDefinition containing information about the activity

```

#### Return

```json
error code indicating success or failure
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

#### execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,uint256)


**execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,uint256)**


Executes the given ActivityInstance based on the information in the provided ProcessDefinition.

```endpoint
CALL execute(BpmRuntime.ActivityInstance storage,DataStorage,ProcessDefinition,uint256)
```

#### Parameters

```solidity
_activityInstance // the ActivityInstance
_instanceCounter // indicates the index position for multi-instance activities to support accessing array-based data mappings
_processDefinition // a ProcessDefinition containing information how to execute the activity
_rootDataStorage // a DataStorage that can be used to resolve process data (typically this is the ProcessInstance itself)

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

### BpmRuntimeDb


The BpmRuntimeDb contract is found within the bpm-runtime bundle.

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


Adds the given address to the registered process instances. Can only be invoked by the owner of this BpmRuntimeDb.

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

### BpmService Interface


The BpmService Interface contract is found within the bpm-runtime bundle.

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

#### getActivityDefinitionDetails(address,bytes32)


**getActivityDefinitionDetails(address,bytes32)**


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
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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
(processId)
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

#### getRuntimeDb()


**getRuntimeDb()**


Returns a reference to the BpmRuntimeDb currently used by this BpmService

```endpoint
CALL getRuntimeDb()
```

#### Return

```json
the BpmRuntimeDb
```


---

#### getUserTaskDetails(address,bytes32)


**getUserTaskDetails(address,bytes32)**


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
assignee the ID of the activity's assignee (for interactive activities)processId ID of the process definitionprocessName Name of the process definitionapplication the activity's application
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
_repository // - the address of the repository

```


---

#### startProcess(address)


**startProcess(address)**


Creates a new ProcessInstance based on the specified ProcessDefinition and starts its execution

```endpoint
CALL startProcess(address)
```

#### Parameters

```solidity
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

#### startProcessFromRepository(bytes32,bytes32)


**startProcessFromRepository(bytes32,bytes32)**


Creates a new ProcessInstance based on the specified IDs of a ProcessModel and ProcessDefinition and starts its execution

```endpoint
CALL startProcessFromRepository(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processDefinitionId // the ID of the process definition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

#### startProcessWithData(address,bytes32,address)


**startProcessWithData(address,bytes32,address)**


Creates a new ProcessInstance based on the specified ProcessDefinition, populates the key/value address-type field and starts its execution

```endpoint
CALL startProcessWithData(address,bytes32,address)
```

#### Parameters

```solidity
_addressKey // the key under which the value should be stored in the ProcessInstance
_addressValue // an address value
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

### BusinessAccount Interface


The BusinessAccount Interface contract is found within the bpm-runtime bundle.

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

### DefaultBpmService


The DefaultBpmService contract is found within the bpm-runtime bundle.

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

#### getActivityDefinitionDetails(address,bytes32)


**getActivityDefinitionDetails(address,bytes32)**


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
id the bytes32 id of the activity definitionactivityType the BpmModel.ActivityType as uint8taskType the BpmModel.TaskType as uint8assignee the ID of the activity's assignee (for interactive activities)multiInstance whether the activity is a multi-instanceapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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
(processId)
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

#### getRuntimeDb()


**getRuntimeDb()**


Returns a reference to the BpmRuntimeDb currently used by this BpmService

```endpoint
CALL getRuntimeDb()
```

#### Return

```json
the BpmRuntimeDb
```


---

#### getUserTaskDetails(address,bytes32)


**getUserTaskDetails(address,bytes32)**


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
assignee the ID of the activity's assignee (for interactive activities)processId ID of the process definitionprocessName Name of the process definitionapplication the activity's applicationinputGateway the activity's input BpmModel.Gatewaytype as uint8outputGateway the activity's output BpmModel.Gatewaytype as uint8
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
_repository // - the address of the repository

```


---

#### startProcess(address)


**startProcess(address)**


Creates a new ProcessInstance based on the specified ProcessDefinition and starts its execution

```endpoint
CALL startProcess(address)
```

#### Parameters

```solidity
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
any error resulting from ProcessInstance.execute() or ProcessBaseErrors.NO_ERROR(), if successfulthe address of a ProcessInstance, if successful
```


---

#### startProcessFromRepository(bytes32,bytes32)


**startProcessFromRepository(bytes32,bytes32)**


Creates a new ProcessInstance based on the specified IDs of a ProcessModel and ProcessDefinition and starts its execution

```endpoint
CALL startProcessFromRepository(bytes32,bytes32)
```

#### Parameters

```solidity
_modelId // the model that qualifies the process ID, if multiple models are deployed, otherwise optional
_processDefinitionId // the ID of the process definition

```

#### Return

```json
BaseErrors.RESOURCE_NOT_FOUND() if ProcessDefinition cannot be located in the ProcessModelRepositoryany error resulting from ProcessInstance.execute() or ProcessBaseErrors.NO_ERROR(), if successfulthe address of a ProcessInstance, if successful //TODO this function should be called startProcess(bytes32, bytes32), but our JS libs have a problem with polymorphism: AN-301
```


---

#### startProcessWithData(address,bytes32,address)


**startProcessWithData(address,bytes32,address)**


Creates a new ProcessInstance based on the specified ProcessDefinition, populates the key/value address-type field and starts its execution

```endpoint
CALL startProcessWithData(address,bytes32,address)
```

#### Parameters

```solidity
_addressKey // the key under which the value should be stored in the ProcessInstance
_addressValue // an address value
_processDefinition // the address of a ProcessDefinition

```

#### Return

```json
error code indicating success or failureinstance the address of a ProcessInstance, if successful
```


---

### DefaultBusinessAccount


The DefaultBusinessAccount contract is found within the bpm-runtime bundle.

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

#### withdrawFunds(uint256)


**withdrawFunds(uint256)**


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```


---

### DefaultProcessInstance


The DefaultProcessInstance contract is found within the bpm-runtime bundle.

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
BaseErrors.NO_ERROR() if successfulBaseErrors.RESOURCE_NOT_FOUND() if the activity instance cannot be locatedBaseErrors.INVALID_STATE() if the activity is not in a state to be completedBaseErrors.INVALID_ACTOR() if the msg.sender or tx.origin is not the assignee of the task
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
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance and access to the BpmRuntimeDb)

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


### ProcessInstance Interface


The ProcessInstance Interface contract is found within the bpm-runtime bundle.

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
_service // the BpmService managing this ProcessInstance (required for changes to this ProcessInstance and access to the BpmRuntimeDb)

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

### SystemOwned


The SystemOwned contract is found within the bpm-runtime bundle.

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

### WorkflowBusinessAccount


The WorkflowBusinessAccount contract is found within the bpm-runtime bundle.

#### addFunds(uint256)


**addFunds(uint256)**


Increases the balance by specified amount

```endpoint
CALL addFunds(uint256)
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
_service // the BpmService required for lookup and access to the BpmRuntimeDb

```

#### Return

```json
error code if the completion failed
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

#### withdrawFunds(uint256)


**withdrawFunds(uint256)**


Decreases the balance by the specified amount

```endpoint
CALL withdrawFunds(uint256)
```


---

### WorkflowProxy


The WorkflowProxy contract is found within the bpm-runtime bundle.

#### completeActivity(bytes32,address)


**completeActivity(bytes32,address)**


Completes the specified activity using the given BpmService to locate the relevant ProcessInstance. This sets the msg.sender of the call to the address of this proxy contract, so that it can be used to authorize the task completion.

```endpoint
CALL completeActivity(bytes32,address)
```

#### Parameters

```solidity
_activityInstanceId // the task ID
_service // the BpmService required for lookup and access to the BpmRuntimeDb

```

#### Return

```json
error code if the completion failed
```


---

## commons-auth

### AccountsManager Interface


The AccountsManager Interface contract is found within the commons-auth bundle.

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

#### createUserAccount(address,bytes32,bytes32)


**createUserAccount(address,bytes32,bytes32)**


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
NO_ERROR, RESOURCE_NOT_FOUND if the organization does not exist, RESOURCE_ALREADY_EXISTS if the user account is already registered
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

#### createUserAccount(address,bytes32,bytes32)


**createUserAccount(address,bytes32,bytes32)**


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
BaseErrors.NO_ERROR or BaseErrors.INVALID_PARAM_STATE if the UserAccount does not have this organization as its organization.
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

### DefaultUserAccount


The DefaultUserAccount contract is found within the commons-auth bundle.

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

#### secretIsValid(bytes32)


**secretIsValid(bytes32)**


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

### Ecosystem Interface


The Ecosystem Interface contract is found within the commons-auth bundle.

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

### Organization Interface


The Organization Interface contract is found within the commons-auth bundle.

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

### UserAccount Interface


The UserAccount Interface contract is found within the commons-auth bundle.

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

#### secretIsValid(bytes32)


**secretIsValid(bytes32)**


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

## commons-management

### Castable


The Castable contract is found within the commons-management bundle.

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. 

```


---

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```


---

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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


---

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

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```


---

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```


---

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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


---

#### setContractLocator(address)


**setContractLocator(address)**


Allows setting the ContractLocator address, if it hadn't been set or if the msg.sender is the currently registered locator.

```endpoint
CALL setContractLocator(address)
```

#### Return

```json
true if successful
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

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### DefaultCastable


The DefaultCastable contract is found within the commons-management bundle.

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```


---

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
```


---

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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

### DefaultDOUG


The DefaultDOUG contract is found within the commons-management bundle.

#### addChild(address)


**addChild(address)**


Overwrites HierarchyEnabled.addChild()

```endpoint
CALL addChild(address)
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

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

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

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
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

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

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


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```


---

#### migrateTo(address)


**migrateTo(address)**


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

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

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

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

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
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

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

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


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```


---

#### migrateTo(address)


**migrateTo(address)**


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

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

#### declareCastableTo(bytes32)


**declareCastableTo(bytes32)**


Adds the specified type to the supported types of this Castable.

```endpoint
CALL declareCastableTo(bytes32)
```

#### Parameters

```solidity
_type // a bytes32 specifying the cast support. Empty bytes32 and keccak256("") are ignored!

```


---

#### getNumberOfCastTypes()


**getNumberOfCastTypes()**


Returns the number of supported cast types.

```endpoint
CALL getNumberOfCastTypes()
```

#### Return

```json
the number of supported types.
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

#### isCastableTo(bytes32)


**isCastableTo(bytes32)**


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


---

#### isDestroyOnUpgrade()


**isDestroyOnUpgrade()**


default implementation returns false. Overwrite to return true, if the module should be destroyed after an upgrade.

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


default implementation of Upgradeable.migrateFrom(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateFrom(address)
```

#### Parameters

```solidity
_predecessor // the predecessor contract from which to migrate

```


---

#### migrateTo(address)


**migrateTo(address)**


default implementation of Upgradeable.migrateTo(address). Returns BaseErrors.UNSUPPORTED_OPERATION()

```endpoint
CALL migrateTo(address)
```

#### Parameters

```solidity
_successor // the successor contract to which to migrate

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

#### upgrade(address)


**upgrade(address)**


Checks the version and invokes migrateTo and migrateTo in order to transfer state (push then pull)

```endpoint
CALL upgrade(address)
```


---

### Migratable Interface


The Migratable Interface contract is found within the commons-management bundle.

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

### Upgradeable


The Upgradeable contract is found within the commons-management bundle.

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

### VersionLinked


The VersionLinked contract is found within the commons-management bundle.

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

### VersionLinkedAppendOnly Interface


The VersionLinkedAppendOnly Interface contract is found within the commons-management bundle.

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

## commons-utils


