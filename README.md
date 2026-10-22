# Exploratory Data Analysis

## Project Goal

The goal is to find out what drives property prices and what a typical listing looks
like. The notebook covers five steps:

1. **Data cleaning.** Fix the data types, remove duplicates and fill in missing values
   for bedrooms, bathrooms, lot size and house size.
2. **Data statistics.** Summarise the numeric columns and show how listings are spread
   across regions and sale statuses.
3. **Market analysis.** Compare mean prices across regions, profile the most and least
   expensive regions, and look closely at one focused market: sold properties in one
   region with sensible limits on size and price.
4. **Correlation.** Measure how price, bedrooms, bathrooms, house size and lot size
   relate to each other, using heatmaps, scatter plots, histograms and box plots.
5. **Insights.** Turn the results into plain-language findings, each linked to the
   notebook cell that produced it.

## Benefits for the User

- **Market overview at a glance.** See which regions have the most listings and which
  are the most and least expensive.
- **What drives price.** In the focused market, price follows the number of bathrooms
  more than house size or bedrooms. Lot size has almost no effect.
- **The typical home.** Shows the most common combination of bedrooms and bathrooms and
  its median price. This gives a realistic baseline for pricing or comparing listings.
- **Honest numbers.** Each finding says whether it applies to the whole dataset or only
  to the focused market. Effects caused by outliers or filled-in values are flagged, so a
  figure from the subset isn't mistaken for a national trend.
- **Reproducible and easy to run.** The data is split into small CSV files, and `requirements.txt` lists the exact package versions. Open the notebook and
  choose Restart Kernel → Run All to reproduce every chart and number.
- **A reusable template.** The same clean → describe → analyse → correlate → summarise
  steps can be applied to any other tabular dataset.
- **Safe to share.** Locations and IDs are replaced by invented codes. The price values
  are still real, though, so a determined person could match rows back to the public
  source.

## Description

This folder holds an exploratory data analysis of ~2.2M real-estate property listings
from realtor.com data (1969-2022), pseudonymised: state, city, zip code, street and broker id
are replaced by invented codes (`Region-01`…, `Region-01-City-01`…, integer ids); every
other value — price, beds, baths, lot and house size, status, sale date — is the real one.

Everything is computed from the pseudonymised dataset — nine CSV parts in `data/`.

The pipeline runs in `notebook-pseudonymised.ipynb`. 

## Folders layout
```
<this folder>/
├── README.md
├── requirements.txt                                      ← pip install -r to rebuild the venv, then run the notebook
├── data/
│   └── realtor-data-pseudonymised-part-01.csv … part-09.csv  (each < 24 MB)
├── notebook-pseudonymised.ipynb                          ← open in Jupyter; Restart Kernel → Run All
```

## Recreate the Environment

Needs Python 3.14. From this folder:

```bash
python3.14 -m venv .venv
.venv/bin/pip install -r requirements.txt
```

Then either open `notebook-pseudonymised.ipynb` in an editor that runs notebooks (e.g. VS Code
with the Jupyter extension, picking `.venv` as the kernel), or run it end to end from
the terminal:

```bash
.venv/bin/jupyter nbconvert --to notebook --execute --inplace notebook-pseudonymised.ipynb
```

The notebook reads `data/realtor-data-pseudonymised-part-*.csv` relative to its own folder,
which is where Jupyter, VS Code and `nbconvert` run it by default. On Windows use `.venv\Scripts\` in place of `.venv/bin/`.
