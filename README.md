# Arbitrum // Ecosystem

An interactive map of the ArbitrumDAO ecosystem: who owns what, who does what, and how the money has moved.

**Live site:** https://xerxes-openclaw.github.io/arbitrum-ecosystem-map/

Made by [zeptimus](https://forum.arbitrum.foundation/t/zeptimus-delegate-communication-thread/28328).

## Pages

| Page | What it shows |
|---|---|
| `index.html` | The live map: DAO at the center, the AAEs around it, what each one does. Drag nodes, zoom, toggle "Show people". |
| `entity.html?e=<key>` | Per-entity detail: role, budget, people, full proposal history (keys: `dao`, `foundation`, `offchain`, `opco`, `entropy`, `atmc`, `agv`, `oat`, `securitycouncil`). |
| `history.html` | The full record: year-by-year P&L, funding ledger, delegate leaderboard. |

## Data

All data lives in `research/*.json`, loaded at page load. Every figure is sourced from its forum proposal and checked against Snapshot + Tally. Sources are linked inline.

- `what_they_do.json` — each entity's workstreams (single source for map bubbles + entity pages)
- `proposals_history.json` — per-entity proposal history, newest first
- `people.json` — 50 deduped people with roles
- `active_initiatives.json` — live workstreams
- `layout.json` — the default map layout (node positions + zoom)

## Deploy

Hosted on GitHub Pages, deployed from the `main` branch root. **Push to `main` and it's live** in about a minute. No build step — it's plain static HTML/JS/JSON.

To run locally:

```
python -m http.server 8000
```

then open http://localhost:8000
