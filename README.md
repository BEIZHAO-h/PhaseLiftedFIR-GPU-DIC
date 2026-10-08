# PhaseLiftedFIR GPU-DIC

**High-accuracy and computationally efficient 2D digital image correlation using CUDA-accelerated phase-lifted FIR texture sampling.**

> **Release status:** The source code and example datasets will be made publicly available upon acceptance of the associated paper.

## Overview

PhaseLiftedFIR GPU-DIC is a CUDA-accelerated implementation of two-dimensional digital image correlation (2D-DIC) for full-field displacement and strain measurement.

The core method introduces a **phase-lifted finite impulse response (FIR) texture representation** to improve the efficiency of subpixel intensity reconstruction. Instead of performing high-quality reconstruction repeatedly during DIC iterations, a fixed 10-tap half-phase FIR filter preconstructs intensity samples at half-integer pixel positions. These samples are interleaved with the original image intensities to form a texture at twice the original spatial resolution. Subsequent subpixel intensity evaluation requires only **a single hardware bilinear texture query**.

This approach substantially reduces repeated reconstruction costs while maintaining high-quality subpixel measurement performance.

## Key Features

- **Phase-lifted FIR texture representation** for efficient subpixel intensity sampling.
- **FIR-aligned reference gradients** for consistent target-image reconstruction and reference-side linearization.
- **CUDA-accelerated 2D-DIC** for high-resolution images and dense full-field measurement.
- **Reference implementations** of direct texture interpolation and cubic B-spline interpolation within the same GPU-DIC framework.

## Development Environment

The implementation has been developed, compiled, and tested in the following environment:

| Component         | Configuration                           |
| ----------------- | --------------------------------------- |
| Operating system  | Windows 11 Home                         |
| GPU               | NVIDIA GeForce RTX 5060 Laptop GPU      |
| CUDA Toolkit      | 12.8.93                                 |
| CUDA architecture | `sm_120`                                |
| Build tools       | Visual Studio 2022 Build Tools 17.14.35 |
| Compiler          | MSVC 14.44.35207                        |
| OpenCV            | 4.10.0                                  |

## Source Code

The CUDA implementation, build instructions, and example datasets will be released in this repository upon acceptance of the associated paper.

## Citation

Citation information for the associated paper and software will be provided when the source code is released.

## License

MIT License. See [LICENSE](LICENSE) for details.
