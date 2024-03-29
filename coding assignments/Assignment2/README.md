# Assignment 2: Creating price feeds

To reflect the value of other assets, we need to first obtain price feeds before minting synthetic assets. While everyone can get the latest price of a stock on NASDAQ and put it on the chain, data consumers may not want to trust any single data provider.

**Data oracles** provide a decentralized and trustworthy way for blockchains to access external data sources. Resources external to the blockchain are considered "off-chain" while data stored on the blockchain is considered on-chain. Oracle is an additional piece of infrastructure to bridge the two environments.

In this part, we will use one of the most popular oracle solutions, [Chainlink](https://docs.chain.link/), to create price feeds for our synthetic tokens.



## Price feed interface
We have provided the interface of the price feed smart contract in `interfaces/IPriceFeed.sol`, you need to implement your `PriceFeed.sol` and deploy one instance for each synthetic asset to provide their prices with respect to USD. You can refer to [this tutorial](https://docs.chain.link/docs/get-the-latest-price/) for help. The proxy addresses of each asset in Sepolia are provided below: 

```
TSLA / USD: 0xC32f0A9D70A34B9E7377C10FDAd88512596f61EA
BNB / USD: 0x8A6af2B75F23831ADc973ce6288e5329F63D86c6
```
1. There is only one function defined in the interface, you are required to implement it to provide the requested information. You can design other parts of the contract as you like.
2. Deploy the price feed contract for each asset, test the interface and copy their addresses. Once the deployment transactions are confirmed, you are able to find the deployed contracts in [etherscan](https://sepolia.etherscan.io/) with https://sepolia.etherscan.io/address/{:your_contract_address}. (The verification process could be found in Assignment1, 'Submission' part)
3. These seeds do not reflect not real prices of TSLA or BNB. As long as your Solidity code can be compiled and obtain a value from seed, your submission will be ok

## Submission
Submit the **addresses/etherscan links** to the two contracts to **canvas**
