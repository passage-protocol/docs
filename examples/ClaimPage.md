---
description: Example on how to set up a claim page for your Passport NFTs
---

# Options

V2 Passports support various options for claiming - this example includes two: open/priced claim & permissioned claim from a list of addresses (claimlist/allowlist).

# Sample Code

A simple example frontend claim page repository can be found [here](https://github.com/passage-protocol/example-claim-page).

## Open Claim

### Configuration

If you want an open claim (anyone can mint a token), a Passport must be deployed with the supporting minting module attached & configured. [`setMintingModule`](../contracts/Passport/v2.md#setMintingModule) can be used to set minting modules. For module specific configuration, see [`Minting Modules`](..).

When you are ready to open up your minting, call [`setIsActive(true)`](../contracts/Passport/v2.md#setIsActive) on the respective minting modules.

### Frontend Integration

Sample frontend integration can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/components/Claim.tsx)

## Permissioned Claim

### Configuration

If you want a permissioned claim from a list of addresses (claimlist/allowlist), you must first configure the claimlist minting module's options. 

First, you need to generate a merkle tree root with your list of addresses. This operation can be done with the [Javascript library `merkletreejs`](https://github.com/miguelmota/merkletreejs). The hashing algorithm should be keccak256 and pair sorting should be enabled. The Leaf is abi encodePacked wallet address & maximum amount the wallet can claim.

[`setClaimlistOptions`](../contracts/Passport/v1.md#setclaimlistoptions) can then be used to configure your desired mint price per token & merkle tree root. If a free mint is desired, a claim fee of `0` can be passed in.

When you are ready to open up your minting, call [`setClaimlistClaimEnabled(true)`](../contracts/Passport/v1.md#setclaimlistclaimenabled) and anyone on your list will be able to claim their token.

When claiming through the claimlist, [`claimClaimlist`](../contracts/Passport/v1.md#claimclaimlist) must be called with the proof, maximum amount of tokens a wallet can mint as recorded in the merkle tree, and desired amount of tokens to claim. The proof can be constructed with the same [`merkletreejs`](https://github.com/miguelmota/merkletreejs) library.

If new wallet addresses needs to be added to the claim list, then the merkle tree root needs to be regenerated & [`setClaimlistRoot`](../contracts/Passport/v1.md#setclaimlistroot) called with the newly generated root.

Sample construction of the merkle tree root & proofs can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/utils/merkleTree.tsx)

### Frontend Integration

Sample frontend integration can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/components/Claimlist.tsx)

# Questions

Question not answered? Need something that is not listed? Please [get in touch](mailto:hello@passage.xyz) with our team.
