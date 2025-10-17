# Security Playbook for Vaults

**Threats**: reentrancy, inflation attacks (share mis‑pricing), oracle manipulation, upgrade misuse, access control misconfig, MEV.

**Controls**
- Patterns: checks‑effects‑interactions, pull‑payments, circuit‑breakers.
- Libraries: OpenZeppelin `ReentrancyGuard`, vetted ERC‑4626 base.
- Testing: fuzz/property tests for share accounting invariants; differential tests for strategies; static analysis: Slither; symbolic: Mythril; fuzz: Echidna/Foundry.
- Process: Plan → Code → Test → **Audit** → Fix → Monitor (bug bounties, on‑chain monitors).

**Runbook**
1) Pre‑deploy checklist
2) Emergency pause & withdrawals
3) Incident comms template
4) Post‑mortem template
