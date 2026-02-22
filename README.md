# PentaSwap V2

Redesigned swap interface for Pentagon Games ecosystem with RainbowKit wallet integration.

**Live:** http://136.116.225.232/swap/

## Features

- RainbowKit wallet connection (MetaMask, WalletConnect, Coinbase, etc.)
- Pentagon Chain auto-configured
- Purple/gold Thai royalty theme
- Token selector with game tokens

## Stack

- React + TypeScript (Vite)
- RainbowKit + wagmi + viem
- TailwindCSS-inspired styling

## Contract Addresses (Pentagon Chain Mainnet)

| Contract | Address |
|----------|---------|
| Factory | `0xC75C7E9352bC1475d7c308E65C0a21969DcEdEe7` |
| Router | `0x60b70E46178CEf34E71B61BDE2E79bbB7bA41706` |
| WPC | `0xAA3d9411DD08FDA149d4545089e241E62EE87860` |

## Related Repositories (V1 Stack)

| Repo | Description | Stack |
|------|-------------|-------|
| [swapfive_web](https://github.com/blockchainsuperheroes/swapfive_web) | V1 swap frontend | React (CRA) |
| [pentaswap-sdk](https://github.com/blockchainsuperheroes/pentaswap-sdk) | Swap SDK (Uniswap V2 fork) | TypeScript |
| [pen-wallet-backend](https://github.com/blockchainsuperheroes/pen-wallet-backend) | Wallet API backend | Django/Python |
| [PG-wallet-Frontend-react-native](https://github.com/blockchainsuperheroes/PG-wallet-Frontend-react-native) | Mobile wallet app (calls swap API) | React Native |

## API Integration

The mobile wallet app calls the swap backend at `https://wallet.pentagon.games`:

```
GET  /wallet/swap_chains              — Supported chains
GET  /wallet/swap_chain/tokens/<id>   — Tokens for chain
POST /wallet/swap_path/<chain_id>     — Get swap routing path
```

## Development

```bash
cd pentaswap-v2-react
npm install
npm run dev
```

## Build & Deploy

```bash
npm run build
# Upload dist/* to web server
```

## Deployment

Currently hosted on ATS server (136.116.225.232) at `/swap/` path.

## Legal

- [Privacy Policy](privacy-policy.html)
- [Terms of Service](terms-of-service.html)
- [Disclaimer](disclaimer.html)

## Security

🛡️ **Audited by CertiK:** https://skynet.certik.com/projects/pentagon-games

---

*Pentagon Games Ecosystem — In-game rewards only*
