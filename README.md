# Hifi Subgraph

Hifi is a fixed-rate, fixed-term lending protocol built on the Ethereum blockchain. This subgraph indexes the events
emitted by our smart contracts.

You can interact with the subgraph via The Graph's [hosted service](https://thegraph.com/explorer/subgraph/hifi-finance/hifi).

## Queries

Below are a few ways to show how to query the Hifi Subgraph for data. The queries show most of the information
that is queryable, but there are many other filtering options that can be used, just check out the querying api.

You can also see the saved queries on the hosted service for examples.

### Accounts

```graphql
{
  accounts(first: 5) {
    id
    accountFyTokens {
      id
      fyTokenBalance
      totalFyTokenBorrowed
      totalFyTokenRedeemed
      totalFyTokenRepaid
      totalUnderlyingSupplied
      vault {
        id
        debt
        freeCollateral
        lockedCollateral
      }
    }
    countLiquidated
    countLiquidator
  }
}
```
