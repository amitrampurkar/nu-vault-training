
# Vaults 101 (ERC‑4626 Primer)

## What problem does ERC‑4626 solve?
DeFi had many bespoke “vault” interfaces. **ERC‑4626** standardizes the accounting API so wallets, UIs, and integrators can reason about deposits/withdrawals consistently.

### Core Functions (mental model)
- `deposit(assets, receiver)` → mints shares for exact assets provided.
- `mint(shares, receiver)` → takes as many assets as needed to mint shares.
- `withdraw(assets, receiver, owner)` → burns shares to return exact assets.
- `redeem(shares, receiver, owner)` → returns assets owed for shares.
- `totalAssets()` → canonical accounting view of asset backing.
- `convertToShares()` / `convertToAssets()` → price discovery.
- `preview*()` → simulate results without state changes.

### Journeys
1. **Deposit** → receive shares → share value tracks growth.
2. **Harvest** (keeper) → claim rewards → reinvest → APY increases.
3. **Withdraw** → burn shares → receive underlying + yield.

### Enhancements
- Pausable, allowlists (KYC), fee modules, upgrade proxies, caps.
