# Vaults 101

## What is ERC‑4626?
- Standard interface for **tokenized vaults** that hold a single ERC‑20 underlying and issue **shares** 1:1 for accounting of deposits/withdrawals and yield. See references at bottom.

## Types of Vaults
- **Yield vaults (DeFi)**: e.g., Yearn yVaults, Beefy vaults (autocompound strategies).
- **Asset‑management vaults**: e.g., Enzyme configurable strategy vaults.
- **RWA vaults / tokenized funds**: e.g., Ondo OUSG, BlackRock BUIDL via Securitize.
- **Treasury/custody vaults**: Safe (Gnosis Safe) smart accounts; Fireblocks MPC custody.

## Why vaults?
- Composability (standard API), operational abstraction for strategies, access control, share‑based accounting, fee/monetization hooks.

## Core mental model
```
Deposit asset → Vault mints shares → Strategy puts assets to work → Profits → Share price ↑ (or shares rebase) → Withdraw burns shares
```
