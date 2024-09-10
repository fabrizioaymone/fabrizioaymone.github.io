---
layout: page
title: "Efficient AI on RISC-V: TFLite Micro Analysis"
description: Performance analysis of TFLite Micro on RISC-V architecture
img: assets/img/riscv-tflite.png
importance: 3
category: university
---
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/riscv-tflite.png" title="RISC-V and TFLite" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Introduction
<p align="justify">
This project explores the deployment of TensorFlow Lite for Microcontrollers (TFLite Micro) on RISC-V architectures. The project focuses on benchmarking MLCommons Tiny models using Spike and Gem5 simulators to evaluate performance on RISC-V 32 implementations. Key performance metrics like CPI and branch mispredictions are investigated, particularly comparing in-order and out-of-order core designs.
</p>

### Key Topics
- **RISC-V Architecture**: Open-source and customizable for specific machine learning tasks.
- **TFLite Micro**: TensorFlow Lite for Microcontrollers used for edge AI inference.
- **MLCommons Tiny Benchmark**: Standard benchmark for TinyML tasks.
- **Simulators**: Spike and Gem5 used for RISC-V simulation and performance analysis.
- **Core Design**: Comparison between in-order vs. out-of-order core designs.

## Repository Structure
- `/models/`: MLCommons-Tiny benchmark models in TFLite and their C byte array versions.
- `/cc/`: Source code for cross-compiling the TFLite Micro API for RISC-V 32-bit.
- `/elf/`: Cross-compiled ELFs for Gem5 simulation.
- `/spike/`: Source code and cross-compiled ELFs for Spike simulation.
- `/results/`: Profiling data from Gem5 simulations.
- `/paper/`: Full project paper in PDF.
- `/scripts/`: Python scripts for configuring RISCV cores for Gem5 simulations.

## Getting Started

### Prerequisites
Ensure the following are installed before running the code:
- **Spike Simulator**: RISC-V ISA simulator with proxy kernel. [Instructions](https://github.com/riscv/riscv-isa-sim).
- **RISC-V 32-bit Cross-Compiler**: For compiling RISC-V 32-bit targets. [Instructions](https://github.com/riscv/riscv-gnu-toolchain).
- **Gem5 Simulator**: Modular platform for system architecture research. [Instructions](https://www.gem5.org/documentation/).
- **TFLite Micro**: TensorFlow Lite for Microcontrollers. [Setup Instructions](https://www.tensorflow.org/lite/microcontrollers).

### Code Usage
To compile the `.a` TFLite-micro static library, modify the Makefile in the TFLite-micro repository by updating the compiler flags with `riscv-gnu-toolchain`. Follow the steps outlined in the Makefile and download the necessary external libraries (e.g., flatbuffers, gemmlowp).

For Spike and Gem5 simulations, refer to the Makefile and details in the project paper.
