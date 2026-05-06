# GeoImage Viewer 🛰

A browser-based geospatial viewer for GeoTIFF rasters and Shapefiles — no server required, runs entirely in the browser.

## Features

- **Load GeoTIFF / Cloud-Optimized GeoTIFF (COG)**
  - Drag & drop or browse local files (`.tif`, `.tiff`)
  - Stream remote COGs directly from a URL
- **Load Shapefiles**
  - Drag & drop `.zip` (containing `.shp` + `.dbf`) or individual `.shp` + `.dbf` files
- **Raster visualization**
  - Multi-band RGB composite or single-band with colormaps (Viridis, Plasma, Jet, Gray, etc.)
  - Interactive stretch min/max controls
  - Per-layer opacity
- **Vector styling**
  - Stroke color, fill color, fill opacity, line width, layer opacity
  - Feature attribute popup on click
- **Basemaps** — Satellite (Esri), Hybrid, OpenStreetMap, None
- **Layout / Cartographic tools** (Layout tab)
  - Coordinate reference frame with draggable scope, tick marks and lat/lon labels
  - Grid lines (dashed, solid, or cross style)
  - North arrow (Classic, Triangle, Compass) with size & color controls
  - Scale bar with unit (km / mi / m), segments, colors
  - Legend with editable layer names
  - Text annotations (drag, double-click to edit)
  - Fit & Lock to layer extent
- **Project save/load** — save the full map state (layers, styling, layout) as a `.json` file and reload it later

## Usage

Open `index.html` in any modern browser — no installation or build step needed.

```
open index.html
```

For COG streaming, serve from a web server that sends CORS headers, or use a public COG URL.

## File Support

| Format | How to load |
|--------|-------------|
| GeoTIFF / COG | Drag & drop file, or paste URL |
| Shapefile | Drag & drop `.zip` (shp + dbf inside), or drop `.shp` + `.dbf` together |

## Technology

- [Leaflet](https://leafletjs.com/) — map rendering
- [GeoTIFF.js](https://geotiffjs.github.io/) + [georaster](https://github.com/GeoTIFF/georaster) + [georaster-layer-for-leaflet](https://github.com/GeoTIFF/georaster-layer-for-leaflet) — raster support
- [shpjs](https://github.com/calvinmetcalf/shapefile-js) — shapefile parsing
- [proj4js](https://github.com/proj4js/proj4js) — coordinate reprojection

## Author

Akkarapon Chaiyana · [akkarapon.c@nie.edu.sg](mailto:akkarapon.c@nie.edu.sg)
