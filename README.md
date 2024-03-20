# MIP Automatic Partitioning

A Python implementation of a mixed integer programming (MIP) strategy to automatically partition a corpus of multilingual code-switched speech.

## Requirements

Both the conda (`environment.yml`) and pip environment (`requirements.txt`) requirements are given in this repo.

## Usage

If you would like to partition your corpus of multilingual speech into training, development and test sets utilising a set of your constraints:

1. Calculate the duration of speech each speaker utters per language combination, and store this in  `speech_per_speker_per_language.csv`. The current file represents the file we utilised to partition our own corpus as presented at LREC 2024.

```
SPEAKER_ID, LANG_1, LANG_1-LANG_2, LANG_1-LANG-3
SPEAKER_1,  1.0,    0.0,           150.3
SPEAKER_1,  10.0,   5.0,           0.0
```

2. Follow/adapt the steps in `PartitionAllocationOptimisation.ipynb`

3. The resulting training, development and test sets will be stored in `train.csv`,`dev.csv`,`test.csv` respectively.

## Further discussion

We provide all the code used to generate the figures (and some additional figures) presented in the LREC paper in `DatasetStats.ipynb`.
This notebook also provides some supplementary discussion about how multilingual the dataset under study is.

## How to cite

The work presented here appeared in the proceedings of LREC 2024, and may be cited as:

```
@inproceedings{jjvv_mip_2024,

}
```