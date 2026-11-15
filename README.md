# ASTRO-HEROES | Marswalk Mission
NASA Space Apps Challenge 2026 · Interplanetary Survival Guide: Martian Map · Jazan

An integrated layered map that plans the safest walking route for the first astronauts on Mars, in Gale Crater / Mount Sharp, and re-plans it instantly when a hazard is reported.

- ▶ **Live demo:** https://sattam-al.github.io/marswalk-mission/
- 💻 **Full code & data:** https://github.com/Sattam-AL/marswalk-mission
- 📓 **Notebook:** `notebooks/ASTRO_HEROES_Marswalk_DEM_Ready.ipynb`

## How it works
1. NASA terrain model: MRO CTX stereo DTM (USGS Astrogeology), 20 m/pixel.
2. Slope and roughness layers → walk-cost map (slopes > 15° are no-go, 20 m safety buffer).
3. A* search finds the safest route to the science stops.
4. Reported hazards become no-go zones and the route is re-planned on site; each hazard is saved as a new map layer.

## Repository
| Folder | Contents |
|---|---|
| `notebooks/` | Colab notebook (full pipeline) |
| `engine/` | Python route engine, API, Colab cells, web game |
| `data/route_outputs/` | Planned & re-routed routes, obstacles (JSON/GeoJSON) |
| `images/` | Terrain layers: elevation, slope, roughness, walk cost |
| `docs/` | NASA sources, project details, AI disclosure |
| Pitch deck | `Space Apps Pitch Deck` (.pptx) |

## NASA data
- MRO CTX DTM T01_000815_1749_XN_05S222W__P22_009571_1756_XI_04S222W (USGS Astrogeology STAC)
- NASA Mars Trek — Gale Crater CTX mosaic
- NASA MSL Curiosity traverse (MMGIS)

## Tools
Python (NumPy, SciPy, Rasterio, PyProj, Pandas), Google Colab, FastAPI, JavaScript + Leaflet, GitHub Pages.

## AI disclosure
AI tools (Claude by Anthropic) assisted in writing the code. All terrain data comes from NASA/USGS sources; all maps were produced by our own code.

## Team
Musab · Remas · Sattam · Shahad · Yaser · Haya
