# Kauaʻi Surf Dashboard — Canonical Version

## Canonical file

**`kauai-surf-live-dashboard.html`** is the single source of truth for the live Kauaʻi surf dashboard. It merges the best from all previous variants.

## What’s in it

- **V1 surf rating** (from `kauai-surf-report-live-dashboard-V1.html`): Per-spot swell direction (`swellOptMin`/`swellOptMax`), offshore wind (`offshoreWindMin`/`offshoreWindMax`), ideal height (`idealHMin`/`idealHMax`), with `angleDiff`, `swellDirScore`, `windScore`, `heightScore`, `periodScore`. Formula: `swellTotal×0.55 + windScore×0.35 + 5` → 1–10. Best decision-maker for “good waves or not.”
- **8 breaks**: Hanalei Bay, Tunnels (Makua), Cannons (Haʻena), Anahola Bay, Kealia Beach, Kalapaki Beach, Shipwreck (Mahaʻulepu), PK’s / Centers (Poipu). Each has `tideStation` (NOAA: north 1611683, south/east 1611400).
- **Real NOAA tide** in the modal via `fetchTide(spot.tideStation)`.
- **Swell compass** in the modal (direction arrow).
- **Wave cross-section** and **bathymetry profile** (from full dashboard).
- **Face + Hawaiian** wave heights and **color scale** legend (1–3 Poor, 4–5 Fair, 6–7 Good, 8–10 Epic).
- **NWS** via `forecastGridData`; **footer**: Phoenix Studios, data credits, GitHub link.

## Other dashboard files

- `kauai-surf-report-live-dashboard-V1.html` — Original 4-spot dashboard with V1 rating; logic merged into canonical.
- `kauai-surf-report-live-dashboard.html` — 4-spot report variant; superseded by canonical.
- `kauai-surf-live-dashboard-1.3.html` — Skeleton / UI ideas only; not runnable as-is.
- `live-kauai-conditions.html` — 4-spot conditions page (different layout); links to canonical dashboard for “Full 8-break dashboard.”

## Links

- From **index.html**: “Live Kauai Surf Ratings” → `./kauai-surf-live-dashboard.html`
- From **live-kauai-conditions.html**: “Full 8-break dashboard” → `./kauai-surf-live-dashboard.html`
