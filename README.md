# CNN-Based Malaria Cell Image Classification

**Table of Contents**
- [Project Overview](#project-overview)
- [Dataset Summary](#dataset-summary)
- [Problem Statement](#problem-statement)
- [Methodology](#methodology)
- [Experiments & Results](#experiments--results)
- [Key Learnings](#key-learnings)
- [Limitations & Future Work](#limitations--future-work)

## Project Overview

Malaria is a life-threatening disease caused by Plasmodium parasites, transmitted through the bites of infected female Anopheles mosquitoes. It remains prevalent in tropical and subtropical regions, leading to over 500,000 deaths in 2023 alone, with 76% of these fatalities occurring in children under five. While malaria is not directly contagious between individuals, it can spread through blood transfusions or contaminated needles.

Early detection is crucial, as malaria is curable if treated promptly. However, without timely intervention, it can become fatal within 24 hours. Symptoms range from mild—such as fever, chills, and headaches—to severe manifestations like extreme fatigue, confusion, seizures, and respiratory distress.

Given the urgency of early diagnosis, this deep learning project aims to develop an efficient and accurate model to identify malaria-infected cells, ultimately supporting faster detection and improving patient outcomes.

## Dataset Summary

There are a total of 24,958 train and 2,600 test images (colored) that we have taken from microscopic images. These images are of the following categories:

**Parasitized**: The parasitized cells contain the Plasmodium parasite which causes malaria.

**Uninfected**: The uninfected cells are free of the Plasmodium parasites.

The dataset does **not** contain class imbalance, 49.6% of the data are uninfected cells and 50.4% are parasitized cells.

The raw dataset contains images with varying spatial resolutions. To ensure consistent model input and enable efficient training, all images were resized to 64×64 pixels and stored with three channels in an HDF5 (.h5) format.

This resolution was selected to balance computational efficiency with sufficient spatial detail for classification. While higher resolutions may preserve more fine-grained features, preliminary experiments indicated diminishing returns relative to increased training cost.

## Problem Statement

This project aims to solve a binary image classification problem. Given an image of a cell $x \in \mathbb{R}^{64 \times 64 \times 3}$, the model learns a function $f(x) \rightarrow y$ where $y \in \{0, 1\}$ represents each class label.



## Methodology

## Experiments & Results

## Key Learnings

## Limitations & Future Work

Evaluate the impact of color space representation by converting input images from RGB to HSV. HSV separates luminance (value) from chromatic information, which may improve robustness to illumination variation and highlight structural features relevant to classification.