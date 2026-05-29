# context-compactor-v2

Next-generation text compression Cloudflare Worker — improved algorithms for fleet context management.

## What This Gives You

- **Smarter compression** — enhanced extractive and abstractive strategies over v1
- **Cloudflare Worker** — edge-deployed, sub-millisecond cold start
- **KV-backed caching** — avoids redundant compression on repeated inputs
- **Fleet-native** — exposes `/vessel.json` for automatic fleet discovery

## Quick Start

```bash
wrangler deploy

# Compress text
curl -X POST https://context-compactor-v2.<your-subdomain>.workers.dev/api/compact \
  -H "Content-Type: application/json" \
  -d '{"text": "Long document...", "strategy": "extractive", "ratio": 0.3}'
```

## How It Fits

A Cocapn Fleet vessel. Successor to [context-compactor](https://github.com/SuperInstance/context-compactor).

Related repos:
- [context-lattice](https://github.com/SuperInstance/context-lattice) — context window orchestration
- [context-recycler](https://github.com/SuperInstance/context-recycler) — recycled context reuse
- [cocapn-shells](https://github.com/SuperInstance/cocapn-shells) — fleet shell infrastructure

## License

Apache 2.0
