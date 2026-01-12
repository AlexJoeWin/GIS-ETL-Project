# 🌍 GIS-ETL Mini Project – Building Density Analysis for Upper Austria

This project demonstrates a **simple GIS-ETL pipeline** using **Python (GeoPandas)** and **QGIS**.  
The goal is to calculate and visualize the **number of buildings per administrative unit** (Katastralgemeinden) based on **OpenStreetMap data** and **data by the State of Upper Austria** (Katastralgemeindegrenzen OÖ - generalisiert, Stand: 01.04.2025).

---

## 📌 Project Goals


- Load and process cadastral municipality boundary data of Upper Austria
- Load and process OpenStreetMap building data
- Make sure all layers use to the same CRS
- Perform spatial join in order to assign each building in Upper Austria to a cadastral municipality
- Remove buildings outside Upper Austria, calculate building counts per polygon and join building counts back to cadastral municipality geometries
- Plot building density and inspect municipalities with the highest building counts
- Export final dataset as a GeoPackage (.gpkg)
- Ready for use in QGIS for final visualization and PDF file export

---

## 🧰 Technologies Used

- **Python geopandas**
- **QGIS 3.40.14-Bratislava**
- **Data Sources**
  - Austrian wide building data (OpenStreetMap by Geofabrik, https://download.geofabrik.de/europe/austria.html, December 2025)
  - cadastral municipality boundaries (OpenData by the State of Upper Austria, https://e-gov.ooe.gv.at/at.gv.ooe.ogd2-citi/#/detail/f0f85138-8b38-42aa-ba1e-ddabf18e6ae0, December 2025)
> Note: This repository intentionally excludes large geospatial datasets. Please download the required data separately and place them in the designated target folders before running the notebook.
---
## 📂 Project Structure
```

gis_project/ 
├── gis_project.ipynb 
├── data/ 
│ ├── raw/
│ │ ├── buildings/ 			# folder for OSM building data
│ │ ├── kg/ 				# folder for administrative boundary data
│ └── output/ 				# output files
├── README.md
├── LICENSE
└── .gitignore

```
---

## 📊 Output Files
- kg_building_density.gpkg (Jupyter Notebook)
- gis_project.qgz (QGIS)
- Katastralgemeinden_OÖ_202504.pdf (QGIS)

---

## ⚠️ Project Scope & Limitations

This project was created **for learning and demonstration purposes**.

For more advanced or production-level analysis, the underlying **project parameters and assumptions** would need to be defined in greater detail.  For example:

- What exactly qualifies as a *building* in OpenStreetMap?
- Which buildings should be included or excluded? etc.
