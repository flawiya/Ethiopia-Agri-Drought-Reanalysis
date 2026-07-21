# Spatio-Temporal Study of Hydro-Climatic Variability and Thermal Intensity in Ethiopia (2000 - 2025)

## 📌 Project Overview
This project identifies district-level drought hotspots across Ethiopia using 26 years of climate and vegetation data. By combining rainfall, temperature, and soil moisture indicators, the study analyzes how drought risk is evolving, with a specific focus on whether historically cooler highland farming zones are becoming more exposed to agricultural drought.

The analysis culminates in an **interactive Climate Diagnostic Dashboard** built with Python, allowing users to explore 26 years of environmental stress across Ethiopian districts.

## 🛠️ Tech Stack

### Data Processing & Analysis
| Category | Tools |
| :--- | :--- |
| **Engine** | ![Google Earth Engine](https://img.shields.io/badge/GEE-4285F4?style=flat-square&logo=google-earth&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **Analysis** | ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![GeoPandas](https://img.shields.io/badge/GeoPandas-150458?style=flat-square) ![NumPy](https://img.shields.io/badge/Numpy-013243?style=flat-square&logo=numpy&logoColor=white) |
| **Visualization** | ![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=flat-square&logo=Matplotlib&logoColor=black) ![Folium](https://img.shields.io/badge/Folium-77B829?style=flat-square&logo=folium&logoColor=white) ![hvPlot](https://img.shields.io/badge/hvPlot-HoloViz-blue?style=flat-square) |
| **Dashboard** | ![Panel](https://img.shields.io/badge/HoloViz_Panel-ED7B0E?style=flat-square) ![Bokeh](https://img.shields.io/badge/Bokeh-white?style=flat-square&logo=bokeh&logoColor=orange) |

**Data Source:** ECMWF ERA5-Land Monthly Aggregated dataset (~9km spatial resolution).

---

## 📊 Methodology & Analytical Framework

### 1. Data Extraction
Climate variables including **2m Temperature**, **Total Precipitation**, and **Volumetric Soil Water** were extracted via Google Earth Engine API. Zonal statistics were applied to Ethiopia’s ADM_2 administrative boundaries to produce district-level summaries.

### 2. Drought Stress Index (DSI)
To assess agricultural drought, the project calculates a combined index of heat and moisture stress:

$$DSI = \frac{T_{norm} + (1 - SM_{norm})}{2}$$

*   **$T_{norm}$**: Normalized temperature (Heat Demand)
*   **$SM_{norm}$**: Normalized soil moisture (Water Availability)

### 3. Spatial Imputation
To ensure 100% spatial coverage for the dashboard, missing values were handled using spatio-temporal mean imputation, filling data gaps with historical monthly averages per district.

---

## 🖥️ Dashboard Features
The interactive dashboard provides a multi-dimensional view of climate risk:
*   🌍 **Choropleth Maps:** Visualizing Temperature, Precipitation, and Warming Intensity.
*   🔥 **Critical Hotspots:** Identifying the top 10 most exposed districts per year.
*   📈 **26-Year History:** National trends for selected climate metrics from 2000 to 2025.
*   🎻 **Zone Distribution:** Comparing climatic behavior between **Arid** and **Humid** zones.

---
