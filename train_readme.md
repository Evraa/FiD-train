# Training gudie
In this readme we illustrate any issues that you might come up with during training.

## Multiple datasets
At first, when fetching datasets, `get-data.sh` will automatically install two different datasets (NQ and TQA),
    along with passsages extracted from wikipedia (12 GB), for memory efficient purposes, you can commnet them out in these fiels:
    `get-data.sh` and `src/preprocess.py`

## Python and Python3
Default value for calling subprocesses is `python` so if you're using updated python in your environment, make sure to update it. I already did.

## NQ dataset sizes
* train.json    5.6 GB
* dev.json      631 MB
* test.json     261 MB


python3 train_reader.py \
        --train_data open_domain_data/NQ/train.json \
        --eval_data  open_domain_data/NQ/dev.json \
        --model_path pretrained_models/nq_reader_base
        --model_size base \
        --per_gpu_batch_size 16 \
        --n_context 100 \
        --name my_experiment_1 \
        --checkpoint_dir checkpoint \
        --use_checkpoint \
        --lr 0.00005 \
        --optim adamw \
        --scheduler linear \
        --weight_decay 0.01 \
        --text_maxlength 250 \
        --total_step 15000 \
        --warmup_step 1000 \