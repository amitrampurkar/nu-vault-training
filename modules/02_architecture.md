# Architecture & Standards

- **Token interface**: ERC‑20 for underlying; **ERC‑4626** for vault shares and accounting.
- **Accounting**: `totalAssets()`, `convertToShares()`, `convertToAssets()` are key to UX, integrations, and safety.
- **Execution**: Strategy adapters, harvest/compound hooks, fee accrual.
- **Access control**: Roles (owner, manager, keeper), pausability, allowlists.
- **Upgrades**: Proxy pattern, timelocks, emergency withdraw.
- **Custody**: Multisig (Safe) and/or MPC (Fireblocks) for ops.

### Security fundamentals (quick list)
- CEI pattern & `ReentrancyGuard`.
- Price oracle sanity + pause on oracle failure.
- Slippage limits and withdrawal throttles.
- Invariant/property‑based testing (Echidna/Foundry) and formal audits.
