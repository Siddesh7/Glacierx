# Glacierx | Zapier of DeFi
## Version 0.0.1

Investing in Cryptocurrencies in a sense is risky and it is also difficult to understand DeFi Jargon, Glacier tries to solve both of these by offering gasless defi experience powered by Gelato Network Relay. To make investing even more compounding, Superfluid money streams are used to buy token reguraly.

*Glacierx* offers 3 products
1. Glacierx Portfolio Rebalancer - Automatically swaps tokens based on predefined logic using Gelato Automation and Uniswap

2. Glacierx SIP - Offers systematic buying experience without head work.
3. Glacierx Triggers - Set trigger to do actions, set buy token action when you receive a token.

# Glacierx Portfolio Rebalancer

The user first creates a vault, deposit the tokens on button click gasless, a automation task is created on Gelato Network which then Rebalances the tokens in the vault by selling surplus tokens and buy deficit tokens on Uniswap.

# Glacierx SIP

The user first create a SIP which creates their own SIP vault, as soon as the user approves the token on the frontend, a Superfluid money stream will be started to their vault contract, now after the interval is hit,Gelato ops calls the function, the vault contract will buy the predefined tokens using Uniswap.

# Glacierx Actions

This is a pretty interesting feature which lets users to set triggers based on some onchain action. For this MVP, it offers a trigger to buy some token when you recieve some token on chain. Glacierx actions also can make use of cross chain actions like to bridge and buy a token on chain B when you receive token on chain A, which is acheived by using Wormhole and Gelato together.


Contracts are deployed in Polygon Mumbai
```
 SIPFactory: "0xFF42b61c2b525ce8D53928256B65b8158852FB4C",
 RebalancerFactory: "0x9B4fd31d624a975D65182f7a9786b0F14a461f9b",
 SocketFactory: "0x87A5A2E29cB8DB7D7622CFc2A01478C92049E5f7",
```

Glacierx uses Gasless transaction using Gelato Network Relay and 1balance. Gelato Automation is used to trigger functions in the contract.
Superfluid money streams are used for SIP usecase to dollar cost average buying tokens.
