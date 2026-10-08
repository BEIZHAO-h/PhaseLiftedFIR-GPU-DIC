# PhaseLiftedFIR GPU-DIC

CUDA-accelerated two-dimensional digital image correlation centered on phase-lifted finite-impulse-response (FIR) interpolation.

## Overview

PhaseLiftedFIR GPU-DIC is a GPU implementation for pointwise displacement measurement in grayscale image sequences. Its main contribution is a phase-lifted FIR interpolation path designed for efficient subpixel image evaluation within an affine inverse-compositional DIC workflow.

The project also contains two reference interpolation paths:

- **Phase-lifted FIR interpolation** — the primary method of this project;
- Direct texture interpolation — a simple reference path;
- Cubic B-spline interpolation — a smooth reference path.

The reference paths share the same measurement framework and are provided for controlled comparison and compatibility. They are not the primary focus of this repository.

## Key capabilities

- CUDA-accelerated 2D DIC on NVIDIA GPUs;
- pointwise displacement estimation from image sequences;
- affine inverse-compositional iterative refinement;
- subpixel interpolation through the phase-lifted FIR path;
- displacement-gradient and strain-related output fields;
- convergence, iteration, quality, and status information;
- binary and CSV result export.

## Input and output

The solver accepts a folder of grayscale reference and target images together with a binary region-of-interest (ROI) mask. It estimates displacement at the nonzero mask points and writes run settings, summary information, and optional frame-level results.

Input images must have identical dimensions. The first image in filename order is used as the reference image, and the remaining images are processed as target frames.

## Project status

This public repository currently serves as the project landing page. The complete source code is maintained in a private development repository and will be released with a versioned tag after the associated manuscript has been accepted.

Until then, this page provides the project description and release information. It does not contain the CUDA implementation or the experimental datasets.

## Planned source release

The source release is planned to include:

- the CUDA solver implementation;
- Windows build instructions and project files;
- the phase-lifted FIR configuration;
- the direct and cubic B-spline reference configurations;
- small example image sets and ROI masks;
- output-format and reproducibility documentation;
- license and third-party notices.

## Citation

A versioned software release and citation information will be added when the source code becomes publicly available. Before that release, please refer to this repository as the project page for PhaseLiftedFIR GPU-DIC.

## License

The planned source release will use the MIT License and will include the complete license text and third-party notices.
