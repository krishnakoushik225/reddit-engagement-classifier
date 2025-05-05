# reddit-engagement-classifier
This project analyzes Reddit posts to predict engagement trends — classifying whether a post will receive high (Up), low (Down), or moderate (Stable) user interaction. We use metadata like Tags, Domain, and Subreddit from a Kaggle dataset and apply Sentence-BERT embeddings combined with structured features like comment counts.


# 📘 Overview

This repository contains a master's-level project on predicting Reddit post engagement trends using hybrid NLP and structured features. The objective is to classify Reddit posts into three engagement categories:

Up: High engagement

Down: Low engagement

Stable: Medium/normal engagement

The classification is based on metadata such as Tags, Subreddit, and Domain using advanced language modeling and tree-based classifiers.


# 📂 Dataset

Source: Kaggle — Predicting Reddit Community Engagement Dataset

Features Used:

Tags, Domain, Subreddit: Used for textual context

Score, NumComments, NumCommenters: Used to generate engagement labels and as numeric features.


# 🧠 Methodology

1. Data Preprocessing

Merged text from Tags, Domain, and Subreddit

Cleaned using Huggingface tokenizer-compatible minimal regex

Engagement labels created from Score:

Up = Score ≥ 10

Down = Score ≤ -5

Stable = Otherwise

2. Feature Engineering

Textual Embeddings: Sentence-BERT (all-MiniLM-L6-v2)

Structured Features: NumComments, NumCommenters

Combined into a hybrid feature vector

3. Modeling

Model Used: XGBoost Classifier

Tuning: Hyperparameter optimization using Optuna

Evaluation Metrics:

Accuracy

Macro F1-Score

Confusion Matrix


# 🧪 Results

Achieved high classification performance on the test set

Macro F1-Score used to account for slight class imbalance

Visualized confusion matrix and model performance

# 🚀 Getting Started

Requirements

Install required libraries:

pip install sentence-transformers xgboost scikit-learn pandas tqdm optuna matplotlib seaborn

# Running the Notebook

Open SMM_Final_Project_latest.ipynb in Google Colab or Jupyter

Upload Reddit_Data.csv (tab-separated)

Run all cells sequentially

# 📈 Sample Visuals
Confusion matrix heatmap

Class distribution bar chart


# 👨‍💻Contributors

Krishna Koushik Unnam, 

Venkata Sai Sudarsana Varma Mandapati,

Kalyan Gutta,

Sai Murali Ravuri

Sudharshan Varma 

University of South Florida

Social Media Mining Course, 2025
