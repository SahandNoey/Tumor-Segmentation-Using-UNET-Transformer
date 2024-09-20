# Brain Tumor Segmentation Using UNETR

## Overview

This project implements **brain tumor segmentation** using the **UNETR (UNet Transformer) 2D** model, leveraging the power of deep learning and transformers to accurately identify and segment tumors in brain MRI images. The model is designed to aid in medical image analysis by providing accurate segmentation masks for tumor regions.

### Features:
- Utilizes **UNETR 2D** for segmentation tasks
- Dice loss function for optimizing the model.
- Model checkpointing and early stopping for efficient training.
- Compatible with medical image formats.

## Dataset

This project uses **medical brain MRI datasets** to perform brain tumor segmentation using this [DATASET](https://www.kaggle.com/datasets/nikhilroxtomar/brain-tumor-segmentation).

## Model Architecture
U-Net + Vision Transformer(ViT)

The 2D version of UNETR simplifies the 3D transformer for 2D medical images.

### Evaluation

The model's performance is evaluated using **Dice Coefficient**

## Results

After training, the model is expected to produce segmentation masks that accurately identify the tumor regions in MRI images. Results can be visualized using matplotlib or any other image plotting library.

**Example of segmented brain MRI image**:
The model generates segmentation masks that highlight tumor regions in MRI images

Example of segmented brain MRI image: 


![](https://github.com/SahandNoey/Tumor-Segmentation-Using-UNETR/blob/master/results/1344.png)

![](https://github.com/SahandNoey/Tumor-Segmentation-Using-UNETR/blob/master/results/114.png)

![](https://github.com/SahandNoey/Tumor-Segmentation-Using-UNETR/blob/master/results/132.png)

_Left: Original MRI image._

_Center: Ground Truth mask of the brain tumor._

_Right: Predicted segmentation mask produced by the model._




## Callbacks

The training process uses the following Keras callbacks:
- ModelCheckpoint
- ReduceLROnPlateau
- EarlyStopping
