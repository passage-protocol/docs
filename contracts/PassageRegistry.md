# PassageRegistry



> Passage Registry

The registry facilitates creation of Passports and Loyalty Ledgers



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

### addLoyaltyImplementation

```solidity
function addLoyaltyImplementation(address implementation) external nonpayable
```

Allows manager to add a new Loyalty Ledger implementation



#### Parameters

| Name | Type | Description |
|---|---|---|
| implementation | address | Address of the implementation |

### addPassportImplementation

```solidity
function addPassportImplementation(address implementation) external nonpayable
```

Allows manager to add a new Passport implementation



#### Parameters

| Name | Type | Description |
|---|---|---|
| implementation | address | Address of the implementation |

### createLoyalty

```solidity
function createLoyalty() external nonpayable returns (address loyaltyAddress)
```

Creates a new Loyalty Ledger

*a convenience function for createLoyalty(bytes memory data)*


#### Returns

| Name | Type | Description |
|---|---|---|
| loyaltyAddress | address | The created Loyalty Ledger contract address |

### createLoyalty

```solidity
function createLoyalty(bytes data) external nonpayable returns (address loyaltyAddress)
```

Creates a new Loyalty Ledger



#### Parameters

| Name | Type | Description |
|---|---|---|
| data | bytes | The encoded function data for the Loyalty Ledger initialize function |

#### Returns

| Name | Type | Description |
|---|---|---|
| loyaltyAddress | address | The created Loyalty Ledger contract address |

### createPassport

```solidity
function createPassport(bytes data) external nonpayable returns (address passportAddress)
```

Creates a new Passport



#### Parameters

| Name | Type | Description |
|---|---|---|
| data | bytes | The encoded function data for the Passport initialize function |

#### Returns

| Name | Type | Description |
|---|---|---|
| passportAddress | address | The created Passport contract address |

### createPassport

```solidity
function createPassport(string _tokenName, string _tokenSymbol, bool _transferEnabled, uint256 _maxSupply) external nonpayable returns (address passportAddress)
```

Creates a new Passport

*a convenience function for createPassport(bytes memory data)*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _tokenName | string | The token name |
| _tokenSymbol | string | The token symbol |
| _transferEnabled | bool | If transfer enabled |
| _maxSupply | uint256 | Max supply of tokens |

#### Returns

| Name | Type | Description |
|---|---|---|
| passportAddress | address | The created Passport contract address |

### ejectLoyaltyLedger

```solidity
function ejectLoyaltyLedger() external nonpayable
```

Removes Loyalty Ledger from managed list

*Only callable from managed Loyalty Ledger*


### ejectPassport

```solidity
function ejectPassport() external nonpayable
```

Removes Passport from managed list

*Only callable from managed Passport*


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

### globalLoyaltyBaseURI

```solidity
function globalLoyaltyBaseURI() external view returns (string)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### globalPassportBaseURI

```solidity
function globalPassportBaseURI() external view returns (string)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

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

### initialize

```solidity
function initialize(string _globalPassportBaseURI, string _globalLoyaltyBaseURI) external nonpayable
```

Initializer function for contract creation instead of constructor to support upgrades



#### Parameters

| Name | Type | Description |
|---|---|---|
| _globalPassportBaseURI | string | The global base URI for Passports |
| _globalLoyaltyBaseURI | string | The global base URI for Loyalty Ledgers |

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

### loyaltyImplementations

```solidity
function loyaltyImplementations(uint256) external view returns (address)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### loyaltyLatestVersion

```solidity
function loyaltyLatestVersion() external view returns (uint256)
```

Get the index of the latest loyalty ledger implementation added




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | latestVersion index of the latest loyalty ledger implementation added |

### managedLoyaltyLedgers

```solidity
function managedLoyaltyLedgers(address) external view returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### managedPassports

```solidity
function managedPassports(address) external view returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### passportImplementations

```solidity
function passportImplementations(uint256) external view returns (address)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### passportLatestVersion

```solidity
function passportLatestVersion() external view returns (uint256)
```

Get the index of the latest passport implementation added




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | latestVersion index of the latest passport implementation added |

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

### setGlobalLoyaltyBaseURI

```solidity
function setGlobalLoyaltyBaseURI(string _uri) external nonpayable
```

Allows manager to set new global Loyalty Ledger URI



#### Parameters

| Name | Type | Description |
|---|---|---|
| _uri | string | New global Loyalty Ledger URI |

### setGlobalPassportBaseURI

```solidity
function setGlobalPassportBaseURI(string _uri) external nonpayable
```

Allows manager to set new global Passport URI



#### Parameters

| Name | Type | Description |
|---|---|---|
| _uri | string | New global Passport URI |

### setTrustedForwarder

```solidity
function setTrustedForwarder(address forwarder) external nonpayable
```

Allows manager to set new trusted forwarder for meta-transactions



#### Parameters

| Name | Type | Description |
|---|---|---|
| forwarder | address | Address of trusted forwarder |

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

### trustedForwarder

```solidity
function trustedForwarder() external view returns (address)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### upgradeLoyalty

```solidity
function upgradeLoyalty(uint256 version, address loyaltyAddress) external nonpayable returns (uint256 newVersion)
```

Upgrades a deployed Passport to new implementation

*Can only upgrade 1 version at a time &amp; caller must have UPGRADER role on Loyalty Ledger*

#### Parameters

| Name | Type | Description |
|---|---|---|
| version | uint256 | The version to upgrade to |
| loyaltyAddress | address | The address of the Loyalty Ledger to upgrade |

#### Returns

| Name | Type | Description |
|---|---|---|
| newVersion | uint256 | The new implementation version of the Passport |

### upgradePassport

```solidity
function upgradePassport(uint256 version, address passportAddress) external nonpayable returns (uint256 newVersion)
```

Upgrades a deployed Passport to new implementation

*Can only upgrade 1 version at a time &amp; caller must have UPGRADER role on Passport*

#### Parameters

| Name | Type | Description |
|---|---|---|
| version | uint256 | The version to upgrade to |
| passportAddress | address | The address of the Passport to upgrade |

#### Returns

| Name | Type | Description |
|---|---|---|
| newVersion | uint256 | The new implementation version of the Passport |

### upgradeTo

```solidity
function upgradeTo(address newImplementation) external nonpayable
```



*Upgrade the implementation of the proxy to `newImplementation`. Calls {_authorizeUpgrade}. Emits an {Upgraded} event.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newImplementation | address | undefined |

### upgradeToAndCall

```solidity
function upgradeToAndCall(address newImplementation, bytes data) external payable
```



*Upgrade the implementation of the proxy to `newImplementation`, and subsequently execute the function call encoded in `data`. Calls {_authorizeUpgrade}. Emits an {Upgraded} event.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newImplementation | address | undefined |
| data | bytes | undefined |

### versionRecipient

```solidity
function versionRecipient() external pure returns (string)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |



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

### LoyaltyBaseUriUpdated

```solidity
event LoyaltyBaseUriUpdated(string uri)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| uri  | string | undefined |

### LoyaltyCreated

```solidity
event LoyaltyCreated(address indexed loyaltyAddress)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| loyaltyAddress `indexed` | address | undefined |

### LoyaltyLedgerEjected

```solidity
event LoyaltyLedgerEjected(address ejectedAddress)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| ejectedAddress  | address | undefined |

### LoyaltyLedgerImplementationAdded

```solidity
event LoyaltyLedgerImplementationAdded(uint256 version, address implementation)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| version  | uint256 | undefined |
| implementation  | address | undefined |

### LoyaltyVersionUpgraded

```solidity
event LoyaltyVersionUpgraded(address indexed loyaltyAddress, uint256 version)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| loyaltyAddress `indexed` | address | undefined |
| version  | uint256 | undefined |

### PassportBaseUriUpdated

```solidity
event PassportBaseUriUpdated(string uri)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| uri  | string | undefined |

### PassportCreated

```solidity
event PassportCreated(address indexed passportAddress)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| passportAddress `indexed` | address | undefined |

### PassportEjected

```solidity
event PassportEjected(address ejectedAddress)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| ejectedAddress  | address | undefined |

### PassportImplementationAdded

```solidity
event PassportImplementationAdded(uint256 version, address implementation)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| version  | uint256 | undefined |
| implementation  | address | undefined |

### PassportVersionUpgraded

```solidity
event PassportVersionUpgraded(address indexed passportAddress, uint256 version)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| passportAddress `indexed` | address | undefined |
| version  | uint256 | undefined |

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

### Upgraded

```solidity
event Upgraded(address indexed implementation)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| implementation `indexed` | address | undefined |



