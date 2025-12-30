# CIFAR-10 CNN Classification Project

## Overview
This project implements, compares, and analyzes multiple Convolutional Neural Network (CNN) architectures on the CIFAR-10 dataset.  
The goal is to evaluate different model architectures, optimization strategies, and hyperparameters in order to identify the best performing model while also providing interpretability through visualization.

---

## Dataset
**CIFAR-10** contains 60,000 RGB images (32×32) in 10 classes:

Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck  
- Training set: 50,000 images  
- Test set: 10,000 images  

---

## Implemented Models

| Model | Description |
|------|-------------|
| Baseline CNN | Custom CNN designed from scratch |
| ResNet18 | Residual Network adapted for CIFAR-10 |
| DenseNet121 | Densely connected CNN adapted for CIFAR-10 |

---

## Experiments

### Architecture Comparison
- Trained all three architectures using identical training conditions  
- Compared using:
  - Training & validation curves  
  - Confusion matrices  
  - Per-class accuracy  

### Optimizer Comparison
- Architecture fixed: **ResNet18**
- Optimizers compared:
  - Adam  
  - SGD with momentum  
  - RMSProp  
- Evaluated using:
  - Training loss curves  
  - Final test accuracy bar chart  

### Hyperparameter Tuning
- Automated search using **Optuna**
- Tuned parameters:
  - Learning rate  
  - Batch size  
  - Optimizer  
  - Weight decay  
- Best model discovered: **DenseNet121**

---

## Model Interpretability
Feature map visualization was applied to ResNet18’s first convolutional layer to inspect learned spatial features and edge-detection behavior.

---

## Final Model
**DenseNet121** was selected as the final model due to:
- Highest test accuracy  
- Stable convergence  
- Strong generalization performance  

---

## How to Run

```bash
git clone <your-repo-url>
cd cifar10-cnn-project
pip install -r requirements.txt
jupyter notebook
