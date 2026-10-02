# Domain-Adaptation-Generalization-ResNet
Implementation of Domain Adaptation (DANN) and Domain Generalization (ERM, FAD, MIRO) techniques on the PACS dataset using PyTorch and ResNet-18.


# Domain Adaptation on PACS Dataset

## Overview
This repository focuses on **Domain Adaptation** techniques to improve the performance of deep neural networks on unseen data distributions. Using ResNet-18 as the backbone, the project explores how a model trained on a source domain can adapt to a target domain with a different visual style.

## Dataset
The experiments are conducted on the **PACS** dataset, which contains images from four distinct domains: `art_painting`, `cartoon`, `photo`, and `sketch`.

## Key Implementations
- **Transfer Learning Baseline**: Evaluating a pre-trained ResNet-18 model without domain-specific fine-tuning.
- **Single-Domain Fine-Tuning**: Analyzing the drop in performance when a model overfits to a specific domain style.
- **Data Augmentation**: Applying transformations like Color Jitter and RandomAffine to increase robustness.
- **DANN (Domain-Adversarial Neural Networks)**: The core contribution of this project. A Gradient Reversal Layer (GRL) is used alongside a domain classifier to extract domain-invariant features.

## Results
- The DANN architecture successfully reduced domain discrepancy. Accuracy on the highly dissimilar `sketch` domain improved significantly from 19.95% (pre-training) to 63.02%.
- **t-SNE Visualizations**: Included in the notebook to demonstrate the overlap and alignment of feature distributions between the training and test domains after adversarial training.

## Usage
Upload and run the `.ipynb` notebook. Ensure the PACS dataset is placed in the correct root directory before execution.
