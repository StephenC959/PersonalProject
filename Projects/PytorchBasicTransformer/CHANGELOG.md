# Changelog

## 2026-04-13 Transformer Tuning Session

### GPU and Training Throughput

- Confirmed CUDA-backed PyTorch was available with `torch 2.7.1+cu128` on an NVIDIA GeForce RTX 3080.
- Added CUDA diagnostics to print the active device, GPU name, CUDA runtime, model device, and AMP status.
- Added CUDA-aware `DataLoader` options:
  - `num_workers=2` when CUDA is available
  - `pin_memory=True` when CUDA is available
  - `persistent_workers=True` when using worker processes
- Added non-blocking device transfers with `to(device, non_blocking=True)`.
- Added automatic mixed precision training and evaluation with `torch.amp.autocast`.
- Added `torch.amp.GradScaler` for CUDA training.
- Changed `optimizer.zero_grad()` to `optimizer.zero_grad(set_to_none=True)`.

### Baseline Mean-Pooling ViT Tuning

- Reduced the training augmentation after stronger augmentation appeared to cap performance:
  - removed `RandomRotation`
  - removed `ColorJitter`
  - kept `RandomCrop(32, padding=4)`
  - kept `RandomHorizontalFlip`
  - reduced `RandomErasing` from `p=0.25`, `scale=(0.02, 0.12)` to `p=0.1`, `scale=(0.02, 0.08)`
- Increased model depth from `4` transformer encoder layers to `6`.
- Kept the mean-pooling baseline at:
  - `embed_dim=128`
  - `num_heads=4`
  - `mlp_dim=512`
  - `patch_size=4`
  - `dropout=0.1`
- Tested a temporary increase to `num_heads=8`, but reverted to `num_heads=4` because performance did not improve and each head became narrower.
- Increased base learning rate from `3e-4` to `5e-4`.
- Replaced the aggressive cosine decay schedule with a warmup plus logarithmic decay schedule:
  - `warmup_epochs=10`
  - `warmup_start_factor=0.2`
  - `min_lr_factor=0.5`
- Increased `AdamW` weight decay during tuning, then settled at `weight_decay=5e-3`.
- Added early stopping with `patience=10`.
- Changed checkpoint selection from best validation loss to best validation accuracy.

### CLS-Token Experiment Notebook

- Added `model_cls_token.ipynb` as a duplicate experiment notebook so CLS-token changes can be compared against the mean-pooling baseline.
- Replaced mean pooling with a learnable CLS token:
  - added `self.cls_token`
  - changed positional embedding length from `num_patches` to `num_patches + 1`
  - prepended the CLS token before the transformer encoder
  - used `x[:, 0]` as the image-level representation
- Widened the CLS-token model:
  - `embed_dim=192`
  - `num_heads=6`
  - `mlp_dim=768`
  - `depth=6`
- Added a convolutional stem before patch projection:
  - `Conv2d(in_channels, 64, kernel_size=3, padding=1)`
  - `GELU`
  - `Conv2d(64, embed_dim, kernel_size=patch_size, stride=patch_size)`
- Tested reducing `patch_size` from `4` to `2`, which increased the patch sequence from `64` to `256` tokens, but reverted back to `patch_size=4` because it was not effective enough to justify the added compute.

### Current End-of-Day State

- `model.ipynb` is the tuned mean-pooling baseline.
- `model_cls_token.ipynb` is the wider CLS-token plus convolutional-stem experiment.
- The latest patch-size experiment was reverted, so both notebooks are back to `patch_size=4`.
- Latest changes are not yet committed.
