# mirna-target-prediction-rl-design
A Python project that extracts biological features from miRNA–target pairs, trains a deep neural network for interaction prediction, and applies reinforcement learning to design new miRNA sequences.
# miRNA-Target Prediction and Sequence Design with Deep Learning & Reinforcement Learning



## 📑 Overview

This repository demonstrates an end-to-end **AI for biology** pipeline:

- **Predict miRNA–target interactions** using a deep neural network (DNN).
- **Extract biologically meaningful features** (alignment score, GC/AU/GU counts, seed-region mismatches, etc.).
- **Generate new candidate miRNA sequences** using a simple reinforcement learning (RL) loop that maximises predicted binding.
- Evaluate the model with **accuracy, F1-score**.

Such an approach can accelerate **RNA therapeutics** discovery and is directly relevant to companies like InstaDeep, BenevolentAI, etc.

---

## 🧬 Workflow

1. **Data Collection**  
   Positive and negative miRNA–target sequence pairs (from `positive.txt` and `negative.txt`).

2. **Data Cleaning & Feature Extraction**  
   - Remove gaps (`-`).
   - Compute alignment and base-pairing features.
   - Build feature matrix.

3. **Model Training (Supervised DNN)**  
   - Train/test split.
   - DNN classifier to predict binding probability.

4. **Reinforcement Learning Sequence Design**  
   - Mutate sequences.
   - Use DNN output as reward.
   - Generate candidate sequences with high predicted binding.

5. **Evaluation & Visualisation**  
   - Accuracy, F1 score, classification report.
   - ROC/PR curves.
   - RL reward curve over time.

---

## 🚀 Quick Start

Run in Google Colab:

```bash
!pip install -r requirements.txt
