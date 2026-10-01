# Broadway Corridor Massing Tool — Vancouver

A single-file, browser-based tool for testing building massing on any Vancouver lot against the Broadway Plan and the City's zoning schedules, with up to 1 km of surrounding buildings, streets, parks and zoning drawn as a clay-model 3D diagram.

**Live page (after enabling GitHub Pages):** `https://josephtong86.github.io/Broadway-Visualizer/`

## What it does
- Look up any civic address; the lot, neighbouring buildings (extruded to measured heights), parks, street centrelines and zoning districts load from City of Vancouver Open Data.
- Assemble a site from several parcels by clicking lots, typing addresses, or adding all adjacent lots.
- Shape a podium-and-tower proposal; see site area, height, floor area and FSR update live, with a program/use mix readout (homes and jobs estimates).
- Test the site under its existing district or a proposed one (R3, R4, R5, C-2, C-3A, Broadway Plan CD-1 archetypes, custom), size the massing to an FSR cap, and compare before/after envelopes.
- Inspect any lot for its district, permitted uses and what pre-zoning or the plan changes; inspect any building to check or correct its height.
- Overlays: pre-zoned R3/R4/R5 districts extruded to their storey caps, indicative Broadway Plan height and FSR tiers, and per-building allowable envelopes.
- Perspective, axonometric, plan and equinox-shadow views; Ctrl+Z / Ctrl+Shift+Z undo and redo.

## Running it
Open `index.html` directly in Chrome, Edge, Firefox or Safari, or serve it from GitHub Pages. Everything runs in the browser; the only network calls are to `opendata.vancouver.ca`. Three.js loads from cdnjs.

## Data sources
- City of Vancouver Open Data: property addresses, property parcel polygons, building footprints 2015 (outlines), building footprints 2009 (LiDAR-derived heights, joined to the 2015 outlines by centroid), public streets, parks, zoning districts and labels.

## Caveats
- Building heights date from the 2009 LiDAR flight; buildings constructed since appear at a flagged 8 m placeholder unless corrected in the inspector (corrections are stored in the browser).
- The Broadway Plan tiers are a geometric approximation by distance to stations and to Broadway, not the plan's official sub-area polygons, which the City publishes only as PDF maps.
- District height, FSR and permitted-use values are condensed from the district schedules for planning-level testing; confirm against the by-law text and the current plan before relying on them. View cones, tower separation, solar-access and tenure rules are not modelled.
