# Global Corporate GHG Emissions: Interactive Engineering Pipeline
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)

## 🎯 Project Overview
This project transforms raw corporate emissions data (2022-2023) into an interactive analytical dashboard. The focus was on building a robust **Data Engineering Pipeline** that handles real-world data "noise" and prepares features for predictive modeling.

## 🛠️ Data Engineering Pipeline (ETL)
The core of this repository is a modular pipeline designed for memory efficiency (optimized for 4GB RAM environments):

1. **Extraction**: Automated discovery of datasets using `os.walk` for environment-agnostic execution.
2. **Transformation**: 
   - Standardized 20+ disparate column names.
   - Handled missing data via **Sector-Median Imputation** (restoring 12.6% of missing revenue records).
   - Engineered `total_ghg_emissions` and `carbon_intensity` metrics.
3. **Normalization**: Scaled features using Min-Max Normalization to prepare the dataset for Machine Learning.
4. **Loading**: Exported to `.parquet` format for high-speed I/O and reduced memory footprint.

## 📊 Key Insights & Visualizations
Utilizing **Plotly Express**, I developed a "Tableau-style" interactive suite:
- **Global Hotspots**: A choropleth map identifying high-emission corporate hubs (USA, China, South Africa).
- **Sector Intensity**: Analysis revealing that while Energy has the highest volume, Utilities often lead in intensity per dollar.
- **Logarithmic Drill-down**: A scatter plot mapping Revenue vs. Emissions to identify "Greenwashing" outliers.

## 🚀 How to Run
1. Clone the repo.
2. Ensure `pandas`, `plotly`, and `pyarrow` are installed.
3. Run the main pipeline script to generate `processed_emissions.parquet`.

## 📜 License
This project is licensed under the MIT License.
