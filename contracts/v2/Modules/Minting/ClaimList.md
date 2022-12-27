# ClaimList









## Methods

### DEFAULT_ADMIN_ROLE

```solidity
function DEFAULT_ADMIN_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### canMint

```solidity
function canMint(address minter, uint256 value, uint256[], uint256[], bytes32[] proof, bytes data) external nonpayable returns (uint256)
```

Mint Passport token(s) to caller

*Must first enable claim &amp; set fee/amount (if desired)*

#### Parameters

| Name | Type | Description |
|---|---|---|
| minter | address | address the address to mint to |
| value | uint256 | uint256 amount eth sent to minting transaction, in wei |
| _2 | uint256[] | undefined |
| _3 | uint256[] | undefined |
| proof | bytes32[] | bytes32[] merkle tree proof of minter claim |
| data | bytes | supplemental data with [uint256 maxAmount, uint256 claimAmount] |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### claimlistClaimed

```solidity
function claimlistClaimed(address) external view returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### claimlistRoot

```solidity
function claimlistRoot() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### decodeCanMint

```solidity
function decodeCanMint(bytes data) external pure returns (uint256 maxAmount, uint256 claimAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| data | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| maxAmount | uint256 | undefined |
| claimAmount | uint256 | undefined |

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



*Grants `role` to `account`. If `account` had not been already granted `role`, emits a {RoleGranted} event. Requirements: - the caller must have ``role``&#39;s admin role. May emit a {RoleGranted} event.*

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

### initialize

```solidity
function initialize(address _admin, address _minter, bytes data) external nonpayable
```

Initializer function for contract creation



#### Parameters

| Name | Type | Description |
|---|---|---|
| _admin | address | The address of the admin |
| _minter | address | The address of the wallet or contract that can call canMint (passport or LL) |
| data | bytes | encoded bytes32 claimlist - merkle root &amp; uint256 mintPrice - price per token in wei |

### isActive

```solidity
function isActive() external view returns (bool)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### maxClaim

```solidity
function maxClaim() external view returns (uint256)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### mintPrice

```solidity
function mintPrice() external view returns (uint256)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### minterAddress

```solidity
function minterAddress() external view returns (address)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### renounceRole

```solidity
function renounceRole(bytes32 role, address account) external nonpayable
```



*Revokes `role` from the calling account. Roles are often managed via {grantRole} and {revokeRole}: this function&#39;s purpose is to provide a mechanism for accounts to lose their privileges if they are compromised (such as when a trusted device is misplaced). If the calling account had been revoked `role`, emits a {RoleRevoked} event. Requirements: - the caller must be `account`. May emit a {RoleRevoked} event.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

### revokeRole

```solidity
function revokeRole(bytes32 role, address account) external nonpayable
```



*Revokes `role` from `account`. If `account` had been granted `role`, emits a {RoleRevoked} event. Requirements: - the caller must have ``role``&#39;s admin role. May emit a {RoleRevoked} event.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| role | bytes32 | undefined |
| account | address | undefined |

### setClaimlistRoot

```solidity
function setClaimlistRoot(bytes32 _claimlistRoot) external nonpayable
```

Allows admin to set the merkle tree root for the claimlist

*Merkle tree can be generated with the Javascript library &quot;merkletreejs&quot;, the hashing algorithm should be keccak256 and pair sorting should be enabled. Leaf is abi encodePacked address &amp; amount*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _claimlistRoot | bytes32 | Merkle tree root |

### setIsActive

```solidity
function setIsActive(bool _isActive) external nonpayable
```

Set isActive



#### Parameters

| Name | Type | Description |
|---|---|---|
| _isActive | bool | boolean |

### setMaxClaim

```solidity
function setMaxClaim(uint256 _maxClaim) external nonpayable
```

Set maxClaim



#### Parameters

| Name | Type | Description |
|---|---|---|
| _maxClaim | uint256 | uint256 |

### setMintPrice

```solidity
function setMintPrice(uint256 _mintPrice) external nonpayable
```

Set mintPrice



#### Parameters

| Name | Type | Description |
|---|---|---|
| _mintPrice | uint256 | uint256 |

### setMinterAddress

```solidity
function setMinterAddress(address _minterAddress) external nonpayable
```

Set minterAddress



#### Parameters

| Name | Type | Description |
|---|---|---|
| _minterAddress | address | new minterAddress |

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) external view returns (bool)
```



*See {IERC165-supportsInterface}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| interfaceId | bytes4 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### validateProof

```solidity
function validateProof(bytes32[] proof, address minter, uint256 maxAmount) external view
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| proof | bytes32[] | undefined |
| minter | address | undefined |
| maxAmount | uint256 | undefined |



## Events

### Initialized

```solidity
event Initialized(uint8 version)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| version  | uint8 | undefined |

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



