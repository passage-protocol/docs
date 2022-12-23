# PermissionedMint









## Methods

### DEFAULT_ADMIN_ROLE

```solidity
function DEFAULT_ADMIN_ROLE() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### addModuleAddress

```solidity
function addModuleAddress(address moduleAddress) external nonpayable
```

Add module address for mint validation



#### Parameters

| Name | Type | Description |
|---|---|---|
| moduleAddress | address | address |

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

### mint

```solidity
function mint(uint256 mmIndex, uint256[] tokenIds, uint256[] mintAmounts, bytes32[] proof, bytes data) external payable
```

Mint Passport token(s) to caller

*Must first enable claim &amp; set fee/amount (if desired)*

#### Parameters

| Name | Type | Description |
|---|---|---|
| mmIndex | uint256 | uint256 index of permission implementation to use for validation |
| tokenIds | uint256[] | uint256[] Held token ID(s) of tokens to mint |
| mintAmounts | uint256[] | uint256[] Amount of tokens to mint for each held token |
| proof | bytes32[] | bytes32[] proof for claimlist |
| data | bytes | bytes[] supplemental data |

### mintingModules

```solidity
function mintingModules(uint256) external view returns (address)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### passport

```solidity
function passport() external view returns (contract IPassport)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract IPassport | undefined |

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

### withdraw

```solidity
function withdraw() external nonpayable
```








## Events

### Mint

```solidity
event Mint(address indexed holderAddress, uint256[] tokenIds, bytes data)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| holderAddress `indexed` | address | undefined |
| tokenIds  | uint256[] | undefined |
| data  | bytes | undefined |

### ModuleAddressAdded

```solidity
event ModuleAddressAdded(address moduleAddress, uint256 index)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| moduleAddress  | address | undefined |
| index  | uint256 | undefined |

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

### Withdraw

```solidity
event Withdraw(uint256 value, address indexed withdrawnBy)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| value  | uint256 | undefined |
| withdrawnBy `indexed` | address | undefined |



