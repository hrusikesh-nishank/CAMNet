# CAMNet (Project): Cross-Attention Mixer for Low-Light Image Enhancement

This repository contains a minimal implementation of:

1. A baseline: multi-scale restoration backbone with a conventional dual-attention unit (DAU)
2. CAMNet: the same backbone with a Cross-Attention Mixer (CAM) integrated inside the DAU

The project is organized as notebooks with a Conda GPU environment, a small configuration file, dataset subset links, and a pretrained model link.

## Folder Structure

- `environment.yml` : Conda environment (GPU)
- `configs/config.yaml` : training and model configuration
- `notebooks/` :
  - `1_baseline_train_or_infer.ipynb`
  - `2_camnet_train_or_infer.ipynb`
- `data/README.md` : dataset subset download + folder structure
- `pretrained/README.md` : pretrained model download + usage
- `results/` : optional outputs (kept empty in the repo)

## Setup (Conda, GPU)

```bash
conda env create -f environment.yml
conda activate camnet
jupyter notebook
```

## Data

Download the subset datasets and follow the folder structure instructions:

- `data/README.md`

## Running

Open one notebook at a time:

- Baseline: `notebooks/1_baseline_train_or_infer.ipynb`
- CAMNet: `notebooks/2_camnet_train_or_infer.ipynb`

Inside each notebook:

- Set `MODE = "train"` to train from scratch
- Set `MODE = "pretrained"` to load a saved model (CAMNet notebook)

Both notebooks prompt for:

- `DATA_ROOT` (path to a dataset folder such as `lol`, `fivek`, `velol_l_subset`, or `loli_street_subset`)

## Configuration

Edit: `configs/config.yaml`

Key sections:

- `data`: `image_size`, `batch_size`
- `train`: `epochs`, `lr`, `mixed_precision`, ReduceLROnPlateau settings
- `model`: backbone depth and width (`num_rrg`, `num_mrb`, `channels`)
- `cam`: CAM settings (`num_heads`, `pooled`, `pool_stride`, etc.)

## References

Baseline architecture reference:

- Zamir et al., 2020 (multi-stage progressive image restoration): [https://arxiv.org/abs/2003.06792](https://arxiv.org/abs/2003.06792)

Dataset references:

- See `data/README.md`
