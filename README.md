# 🎧 HitSense: Predicting Hit Potential of Songs

## Author
Joseph Epperson  
Capstone project for Data Science Certification, 2025

## Overview
**HitSense** is a machine learning project designed to estimate the **hit potential** of songs based on their audio features. By using Spotify audio features like danceability, energy, tempo, and valence, I trained a regression model to predict a track’s likelihood of being a hit, expressed as a **percentage score**.

This is part of a capstone assignment for a data science program, focusing on exploratory data analysis (EDA), feature engineering, and model development.

---

## Dataset
Using a simplified version of the [Spotify Audio Features Dataset](https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-160k-tracks). A sample subset is included here for demonstration purposes.

**Files:**
- `data/hitsense_raw.csv` — raw input data
- `data/hitsense_cleaned.csv` — feature-engineered dataset used for modeling

---

## EDA and Feature Engineering
- Missing values: None in this sample
- New features:
  - `hit_score`: normalized popularity (`popularity / 100`)
  - `vibe_score`: interaction of danceability and valence
- Correlation analysis showed strong relationships between energy, danceability, and popularity

---

## Model
We used a simple **Linear Regression** model to serve as a baseline.

### Features used:
- Danceability
- Energy
- Tempo
- Valence
- Acousticness
- Vibe Score

### Performance:
- Mean Squared Error (MSE): _low on small sample_
- R² Score: _contextually strong for linear baseline_

Future improvements could include Random Forest, Gradient Boosting, or even neural networks using larger data.

---

## How to Run
1. Clone this repo
2. Make sure you have Python 3.10+ and Jupyter installed
3. Install required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. Run `HitSense_EDA_and_Model_Full.ipynb`

---

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bedrock510/Hit-SENSE/blob/main/HitSense_EDA_and_Model_Full.ipynb)

