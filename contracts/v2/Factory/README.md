# PassageFactory

The `PassageFactory` smart-contract is Passage's V2 factory to deploy Passports and Loyalty Ledgers. Additional configuration parameters can be provided with creation: for Passports, we can specify [minting modules](../Modules/Minting/README.md), transferrability (via [beforeTransfer modules](../Modules/BeforeTransfers/README.md)), and initial airdropping parameters. For Loyalty Ledgers, we can provide initial Token parameters for Token 0, [minting modules](../Modules/Minting/README.md) for this Token, the Token's transferrability (via [beforeTransfer modules](../Modules/BeforeTransfers/README.md)), and airdropping parameters for Token 0.

## Passport Creation

Creating passports can be done with [createPassport](../Factory/v0.md#createpassport).

## Loyalty Ledger Creation

Creating loyalty ledgers can be done with [createLoyalty](../Factory/v0.md#createLoyalty).



For Passage's current deployed Factory's by network, [see here](../DeployedContracts.md#factory). 
