# Adversarial Attacks on GANs for Medical Image Synthesis

This project investigates how adversarial data poisoning affects GAN training in the context of medical image generation (MRI). Specifically, we simulate black-box attacks (e.g., tumor injection, Gaussian noise) on GAN training data and evaluate the impact on image quality. Defense strategies such as MedGAN-based inpainting and noise detection are also implemented and assessed.

---

## Table of Contents

- [Project Description](#project-description)
- [Key Features](#key-features)
- [Datasets](#datasets)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Data Processing Pipeline](#data-processing-pipeline)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Notebook Descriptions](#notebook-descriptions)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

---

## Project Description

We explore how adversarial data poisoning—through imperceptible modifications like fake tumor insertion or Gaussian noise—can degrade the performance of GANs in medical imaging tasks. Our experiments are conducted on axial brain MRI slices using multiple GAN models (DCGAN, LSGAN, WGAN-GP). We simulate attacks on the training data and assess the GANs' output quality under these scenarios. In response, we also experiment with defense mechanisms such as image restoration using MedGAN and attack detection models.

---

## Key Features

✅ **Black-box adversarial data poisoning simulation**  
✅ **Training GANs on clean vs. poisoned datasets**  
✅ **Defense pipeline using MedGAN-based inpainting**  
✅ **Quantitative evaluation with FID, SSIM, LPIPS**  
✅ **Tumor/noise attack detection with classification model**  
✅ **Modular Jupyter Notebooks for reproducibility**  

---

## Datasets

We use publicly available and preprocessed axial brain MRI datasets:

- 🧠 **Clean MRI dataset**  
  [Axial MRI Normal Dataset](https://www.kaggle.com/datasets/v38nguynvit/axial-mri-norm/data)  
  - Skull-stripped, grayscale, resized MRI slices.  
  - Used as the baseline training data.

- 💣 **Tumor attack dataset**  
  [Tumor Injection Attack Dataset](https://www.kaggle.com/datasets/v38nguynvit/tumor-mri-attack)  
  - Subset of clean training data with synthetic tumors injected to simulate malicious poisoning.

- 💥 **Gaussian noise attack dataset**  
  [Gaussian Noise Attack Dataset](https://www.kaggle.com/datasets/v38nguynvit/gaussian-noise-attack)  
  - Subset of training images with low-variance Gaussian noise added.

---

## System Requirements

- Python 3.10+
- CUDA-enabled GPU (recommended: P100)

---

## Installation

```bash
git clone https://github.com/your-org/adversarial-mri-gan.git
