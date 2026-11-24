# Project Brief: MIMO CSI Compression

## Overview

This project studies autoencoder-based compression of multiple-input multiple-output (MIMO) channel state information (CSI) for feedback from a user equipment (UE) to a base station (gNB). It was developed as Project 22 for the Big Data for Communication course at the University of Bologna.

## Dataset

The experiments use synthetic, ray-traced CSI generated with [NVIDIA Sionna](https://nvlabs.github.io/sionna/). There are 5,000 channel realizations for each of the Munich and Bologna scenes. Each sample is an 8 × 8 complex matrix, represented by 128 real values (real and imaginary parts).

## Method

The UE encoder maps the 128 real-valued channel components to a latent vector of dimension `d`; the gNB decoder reconstructs the channel. The tested dimensions are `d ∈ {32, 16, 8}`, corresponding to dimension compression ratios of 4×, 8×, and 16×.

The project compares a dense multilayer perceptron (MLP) autoencoder and a residual 2D convolutional neural network (CNN) autoencoder against a linear principal component analysis (PCA) baseline. Models are trained with mean squared error, and reconstruction quality is evaluated using normalized mean squared error (NMSE) and complementary channel metrics.

## Deliverables

- Side-by-side heatmaps of original and reconstructed CSI magnitudes at each compression ratio.
- NMSE versus compression ratio results for the MLP, CNN, and PCA baseline.
- A comparison of the Munich and Bologna simulated scenes and an analysis of limitations.

See the [main notebook](../Project_22_MIMO_CSI_Compression.ipynb) for the workflow and [results discussion](RESULTS_AND_LIMITATIONS.md) for archived metrics and figures.
