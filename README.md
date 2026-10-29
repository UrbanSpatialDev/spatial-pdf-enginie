# 🌍 Spatial PDF & Vectorization Engine (Node.js/JS)

**A pure JavaScript/Node.js module for generating true Geospatial PDFs (GeoPDF) and vectorizing spatial data without heavy C++ or GDAL dependencies.**

## 📌 About The Project
This repository houses the core PDF processing and vectorization engine extracted from a much larger, proprietary **Electron-based Desktop GIS & Spatial Analysis Suite**. 

Designed by a Senior Spatial Data Architect & Urban Planner with 26 years of field experience, the most striking feature of this system is that **it does not rely on third-party map libraries like Leaflet, Mapbox, or OpenLayers.** The entire system runs on a custom-built, Canvas-based map rendering engine written completely from scratch. It seamlessly bridges the gap between WebGIS interfaces and strict CAD/GIS desktop applications (such as QGIS, ArcGIS, and NetCAD).

## 🚀 Core Capabilities

### 1. True GeoPDF Generation (ISO 32000-1 & OGC Compliant)
- Converts live spatial data (GeoJSON, WFS, XYZ) into OGC-compliant, coordinate-aware Geospatial PDFs using pure JavaScript.
- Injects precise Affine transformation matrices and spatial metadata directly into the PDF structure.
- Preserves native geometric alignments, layer styles, and custom zoom rules from our custom rendering engine.

### 2. Smart Spatial OCR (PDF-to-Map)
- Directly reads coordinate tables from raster plans or scanned PDFs using Optical Character Recognition (OCR).
- Automatically performs coordinate transformations across different EPSG projections (e.g., local UTM to WGS84).
- Instantly renders extracted data as GIS-ready Point and Polygon geometries **on our custom map engine**.

### 3. Auto-Vectorization & Topological Node Snapping (Experimental)
- **Vectorization:** Extracts clean linework from digital (native) PDFs with near 100% accuracy using pure JS canvas pixel scanning.
- **Noise Reduction:** Applies the Douglas-Peucker algorithm to smooth out noisy or complex lines.
- **Magnetic Node Snapping:** Automatically detects and snaps loose ends within a specific tolerance to create closed, topology-ready geometries for advanced GIS intersection analysis.

## 🚧 Status
**Work in Progress (WIP) - Active Development.** 
This engine is currently being integrated and optimized within our main Desktop GIS application (which also includes advanced PostGIS integrations and spatial intersection analytics). The standalone source code, documentation, and NPM package for this specific PDF module will be published here once the system is complete.
## ⚖️ License & Usage
All intellectual property rights and the underlying methodology of this engine belong to us. You are welcome to use, study, and build upon this work in your own projects, **provided that you explicitly credit Çetin Maraşlıoğlu (UrbanSpatialDev)** as the original creator and source.
---
*Developed by Çetin Maraşlıoğlu (UrbanSpatialDev) - Senior Spatial Data Architect & Urban Planner*
