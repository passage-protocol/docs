# OpenSeaCreatorFeeFilter1155









## Methods

### OPERATOR_FILTER_REGISTRY

```solidity
function OPERATOR_FILTER_REGISTRY() external view returns (contract IOperatorFilterRegistry)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract IOperatorFilterRegistry | undefined |

### beforeTokenTransfers

```solidity
function beforeTokenTransfers(address sender, address from, address, uint256[], uint256[]) external view
```

Restricts NFT sales from marketplaces that do not enforce creator fees via OpenSea operator filter registry

*see https://github.com/ProjectOpenSea/operator-filter-registry*

#### Parameters

| Name | Type | Description |
|---|---|---|
| sender | address | original tx sender |
| from | address | holder fo token being transferred |
| _2 | address | undefined |
| _3 | uint256[] | undefined |
| _4 | uint256[] | undefined |




## Errors

### OperatorNotAllowed

```solidity
error OperatorNotAllowed(address operator)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| operator | address | undefined |


