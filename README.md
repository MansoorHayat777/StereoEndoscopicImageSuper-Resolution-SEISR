# Saliency-Aware Deep Learning Approach for Enhanced Endoscopic Image Super-Resolution

This repository contains the official implementation of the methods presented in our paper "Saliency-Aware Deep Learning Approach for Enhanced Endoscopic Image Super-Resolution," currently under review.
<p align="center">
  <img src="https://github.com/MansoorHayat777/StereoEndoscopicImageSuper-Resolution-SEISR/raw/main/SEISR/Block%20Diagram.JPG" width="100%">
</p>

## Abstract
Our work introduces a novel deep learning framework tailored for endoscopic image super-resolution, with a focus on saliency-aware mechanisms to preserve and highlight critical diagnostic features in the upsampled images.
## Codes and Models

### Requirements
- **PyTorch 1.3.0, torchvision 0.4.1**: The code is tested with `python=3.7, cuda=9.0`.
- **Matlab**: For training/test data generation and performance evaluation.

### Train
- **Data Preparation**: Download the training sets from (https://endovis.grand-challenge.org) for SCARED dataset unzip this into `./data/train/`.
- **Generate Patches**: Run `./data/train/GenerateTrainingPatches.m` in Matlab to generate training patches.
- **Training**: Execute `python train.py` to start the training process. The checkpoints will be saved to `./log/`.

### Test
- **Data Preparation**: Download the full test sets the SCARED dataset, the MICCAI 2017 Kidney Boundary Detection SubChallenge; the Kidney Boundary Detection dataset, the MICCAI 2017 Robotic Instrument Segmentation Sub-Challenge; Robotic Instrument Segmentation, and the MICCAI 2019 challenge on Stereo Correspondence and Reconstruction of Endoscopic Data; Stereo Correspondence and Reconstruction from (https://endovis.grand-challenge.org) and da Vinci dataset from (https://github.com/hgfe/DCSSR) unzip them into `./data`.
- **Inference**: Run `python test.py` to perform a demo inference. The resulting images (`.png` files) will be saved in `./results`.
- **Evaluation**: Execute `evaluation.m` in Matlab to compute the PSNR and SSIM scores.

## Quantitative Results

  <p align="center">
    <img src="https://github.com/MansoorHayat777/StereoEndoscopicImageSuper-Resolution-SEISR/raw/main/SEISR/Capture.JPG" width="100%">
  </p>

## Assessment of the Visual Quality of SR Images Created Through Image Super-Resolution Techniques

- **At a $\times2$ Scale Factor on the SCARED Dataset:**
  <p align="center">
    <img src="https://github.com/MansoorHayat777/StereoEndoscopicImageSuper-Resolution-SEISR/raw/main/SEISR/scale_2.jpeg" width="100%">
  </p>

- **At a $\times4$ Scale Factor on the Robotic Instrument Segmentation Dataset:**
  <p align="center">
    <img src="https://github.com/MansoorHayat777/StereoEndoscopicImageSuper-Resolution-SEISR/raw/main/SEISR/scale_4.jpeg" width="100%">
  </p>

- **At a $\times8$ Scale Factor on the Stereo Correspondence and Reconstruction Dataset:**
  <p align="center">
    <img src="https://github.com/MansoorHayat777/StereoEndoscopicImageSuper-Resolution-SEISR/raw/main/SEISR/scale_8.jpeg" width="100%">
  </p>


