# ImageNet10 ResNet18 PGD Attacks

This repository contains the code for training a ResNet18 model on the ImageNet10 dataset and evaluating its robustness using PGD (Projected Gradient Descent) attacks. This project demonstrates the process of preparing a custom dataset, training a neural network, and applying adversarial attacks to test the model's robustness.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#Setup)
- [Dataset](#dataset)
- [Model](#model)
- [Adversarial Attacks](#adversarial-attacks)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)

## Introduction
Adversarial attacks are used to evaluate the robustness of neural networks by introducing small perturbations to the input data. This project focuses on applying PGD attacks to a ResNet18 model trained on a subset of the ImageNet dataset, referred to as ImageNet10. 

## Setup
Ensure you have the following libraries installed 
- numpy
- pandas
- torch
- torchvision
- matplotlib
- tqdm
- torchattacks
- time
Install the required libraries using pip:

```bash
pip install numpy pandas torch torchvision matplotlib tqdm torchattacks
```

## Dataset
ImageNet10 is a subset of the ImageNet dataset, containing 10 selected classes. The dataset should be organized in the following structure:
```
/path/to/imagenet10data/
    ├── train/
    │   ├── class_1/
    │   ├── class_2/
    │   └── ...
    └── val/
        ├── class_1/
        ├── class_2/
        └── ...
```
Update the paths in the code to point to the correct dataset directory 

## Model
I used the ResNet18 model, a widely used convolutional neural network architecture. The final layer of the pre-trained ResNet18 model is modified to match the number of classes in the ImageNet10 dataset.

## Adversarial Attacks
PGD (Projected Gradient Descent) is used to generate adversarial examples and evaluate the model's robustness. The parameters for PGD are:
- 

## Results
The model's accuracy under PGD attack is reported to assess its robustness. Since ImageNet10 has a small amount of data, the ResNet18 model that was pre-trained was only able to obtain a 50% accuracy. After applying PGD attacks, the model had an accuracy of 0%. The two other variations were able to achieve a maximum of 40% accuracy. One model was made by fine-tuning all layers and the other had frozen layers except for the top one. However, since the dataset was so small, it was unable to achieve good accuracy. 

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/imagenet10-resnet18-pgd-attacks.git
    cd imagenet10-resnet18-pgd-attacks
    ```
2. Install the required packages as stated above. 

## Usage
1. Prepare the ImageNet10 dataset and place it in the appropriate directory.

## Acknowledgements: 
- TorchAttacks: The adversarial attack library used in this project. More Details can be found on their github page
- ImageNet10: The dataset used for training and evaluation. The datasertr is a subset of ImageNet dataset. 
