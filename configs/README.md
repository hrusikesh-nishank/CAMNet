# Configuration

The notebooks read settings from `config.yaml`.

## Main sections

### data

- `image_size`: patch size for random cropping
- `batch_size`: batch size
- `num_workers`: reserved (not used directly in the notebooks)

### train

- `epochs`: training epochs
- `lr`: learning rate
- `mixed_precision`: enable mixed precision training if `true`
- `reduce_lr_patience`, `reduce_lr_factor`, `reduce_lr_min_delta`: ReduceLROnPlateau settings

### model

- `num_rrg`, `num_mrb`, `channels`: backbone configuration

### cam

Used by CAMNet notebook:

- `enabled`: enables CAM module logic
- `num_heads`: number of attention heads
- `key_dim_div`: key dimension divisor (key_dim = channels / key_dim_div)
- `pooled`: whether to pool keys/values
- `pool_stride`: stride used for pooling in CAM
