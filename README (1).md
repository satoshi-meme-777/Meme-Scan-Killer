# MemeScan

Free, open-source scanner for micro-cap meme coins (default: under $5k market cap).
Pure static HTML/CSS/JS. No build step, no API key, no backend.

Data comes from the public [DexScreener API](https://docs.dexscreener.com/api/reference).

## Features

- Scan Solana, Base, Ethereum, BNB Chain, or all chains
- Filters: min liquidity, max market cap, name/symbol search
- Sort by newest, liquidity, 24h volume, market cap, 24h change
- Basic red-flag badges (very low liquidity, thin liquidity vs market cap, brand new pair, no website)
- Dark and light themes (follows your system setting, remembers your choice)
- Optional 60s auto-refresh
- All API data is rendered with `textContent` and links are validated, so token metadata can't inject HTML or scripts

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy to GitHub Pages

1. Create a repo (for example `meme-scanner`) and push these files.
2. Settings → Pages → Deploy from branch → `main` / root.
3. Edit the `CONFIG` block at the top of the script in `index.html`:
   - `REPO_URL`: your repository link
   - `DONATION_ADDRESS`: your own Solana address (or remove the donation panel)

## Disclaimer

Micro-cap tokens are extremely high risk, and many are scams. This tool displays market data only
and does not verify contracts, ownership, or liquidity locks. Not financial advice. Do your own research.

## License

MIT. See [LICENSE](LICENSE).
