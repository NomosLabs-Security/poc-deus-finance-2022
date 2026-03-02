# Deus Finance Solidly TWAP Oracle Manipulation — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-deus-finance-2022
cd poc-deus-finance-2022
forge install foundry-rs/forge-std --no-git
forge test -vvvv
```

## Details

- **Exploit Date:** 2022-04-28
- **Fork Block:** N/A (simplified simulation)
- **Expected Output:** TWAP oracle manipulation enabling over-borrowing against inflated collateral value
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/deus-finance-2022)

## Description

Deus Finance used a Solidly DEX TWAP oracle with a short observation window for DEI stablecoin pricing. The attacker manipulated the DEI/USDC pair across multiple blocks to shift the TWAP, then borrowed against undervalued DEI collateral.

## Key Contracts

- `src/Exploit.sol` — Vulnerable lending with manipulable TWAP oracle
- `test/Exploit.t.sol` — Foundry test demonstrating the exploit

## License

MIT — For educational use only.
