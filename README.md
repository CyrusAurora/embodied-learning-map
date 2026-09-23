# Embodied AI Learning Map

Cyrus Embodied AI learning map — a Three.js / 3d-force-graph knowledge graph for Month1 Embodied Expert (Path3 dense cards). **Course is locked to Embodied-AI-Guide** (not a parallel curriculum).

## Open locally

Serve this directory as static files (browser needs CDN + `data/graph.json`; do not open via `file://`):

```bash
python3 -m http.server 8765
```

Then open <http://localhost:8765/>.

## Production

Public site will be served via **Cloudflare Pages** (not GitHub Pages). Attach this repo as the Pages source; root is the site root (`index.html`).

## Layout

| Path | Role |
|------|------|
| `index.html` | Force-directed graph UI |
| `data/graph.json` | Nodes + edges (`done` / `learning` / `pushed` / `parked`) |
| `data/daily/` | Daily learning deposits (`YYYY-MM-DD.json` + `index.json`) |
| `guide-curriculum.md` | Guide curriculum notes |
| `progress-log.md` | Progress log |
| `x-embodied-watchlist.json` | Public X handles watchlist |

## Daily deposits

1. Add `data/daily/YYYY-MM-DD.json` (learning + digest).
2. Prepend the date in `data/daily/index.json`.
3. Update `data/graph.json` as needed; refresh the site.
