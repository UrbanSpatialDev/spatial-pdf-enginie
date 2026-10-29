# 🌍 Spatial PDF & Vectorization Engine (Node.js/JS)

**A high-performance spatial processing engine designed for true Geospatial PDF (GeoPDF) generation, optical coordinate reading, and auto-vectorization—built entirely without heavy C++ or GDAL dependencies.**

## 📌 Architecture & Design Philosophy
This repository outlines the core architecture of a proprietary **Electron-based Desktop GIS & Spatial Analysis Suite**. 

Designed by **Çetin Maraşlıoğlu (UrbanSpatialDev)** with 26 years of field and planning experience, this system breaks away from standard browser rendering limits. Instead of relying on third-party map libraries (like Leaflet or Mapbox), it runs on a **custom-built, Canvas-based map rendering engine** engineered from scratch to handle strict CAD/GIS data flows, local metric projections, and topological node snapping seamlessly.

---

## ⚙️ Core Modules & Integration Blueprint

While the full proprietary source code (including advanced Affine transformation matrices, Y-axis normalization, and native UTM projection engines) remains private, this repository serves as the public architectural specification and integration blueprint.

### 1. GeoPDF Generation Pipeline (`geopdfManager.js`)
- **Objective:** Translates live spatial datasets (GeoJSON, WFS, XYZ) into ISO 32000-1 and OGC-compliant GeoPDFs.
- **Methodology:** Injects spatial metadata, coordinate boundaries, and custom rendering styles directly into the document structure, ensuring zero geometric loss when exported from the desktop canvas.

### 2. Smart Spatial OCR & Point Extraction (`pdfPointReader.js`)
- **Objective:** Parses raster plans and scanned PDFs to extract coordinate tables and spatial markers.
- **Methodology:** Utilizes custom OCR text-reading panels that remain active during multi-pafta workflows, instantly projecting extracted points as GIS-ready geometries onto the map canvas.

### 3. Auto-Vectorization & Topological Node Snapping
- **Objective:** Converts digital vector PDF linework into clean, queryable GIS layers.
- **Methodology:** Combines pure JS canvas pixel scanning, noise reduction via the **Douglas-Peucker algorithm**, and magnetic node snapping to automatically close gaps and prepare data for advanced PostGIS spatial intersection analytics.

---

## 🚀 Coming Soon: UrbanSpatial Web (SaaS)
We are currently developing a cloud-powered SaaS web interface (`UrbanSpatial Web`) allowing users to execute GeoPDF generation, spatial OCR, and coordinate transformations directly via browser without any desktop installation.

---

## 🔌 Integration & Collaboration
This engine is built for enterprise environments requiring strict data sovereignty and high-speed local GIS processing without external cloud dependencies. 

If you are an international engineering firm, consulting agency, or technology partner looking to license this engine, integrate our custom GIS desktop modules, or commission bespoke spatial solutions, feel free to reach out via our professional network.

## ⚖️ License & Usage
All intellectual property rights, proprietary algorithms, and the underlying methodology of this engine belong exclusively to the author. 

You are welcome to study and review this architectural overview, **provided that you explicitly credit Çetin Maraşlıoğlu (UrbanSpatialDev)** as the original creator and source for any derived concepts.

---
*Developed by Çetin Maraşlıoğlu (UrbanSpatialDev) - Senior Spatial Data Architect & Urban Planner*
