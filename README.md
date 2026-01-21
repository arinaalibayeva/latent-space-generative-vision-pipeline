# Latent-Space Generative Vision Pipeline

This repository contains an end-to-end machine learning project that explores how structured latent representations can be learned from images and later leveraged for generative modeling. The project is built on a personal food photo archive and progresses from representation learning with autoencoders to image generation using latent diffusion models.

The primary goal is to study how different latent-space modeling choices affect reconstruction quality, semantic structure, and generative performance under realistic data and compute constraints.

---

## Project Overview

The project is organized into two stages, each building directly on the previous one:

- **Stage 1** focuses on learning and analyzing latent representations using autoencoder-based models.
- **Stage 2** extends the pipeline to latent diffusion, shifting from representation learning to image generation.

Both stages use the same underlying image dataset, allowing for direct comparison and iterative improvement.

---

## Repository Structure


- Jupyter notebooks contain the full implementation and experiments.
- PDF files provide structured explanations, analysis, and discussion of results.

---

## Stage 1: Latent Representation Learning

In the first stage, the project investigates how effectively autoencoder-based models can learn compact and meaningful latent representations of images.

Key components include:
- Convolutional Autoencoders (CAE)
- Variational Autoencoders (VAE)
- Reconstruction error analysis
- Latent space visualization using PCA
- Clustering to assess semantic structure in the learned representations

This stage focuses on understanding the strengths and limitations of autoencoders for capturing image structure, texture, and composition.

---

## Stage 2: Latent Diffusion and Image Generation

The second stage builds on the insights from Stage 1 and moves toward generative modeling.

Key components include:
- Encoding images using a pretrained Stable Diffusion VAE
- Training a denoising diffusion model (DDPM) in latent space
- UNet-based noise prediction
- LoRA fine-tuning to adapt generation with limited compute

This stage evaluates whether latent diffusion models can produce more coherent and expressive generations than autoencoder-based approaches alone.

---

## Notes on Data and Compute

- The dataset consists of a personal image archive and is not included in this repository.
- Experiments were designed to run under limited GPU availability, influencing model size and training strategy.
- All results should be interpreted in the context of these practical constraints.

---

## How to Use This Repository

Each stage can be explored independently:
1. Start with the notebook in `stage-1-latent-representation-learning` to understand representation learning and analysis.
2. Continue with `stage-2-latent-diffusion-generation` to see how the pipeline is extended to image generation.
