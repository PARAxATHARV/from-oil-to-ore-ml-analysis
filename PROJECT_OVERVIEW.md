# From Oil to Ore

## Machine Learning Analysis of Global Mineral Dependency

The transition to renewable energy reduces reliance on fossil fuels, but it also increases demand for critical minerals. This project investigates whether that transition shifts dependency rather than eliminating it: from oil-producing regions to a relatively small number of mineral-producing countries.

## Research question

**How concentrated is global mineral production, and what can historical production data tell us about future supply dependency?**

## Dataset

- **Source:** [Global Coal and Metal Mine Production Dataset](https://doi.org/10.5281/zenodo.6325109)
- **Coverage:** Country-level mineral production data
- **Period:** 2000–2020

The analysis combines mining, reserves, capacity, commodity, ownership, transport, and processing datasets to build a structured production dataset with country, year, material, and production fields.

## Approach

1. **Prepare the data** — merge source tables, resolve inconsistencies, remove duplicates, and create analysis-ready features.
2. **Model realistic uncertainty** — inject controlled noise and apply smoothing and clipping during cleaning.
3. **Explore production patterns** — examine distributions, country-level aggregation, trends, skewness, and concentration.
4. **Forecast production** — predict next-year production using lag features, growth rates, and encoded country and material variables. Linear Regression and Random Forest models are evaluated with RMSE and R².
5. **Identify supply structures** — standardize aggregated production data, then use K-Means clustering and PCA to reveal groups of dominant and lower-producing countries.

## Key findings

- Global mineral production is highly concentrated among a small number of countries.
- Historical production patterns show strong persistence, supporting accurate near-term forecasts.
- Clustering separates dominant producers from less influential production groups.
- The energy transition can reduce fossil-fuel dependency while creating new supply-chain exposure around critical minerals.

## Results

The supervised-learning models achieved strong predictive performance, with an R² score of approximately **0.98**. PCA visualizations and cluster analysis highlight the structural imbalance in global mineral supply.

## Technology

- Python
- Pandas and NumPy
- scikit-learn
- Matplotlib
- Jupyter / Google Colab

## Repository contents

- `Final_Group_Project_StatML_QC.ipynb` — main analysis notebook
- `open_database_mining/data/` — source datasets
- `exer1st.py` to `exer5st_SL&USL.py` — analysis exercises and supporting scripts
- `From Oil to Ore.docx` — project report

## Collaboration note

This was developed as a group academic project. Any public presentation should accurately credit collaborators and describe each person’s contribution.
