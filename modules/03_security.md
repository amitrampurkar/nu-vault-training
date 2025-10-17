
# Security Playbook

**Threats**: reentrancy, share inflation, oracle manipulation, access misconfig, upgrade backdoors, MEV around harvests.

**Controls**
- Vetted ERC‑4626 base, `ReentrancyGuard`, CEI.
- Property/fuzz tests on share math; differential tests for strategies.
- Upgrade **timelock**, multi‑sig approvals, emergency **pause**.
- External audits + continuous static/dynamic analysis.
- Harvest throttles, profit lockups, deposit caps.

**Incident Response**
Detect → Pause → Communicate → Patch + independent review → Post‑mortem.
