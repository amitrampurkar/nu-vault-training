
# Glossary (Vaults & RWAs)

- **Vault (ERC‑4626)** — A smart contract that accepts an *underlying* ERC‑20 token and issues **shares** that track pro‑rata ownership over the vault’s total assets.
- **Shares / Assets** — `convertToShares()` and `convertToAssets()` are the canonical functions for pricing deposits/withdrawals without slippage.
- **Strategy Adapter** — Component a vault uses to deploy capital into external protocols (lending, LPing, staking) and harvest yield.
- **Autocompounding** — Harvest rewards and re‑invest to increase principal.
- **Tokenized Fund / RWA** — Off‑chain asset (e.g., T‑Bills, credit) represented on‑chain with legal/transfer‑agent plumbing.
- **Qualified Investor** — Jurisdictional eligibility required by some RWA tokens.
- **Custody** — Multisig (Safe), MPC (Fireblocks), HSMs; plus policy controls.
- **Redemption Queue** — Exit requests processed FIFO/batched (RWA norm).
- **NAV** — Net Asset Value; share price or stable NAV with interest accrual.
- **Oracle Risk** — Manipulated reference data that distorts accounting.
