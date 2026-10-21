# Data Analysis

## Exploratory Data Analysis notebook

This folder holds an exploratory data analysis of ~2.2M synthetic real-estate property
listings modelled on realtor.com data (1969-2022).

Everything is computed from the **synthetic** dataset — nine CSV parts in `data/`.

The pipeline runs in `notebook-synthetic.ipynb`. 

## Folders layout
```
<this folder>/
├── README.md
├── requirements.txt                                      ← pip install -r to rebuild the venv, then run the notebook
├── data/
│   └── realtor-data-synthetic-part-01.csv … part-09.csv  (each < 24 MB)
├── notebook-synthetic.ipynb                              ← open in Jupyter; Restart Kernel → Run All
```
