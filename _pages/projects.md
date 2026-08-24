---
permalink: /projects/
title: "Projects"
author_profile: true
redirect_from:
  - /md/
  - /projects.html
---

## Data Science / Machine Learning

### Crop & Plant Image Classifier
A deep learning image classifier that recognizes 139 crop and plant species using transfer learning on a MobileNetV2 backbone. A two-phase training strategy (frozen head, then full fine-tuning) is trained on GPU with mixed precision, and the trained model is served through an interactive Streamlit web app for drag-and-drop classification.

**Tools Used:** Python, PyTorch, PyTorch Lightning, torchvision, TensorBoard, scikit-learn, Streamlit  
**Output:** 139-class classifier with top-1/top-5 accuracy, per-class classification report, confusion matrix, and a Streamlit app returning top-K predictions with confidence scores  
**GitHub:** [View Repository](https://github.com/rafimt/crop_classification)

### Crop Disease Detection
A deep learning classifier that identifies 26 crop diseases across corn, potato, rice, and wheat from leaf images, using transfer learning on a ResNet18 backbone. A stratified 70/15/15 split is built from the raw dataset, the model is trained in two phases (frozen head, then full fine-tuning) on GPU, and predictions are served through a FastAPI web service with an upload page and JSON API.

**Tools Used:** Python, PyTorch, PyTorch Lightning, torchvision, TensorBoard, scikit-learn, FastAPI, Uvicorn  
**Output:** 26-class disease classifier reaching ~77% test accuracy, with a per-class report, confusion matrix, and a web API returning top-K predictions with confidence scores  
**GitHub:** [View Repository](https://github.com/rafimt/crop-diseases-detection)

### Weather Analytics Dashboard
An end-to-end data engineering project that fetches historical weather data for 24 global megacities, stores it in a cloud PostgreSQL database (Supabase), and visualizes it in an interactive multi-page dashboard. The pipeline runs daily via GitHub Actions CI/CD.

**Tools Used:** Python, PostgreSQL, Supabase, Streamlit, Plotly, pandas, GitHub Actions, pytest, Docker  
**Output:** Live dashboard with temperature trends, monthly heatmaps, year-over-year comparisons, and anomaly detection via z-score  
**Live App:** [weather-analytics-dashboard-rafi.streamlit.app](https://weather-analytics-dashboard-rafi.streamlit.app)  
**GitHub:** [View Repository](https://github.com/rafimt/weather-analytics-dashboard)

### End-to-End Geospatial Data Pipeline
A reproducible data engineering pipeline built to learn PostGIS and Docker hands-on. Uses Denver, Colorado as the study area, ingesting real-world data from USGS, OpenStreetMap, and Google Earth Engine, then processing and loading it into a PostGIS spatial database with fully automated Python scripts.

**Tools Used:** Python, PostgreSQL, PostGIS, Docker, GDAL, GeoPandas, PDAL, Google Earth Engine, Folium, osmnx  
**Output:** Spatial database with road buffers, building height extraction, cluster analysis, land suitability scores, and an interactive Folium map  
**GitHub:** [View Repository](https://github.com/rafimt/geospatial-data-pipeline)

### Energy Timeseries EDA
Exploratory data analysis and feature engineering for household appliance energy consumption forecasting. Based on the UCI Appliances Energy Prediction dataset — 10-minute interval sensor readings from a low-energy building, resampled to hourly and enriched with lag and cyclical time features.

**Tools Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Jupyter Notebooks  
**Output:** Processed feature set with chronological train/val/test splits, fitted scalers, and EDA visualizations covering seasonality, occupancy proxies, and autocorrelation patterns  
**GitHub:** [View Repository](https://github.com/rafimt/energy-timeseries-eda)

### Credit Risk Prediction
A supervised machine learning project predicting whether loan borrowers will become seriously delinquent (90+ days overdue) within two years, using Kaggle's "Give Me Some Credit" dataset of 150,000 borrowers. Emphasizes model explainability with SHAP, essential for regulated lending environments that must justify risk decisions.

**Tools Used:** Python, scikit-learn, XGBoost, Random Forest, SHAP, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebooks  
**Output:** XGBoost model achieving 0.862 ROC-AUC, SHAP-based feature importance and waterfall plots, and the finding that payment behavior outpredicts demographics  
**GitHub:** [View Repository](https://github.com/rafimt/credit-risk)

### Customer Segmentation
An unsupervised machine learning project segmenting ~8,950 credit card customers into behavioral personas using K-Means clustering, with optimal cluster count selected via elbow method and silhouette scores, and PCA used for visualization.

**Tools Used:** Python, scikit-learn, pandas, Matplotlib, Seaborn, Jupyter Notebooks  
**Output:** Four actionable customer segments (high-value, cash-advance users, installment purchasers, low-activity accounts) with seven analytical visualizations to guide marketing, retention, and risk strategy  
**GitHub:** [View Repository](https://github.com/rafimt/customer-segmentation)

### Credit Card Fraud Detection
An end-to-end fraud detection project tackling extreme class imbalance (fraud is 0.17% of transactions) across 284,807 anonymized European cardholder transactions, with a focus on imbalance-appropriate evaluation metrics and business-driven threshold tuning.

**Tools Used:** Python, XGBoost, scikit-learn, Random Forest, Logistic Regression, Isolation Forest, pandas, Matplotlib, Seaborn, Jupyter Notebooks  
**Output:** XGBoost model reaching 0.983 ROC-AUC and 0.825 PR-AUC (77% of fraud caught at 93% precision), with 12 supporting visualizations  
**GitHub:** [View Repository](https://github.com/rafimt/credit-card-fraud-detection)

### Wildfire Analysis
This project provides a complete framework for analyzing wildfire data with focus on temporal patterns, geographical distributions, fire size analysis, and correlations between various wildfire characteristics. The analysis is specifically designed for 2022 wildfire data but can be adapted for multi-year datasets.

**Tools Used:** Python, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn  
**Output:** Statistical analysis reports  
**GitHub:** [View Repository](https://github.com/rafimt/Wildfire_Analysis_2022)

---

## Geographic Information Systems (GIS)

### Deforestation Monitoring
This project analyzes deforestation patterns in the Llanos del Yari-Yaguara II Indigenous Reserve in Colombia over a 10-year period (2016-2025) using satellite imagery and vegetation indices. The study focuses on understanding vegetation changes and identifying deforestation patterns to support informed decision-making in forest management.

**Tools Used:** QGIS, Google Earth Engine, matplotlib/seaborn, numpy, QGIS, Jupyter Notebooks  
**Output:** Deforestation maps, temporal analysis, before-after comparison, seasonal variation and land cover change  
**GitHub:** [View Repository](https://github.com/rafimt/Deforestation-Analysis)

### Cycling Coverage Assessment
Spatial analysis of cycling network accessibility in Berlin, identifying gaps between high population density areas and cycling infrastructure coverage.

**Tools Used:** Python, GeoPandas, Matplotlib, Contextily  
**Output:** Population density maps, accessibility gap identification, and cycling coverage analysis  
**GitHub:** [View Repository](https://github.com/rafimt/Maps/blob/main/notebook/continent.ipynb)

---

## Academic Research

### Project Geoinformatics
This project analyzes Land Surface Temperature (LST) patterns using Google Earth Engine (GEE). It focuses on understanding the relationship between urban land use/land cover changes and their impacts on surface temperature variations.

**Tools Used:** Python, Google Earth Engine, geemap, matplotlib/seaborn, numpy, QGIS, contextily, Jupyter Notebooks  
**Output:** Calculation of various spectral indices (NDVI, NDBI, NDWI), temporal LST changes, correlation analysis between LST and land cover types, LST patterns and thermal variations  
**GitHub:** [View Repository](https://github.com/rafimt/Project-Geoinformatics-2024)

---

## Web GIS Development

### First GeoDjango Map Application
Interactive web mapping application built using Django's geographic framework for spatial data visualization.

**Tools Used:** Django, GeoDjango, GDAL, Leaflet.js, HTML/CSS  
**Output:** Responsive web application with interactive mapping capabilities  
**GitHub:** [View Repository](https://github.com/rafimt/first_geodjango_project)

### BanglaGIS Explorer
A geospatial web application for exploring Bangladesh's administrative boundaries, letting users view districts on an interactive map, filter them live by population range, and browse summary statistics and charts. District boundaries are sourced from GADM with population data added programmatically.

**Tools Used:** Python, FastAPI, PostgreSQL, PostGIS, SQLAlchemy, GeoAlchemy2, Leaflet.js, Chart.js, Docker Compose  
**Output:** Interactive web app with multiple basemaps, live population filtering, summary stat tiles, and REST API endpoints serving filtered GeoJSON  
**GitHub:** [View Repository](https://github.com/rafimt/webgis-bd)

---

## Python Automation

### Geocoding Application
A Python GUI application that converts German addresses from Excel files into geographical coordinates (latitude and longitude) using the Nominatim geocoding service.

**Tools Used:** Python, Geocoding APIs, Pandas, Tkinter  
**Output:** Desktop/web application with batch geocoding functionality and data export features  
**GitHub:** [View Repository](https://github.com/rafimt/Geocoding-App)