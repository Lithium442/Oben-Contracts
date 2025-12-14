### Liquidity Pool Design (OBEN_Pools_v3)

Each rail token (ORION, LITHIUM, LIBRA) uses **two Uniswap v3 pools**: one anchored to WETH and one anchored to USDC.  

This gives:
- A **stable-value axis** (USDC) for pricing and accounting
- A **crypto-native axis** (WETH) for on-chain liquidity and arbitrage
- Redundancy: if one quote asset becomes volatile or illiquid, the other pool can still function

**Price bands** are defined in ETH for consistency:

- ORION: mid `0.10 ETH`, band `0.07 – 0.13 ETH`
- LITHIUM: mid `0.03 ETH`, band `0.02 – 0.06 ETH`
- LIBRA: mid `0.01 ETH`, band `0.001 – 0.09 ETH`

For USDC pools, initial prices are chosen so that:

> Token price in USDC ≈ (token price in ETH) × (ETH/USD at launch)

The CSV file [`data/OBEN_Pools_v3.csv`](data/OBEN_Pools_v3.csv) stores:
- Pool codes (O1, O2, L1, L2, B1, B2)
- Pair (e.g. `ORION/USDC`, `LITHIUM/WETH`)
- Treasury launch share per pool (how much of initial liquidity goes into each pool)
- ETH-denominated price band (mid, min, max)
- Fee tier (Uniswap v3)
- Free-text notes