# Shenkottai CF Service Area Mapper — Leaflet edition

This version replaces Google Maps with OpenStreetMap tiles displayed through Leaflet. No Google Maps API key is required and there is no Google Maps Platform API usage charge.

## Included
- CF-1 automatically linked to NC-1 (Ayikudi)
- CF-2 automatically linked to NC-2 (Achamputhur)
- CF-3 automatically linked to NC-3 (Shenkottai)
- Localities transcribed from `Shenkottai Area.xlsx`
- Draw, edit and delete polygon boundaries
- Area calculation using Turf.js
- Place/move the three NC markers
- Optional CRW allocation per coverage locality
- Browser print dialog for Save as PDF
- JSON backup and restore
- Browser local storage

## Run
1. Extract this ZIP.
2. Open a terminal in the extracted folder.
3. Run `python -m http.server 8000`
4. Open `http://localhost:8000`
5. Use the polygon icon in the map's upper-left corner to draw a boundary. Select the correct NC and locality first.
6. Use the edit icon to adjust saved polygons. Export JSON regularly.

No API key is needed. The app loads Leaflet, Leaflet.draw and Turf.js from public CDNs and map tiles from OpenStreetMap. Internet access is needed to load these libraries and map tiles.

## Important
- OpenStreetMap is a map data project, not an unlimited hosted tile service. Follow the tile usage policy: https://operations.osmfoundation.org/policies/tiles/
- No API usage fee is charged by OpenStreetMap for ordinary use of its public standard tile service, but it has usage limits and is not a guaranteed production hosting service. For heavy/official deployment, choose a suitable tile provider or host tiles yourself.
- Area is calculated from the drawn polygon, not from official land records. Boundaries must be verified against authoritative revenue / Panchayat GIS data.
- NC marker positions must be placed manually at the actual centre locations.
- CRW assignments are blank until entered by the user.
- Data is stored only in this browser on this device. Use Export JSON for backup; local storage is not shared across staff/devices.
- PDF export uses browser Print. Choose "Save as PDF". Browser print output may not include map tiles depending on print settings/browser.
- The Excel workbook contains coverage names and NC groupings, not coordinates. No boundaries or exact centre coordinates have been fabricated.
