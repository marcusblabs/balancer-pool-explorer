# Balancer Pool Explorer

A single-file pool explorer for Balancer v2 and v3 pools across every supported chain, with filters, a CSV export, and a 24h yield breakdown (swap fees, token yield, CoW AMM surplus).

Data comes from Balancer's public GraphQL API (`https://api-v3.balancer.fi/`). No backend, no build step, no API keys.

## Features

- Live pool data across all supported chains
- Filter by chain, pool type, protocol version, hook presence, and minimum TVL
- Sortable columns: TVL, Volume 24h, Fees 24h, Yield APR, Usage (Vol/TVL), Holders, etc.
- Aggregate header stats that update with every filter change
- 24h yield breakdown matching Balancer's frontend: **Swap Fees**, **Yield**, **Surplus**
- Hides BLACK_LISTED pools and deprecated pool types (LBP, Investment, Element, Linear) by default — same as the official Balancer frontend
- CSV export of the currently filtered pools
- Responsive layout for phone, tablet, and desktop

## Run locally

Just open `index.html` in a browser, or serve the directory:

```bash
python3 -m http.server 8080
# then open http://localhost:8080/
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). This repo is set up for GitHub Pages from the `main` branch root.
