# finetune-transformer-lm
Code and model for the paper "Improving Language Understanding by Generative Pre-Training"

Before running this code, you need to:
1. `pip install -r requirements.txt`. If you lack a GPU, see `requirements.txt` for necessary modifications
2.  `python -m spacy download en`
3. Export the "val set" and "test set" from the ROC stories corpus (see below) as CSV files 
    with the default filenames and place them in a `data` subdirectory under this repository.

Currently this code implements the ROCStories Cloze Test result reported in the paper by running:
`python train.py --dataset rocstories --desc rocstories --submit --analysis --data_dir [path to data here]`

Note: The code is currently non-deterministic due to various GPU ops. The median accuracy of 10 runs with this codebase (using default hyperparameters) is 85.8% - slightly lower than the reported single run of 86.5% from the paper. 

The ROCStories dataset can be downloaded from the associated [website](http://cs.rochester.edu/nlp/rocstories/).
