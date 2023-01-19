---
description: Use a subgraph to query data about your memberships.
---

# 📈 Subgraph

Passage uses [subgraphs](https://thegraph.com/docs/en/about/introduction/#what-the-graph-is) for indexing and organizing data from the Passage smart contracts. These subgraphs are hosted on The Graph hosted service and can be used to query your memberships data.

## Networks

Each network has it's own unique subgraph [endpoint](SubgraphEndpoints2.md). Every Passport or Loyalty Ledger contract that is created from the Passage Registry is automatically indexed by the subgraph.

## Queries

Example subgraph queries can be found [here](SubgraphQueries.md). 

Currently, our mainnet subgraph is deployed on The Graph's network, therefore it requires an API_KEY to be used when querying to pay query fees.
