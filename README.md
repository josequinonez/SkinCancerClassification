# SkinCancerClassification
Classification analysis of three types of skin lesions: melanoma (deadliest skin cancer), nevus, and seborrheic keratosis (benign lesions)

This is an optional project assignment in **Udacity Deep Learning Nanodegree program**.

The data and objective are pulled from the 2017 ISIC Challenge on Skin Lesion Analysis Towards Melanoma Detection (https://challenge.kitware.com/#challenge/583f126bcad3a51cc66c8d9a). As part of the challenge, participants were tasked to design an algorithm to diagnose skin lesion images as one of three different skin diseases: melanoma, nevus, or seborrheic keratosis.

Melanoma is a malignant skin tumor, while nevus and seborrheic keratosis are two types of benign lesions. The project aims to design an algorithm to correctly classify these skin lesions through using Transfer Learning and CNNs.

In order to reduced the number of training epochs, I followed Dr. Leslie N. Smith's Cyclical learning rates strategy. See "Cyclical Learning Rates for Training Neural Networks" (https://arxiv.org/pdf/1506.01186.pdf).

### Data requirements:
- Create a folder named 'data'
- Create subfolders 'train', 'valid', and 'test' under 'data'
- Download data files and save them in the corresponding subfolders:
  - https://s3-us-west-1.amazonaws.com/udacity-dlnfd/datasets/skin-cancer/train.zip
  - https://s3-us-west-1.amazonaws.com/udacity-dlnfd/datasets/skin-cancer/valid.zip
  - https://s3-us-west-1.amazonaws.com/udacity-dlnfd/datasets/skin-cancer/test.zip

### Library requirements:
- numpy
- glob
- cv2
- matplotlib
- os
- torch
- torchvision
- PIL

### Lessons learned:
The use of cyclical learning rates helped to reach better test accuracies faster than as compared to using a fixed learning rate.

Test accuracy reached a plateau around 0.60s after only 2,000 iterations, whilst the equivalent test using a fixed learning rate hardly exceeded 0.50s.

Further performance analysis is required.
