# API3 hacker challenges at EthLondon 🇬🇧👑🔨🌆

Hackers, we hope you are excited for the EthLondon Hackathon! Bringing the Ethereum ecosystem together in the city of London, we are looking forward to seeing what you build.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

# API3 Bounties: Total of $5000 API3

We are pleased to share that API3 will be offering a total of $5000 API3 tokens in bounties for the EthLondon Hackathon. 

### 💸 Top Prize: Best DeFi Concept/Application: $1500 API3 ###
    
-  **Must be deployed to a testnet**

### 🏆 Overall best use of an API3 oracle: $2500 API3 
- **Criteria:**
    - ChainAPI Integration
    - dAPIs Implementation
    - QRNG (Specifically for Gaming Usage)

- **1st Place:** 1,500 API3

    **2nd Place:** 1,000 API3

    **3rd Place:** 500 API3

### 😃 Best collaborator $500 API3 

# Introduction to API3

[API3](https://api3.org/) is a collaborative project that delivers Oracle services to smart contracts in a decentralized and trust-minimized way. It is governed by a decentralized autonomous organization (DAO), namely the [API3 DAO](https://api3.org/dao).

- [API3 Docs](https://docs.api3.org/)
- [Github](https://github.com/api3dao/)
- [Medium](https://medium.com/@api3)

### Airnode and dAPIs

Airnode is a serverless function that lets API providers run their own oracle nodes. That way, they can provide data to any on-chain dApp that's interested in their services without an intermediary.

First-party oracles provide a more secure and reliable oracle, whilst enabling dApps to verify the data source.

You can [learn more about first-party oracles](https://docs.api3.org/guides/airnode/calling-an-airnode/) or [dAPIs](https://docs.api3.org/explore/dapis/what-are-dapis.html) within the API3 Documentation.

### Data feeds: dAPIs

dAPIs provide smart contracts with access to continuously updated feeds of market data. API3 data feeds can be accessed in two methods:

- Self-funded dAPIs see users add collateral for oracle operation and are permissionless. They provide a data feed source with off-chain aggregation as a single-source. 

- Managed dAPIs are powered by multiple first-party oracles with native-chain aggregation offering a verifiable, decentralized oracle solution.

Once a dAPI has been integrated a smart contract can access a range of data feed services through the [API3 Market](https://market.api3.org/dapis).

### API3 QRNG 

API3 QRNG is a public utility API3 provides on behalf of well-established, prestigious organizations serving Quantum random number generation (QRNG). QRNG is a method of random number generation based on quantum phenomena and considered within the scientific community to be the most secure method of random number generation.

It operates as a public good, where users simply add gas to a wallet correlated to the oracle node, enabling the oracle node to return a random number when requested by a contract.

Learn more about QRNG within the [API3 explore section](https://docs.api3.org/explore/qrng/). 

<!--

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
-->

<!-- Do we need to add a link to the above?-->

# Learning resources 

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

# Community link

Looking for help or just want to hang with industry leading developers? Head to the API3 Discord and drop questions in the #dev-support channel: https://discord.gg/api3dao

## Submission Requirements

All hackathon participants who are competing for the API3 bounties are required to submit a project that meets the following requirements:

- The project should be submitted to the ETH London Hackathon 2023 by the deadline.
- Use of API3’s self-funded dAPIs that facilitates a proper use-case.
- The project should be live with a working frontend deployed.
- The project should be open-source with a public Github repository with the codebase, 
- The repo must be licenced with one of the following open source licences: GPL-3.0, or MIT.

# Judging criteria

Participants may submit a maximum of 1 project by the hackathon deadline. After submission, projects will be judged by the following criteria:

- **Real-world Functionality**: How well does the project work? Does it meet the minimum requirements?

- **Technical Difficulty**: How technically challenging was it to build the project?

- **Originality**: How original is the idea? How much does it differ from other existing solutions?

- **Design**: How well-designed is the project? Is it easy to use? Is it visually appealing?

- **BONUS** - Adding functionality to the Airnode protocol that will improve performance, interoperability, or further develop use cases.