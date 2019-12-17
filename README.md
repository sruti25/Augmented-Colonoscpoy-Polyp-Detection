## Augmented-Colonoscpoy-Polyp-Detection

This project implements a CNN based polyp detector.

# Dataset
1. Extracted from ASU Mayo Polyp Databse: https://polyp.grand-challenge.org/AsuMayo/
2. Synthetic images generated using XD-Cycle GAN
3. Combination of above two.

# Network
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
===================================================
conv2d_4 (Conv2D)            (None, 148, 148, 64)      1792      
_________________________________________________________________
activation_6 (Activation)    (None, 148, 148, 64)      0         
_________________________________________________________________
max_pooling2d_4 (MaxPooling2 (None, 74, 74, 64)        0         
_________________________________________________________________
conv2d_5 (Conv2D)            (None, 72, 72, 64)        36928     
_________________________________________________________________
activation_7 (Activation)    (None, 72, 72, 64)        0         
_________________________________________________________________
max_pooling2d_5 (MaxPooling2 (None, 36, 36, 64)        0         
_________________________________________________________________
conv2d_6 (Conv2D)            (None, 34, 34, 128)       73856     
_________________________________________________________________
activation_8 (Activation)    (None, 34, 34, 128)       0         
_________________________________________________________________
max_pooling2d_6 (MaxPooling2 (None, 17, 17, 128)       0         
_________________________________________________________________
flatten_2 (Flatten)          (None, 36992)             0         
_________________________________________________________________
dense_3 (Dense)              (None, 128)               4735104   
_________________________________________________________________
activation_9 (Activation)    (None, 128)               0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 128)               0         
_________________________________________________________________
dense_4 (Dense)              (None, 1)                 129       
_________________________________________________________________
activation_10 (Activation)   (None, 1)                 0         
==============================================

# References:
1. https://github.com/muntisa/Colonoscopy-polyps-detection-with-CNNs

