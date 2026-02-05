# Dataset Subsets (Download + Structure)

This project uses curated subsets of paired low-light (input) and well-exposed (ground truth) images.
Download the subsets from Google Drive and provide the dataset folder path to the notebooks.

## Download Link (Google Drive)

```text
https://drive.google.com/drive/folders/18smkSEl6DAauFUqkHaq0P6pMcdl3iXae?usp=sharing
```

## Folder Names in the Drive Package

After downloading, you will see these dataset folders:

* `lol`
* `fivek`
* `velol_l_subset`
* `loli_street_subset`

Each dataset folder contains `train/`, `val/`, and `test/` splits with `low/` and `high/` subfolders.

## Required Folder Structure (inside each dataset folder)

Example (`lol`):

<pre class="overflow-visible! px-0!" data-start="875" data-end="972"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(var(--sticky-padding-top)+9*var(--spacing))]"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-text"><span><span>lol/
  train/
    low/
    high/
  val/
    low/
    high/
  test/
    low/
    high/
</span></span></code></div></div></pre>

Important:

* Filenames must match between `low/` and `high/`.

  Example:

  * `train/low/0001.png`
  * `train/high/0001.png`

## How to Use in the Notebooks

When the notebook asks for `DATA_ROOT`, provide the path to ONE dataset folder, for example:

* `.../lol`
* `.../fivek`
* `.../velol_l_subset`
* `.../loli_street_subset`

## Original Dataset References (for citation)

LOL dataset:

* Wei et al., 2018: [https://arxiv.org/abs/1808.04560](https://arxiv.org/abs/1808.04560?utm_source=chatgpt.com)

MIT-Adobe FiveK:

* Official dataset page: [https://groups.csail.mit.edu/graphics/fivek_dataset/](https://groups.csail.mit.edu/graphics/fivek_dataset/?utm_source=chatgpt.com)

VE-LOL (VE-LOL-L subset derived from this dataset):

* Project page: [https://flyywh.github.io/IJCV2021LowLight_VELOL/](https://flyywh.github.io/IJCV2021LowLight_VELOL/?utm_source=chatgpt.com)

LoLI-Street:

* Paper (Islam et al., ACCV 2024):

  [https://openaccess.thecvf.com/content/ACCV2024/papers/Islam_LoLI-Street_Benchmarking_Low-light_Image_Enhancement_and_Beyond_ACCV_2024_paper.pdf](https://openaccess.thecvf.com/content/ACCV2024/papers/Islam_LoLI-Street_Benchmarking_Low-light_Image_Enhancement_and_Beyond_ACCV_2024_paper.pdf?utm_source=chatgpt.com)
* Reference implementation repo (TriFuse):

  [https://github.com/tanvirnwu/TriFuse_ACCV_2024](https://github.com/tanvirnwu/TriFuse_ACCV_2024?utm_source=chatgpt.com)
