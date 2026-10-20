# Data Analysis

This repository holds an **Exploratory Data Analysis** (EDA) of a real-estate listings dataset
from realtor.com (≈2.2 M rows, 12 columns, covering listings from 1969–2022),
run end-to-end in Notebook/notebook-synthetic.ipynb:
  * clean data (dtypes, duplicates, missing values)
  * summarize column statistics
  * analyze each regional market
  * examine correlations and distributions
  * and finish with written insights.

To keep the analysis reproducible while guaranteeing that no row can be traced to a real record,
the pipeline runs on a synthetic dataset (realtor-data-synthetic.csv, regenerated deterministically
by generate_synthetic.py, seed 20261020) that preserves the original schema, per-column missing-value counts,
and per-region row counts but resamples every column's values from its own empirical distribution —
region and city labels are invented (Region-XX with Region-XX-City-YY cities), and joint structure (correlations)
is destroyed by that resampling, so the §4/§5 claims must be re-derived from the synthetic file.
