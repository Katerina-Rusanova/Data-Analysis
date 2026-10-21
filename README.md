# EDA notebook — synthetic realtor.com listings

This folder holds an exploratory data analysis of ~2.2M synthetic real-estate property
listings modelled on realtor.com data (1969-2022). The pipeline runs in
`notebook-synthetic.ipynb`: clean the data (dtypes, duplicates, missing values), inspect
column statistics, compare sold vs. not-sold pricing, look at bedroom/bath counts and
acreage, then answer the questions in each markdown heading. Everything is computed from
the **synthetic** dataset — nine CSV parts in `data/` (sliced from the > 100 MB whole
file precisely so each part stays under GitHub's per-file limit; the parts *are* the
dataset, there is no regeneration step here). Each column was resampled with replacement
from its own distribution per region and every region label is invented (`Region-01`…
`Region-56`), so statistics copied from the original dataset's notebook will not hold —
re-derive them from these files instead of trusting old numbers.

## Layout

```
<this folder>/
├── notebook-synthetic.ipynb     ← open in Jupyter; Restart Kernel → Run All
├── requirements.txt             ← pip install -r to rebuild the venv, then run the notebook
├── README.md
├── data/
│   └── realtor-data-synthetic-part-01.csv … part-09.csv   (each < 24 MB → uploadable)
```


