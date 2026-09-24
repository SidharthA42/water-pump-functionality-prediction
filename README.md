# Water Pump Functionality Prediction

Predicting the operating condition of water pumps across Tanzania — functional, functional but needs repair, or non-functional — to support smarter maintenance planning and improve access to clean water.

## Overview

This project builds machine learning models to classify the status of ~60,000 water points across Tanzania using data on location, water quality, management structure, and technical specifications. It's based on the [DrivenData "Pump it Up: Data Mining the Water Table"](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/) competition, using data aggregated by Taarifa and the Tanzanian Ministry of Water.

Identifying which pumps are functional, which need repair, and which are non-functional helps target maintenance resources efficiently and ensures communities retain access to clean water.

## Goals

- Build multi-class classification models to predict pump status (`functional`, `functional needs repair`, `non functional`)
- Identify which factors most strongly influence pump functionality
- Create geospatial visualizations of pump distribution and condition across regions
- Deploy an interactive dashboard to communicate findings

## Dataset

- **Source**: Taarifa and the Tanzanian Ministry of Water
- **Size**: 40+ features per record, including:
  - Geographic info (coordinates, region, basin)
  - Technical specs (pump type, extraction method)
  - Management details (installer, funder, payment type)
  - Water characteristics (quality, quantity, source)
  - Temporal info (construction year, recording date)
- **Target**: `status_group` — `functional`, `functional needs repair`, `non functional`

Raw data files are not committed to this repository 

## Getting Started

### Prerequisites
- Python 3.8+
- Git

### Setup
```bash
git clone <repo-url>
cd water-pump-functionality-prediction
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Key libraries
`pandas` · `numpy` · `scikit-learn` · `matplotlib` · `seaborn` · `geopandas` · `folium` · `streamlit` · `plotly`

> **Note**: GeoPandas can be tricky to install on some systems (especially Windows). If `pip install` fails, try `conda install -c conda-forge geopandas` instead.

## Team Workflow

- **Branching**: `feature/<analysis-name>` for every ticket
- **Commits**: small, with clear messages
- **Pull requests**: mandatory peer review before merging to `main`
- **Environment**: keep `requirements.txt` up to date so everyone runs the same versions

## Evaluation Metrics

- Classification accuracy (primary)
- F1-score, precision, recall
- Confusion matrix (per-class performance)

## Team

| Name | Role |
|---|---|
| | Data preprocessing lead |
| | Modelling specialist |
| | Visualization / dashboard developer |

## Acknowledgments

- Data provided by Taarifa and the Tanzania Ministry of Water
- Project adapted from the [DrivenData](https://www.drivendata.org/) competition
