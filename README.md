# Interactive Map of Fast-Charging Policy Simulation

This repository hosts an interactive Leaflet map that visualizes the spatial redistribution of DC fast-charging demand in Beijing under different pricing policies. Each bubble represents a public fast-charging station, with bubble size and color reflecting its simulated station-choice probability under the selected policy scenario.

## Current data (2026-10-15)

The map covers 667 public stations from 3,808 choice events (91,963 event-alternative rows), with a baseline and six policy scenarios. A station's displayed share is its summed choice probability divided by the total across stations in the selected scenario. It is not an energy-weighted share. Probabilities come from the saved formal policy results; no model or policy was re-estimated for this update. Existing station locations and contextual layers are retained. See `data/provenance.json` for input and output checksums.

## Run locally

From this directory, run `python -m http.server 8765`, then open http://localhost:8765 in a browser. Opening index.html directly as a local file may block data loading. Leaflet is loaded from unpkg.com and requires an internet connection. The remaining assets are included in this directory.
