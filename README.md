# Malaysia Unemployment Analysis (1991–2022)

End-to-end data analysis project exploring Malaysia's unemployment trends, employment sector shifts, the relationship with GDP and also Malaysia's economy changes during Covid period.

## About the Project

This project analyses 30 years of employment and GDP data for Malaysia using a public Kaggle dataset (183 countries, 1991–2022). I built a clean data pipeline and performed EDA + economic analysis, with separate views for the full period (1991–2022) and the recent 10 years (2012–2022) to better understand COVID effects.

## Notebooks

- **01_data_ingestion.ipynb** – Data loading, validation, checksum, metadata, and clean processed files.
- **02_eda.ipynb** – Exploratory data analysis, trends, distributions, sector changes, and pre/post-COVID comparison (both full and 10-year views).
- **03_economic_analysis.ipynb** – Okun’s Law testing (with and without 1-year lag), regression, ASEAN comparison, and simple forecast.

## Key Findings
- Unemployment rate increased noticeably after COVID (pre-COVID average ~3.3%, post-COVID ~4.4%).
- Services sector has remained very stable (~60–62% of employment) and continues to be the main source of labour market resilience.
- Malaysia maintains one of the lower unemployment rates among ASEAN countries (2010–2022 average).

## Key Findings for OKUN's Law
- Okun’s Law direction is consistent with economic theory: higher GDP growth is associated with lower unemployment (negative slope).
- However, the relationship is weak:
   1.Without lag: Slope = -0.002, R² = 0.002, p-value = 0.805 (not statistically significant)
   2.With 1-year lag: Slope = -0.009, R² = 0.047, p-value = 0.248 (still not significant at 5% level)

## Policy Notes

Based on the analysis, maintaining GDP growth above 5% annually would help keep unemployment low. Continued focus on services sector development and youth reskilling would support long-term stability.

## Tech Stack

- Python 3
- pandas, numpy
- matplotlib, seaborn
- scipy, scikit-learn

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook

Run notebooks in order: 01 → 02 → 03.

Dataset
Kaggle – Global Jobs, GDP and Unemployment Data (1991–2022)
https://www.kaggle.com/datasets/akshatsharma2/global-jobs-gdp-and-unemployment-data-19912022

Limitations 
This dataset contains general unemployment rate (not youth 15–24 specific).

Malaysia-Unemployment Project 2.0 concept
can replace with official DOSM monthly youth unemployment data for deeper analysis.