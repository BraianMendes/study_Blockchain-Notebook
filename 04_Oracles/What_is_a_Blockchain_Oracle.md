# What Is a Blockchain Oracle?

DEFINITION
Blockchain oracles are entities that connect blockchains to external systems, thereby enabling smart contracts to execute based upon inputs and outputs from the real world. 

Oracles provide a way for the decentralized Web3 ecosystem to access existing data sources, legacy systems, and advanced computations. Decentralized oracle networks (DONs) enable the creation of hybrid smart contracts, where on-chain code and off-chain infrastructure are combined to support advanced decentralized applications (dApps) that react to real-world events and interoperate with traditional systems.

![](.gitbook/assets/04_Oracles/Oracle01.png)

For example, let’s assume Alice and Bob want to bet on the outcome of a sports match. Alice bets $20 on team A and Bob bets $20 on team B, with the $40 total held in escrow by a smart contract. When the game ends, how does the smart contract know whether to release the funds to Alice or Bob? The answer is it requires an oracle mechanism to fetch accurate match outcomes off-chain and deliver it to the blockchain in a secure and reliable manner.

## Solving the Oracle Problem

The blockchain oracle problem outlines a fundamental limitation of smart contracts—they cannot inherently interact with data and systems existing outside their native blockchain environment. Resources external to the blockchain are considered “off-chain,” while data already stored on the blockchain is considered on-chain. By being purposely isolated from external systems, blockchains obtain their most valuable properties like strong consensus on the validity of user transactions, prevention of double-spending attacks, and mitigation of network downtime. Securely interoperating with off-chain systems from a blockchain requires an additional piece of infrastructure known as an “oracle” to bridge the two environments.

![](.gitbook/assets/04_Oracles/Oracle02.jpeg)

Solving the oracle problem is of the utmost importance because the vast majority of smart contract use cases like DeFi require knowledge of real-world data and events happening off-chain. Thus, oracles expand the types of digital agreements that blockchains can support by offering a universal gateway to off-chain resources while still upholding the valuable security properties of blockchains. Major industries benefit from combining oracles and smart contracts including asset prices for finance, weather information for insurance, randomness for gaming, IoT sensors for supply chain, ID verification for government, and much more.

Because the data delivered by oracles to blockchains directly determines the outcomes of smart contracts, it is critically important that the oracle mechanism is correct if the agreement is to execute exactly as expected.

## Decentralized Oracles

Blockchain oracle mechanisms using a centralized entity to deliver data to a smart contract introduce a single point of failure, defeating the entire purpose of a decentralized blockchain application. If the single oracle goes offline, then the smart contract will not have access to the data required for execution or will execute improperly based on stale data.
‍
Even worse, if the single oracle is corrupted, then the data being delivered on-chain may be highly incorrect and lead to smart contracts executing very wrong outcomes. This is commonly referred to as the “garbage in, garbage out” problem where bad inputs lead to bad outputs. Additionally, because blockchain transactions are automated and immutable, a smart contract outcome based on faulty data cannot be reversed, meaning user funds can be permanently lost. Therefore, centralized oracles are a non-starter for smart contract applications. 

![](.gitbook/assets/04_Oracles/Oracle03.jpeg)

Truly overcoming the oracle problem necessitates decentralized oracles to prevent data manipulation, inaccuracy, and downtime. A Decentralized Oracle Network, or DON for short, combines multiple independent oracle node operators and multiple reliable data sources to establish end-to-end decentralization.
‍
Even more, many Chainlink DONs, such as Chainlink Price Feeds, incorporate three layers of decentralization—at the data source, individual node operator, and oracle network levels—to eliminate any single point of failure. Chainlink Price Feeds already help secure tens of billions of dollars across smart contract ecosystems through this multi-layered decentralization approach, ensuring smart contracts can safely rely on data inputs during their execution.

![](.gitbook/assets/04_Oracles/Oracle04.jpeg)


## Types of Blockchain Oracles
Given the extensive range of off-chain resources, blockchain oracles come in many shapes and sizes. Not only do hybrid smart contracts need various types of external data and computation, but they require various mechanisms for delivery and different levels of security. Generally, each type of oracle involves some combination of fetching, validating, computing upon, and delivering data to a destination.

### Input Oracles
The most widely recognized type of oracle today is known as an “input oracle,” which fetches data from the real-world (off-chain) and delivers it onto a blockchain network for smart contract consumption. These types of oracles are used to power Chainlink Price Feeds, providing DeFi smart contracts with on-chain access to financial market data. 

### Output Oracles
The opposite of input oracles are “output oracles,” which allow smart contracts to send commands to off-chain systems that trigger them to execute certain actions. This can include informing a banking network to make a payment, telling a storage provider to store the supplied data, or pinging an IoT system to unlock a car door once the on-chain rental payment is made. 

### Cross-Chain Oracles
Another type of oracle are cross-chain oracles that can read and write information between different blockchains. Cross-chain oracles enable interoperability for moving both data and assets between blockchains, such as using data on one blockchain to trigger an action on another or bridging assets cross-chain so they can be used outside the native blockchain they were issued on.

### Compute-Enabled Oracles
A new type of oracle becoming more widely used by smart contract applications are “compute-enabled oracles,” which use secure off-chain computation to provide decentralized services that are impractical to do on-chain due to technical, legal, or financial constraints. This can include using Chainlink Automation to trigger the running of smart contracts when predefined events take place, computing zero-knowledge proofs to generate data privacy, or running a verifiable randomness function to provide a tamper-proof and provably fair source of randomness to smart contracts.

![](.gitbook/assets/04_Oracles/Oracle05.jpeg)


## Oracle Reputation Derived From On-chain Performance History

The broad range of oracle services means reputation is key to choosing between oracle service providers. Reputation in blockchain oracle systems gives users and developers the ability to monitor and filter between oracles based on parameters they deem important. Oracle reputation is aided by the fact that oracles sign and deliver their data onto an immutable public blockchain ledger, and so their historical performance history can be analyzed and presented to users through interactive dashboards such as market.link and reputation.link. 
‍
Reputation frameworks provide transparency into the accuracy and reliability of each oracle network and individual oracle node operator. Users can then make informed decisions about which oracles they want to service their smart contracts. Oracle service providers can also leverage their off-chain business reputation to provide users additional guarantees of their reliability. 

## Blockchain Oracle Use Cases

Smart contract developers use oracles to build more advanced decentralized applications across a wider range of blockchain use cases. While there are a potentially infinite number of possibilities, below are the use cases with the most current adoption.

### Decentralized Finance (DeFi)

A large portion of the decentralized finance (DeFi) ecosystem requires oracles to access financial data about assets and markets. For example, decentralized money markets use price oracles to determine users’ borrowing capacity and check if users’ positions are undercollateralized and subject to liquidation. Similarly, synthetic asset platforms use price oracles to peg the value of tokens to real-world assets and automated market makers (AMMs) use price oracles to help concentrate liquidity at the current market price to improve capital efficiency. 

### Dynamic NFTs and Gaming

Oracles enable non-financial use cases for smart contracts too such as dynamic NFTs—Non-Fungible Tokens that can change in appearance, value, or distribution based on external events like the time of day or the weather. Additionally, compute oracles are used to generate verifiable randomness that projects then use to assign randomized traits to NFTs or to select random lucky winners in high-demand NFT drops. On-chain gaming applications also use verifiable randomness to create more engaging and unpredictable gameplay experiences like the appearance of random loot boxes or randomized matchmaking during a tournament. 

### Insurance

Insurance smart contracts use input oracles to verify the occurrence of insurable events during claims processing, opening up access to physical sensors, web APIs, satellite imagery, and legal data. Output oracles can also provide insurance smart contracts with a way to make payouts on claims using other blockchains or traditional payment networks.

### Enterprise

Cross-chain oracles offer enterprises a secure blockchain middleware that allows them to connect their backend systems to any blockchain network. In doing so, enterprise systems can read/write to any blockchain and perform complex logic on how to deploy assets and data across chains and with counterparties using the same oracle network. The result is institutions being able to quickly join blockchains in high demand by their counterparties and swiftly create support for smart contract services wanted by their users without having to spend time and development resources integrating with each individual blockchain.

### Sustainability

Hybrid smart contracts are advancing environmental sustainability by creating better incentives to partake in green practices through advanced verification techniques around the true impact of green initiatives. Oracles are a critical tool to supplying smart contracts with environmental data from sensor readings, satellite imagery, and advanced ML computation, which then allow smart contracts to dispense rewards to people practicing reforestation or engaging in conscious consumption. Oracles are also supporting many new forms of carbon credits to offset the impacts of climate change.

![](.gitbook/assets/04_Oracles/Oracle06.jpeg)

Oracles extend the capabilities of blockchain networks by providing access to all the external resources required to harness useful and advanced hybrid smart contract use cases beyond simple tokenization. Similar to how the Internet brought forth a significant change in the way information is exchanged, oracle-powered hybrid smart contracts are redefining the way society exchanges value and enforces contractual agreements.