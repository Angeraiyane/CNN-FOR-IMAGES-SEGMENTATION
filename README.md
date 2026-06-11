#  Oxford-IIIT Pet Image Segmentation (U-Net & Transfer Learning)

This repository contains the complete implementation and benchmark analysis for **Exercise 1** of the Advanced Deep Learning module (Master AIDC). 

###  Key Features:
* **Data Pipeline:** Complete data loading, class distribution imbalance analysis, and synchronized tensor-based data augmentation (flips and rotations).
* **SimpleUNet from Scratch:** A symmetric Encoder-Decoder CNN architecture implementing skip connections to preserve edge and contour spatial details.
* *Transfer Learning:** Advanced segmentation utilizing a pretrained **ResNet50** backbone, benchmarking two distinct strategies:
  1. *Frozen Encoder:* Training only the newly initialized decoder to optimize computational efficiency.
  2. *Differential Fine-Tuning:* Full-network training with differential learning rates ($10^{-4}$ for the deep backbone and $10^{-3}$ for the decoder).
* **Loss Functions:** Implementation of a weighted Cross-Entropy loss combined with multi-class Dice Loss ($\alpha = 0.5$) to counter severe class imbalance.
* **Evaluation Metrics:** Full evaluation using Mean Intersection-over-Union (mIoU) and Dice Score metrics.
