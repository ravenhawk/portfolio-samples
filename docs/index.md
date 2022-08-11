Note: For confidentiality purposes, the product name is expressed as _XXXXX_ and the token is expressed as _YYYYY_

# Protocol Overview

_XXXXX_ delivers a cross-ledger DEX aggregator that allows for optimum execution through market aggregation, tapping into Automated Market Makers (AMMs) on multiple chains to achieve dark pool- like order execution. The user can initiate a swap of any supported token and the protocol finds the best route for that swap, whether that be a simple swap in an AMM or via a more complex system moving tokens between different networks to achieve the best result.

The protocol boasts the following **3 main features**:

### 1.	Coincidence of Wants

_XXXXX_ introduces a cross-chain version of Coincidence of Wants (CoW). It collects CoWs from any ledger and matches orders off-chain. This cross-ledger smart matching engine organizes orders that can be matched and seeks routes through larger networks and tokens to get to the more exotic networks and tokens. _XXXXX_'s algorithm optimizes output for the user since CoW can be cheaper, faster, and often more reliable.

### 2. Cross-Chain
_XXXXX_ can be used to transfer any cryptographic asset from one ledger to another and is thus, by definition, cross-chain and cross-layer. We leverage _YYYYY_ for cross-chain transfers and swaps by bundling swaps, settling the exchange of assets via cross-chain CoWs, and the rest of the order is processed through bridges.

### 3. DEXA
_XXXXX_ is designed to utilize the power of chain-agnostic computing to obtain best execution through DEX aggregation, across multiple EVM-compatible L1s, L2s, and other ecosystems. A user can start a swap of any token and _XXXXX_ intelligently routes this swap through a network of blockchain bridges, being sensitive to transfer cost and time. Token information is aggregated from DEXs (interacting with, e.g., Uniswap, Sushiswap, or other protocols that are able to perform token swaps), and it sources liquidity data as well as liquidity to find the best route to swap tokens. 
 
   ___
   
# Process

The basic _XXXXX_ process is as follows:

1. An API gathers all the configurations from the user to be sent for processing; the algorithm operates off-chain* but against multiple networks (chains and layers) with bridging included.
2. Batches of orders are gathered over a set period of time. Once gathered, the protocol tries to find the optimum swap routes (including DEXs and bridges)
3. The problem is sent out to **external solvers** (listening to an API) who try to solve it using their custom algorithms. Solvers stake $_YYYYY_ before submitting their solution.
4. The protocol also solves the problem using our in-house algorithm.
5. We compare our solution with the solvers' solutions and reward the best solver.
6. Lastly, we submit the best solution on the chain.

* Initializing a request for the swap is not based on a blockchain event. Instead, it is initialized directly by the user entering information into a database, either using a front-end desktop tool or mobile application. This was conceived because we need a certain period of time to find the best route and also to check whether a CoW exists.
