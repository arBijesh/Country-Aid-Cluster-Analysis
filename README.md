# HELP International: Country Categorization for Strategic Aid Allocation
### Application Link: https://country-aid-cluster-analysis-h.streamlit.app/
## Problem Statement

### Objective:
To categorize the countries using socio-economic and health factors that determine the overall development of the country.

### About the Organization:
HELP International is an international humanitarian NGO that is committed to fighting poverty and providing the people of backward countries with basic amenities and relief during times of disasters and natural calamities.

### Problem Statement:
HELP International has successfully raised around **$10 million**. Now, the CEO of the NGO needs to decide how to use this money strategically and effectively. 

The CEO must make a decision to choose the countries that are in the direst need of aid. 

#### Your Role:
As a Data Scientist, your job is to:
1. Categorize the countries using socio-economic and health factors that determine their overall development.
2. Suggest the countries which the CEO should focus on the most.

---

## Application Link
Explore the interactive application here: [Country Aid Cluster Analysis](https://country-aid-cluster-analysis-h.streamlit.app/)

---

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
This project leverages unsupervised learning techniques, such as PCA and K-Means clustering, to analyze socio-economic and health data of countries. By grouping countries into developed, developing, and underdeveloped categories, this project aims to help HELP International allocate funds effectively to countries that require aid the most.

## Dataset
The dataset includes the following columns:
- **`country`**: Name of the country.
- **`child_mort`**: Death of children under 5 years of age per 1000 live births.
- **`exports`**: Exports as a percentage of GDP per capita.
- **`health`**: Health spending as a percentage of GDP per capita.
- **`imports`**: Imports as a percentage of GDP per capita.
- **`income`**: Net income per person.
- **`inflation`**: Annual growth rate of the GDP.
- **`life_expec`**: Average life expectancy.
- **`total_fer`**: Average number of children per woman.
- **`gdpp`**: GDP per capita.

---

## Methods
1. **Data Preprocessing**:
   - Outlier handling using IQR-based capping.
   - Standardizing data using `StandardScaler`.

2. **Dimensionality Reduction**:
   - Applied PCA to reduce dimensionality while retaining ~95% variance.

3. **Clustering**:
   - Used K-Means to cluster countries.
   - Determined optimal `k` using Elbow and Silhouette methods.

4. **Insights and Business Recommendations**:
   - Provided actionable insights to guide aid allocation decisions.

---

## Insights
- **Underdeveloped Countries**:
  - High child mortality, inflation, and fertility rates.
  - Low GDP, income, and life expectancy.

- **Developing Countries**:
  - Moderate levels of all socio-economic indicators.

- **Developed Countries**:
  - High GDP, income, and life expectancy with low child mortality and fertility rates.

---
