# Eth London x API3

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

## Introduction to API3

[API3](https://api3.org/) is a collaborative project that delivers Oracle services to smart contracts in a decentralized and trust-minimized way. It is governed by a decentralized autonomous organization (DAO), namely the [API3 DAO](https://api3.org/dao).

- [API3 Docs](https://docs.api3.org/)
- [Github](https://github.com/api3dao/)
- [Medium](https://medium.com/@api3)

### Airnode and dAPIs

Airnode is a serverless function that lets API providers run their own oracle nodes. That way, they can provide data to any on-chain dApp that's interested in their services without an intermediary.

First-party oracles provide a more secure and reliable oracle, whilst enabling dApps to transparently understand the data source.

ou can [learn more about first-party oracles](https://docs.api3.org/guides/airnode/calling-an-airnode/) or [dAPIs](https://docs.api3.org/explore/dapis/what-are-dapis.html) within the API3 Documentation.

### API3 data feeds: dAPIs

dAPIs provide smart contracts with access to continuously updated feeds of market data. API3 data feeds can be accessed in two methods:

- Self-funded dAPIs see users add collateral for oracle operation and are permissionless. They provide an efficient and secure data feed source, with off-chain aggregation.

- Managed dAPIs are operated by the API3 DAO and require authorization. They are powered by multiple first-party oracles with native-chain aggregation, offering a decentralized oracle solution.

Once a dAPI has been imported a smart contract can access a range of data feed services through the [API3 Market](https://market.api3.org/dapis).

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

### Additional learning resources 

dAPIs give DeFi builders access to over 130 forex & crypto dAPIs that serve real-time market data to 10 networks (and 11 testnets). The below resources will help you get started with first-party data feeds.

Learn more: 

- [Activating a self-funded dAPI](https://docs.api3.org/guides/dapis/subscribing-self-funded-dapis/)
- [Reading a dAPI](https://docs.api3.org/guides/dapis/read-self-funded-dapi/)
- [API3 data feed reader example](https://github.com/api3dao/data-feed-reader-example)

Tutorials: 

- [Making on-chain Payments and mint NFT Receipts using dAPIs](https://medium.com/@vanshwassan/making-an-on-chain-payment-and-minting-an-nft-receipt-with-permissionless-price-oracles-a7339f7b8c3e)
- [Using dAPIs on zkSync Era Testnet](https://vanshwassan.medium.com/using-dapis-on-zksync-era-testnet-30f12efdd95f)
- [zkSync Paymasters with dAPIs](https://era.zksync.io/docs/dev/tutorials/api3-usd-paymaster-tutorial.html)

Or get started now with the API3 Market.

- [API3 Market](https://market.api3.org/)

# Bounty Challenge: ---

## Prize: $2500 (5 x $500) and Opportunity to Win a $10k Grant!

Mantle, the all-inclusive, scalable, and interoperable blockchain network, is thrilled to announce an exciting bounty challenge for innovative developers! We are inviting talented developers to fork a leading EVM (Ethereum Virtual Machine) lending protocol and deploy it on the Mantle Network.
The catch? You need to seamlessly integrate dAPIs (Decentralized Application Interfaces) into your solution. Your task is to show a fully functional lending decentralized application (dApp) running smoothly on the Mantle Network. 

### Getting Started

API3 Hacker Repo: https://github.com/vanshwassan/SozuHack
Real-time Market Data: https://market.api3.org/dapis?chains=mantle-goerli-testnet

### Challenge Breakdown:

1. **Fork an EVM Lending Protocol:** Choose a leading, well-established EVM lending protocol and fork it. The protocol should offer robust lending functionalities and maintain a high standard of security.
2. **Deploy on Mantle:** Adapt the forked protocol to be deployable on the Mantle Network. Leverage Mantle's unique capabilities and adapt the code as needed to ensure smooth operation on our network.
3. **Integrate dAPIs:** Incorporate Mantle's dAPIs into your application to facilitate secure, decentralized user interaction. The application's functionalities must be accessible and smoothly operable via these dAPIs.
4. **Launch a Working DeFi protocol:** Your ultimate deliverable will be a live, operational lending dApp that can facilitate loan origination, tracking, and repayment in a decentralized manner.

### Prizes

- **Bounty:** Each winning team will receive a bounty of $500, broken down into five payments of $500 each, upon the successful completion and demonstration of the lending dApp.
- **Grant Opportunity:** Additionally, three outstanding projects will be selected for a $10,000 grant each from Mantle. These grants are designed to support further development and scaling of the project on our platform.
### Evaluation Criteria:
- Quality of the forked code and deployment on Mantle with dAPIs integrated. 
- Interesting concepts for DeFi UX/UI that leverage the unique features of the Mantle Network.
- Some thought into deployment to Mantle and depth of documentation.
- Innovative approach of crypto, forex, equities and commodities data feeds can underpin DeFi markets and services
