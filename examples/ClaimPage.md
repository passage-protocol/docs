---
description: Example on how to set up a claim page for your Passport NFTs
---

# Options

Passports provider two options for claims: open claim & permissioned claim from a list of addresses (claimlist/allowlist).

# Sample Code

An simple example frontend claim page repository can be found [here](https://github.com/passage-protocol/example-claim-page).

## Open Claim

### Configuration

If you want an open claim (anyone can mint a token), you first need to set the claim options. [`setClaimOptions`](contracts/Passport/v1.md#setClaimOptions) can be used to configure your desired mint price per token & maximum claim amount per transaction. If a free mint is desired, a claim fee of `0` can be passed in.

When you are ready to open up your minting, call [`setClaimEnabled(true)`](contracts/Passport/v1.md#setClaimEnabled) and anyone will be able to claim their token.

### Frontend Integration

Sample frontend integration can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/components/Claim.tsx)

## Permissioned Claim

### Configuration

If you want an permissioned claim from a list of addresses (claimlist/allowlist), you first can setup the claimlist claim options. Each wallet address can only claim `1` time, up to the maximum amount of tokens specified in the claimlist.

First, you need to generate a merkle tree root with your list of addresses. This operation can be done with the [Javascript library `merkletreejs`](https://github.com/miguelmota/merkletreejs). The hashing algorithm should be keccak256 and pair sorting should be enabled. The Leaf is abi encodePacked wallet address & maximum amount the wallet can claim.

[`setClaimlistOptions`](contracts/Passport/v1.md#setClaimlistOptions) can then be used to configure your desired mint price per token & merkle tree root. If a free mint is desired, a claim fee of `0` can be passed in.

When you are ready to open up your minting, call [`setClaimlistClaimEnabled(true)`](contracts/Passport/v1.md#setClaimlistClaimEnabled) and anyone on your list will be able to claim their token.

When claiming through the claimlist, [`claimClaimlist`](contracts/Passport/v1.md#claimClaimlist) must be called with the proof, maximum amount of tokens a wallet can mint as recorded in the merkle tree, and desired amount of tokens to claim. The proof can be constructed with the same [`merkletreejs`](https://github.com/miguelmota/merkletreejs) library.

If new wallet addresses needed to be added to the claim list, then the merkle tree root needs to be regenerated & [`setClaimlistRoot`](contracts/Passport/v1.md#setClaimlistRoot) called with the newly generated root.

Sample construction of the merkle tree root & proofs can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/utils/merkleTree.tsx)

### Frontend Integration

Sample frontend integration can be found [here](https://github.com/passage-protocol/example-claim-page/blob/master/src/components/Claimlist.tsx)
