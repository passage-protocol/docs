# LoyaltyLedger



> Passage Loyalty Ledger

Loyalty Ledger ERC-1155 Token



## Methods

### DEFAULT_ADMIN_ROLE

```solidity
function DEFAULT_ADMIN_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### MANAGER_ROLE

```solidity
function MANAGER_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### MINTER_ROLE

```solidity
function MINTER_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### UPGRADER_ROLE

```solidity
function UPGRADER_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### balanceOf

```solidity
function balanceOf(address account, uint256 id) external view returns (uint256)
```



*See {IERC1155-balanceOf}. Requirements: - `account` cannot be the zero address.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| id | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### balanceOfBatch

```solidity
function balanceOfBatch(address[] accounts, uint256[] ids) external view returns (uint256[])
```



*See {IERC1155-balanceOfBatch}. Requirements: - `accounts` and `ids` must have the same length.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| accounts | address[] | undefined |
| ids | uint256[] | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256[] | undefined |

### burn

```solidity
function burn(address account, uint256 id, uint256 value) external nonpayable
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| id | uint256 | undefined |
| value | uint256 | undefined |

### burnBatch

```solidity
function burnBatch(address account, uint256[] ids, uint256[] values) external nonpayable
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| ids | uint256[] | undefined |
| values | uint256[] | undefined |

### claim

```solidity
function claim(uint256 _id, uint256 _amount) external payable
```

Mint token to caller

*Token must exist. Need to enable claim &amp; set fee/amount (if desired)*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | Token ID to mint |
| _amount | uint256 | Number of tokens to mint |

### claimWhitelist

```solidity
function claimWhitelist(uint256 _id, bytes32[] _proof, uint256 _maxAmount, uint256 _claimAmount) external payable
```

Mint token to caller if they are on the supplied whitelist

*Must first set whitelist root, enable claim, &amp; set fee (if desired). Merkle tree can be generated with the Javascript library &quot;merkletreejs&quot;, the hashing algorithm should be keccak256 and pair sorting should be enabled*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | Token ID to mint |
| _proof | bytes32[] | Proof for merkle tree |
| _maxAmount | uint256 | Maximum number of tokens a user can mint, must be the same as merkle tree leaf |
| _claimAmount | uint256 | Number of tokens to mint, must be less than or equal to max amount |

### createToken

```solidity
function createToken(string _name, uint256 _maxSupply, bool _transferEnabled, uint256 _claimFee, uint256 _claimAmount, uint256 _whitelistClaimFee) external nonpayable returns (uint256)
```

Creates a new token



#### Parameters

| Name | Type | Description |
|---|---|---|
| _name | string | The token name |
| _maxSupply | uint256 | Max supply of tokens |
| _transferEnabled | bool | If transfer enabled |
| _claimFee | uint256 | The claim fee in wei |
| _claimAmount | uint256 | undefined |
| _whitelistClaimFee | uint256 | The whitelist claim fee in wei |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | ID of created token |

### eject

```solidity
function eject() external nonpayable
```

Allows admin to eject from Passage management &amp; upgrade contract independently of the registry

*This is a one-way operation, there is no way to become managed again*


### exists

```solidity
function exists(uint256 _id) external view returns (bool)
```

Returns if a given token has been created



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | Token ID to check |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | if token exists |

### getRoleAdmin

```solidity
function getRoleAdmin(bytes32 role) external view returns (bytes32)
```



*Returns the admin role that controls `role`. See {grantRole} and {revokeRole}. To change a role&#39;s admin, use {_setRoleAdmin}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### grantRole

```solidity
function grantRole(bytes32 role, address account) external nonpayable
```



*Grants `role` to `account`. If `account` had not been already granted `role`, emits a {RoleGranted} event. Requirements: - the caller must have ``role``&#39;s admin role.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

### hasRole

```solidity
function hasRole(bytes32 role, address account) external view returns (bool)
```



*Returns `true` if `account` has been granted `role`.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### hasUpgraderRole

```solidity
function hasUpgraderRole(address _address) external view returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _address | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### initialize

```solidity
function initialize(address _creator) external nonpayable
```

Initializer function for contract creation instead of constructor to support upgrades

*Only intended to be called from the registry*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _creator | address | The address of the original creator |

### isApprovedForAll

```solidity
function isApprovedForAll(address account, address operator) external view returns (bool)
```



*See {IERC1155-isApprovedForAll}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| operator | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### isManaged

```solidity
function isManaged() external view returns (bool)
```

Returns if Loyalty Ledger is still managed in registry




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | if Loyalty Ledger is still managed in registry |

### isTrustedForwarder

```solidity
function isTrustedForwarder(address forwarder) external view returns (bool)
```

return if the forwarder is trusted to forward relayed transactions to us. the forwarder is required to verify the sender&#39;s signature, and verify the call is not a replay.



#### Parameters

| Name | Type | Description |
|---|---|---|
| forwarder | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### lockMaxSupply

```solidity
function lockMaxSupply(uint256 _id) external nonpayable
```

Locks the maxSupply for a token which prevents any future maxSupply updatesthis is a one way operation and cannot be undonethe current version must be locked



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | id of the token to update |

### lockTransferEnabled

```solidity
function lockTransferEnabled(uint256 _id) external nonpayable
```

Locks the transferEnabled for a token which prevents any future transferEnabled updatesthis is a one way operation and cannot be undonethe current version must be locked



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | id of the token to update |

### lockVersion

```solidity
function lockVersion() external nonpayable
```

Locks the version of the contract preventing any future upgradesthis is a one way operation and cannot be undone




### loyaltyLedgerVersion

```solidity
function loyaltyLedgerVersion() external pure returns (uint256)
```

Returns Loyalty Ledger implementation version




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | version number |

### mint

```solidity
function mint(address _to, uint256 _id, uint256 _amount) external nonpayable
```

Allows MINTER role to mint any number of a token to a given address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _to | address | Address to mint token to |
| _id | uint256 | Token ID to mint |
| _amount | uint256 | Number of tokens to mint |

### mintBatch

```solidity
function mintBatch(address _to, uint256[] _ids, uint256[] _amounts) external nonpayable
```

Allows MINTER role to mint tokens to a given address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _to | address | Address to mint token to |
| _ids | uint256[] | List of token IDs |
| _amounts | uint256[] | List of token amounts |

### mintBulk

```solidity
function mintBulk(address[] _addresses, uint256[] _ids, uint256[] _amounts) external nonpayable
```

Allows MINTER role to mint tokens to addresses

*All input lists should be the same length*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _addresses | address[] | List of address to mint token to |
| _ids | uint256[] | List of token IDs |
| _amounts | uint256[] | List of token amounts |

### owner

```solidity
function owner() external view returns (address)
```

returns the address of the current _convenienceOwner

*not used for access control, used by services that require a single owner account*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | _convenienceOwner address |

### passageRegistry

```solidity
function passageRegistry() external view returns (contract IPassageRegistry)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract IPassageRegistry | undefined |

### proxiableUUID

```solidity
function proxiableUUID() external view returns (bytes32)
```



*Implementation of the ERC1822 {proxiableUUID} function. This returns the storage slot used by the implementation. It is used to validate that the this implementation remains valid after an upgrade. IMPORTANT: A proxy pointing at a proxiable contract should not be considered proxiable itself, because this risks bricking a proxy that upgrades to it, by delegating to itself until out of gas. Thus it is critical that this function revert if invoked through a proxy. This is guaranteed by the `notDelegated` modifier.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### renounceRole

```solidity
function renounceRole(bytes32 role, address account) external nonpayable
```



*Revokes `role` from the calling account. Roles are often managed via {grantRole} and {revokeRole}: this function&#39;s purpose is to provide a mechanism for accounts to lose their privileges if they are compromised (such as when a trusted device is misplaced). If the calling account had been revoked `role`, emits a {RoleRevoked} event. Requirements: - the caller must be `account`.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

### revokeRole

```solidity
function revokeRole(bytes32 role, address account) external nonpayable
```



*Revokes `role` from `account`. If `account` had been granted `role`, emits a {RoleRevoked} event. Requirements: - the caller must have ``role``&#39;s admin role.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

### safeBatchTransferFrom

```solidity
function safeBatchTransferFrom(address from, address to, uint256[] ids, uint256[] amounts, bytes data) external nonpayable
```



*See {IERC1155-safeBatchTransferFrom}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| from | address | undefined |
| to | address | undefined |
| ids | uint256[] | undefined |
| amounts | uint256[] | undefined |
| data | bytes | undefined |

### safeTransferFrom

```solidity
function safeTransferFrom(address from, address to, uint256 id, uint256 amount, bytes data) external nonpayable
```



*See {IERC1155-safeTransferFrom}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| from | address | undefined |
| to | address | undefined |
| id | uint256 | undefined |
| amount | uint256 | undefined |
| data | bytes | undefined |

### setApprovalForAll

```solidity
function setApprovalForAll(address operator, bool approved) external nonpayable
```



*See {IERC1155-setApprovalForAll}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| operator | address | undefined |
| approved | bool | undefined |

### setOwnership

```solidity
function setOwnership(address newOwner) external nonpayable
```

Allows default admin to set the owner address

*not used for access control, used by services that require a single owner account*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newOwner | address | address of the new owner |

### setTokenClaimEnabled

```solidity
function setTokenClaimEnabled(uint256 _id, bool _enabled) external nonpayable
```

Allows manager to set if claim is enabled



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _enabled | bool | If claim is enabled |

### setTokenClaimOptions

```solidity
function setTokenClaimOptions(uint256 _id, uint256 _claimFee, uint256 _claimAmount) external nonpayable
```

Allows manager to set the minting claim fee &amp; amount



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _claimFee | uint256 | The claim fee in wei |
| _claimAmount | uint256 | Max number of tokens someone can claim per tx |

### setTokenMaxSupply

```solidity
function setTokenMaxSupply(uint256 _id, uint256 _maxSupply) external nonpayable
```

Allows manager to set max supply of a token



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _maxSupply | uint256 | New max supply for token |

### setTokenTransferEnabled

```solidity
function setTokenTransferEnabled(uint256 _id, bool _enabled) external nonpayable
```

Allows manager to set the ability for token to be transferred



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _enabled | bool | If transfer is enabled |

### setTokenWhitelistClaimEnabled

```solidity
function setTokenWhitelistClaimEnabled(uint256 _id, bool _enabled) external nonpayable
```

Allows manager to set if the whitelist claim is enabled



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _enabled | bool | If the whitelist claim is enabled |

### setTokenWhitelistClaimFee

```solidity
function setTokenWhitelistClaimFee(uint256 _id, uint256 _claimFee) external nonpayable
```

Allows manager to set the fee for the whitelist claim



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _claimFee | uint256 | Fee in wei |

### setTrustedForwarder

```solidity
function setTrustedForwarder(address forwarder) external nonpayable
```

Allows manager to set trusted forwarder for meta-transactions



#### Parameters

| Name | Type | Description |
|---|---|---|
| forwarder | address | Address of trusted forwarder |

### setURI

```solidity
function setURI(string newUri) external nonpayable
```

Allows manager to set the ability to set a new URI rather than use the Loyalty Ledger Global URI



#### Parameters

| Name | Type | Description |
|---|---|---|
| newUri | string | Token base URI |

### setWhitelistOptions

```solidity
function setWhitelistOptions(uint256 _id, uint256 _claimFee, bytes32 _whitelistRoot) external nonpayable
```

Allows manager to set the whitelist claim fee &amp; merkle root for a given token

*Merkle tree can be generated with the Javascript library &quot;merkletreejs&quot;, the hashing algorithm should be keccak256 and pair sorting should be enabled*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _claimFee | uint256 | Fee in wei |
| _whitelistRoot | bytes32 | Merkle tree root |

### setWhitelistRoot

```solidity
function setWhitelistRoot(uint256 _id, bytes32 _whitelistRoot) external nonpayable
```

Allows manager to set the merkle tree root for the whitelist for a given token

*Merkle tree can be generated with the Javascript library &quot;merkletreejs&quot;, the hashing algorithm should be keccak256 and pair sorting should be enabled*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | ID of token to update |
| _whitelistRoot | bytes32 | Merkle tree root |

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) external view returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| interfaceId | bytes4 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### tokens

```solidity
function tokens(uint256) external view returns (string name, bool transferEnabled, bool claimEnabled, bool whitelistClaimEnabled, bool maxSupplyLocked, bool transferEnabledLocked, uint256 maxSupply, uint256 claimFee, uint256 claimAmount, uint256 whitelistClaimFee, bytes32 whitelistRoot)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| name | string | undefined |
| transferEnabled | bool | undefined |
| claimEnabled | bool | undefined |
| whitelistClaimEnabled | bool | undefined |
| maxSupplyLocked | bool | undefined |
| transferEnabledLocked | bool | undefined |
| maxSupply | uint256 | undefined |
| claimFee | uint256 | undefined |
| claimAmount | uint256 | undefined |
| whitelistClaimFee | uint256 | undefined |
| whitelistRoot | bytes32 | undefined |

### totalSupply

```solidity
function totalSupply(uint256 id) external view returns (uint256)
```



*Total amount of tokens in with a given id.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| id | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### trustedForwarder

```solidity
function trustedForwarder() external view returns (address)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### upgradeTo

```solidity
function upgradeTo(address newImplementation) external nonpayable
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| newImplementation | address | undefined |

### upgradeToAndCall

```solidity
function upgradeToAndCall(address newImplementation, bytes data) external payable
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| newImplementation | address | undefined |
| data | bytes | undefined |

### uri

```solidity
function uri(uint256 _id) external view returns (string)
```

Returns URI for associated token



#### Parameters

| Name | Type | Description |
|---|---|---|
| _id | uint256 | Token ID to get URI for |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | uri for token ID |

### versionLocked

```solidity
function versionLocked() external view returns (bool)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### versionRecipient

```solidity
function versionRecipient() external pure returns (string)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### withdraw

```solidity
function withdraw() external nonpayable
```

Allows manager to transfer eth from contract






## Events

### AdminChanged

```solidity
event AdminChanged(address previousAdmin, address newAdmin)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| previousAdmin  | address | undefined |
| newAdmin  | address | undefined |

### ApprovalForAll

```solidity
event ApprovalForAll(address indexed account, address indexed operator, bool approved)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| account `indexed` | address | undefined |
| operator `indexed` | address | undefined |
| approved  | bool | undefined |

### BaseUriUpdated

```solidity
event BaseUriUpdated(string uri)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| uri  | string | undefined |

### BeaconUpgraded

```solidity
event BeaconUpgraded(address indexed beacon)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| beacon `indexed` | address | undefined |

### Initialized

```solidity
event Initialized(uint8 version)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| version  | uint8 | undefined |

### MaxSupplyLocked

```solidity
event MaxSupplyLocked(uint256 id)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| id  | uint256 | undefined |

### MaxSupplyUpdated

```solidity
event MaxSupplyUpdated(uint256 id, uint256 maxSupply)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| id  | uint256 | undefined |
| maxSupply  | uint256 | undefined |

### OwnershipSet

```solidity
event OwnershipSet(address indexed previousOwner, address indexed newOwner)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| previousOwner `indexed` | address | undefined |
| newOwner `indexed` | address | undefined |

### RoleAdminChanged

```solidity
event RoleAdminChanged(bytes32 indexed role, bytes32 indexed previousAdminRole, bytes32 indexed newAdminRole)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| role `indexed` | bytes32 | undefined |
| previousAdminRole `indexed` | bytes32 | undefined |
| newAdminRole `indexed` | bytes32 | undefined |

### RoleGranted

```solidity
event RoleGranted(bytes32 indexed role, address indexed account, address indexed sender)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| role `indexed` | bytes32 | undefined |
| account `indexed` | address | undefined |
| sender `indexed` | address | undefined |

### RoleRevoked

```solidity
event RoleRevoked(bytes32 indexed role, address indexed account, address indexed sender)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| role `indexed` | bytes32 | undefined |
| account `indexed` | address | undefined |
| sender `indexed` | address | undefined |

### TokenCreated

```solidity
event TokenCreated(uint256 id, string name, uint256 maxSupply, bool transferEnabled)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| id  | uint256 | undefined |
| name  | string | undefined |
| maxSupply  | uint256 | undefined |
| transferEnabled  | bool | undefined |

### TransferBatch

```solidity
event TransferBatch(address indexed operator, address indexed from, address indexed to, uint256[] ids, uint256[] values)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| operator `indexed` | address | undefined |
| from `indexed` | address | undefined |
| to `indexed` | address | undefined |
| ids  | uint256[] | undefined |
| values  | uint256[] | undefined |

### TransferEnableUpdated

```solidity
event TransferEnableUpdated(uint256 id, bool transferable)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| id  | uint256 | undefined |
| transferable  | bool | undefined |

### TransferEnabledLocked

```solidity
event TransferEnabledLocked(uint256 id)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| id  | uint256 | undefined |

### TransferSingle

```solidity
event TransferSingle(address indexed operator, address indexed from, address indexed to, uint256 id, uint256 value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| operator `indexed` | address | undefined |
| from `indexed` | address | undefined |
| to `indexed` | address | undefined |
| id  | uint256 | undefined |
| value  | uint256 | undefined |

### URI

```solidity
event URI(string value, uint256 indexed id)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| value  | string | undefined |
| id `indexed` | uint256 | undefined |

### Upgraded

```solidity
event Upgraded(address indexed implementation)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| implementation `indexed` | address | undefined |

### VersionLocked

```solidity
event VersionLocked()
```






### Withdraw

```solidity
event Withdraw(uint256 value, address indexed withdrawnBy)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| value  | uint256 | undefined |
| withdrawnBy `indexed` | address | undefined |



