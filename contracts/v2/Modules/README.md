# Modules

In V2, we introduce a much more composable & robust framework using _modules_, which act almost as plugins for our Passports & Loyalty Ledgers - increasing flexibility and reducing coupling from core functionality.

There are currently three different types:

- `BeforeTransfers`
- `Minting`
- `Render`

## BeforeTransfers Modules
[BeforeTransfers modules](./BeforeTransfers/README.md) handle logic surrounding transferability, such as disabling transfers. 

### Configuration

| Method | Contract | Description |
|---|---|---|
| [`setBeforeTransfersModule`](../Passport/v0.md#setBeforeTransfersModule) | Passport | set the Passports before transfers module |
| [`setBeforeTransfersModule`](../LoyaltyLedger/v0.md#setBeforeTransfersModule) | Loyalty Ledger | set a Loyalty Token's before transfers module |

## Minting Modules
[Minting modules](./Minting/README.md) handle logic surrounding minting, such as priced mints, or whitelisted/permissioned mints.

### Configuration

| Method | Contract | Description |
|---|---|---|
| [`setMintingModule`](../Passport/v0.md#setMintingModule) | Passport | set the Passports minting module |
| [`setMintingModule`](../LoyaltyLedger/v0.md#setTokenMintingModule) | Loyalty Ledger | set a Loyalty Token's minting module |

## Render Modules
[Render modules](./Rendering/README.md) are responsible for URI rendering semantics, such as custom overrides or more bespoke URI aquisition.

### Configuration

| Method | Contract | Description |
|---|---|---|
| [`setRenderModule`](../Passport/v0.md#setRenderModule) | Passport | set the Passports render module |
| [`setRenderModule`](../LoyaltyLedger/v0.md#setRenderModule) | Loyalty Ledger | set a Loyalty Token's render module |