# EDA notebook — synthetic realtor.com listings

This folder holds an exploratory data analysis of ~2.2M synthetic real-estate property
listings modelled on realtor.com data (1969-2022).

The pipeline runs in `notebook-synthetic.ipynb`. Everything is computed from the
**synthetic** dataset — nine CSV parts in `data/`.

## Layout

```
<this folder>/
├── notebook-synthetic.ipynb     ← open in Jupyter; Restart Kernel → Run All
├── requirements.txt             ← pip install -r to rebuild the venv, then run the notebook
├── README.md
├── data/
│   └── realtor-data-synthetic-part-01.csv … part-09.csv   (each < 24 MB → uploadable)
```


