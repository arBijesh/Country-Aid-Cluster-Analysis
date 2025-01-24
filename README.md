# Country Aid Cluster Analysis

This project uses unsupervised machine learning techniques, including PCA and K-Means clustering, to classify countries into developed, developing, and underdeveloped categories. The goal is to identify countries that may require financial aid based on various socio-economic indicators.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methods](#methods)
- [Insights](#insights)
- [Requirements](#requirements)
- [How to Use](#how-to-use)
- [Visualizations](#visualizations)
- [Deployment](#deployment)
- [Acknowledgments](#acknowledgments)

---

## Overview
This project analyzes country-level data, including metrics such as child mortality, GDP, income, and life expectancy, to understand global development patterns. Using dimensionality reduction and clustering, countries are grouped into three categories:
1. Developed
2. Developing
3. Underdeveloped

## Dataset
The dataset contains the following columns:
- **country**: Name of the country
- **child_mort**: Death of children under 5 years of age per 1000 live births
- **exports**: Exports as a percentage of GDP per capita
- **health**: Health spending as a percentage of GDP per capita
- **imports**: Imports as a percentage of GDP per capita
- **income**: Net income per person
- **inflation**: Annual growth rate of the total GDP
- **life_expec**: Average life expectancy
- **total_fer**: Average number of children per woman
- **gdpp**: GDP per capita

## Methods
1. **Data Preprocessing**:
   - Handled outliers using IQR-based capping.
   - Standardized data using `StandardScaler`.

2. **Dimensionality Reduction**:
   - Used Principal Component Analysis (PCA) to reduce features while retaining ~95% variance.

3. **Clustering**:
   - Applied K-Means clustering.
   - Determined optimal `k` using Elbow Method and Silhouette Analysis.
   - Categorized countries into three groups:
     - Developed
     - Developing
     - Underdeveloped

4. **Business Insights**:
   - Explored correlations between socio-economic factors.
   - Visualized country classifications on a world map.

## Insights
- **Developed Countries**: High GDP, income, and life expectancy, with low child mortality and fertility rates.
- **Developing Countries**: Moderate values for most socio-economic indicators.
- **Underdeveloped Countries**: Low GDP and income, high child mortality, and high fertility rates.

## Requirements
Install the required libraries using:
```bash
pip install -r requirements.txt
