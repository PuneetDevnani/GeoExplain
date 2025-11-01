# 🌊 GeoExplain: Interpretable Geospatial ML for Urban Flood Risk

**Author:** Puneet Devnani  
*M.Tech – Artificial Intelligence & Data Science, VIT Bhopal*

---

## 🚀 Overview

**GeoExplain** integrates **Machine Learning**, **Explainable AI (SHAP)**, and **Spatial Statistics** to predict and interpret **urban flood risk**.  
The framework identifies high-risk flood zones and explains their causes through interpretable geospatial modeling.

The complete, end-to-end workflow — including preprocessing, model training, SHAP explainability, and hotspot detection — is contained in a single Jupyter notebook:  
👉 **[View GeoExplain1.ipynb](https://github.com/PuneetDevnani/GeoExplain/blob/main/notebooks/GeoExplain1.ipynb)**


---

## 📂 Project Structure

```
GeoExplain/
│
├── data/          → geospatial grids and processed parquet files  
├── models/        → trained model artifacts (.pkl)  
├── maps/          → final maps and analytical visuals  
├── notebooks/     → main notebook (GeoExplain1.ipynb)  
├── dashboard/     → optional Streamlit app (interactive visualization)  
├── README.md      → project documentation  
├── requirements.txt → dependencies list  
├── LICENSE  
└── .gitignore
```

---

## 📊 Results Summary

| Metric | Value | Description |
|:--------|:------:|-------------|
| **Grid Cells** | 1,530 | 1-km² cells covering Mumbai region |
| **Moran’s I (Smoothed Flood Rate)** | 0.4074 *(p = 0.0010)* | Indicates strong spatial clustering |
| **Hotspot Analysis (Gi\*)** | 259 Hotspots / 251 Coldspots | 510 statistically significant zones |
| **AUC (Ensemble)** | 0.7016 | Predictive strength of ensemble model |
| **Accuracy (Ensemble)** | 0.6319 | On 50,000-row subset of 1.1M dataset |
| **Mean Neighbors per Cell** | 7.69 | Spatial connectivity measure |

---

## 📈 Key Highlights

- **XGBoost + Random Forest Ensemble** for flood prediction  
- **SHAP Explainability** to interpret model outputs  
- **Getis–Ord Gi\*** for hotspot detection  
- **Moran’s I** for spatial autocorrelation analysis  
- **Interactive Folium maps** for visualizing risk zones  
- Entire pipeline in **one reproducible notebook**

---

---
## 📘 Dataset Source

The base dataset used for GeoExplain was sourced from Kaggle, titled:
flood.csv 
👉 **[Download flood.csv](https://www.kaggle.com/datasets/naiyakhalid/flood-prediction-dataset/data)**

mumbai_grid.parquet – base geospatial grid

mumbai_grid_enhanced_v2.parquet – feature-enhanced dataset

mumbai_grid_enhanced_with_probs.parquet – model probability outputs

mumbai_grid_enhanced_with_ensemble_probs.parquet – ensemble risk map

Note: Only a 50,000-row subset of the full dataset was used during model prototyping due to computational limits.
---

## ▶️ Run the Notebook

You can reproduce all results by opening the notebook locally:

```bash
jupyter notebook notebooks/GeoExplain1.ipynb
```

or view it directly on GitHub / nbviewer after upload.

---

## ⚙️ Requirements

Install dependencies once using:

```bash
pip install -r requirements.txt
```

**Main Libraries:**  
`geopandas`, `xgboost`, `shap`, `scikit-learn`,  
`folium`, `libpysal`, `esda`, `matplotlib`, `pandas`

---

## 📜 License

MIT License © 2025 **Puneet Devnani**  
Software is provided **“AS IS”**, without warranty of any kind.

---

## 🌍 Vision

The next phase of **GeoExplain** aims to build a fully interpretable and deployable GeoAI system with:
- **Causal Inference** (DoWhy) for intervention modeling  
- **Real-time Streamlit Dashboard** for urban flood monitoring  
- **Scalable geospatial pipelines** for smart city planning  

---

