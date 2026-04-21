# Language Detection Model

This project is a machine learning tool that automatically identifies the language of a given text.

## Overview
Detecting languages is challenging because many languages share the same alphabet. Our model solves this by looking at "statistical fingerprints" - the frequency of specific character combinations (n-grams) unique to each language.

## Dataset
We used a Kaggle dataset containing **10,337 sentences** across **17 different languages**, including English, Arabic, French, Greek, and more.

## Technical Stack
The project is built using:
* **Python**
* **Pandas & NumPy**: For data manipulation.
* **Scikit-learn**: For feature engineering and evaluation metrics.
* **Matplotlib**: For data visualization.

## How It Works
1. **Data Splitting**: We split the data into 80% for training and 20% for testing.
2. **Feature Engineering**: We used **TF-IDF Vectorization** with character n-grams. This turns text into numbers based on how unique a letter sequence is to a specific language.
3. **The Algorithm**: We built a custom **K-Nearest Neighbors (KNN)** model. It predicts a language by finding the most similar sentences in the training data using **Cosine Similarity**.
4. **Optimization**: We used **Grid Search** and **5-Fold Cross-Validation** to find the best settings for the model.

## Results
The model is highly accurate:
* **Best Settings**: $k=11$ and an n-gram range of (2, 3).
* **F1-Macro Score**: **0.985** (approx. 98.5% accuracy).
* The model successfully identifies language patterns and performs reliably across all 17 languages.

## Project Members
* Almog S (5890)
* Eliad B (6279)