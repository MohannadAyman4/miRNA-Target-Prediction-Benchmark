# miRNA-Target-Prediction-Benchmark
Benchmarking computational tools for miRNA–target interaction prediction.
# miRNA–Target Interaction Benchmarking

## Overview

This repository contains the computational benchmarking of miRNA–target interaction prediction tools using the official **miRBench AGO2_CLASH_Hejret2023 test dataset**.

The analysis evaluates three prediction methods:

* **TargetNet**
* **RNACofold**
* **GraphTar**

The goal is to compare the performance of different computational approaches for predicting miRNA–target interactions.

---

## Dataset

**Dataset:** AGO2_CLASH_Hejret2023 — Test Set

* Total samples: **1018**
* Positive interactions: **495**
* Negative interactions: **523**

The official test dataset was used for all benchmarking analyses.

---

## Evaluated Methods

### 1. TargetNet

TargetNet was evaluated using the pretrained **TargetNet_Min2021** predictor available through the miRBench framework.

The model was used directly for inference without retraining.

### 2. RNACofold

RNACofold was evaluated using the miRBench predictor and ViennaRNA-based RNA secondary-structure/interaction calculations.

The pretrained implementation was used without model retraining.

### 3. GraphTar

GraphTar was evaluated using a pretrained GraphTar checkpoint based on a **Graph Convolutional Network (GCN)** with pretrained Word2Vec sequence representations.

Because the AGO2_CLASH dataset format was not directly compatible with the expected GraphTar input format, an adapter was used to prepare the miRNA and target sequences for inference.

No retraining was performed.

---

## Evaluation

Predictions were evaluated using two classification thresholds:

* **0.5**
* **0.7**

### Threshold-independent metrics

* Average Precision (AP)
* ROC-AUC

### Threshold-dependent metrics

* Accuracy
* Precision
* Recall / Sensitivity
* Specifici
