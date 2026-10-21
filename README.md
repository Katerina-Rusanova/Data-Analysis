# Data Analysis

## Description

This folder holds an exploratory data analysis of ~2.2M pseudonymised real-estate property
listings modelled on realtor.com data (1969-2022), computed from the **pseudonymised** dataset — nine CSV parts in `data/`.

The pipeline runs in `notebook-pseudonymised.ipynb`. 

## Folders layout
```
<this folder>/
├── README.md
├── requirements.txt                                          ← pip install -r to rebuild the venv, then run the notebook
├── data/
│   └── realtor-data-pseudonymised-part-01.csv … part-09.csv  (each < 24 MB)
├── notebook-pseudonymised.ipynb                              ← open in Jupyter; Restart Kernel → Run All
```
