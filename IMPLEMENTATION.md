# Implementation Proof

This repo implements FSRCNN for single-image super-resolution and evaluates it against bicubic interpolation.

## Paper Concepts Mapped To Code

| Paper / concept | Where | What it proves |
| --- | --- | --- |
| Feature extraction stage | `FSRCNN` in `fsrcnn_super_resolution.ipynb` | Implements the initial convolution stage that lifts low-resolution input into feature space. |
| Shrinking / mapping / expanding | `FSRCNN` | Implements the middle FSRCNN pipeline instead of relying on a pretrained super-resolution package. |
| Deconvolution upsampling | `FSRCNN` | Learns the final upscaling operation rather than using only interpolation. |
| Patch-based dataset flow | `T91_images` and `Set5` | Builds training and evaluation datasets for high/low-resolution image pairs. |
| PSNR evaluation | evaluation cells and `skimage.metrics` | Quantifies reconstruction quality and compares against bicubic interpolation. |

## Reviewer Notes

- The key implementation evidence is the `FSRCNN` class plus the PSNR/result visualization cells.
- The notebook preserves qualitative image outputs because super-resolution quality is easier to judge visually alongside PSNR.
- The final discussion reports improvement over bicubic interpolation, which makes the implementation measurable rather than purely architectural.
