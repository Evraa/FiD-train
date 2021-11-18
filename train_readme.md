# Training gudie
In this readme we illustrate any issues that you might come up with during training.

## Multiple datasets
At first, when fetching datasets, `get-data.sh` will automatically install two different datasets (NQ and TQA),
    along with passsages extracted from wikipedia (12 GB), for memory efficient purposes, you can commnet them out in these fiels:
    `get-data.sh` and `src/preprocess.py`

## Python and Python3
Default value for calling subprocesses is `python` so if you're using updated python in your environment, make sure to update it. I already did.