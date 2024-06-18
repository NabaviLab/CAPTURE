# CAPTURE: A Clustered Adaptive Patchwork Technique for Unified Registration Enhancement in Biological Imaging
 
This repository contains the implementation of our image registration method, as described in our paper titled "CAPTURE: A Clustered Adaptive Patchwork Technique for Unified Registration Enhancement in Biological Imaging". Our method address on of the issues in the image registration for the biology dataset, which is "Distortion".

## Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Datasets](#datasets)

## Introduction

Our image registration method bridge the gap between non-linear registration and linear registration. We introduce a method in order to consider the geometrical ldistortion between two images "fixed" and "moving" in the context of the image registration, and based on the information divided images to isolate the patches. Then by using the global registration, which is effective in the case of the time and computational complexity, we aim to address both global and local transaformation between two images.

## Installation

To install and run this project, you will need Python 3.6 or later. Clone the repository and install the necessary requirements:

```bash
[git clone https://github.com/NabaviLab/Biological-Biomedical-Image-Registration](https://github.com/NabaviLab/CAPTURE.git)
```
And to. install libraries, please follow the below command in the first cell of the Google Colab/Jupyter Notebook:
```bash
!pip install opencv-python-headless numpy torch pillow scipy pandas matplotlib seaborn scikit-image psutil scikit-learn
```
This repository contains five `.ipynb` (Jupyter Notebook) files:
1. `Global_Registration.ipynb`: This file is our global features-based image registration
2. `Extract_Information.ipynb`: This is the first step of the geomatrical distortion analysis, which you can extract information from SIFT features extractor.
3. `Geometrical_Distortion.ipynb`: In this file, you can analyzde the geomatrical distortion, having hertamap and extract some information for the upcoming patch division.
4. `Patch_Division.ipynb`: Upon extracting necessary information, by considering this file, you can divided images to different patches.
5. `Pach_Reconstruction.ipynb`: After division, you can reconstruct patches by considering this file.

**** Important Note ****
While for the patch registration, you can use any features-based algorithm, we highly recomend you to use the `Global_Registration.ipynb` for more consistency.


