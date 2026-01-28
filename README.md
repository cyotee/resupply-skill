# Resupply Skills Plugin

Progressive disclosure skills for the [Resupply](https://resupply.fi) CDP-based stablecoin lending protocol.

## Overview

Resupply is a DeFi protocol that enables users to borrow **reUSD** stablecoins against ERC4626 vault tokens as collateral. It integrates with Curve Lend, Frax Lend, Convex, and Yearn for yield-bearing collateral support.

This plugin provides 8 specialized skills covering all major protocol domains.

## Skills

| Skill | Trigger Phrases | Description |
|-------|-----------------|-------------|
| `resupply-architecture` | "Resupply architecture", "Core contract", "ResupplyRegistry" | Protocol overview, registry, operator pattern |
| `resupply-lending` | "ResupplyPair", "borrow reUSD", "add collateral" | Lending pairs, borrowing, interest rates |
| `resupply-liquidation` | "liquidation", "LiquidationHandler", "bad debt" | Liquidation mechanics, collateral seizure |
| `resupply-redemption` | "redemption", "redeem collateral", "redemption fees" | Collateral redemption, dynamic fees |
| `resupply-insurance` | "insurance pool", "reIP", "InsurancePool" | Insurance vault, bad debt coverage |
| `resupply-staking` | "staking RSUP", "GovStaker", "voting power" | RSUP staking, cooldowns, rewards |
| `resupply-governance` | "governance", "proposals", "Voter contract" | DAO voting, proposal execution |
| `resupply-rewards` | "rewards", "RewardHandler", "emissions" | Reward distribution, claiming |

## Installation

### Via Claude Code Plugin Manager

```bash
claude plugins add resupply
```

### Manual Installation

Clone into your plugins directory:

```bash
git clone https://github.com/cyotee/resupply-skill.git ~/.claude/plugins/resupply
```

## Usage

Once installed, skills activate automatically when you ask questions matching their trigger phrases:

```
"How does the Resupply lending system work?"
→ Activates resupply-lending skill

"Explain the liquidation process"
→ Activates resupply-liquidation skill

"How do I stake RSUP tokens?"
→ Activates resupply-staking skill
```

## Protocol Resources

- **Documentation**: https://docs.resupply.fi
- **Source Code**: https://github.com/resupplyfi/resupply
- **Contract Addresses**: See protocol documentation

## Key Concepts

### Token Architecture

- **reUSD**: Protocol stablecoin (LayerZero OFT)
- **RSUP**: Governance token
- **reIP**: Insurance pool shares

### Precision Values

```solidity
LTV_PRECISION = 1e5        // 95% = 95_000
EXCHANGE_PRECISION = 1e18  // Exchange rates
RATE_PRECISION = 1e18      // Interest rates
```

### Epoch System

- Epoch length: 1 week (604,800 seconds)
- Used for: Rewards, governance voting, staking cooldowns

## Contributing

Contributions welcome! Please submit issues and pull requests to improve these skills.

## License

MIT
