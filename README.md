# ImageNet10 ResNet18 PGD Attacks

This repository contains the code for training a ResNet18 model on the ImageNet10 dataset and evaluating its robustness using PGD (Projected Gradient Descent) attacks. This project demonstrates the process of preparing a custom dataset, training a neural network, and applying adversarial attacks to test the model's robustness.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model](#model)
- [Training](#training)
- [Adversarial Attacks](#adversarial-attacks)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)

## Introduction
Adversarial attacks are used to evaluate the robustness of neural networks by introducing small perturbations to the input data. This project focuses on applying PGD attacks to a ResNet18 model trained on a subset of the ImageNet dataset, referred to as ImageNet10.

## Dataset
ImageNet10 is a subset of the ImageNet dataset, containing 10 selected classes. The dataset should be organized in the following structure:

## Model
We use the ResNet18 model, a widely used convolutional neural network architecture. The final layer of the pre-trained ResNet18 model is modified to match the number of classes in the ImageNet10 dataset.

## Training
The model is trained on the ImageNet10 dataset using the following setup:
- 

## Adversarial Attacks
PGD (Projected Gradient Descent) is used to generate adversarial examples and evaluate the model's robustness. The parameters for PGD are:
- 

## Results
The model's accuracy under PGD attack is reported to assess its robustness.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/imagenet10-resnet18-pgd-attacks.git
    cd imagenet10-resnet18-pgd-attacks
    ```
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Prepare the ImageNet10 dataset and place it in the appropriate directory.


## Acknowledgements: 
@article{ILSVRC15,
         author = {Olga Russakovsky and Jia Deng and Hao Su and Jonathan Krause and Sanjeev Satheesh and Sean Ma and Zhiheng Huang and Andrej Karpathy and Aditya Khosla and Michael Bernstein and Alexander C. Berg and Li Fei-Fei},
         title={ImageNet Large Scale Visual Recognition Challenge},
         year={2015},
         journal={International Journal of Computer Vision (IJCV)},
         volume={115},
         number={3},
         pages={211-252}
}
