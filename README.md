# FSRCNN Image Super-Resolution in PyTorch

Portfolio project by `@pkim02`.

## Project Goal

A PyTorch implementation of FSRCNN for single-image super-resolution, comparing learned reconstruction against bicubic interpolation.

## Notebooks

- `fsrcnn_super_resolution.ipynb`: FSRCNN Image Super-Resolution in PyTorch

## What I Implemented

- FSRCNN feature extraction, shrinking, mapping, expanding, and deconvolution stages.
- Patch-based training workflow for super-resolution.
- PSNR-based evaluation using scikit-image metrics.
- Qualitative comparison of low-resolution, bicubic, model output, and ground-truth images.

## Results

The final run improved PSNR over training and produced visual comparisons against bicubic interpolation.

The notebooks keep most executed outputs so reviewers can inspect the results directly on GitHub. Full reproduction may require downloading the referenced public datasets or pretrained weights.

## How To Run

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Open the notebook listed above and run cells in order. GPU is optional for review, but recommended for rerunning training-heavy experiments.

## Citations

- Accelerating the Super-Resolution Convolutional Neural Network: https://arxiv.org/abs/1608.00367
- scikit-image metrics: https://scikit-image.org/docs/stable/api/skimage.metrics.html

## Copyright And Data Note

This repository contains a cleaned portfolio version of my own implementation work. Assignment prompts, submission metadata, personal identifiers, and course-provided local figures were removed. The MIT license applies only to the code and documentation in this repository. Papers, datasets, pretrained weights, and any third-party libraries or assets keep their original licenses and terms.
