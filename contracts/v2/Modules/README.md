# Modules

In V2, we introduce a much more composable & robust framework using _modules_, which act almost as plugins - enabling both increased flexibility, as well as decreased coupling with our Passports & Loyalty Ledgers and some of their core functionalities.

There are currently three different types:

- BeforeTransfers
- Minting
- Render

## BeforeTransfers Modules
[These modules](./BeforeTransfers/README.md) handle logic surrounding transferability, such as disabling transfers. 

## Minting Modules
[These modules](./Minting/README.md) handle logic surrounding minting, such as priced mints, or whitelisted/permissioned mints.

## Render Modules
[These modules](./Render/README.md) are responsible for URI rendering semantics, such as custom overrides or more elaborate URI logic.