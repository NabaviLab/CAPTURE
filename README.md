# CAPTURE: A Clustered Adaptive Patchwork Technique for Unified Registration Enhancement in Biological Imaging

![Diagram](Diagram.png)
 
This repository contains the implementation of our image registration method, as described in our paper titled "CAPTURE: A Clustered Adaptive Patchwork Technique for Unified Registration Enhancement in Biological Imaging." Our method addresses one of the issues in image registration for biological datasets, which is "Distortion."

## Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Datasets](#datasets)

## Introduction

Our image registration method bridges the gap between non-linear and linear registration. We introduce a technique to consider the geometrical distortion between two images, "fixed" and "moving," in the context of image registration. Based on this information, images are divided to isolate patches. Then, by using global registration, which is effective in terms of time and computational complexity, we aim to address both global and local transformations between two images.

## Installation

To install and run this project, you will need Python 3.6 or later. Clone the repository and install the necessary requirements:

```bash
git clone https://github.com/NabaviLab/CAPTURE.git
```
To install the required libraries, run the following command in the first cell of your Google Colab/Jupyter Notebook:

```bash
!pip install opencv-python-headless numpy torch pillow scipy pandas matplotlib seaborn scikit-image psutil scikit-learn
```
This repository contains five `.ipynb` (Jupyter Notebook) files:

1. `Global_Registration.ipynb`: This file is our global features-based image registration.
2. `Extract_Information.ipynb`: This is the first step of the geometrical distortion analysis, where you can extract information using the SIFT features extractor.
3. `Geometrical_Distortion.ipynb`: In this file, you can analyze the geometrical distortion, generate heatmaps, and extract some information for the upcoming patch division.
4. `Patch_Division.ipynb`: After extracting the necessary information, use this file to divide images into different patches.
5. `Patch_Reconstruction.ipynb`: After division, use this file to reconstruct patches.

**** Important Note ****
While you can use any features-based algorithm for patch registration, we highly recommend using `Global_Registration.ipynb` for more consistency.

