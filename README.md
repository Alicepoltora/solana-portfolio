# Solana Portfolio

DeBank-style portfolio tracker for Solana. Single-file static web app (`index.html`), no build step required.

## Features
- Connect Wallet (Phantom / Solflare / Backpack)
- SOL + SPL token balances (incl. Token-2022) with live USD pricing via Jupiter
- Native staking positions
- NFT grid (optional, requires a free Helius API key)
- DeFi positions section (optional, requires a Birdeye API key — beta)

## Configuration
Click the gear icon in the app to set:
- RPC endpoint (defaults to public Solana RPC — swap in your own Alchemy/Helius endpoint for reliability)
- Helius API key (NFTs)
- Birdeye API key (DeFi positions)

Keys are stored only in your browser's `localStorage`.

## Run locally
```
python3 -m http.server 8420
```
Then open `http://localhost:8420`.

## Deployment
Served on the project server via a systemd unit (`solana-portfolio.service`) running `python3 -m http.server` on port 8420, independent of any other services already running on the box.
