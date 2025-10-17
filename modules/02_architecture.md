
# Architecture & Design

## Components
- **Vault (4626)**: accounting + hooks.
- **Strategy Adapters**: encapsulate external protocol logic; rate‑limited.
- **Keeper/Harvester**: automation.
- **Access Control**: `OWNER`, `MANAGER`, `KEEPER`, `GUARDIAN`.
- **Upgrade Path**: proxy + timelock + emergency pause.
- **Custody**: Safe multisig / Fireblocks MPC; policy engine (who/when/how).

## Invariants
- `convertToAssets(convertToShares(a)) ≈ a` (rounding aside).
- `totalAssets()` equals external balances + accrued rewards.
- For autocompounders, share price should be monotonic barring loss/fees.

## UX/Gas
- Use `preview` for estimates; batch calls.
- Provide `maxSlippageBps` on integrations where relevant.
