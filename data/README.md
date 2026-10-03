# PACS Dataset Guide

This directory is designated for the **PACS** dataset. The PACS dataset is a standard benchmark for evaluating Domain Generalization and Domain Adaptation methods.

## Expected Directory Structure

Before running the code in the `notebooks` directory, ensure you have downloaded and extracted the dataset. The file structure in this folder must look exactly like this:

```
data/
├── art_painting/
│   ├── dog/
│   ├── elephant/
│   ├── giraffe/
│   ├── guitar/
│   ├── horse/
│   ├── house/
│   └── person/
├── cartoon/
│   ├── dog/
│   ├── ...
├── photo/
│   ├── dog/
│   ├── ...
└── sketch/
    ├── dog/
    ├── ...

```

## How to Obtain the Dataset

You can download the PACS dataset from standard research repositories or via the links provided in your assignment instructions.

**Note:**
* This dataset contains 7 common classes across 4 different domains.
* The code in this project uses `torchvision.datasets.ImageFolder` to automatically load the data and labels from these directories. Please do not alter the folder names.
