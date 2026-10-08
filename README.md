# PhaseLiftedFIR GPU-DIC

CUDA-accelerated two-dimensional digital image correlation with phase-lifted finite-impulse-response (FIR) interpolation.

## Features

- GPU-accelerated pointwise 2D DIC for grayscale image sequences;
- phase-lifted FIR interpolation for subpixel image evaluation;
- affine inverse-compositional iterative refinement;
- displacement-gradient and strain-related outputs;
- convergence, correlation-quality, iteration, and status fields;
- binary and CSV result export.

Direct texture and cubic B-spline interpolation are also available as reference paths within the same measurement framework.

## Input

The solver uses:

- a folder containing grayscale reference and target images;
- a binary region-of-interest (ROI) mask.

All images must have identical dimensions. The first image in filename order is treated as the reference image, and the remaining images are processed as target frames. Nonzero pixels in the ROI mask define the points of interest.

## Output

A run produces a result directory containing the run settings and summary information. Optional frame-level displacement, gradient, strain, quality, convergence, iteration, and status data can be written in binary or CSV format.

## Source availability

The source release is in preparation. This repository currently contains the project description; the CUDA implementation and example data will be added in a subsequent version.

## Citation

A versioned release and citation information will be provided with the source distribution.

## License

MIT License. See [LICENSE](LICENSE) for the license text.
