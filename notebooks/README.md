# Notebooks

- `1_baseline_train_or_infer.ipynb`Baseline model: multi-scale restoration backbone with conventional DAU.
- `2_camnet_train_or_infer.ipynb`
  CAMNet: same backbone with a Cross-Attention Mixer (CAM) inside the DAU.

## Dataset input

Both notebooks ask for `DATA_ROOT` and expect this structure inside that folder:

```text
<DATA_ROOT>/
  train/low, train/high
  val/low,   val/high
  test/low,  test/high
```

## Modes

Inside each notebook:

* `MODE = "train"` trains from scratch
* `MODE = "pretrained"` loads a SavedModel (CAMNet notebook)
