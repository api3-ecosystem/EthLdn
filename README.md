# API3 hacker challenges at EthLondon 🇬🇧👑🔨🌆

Hackers, we hope you are excited for the EthLondon Hackathon! Bringing the Ethereum ecosystem together in the city of London, we are looking forward to seeing what you build.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

# API3 Bounties: Total of $6000 API3

We are pleased to share that API3 will be offering a total of $6000 API3 tokens in bounties for the EthLondon Hackathon. 

### 💸 Best DeFi Concept/Application: $2000 API3 

### 🏆 Best use of an API3 oracle: $2000 API3 

### 🤓 Most innovative use of price feed or QRNG $1000 API3

### 😃 Best collaborator $1000 API3 

# Introduction to API3

[API3](https://api3.org/) is a collaborative project that delivers Oracle services to smart contracts in a decentralized and trust-minimized way. It is governed by a decentralized autonomous organization (DAO), namely the [API3 DAO](https://api3.org/dao).

- [API3 Docs](https://docs.api3.org/)
- [Github](https://github.com/api3dao/)
- [Medium](https://medium.com/@api3)

### Airnode and dAPIs

Airnode is a serverless function that lets API providers run their own oracle nodes. That way, they can provide data to any on-chain dApp that's interested in their services without an intermediary.

First-party oracles provide a more secure and reliable oracle, whilst enabling dApps to verify the data source.

You can [learn more about first-party oracles](https://docs.api3.org/guides/airnode/calling-an-airnode/) or [dAPIs](https://docs.api3.org/explore/dapis/what-are-dapis.html) within the API3 Documentation.

# API3 Oracles

### Data feeds: dAPIs

dAPIs provide smart contracts with access to continuously updated feeds of market data. API3 data feeds can be accessed in two methods:

- Self-funded dAPIs see users add collateral for oracle operation and are permissionless. They provide a data feed source with off-chain aggregation as a single-source. 

- Managed dAPIs are powered by multiple first-party oracles with native-chain aggregation offering a verifiable, decentralized oracle solution.

Once a dAPI has been integrated a smart contract can access a range of data feed services through the [API3 Market](https://market.api3.org/dapis).

### API3 QRNG 

API3 QRNG is a public utility API3 provides on behalf of well-established, prestigious organizations serving Quantum random number generation (QRNG). QRNG is a method of random number generation based on quantum phenomena and considered within the scientific community to be the most secure method of random number generation.

It operates as a public good, where users simply add gas to a wallet correlated to the oracle node, enabling the oracle node to return a random number when requested by a contract.

Learn more about QRNG within the [API3 explore section](https://docs.api3.org/explore/qrng/). 


# Get started with dAPIs

To get started all you have to do is import the `IProxy` interface and call the `read()` function.

```solidity
pragma solidity 0.8.17;

import "@api3/contracts/v0.8/interfaces/IProxy.sol";

contract DataFeedReaderExample {
    ...

    function readDataFeed()
        external
        view
        returns (int224 value, uint256 timestamp)
    {
        // proxyAddress is the address of the proxy contract for
        // the dAPI you want to read.
        // Head over to https://market.api3.org to get the proxy
        // address for the dAPI you want. 
        (value, timestamp) = IProxy(proxyAddress).read();
    } 
}
``` 

<!-- Do we need to add a link to the above?-->

### Learning resources 

Learn more: 

- [Activate self-funded dAPI](https://docs.api3.org/guides/dapis/subscribing-self-funded-dapis/)
- [Read a dAPI value](https://docs.api3.org/guides/dapis/read-self-funded-dapi/)
- [Feed Reader example](https://github.com/api3dao/data-feed-reader-example)

Tutorials: 

- [Making on-chain Payments and mint an NFT receipt using dAPIs](https://medium.com/@vanshwassan/making-an-on-chain-payment-and-minting-an-nft-receipt-with-permissionless-price-oracles-a7339f7b8c3e)

- [zkSync Paymasters with dAPIs](https://era.zksync.io/docs/dev/tutorials/api3-usd-paymaster-tutorial.html)

### References For Hackathons

Links to different repos for examples and help.

- ETH CHI Workshop Repo:
https://github.com/billyjitsu/API3-PriceFeeds-Hardhat-Foundry

- Prediction bet between two Parties
https://github.com/billyjitsu/prediction

- Modified Paymaster for zkSync (Use dAPI to calculate USDC prices of Gas instead of ETH)
https://github.com/billyjitsu/zk-paymaster-dapi-vip

- Fork of Aave with a simulation of a flashloan
https://github.com/billyjitsu/Aave-Api3 

- Starter kit - Starting a borrow/lend setup with WAGMI/rainbowkit front end
https://github.com/billyjitsu/aa-oracle-zkevm

Or get started now with the [API3 Market](https://market.api3.org/).







