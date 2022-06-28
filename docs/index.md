# Overview

_XXXXX_ delivers a cross-ledger DEX aggregator that allows for best execution through market aggregation, tapping into AMMs on multiple chains, for dark pool- like order execution. The user can initiate a swap of any of the tokens we support and we find the best route for that swap, whether that is a simple swap in an Automated Market Maker (AMM) or via a more complex system moving tokens between different networks to achieve the best result.

More information on the **3 main features**:

## 1.	CoW

_XXXXX_ introduces a cross-chain version of Coincidence of Wants (CoW), it collects CoWs from any ledger and matches orders while off-chain. This cross-ledger smart matching engine organizes orders to be matched and seeks ways to go through larger networks and tokens to get to the more exotic networks and tokens. _XXXXX_'s algorithm optimizes output for the user since CoW can be cheaper, faster, and sometimes more reliable.

## 2. Cross-Chain
_XXXXX_ can be used to transfer any cryptographic asset from one ledger to another and thus, by definition, it is cross-chain and cross-layer. We leverage YYYYY for cross-chain transfers and swaps by bundling swaps, settling the exchange of assets via cross-chain CoWs, and the rest of the order through bridges.

## 3. DEXA
_XXXXX_ is designed to utilize the power of chain-agnostic computing to obtain the best execution through DEX aggregation, across multiple EVM-compatible L1s, L2s, and other ecosystems. A user can start a swap of any token and _XXXXX_ intelligently routes this swap through a network of blockchain bridges, being sensitive to transfer cost and time. Token information is aggregated from DEXs (interacting with, e.g., Uniswap, Sushiswap, or other protocols that are able to perform swaps of tokens), and it sources liquidity data as well as liquidity to find the best route to swap tokens. 
 
   ___
   
# Process

The basic _XXXXX_ process is as follows:

1. An API gathers all the configurations from the user to be sent for processing; the algorithm operates off-chain* but against multiple networks (chains and layers) with bridging included.
2. Batches of orders are gathered over a set period of time. Once gathered, we try to find the optimum swap routes (including DEXs and bridges)
3. The problem is sent out to **external solvers** (listening to an API) who try to solve it using their custom algorithms. Solvers stake $XXXX before submitting their solution.
4. We also solve the problem using our in-house algorithm.
5. We then compare our solution with the solvers' solutions and reward the best solver.
6. Lastly, we submit the best solution on the chain.

* Initializing a request for the swap is not based on a blockchain event. Instead, it is initialized directly by the user entering information into a database, either using a front-end desktop tool or mobile application. This was conceived because we need a time period to find the best route and also to check whether a CoW exists. This requires a baseline database from which we can obtain the information and this database will select the best alternative route to be executed if, for example, no CoW is found after a given period of time.
