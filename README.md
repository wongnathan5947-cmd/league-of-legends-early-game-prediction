# league-of-legends-early-game-prediction
Exploratory analysis and machine learning modeling of early-game League of Legends data, featuring feature engineering, visualization, and win prediction using logistic regression.

## Overview
This project analyzes early-game (first 10 minutes) League of Legends match data to identify factors that influence match outcomes and to predict blue team victories using machine learning.

## Dataset
- ~9,800 ranked matches (Diamond tier)
- Early-game statistics including gold, experience, objectives, and combat metrics
- Target variable: `blueWins` (binary)

## Exploratory Data Analysis
- Early gold, experience, and kill advantages strongly correlate with winning
- Dragon control showed a stronger relationship with victory than Heralds or early towers
- Vision-based features (wards placed/destroyed) had minimal predictive impact

## Feature Engineering
- Converted team-level statistics into **difference-based features** from the blue team’s perspective
- Removed redundant and highly correlated features to improve interpretability

## Modeling
- Logistic Regression with standardized features
- 80/20 train-test split
- Achieved ~72% accuracy on unseen data

## Key Insights
- Early economic advantage (gold + experience) had the largest influence on predictions
- Objective control, especially dragons, provided meaningful early-game signals
- Match outcomes remain dynamic beyond the early game

## Tools Used
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

## Future Work
- Incorporate champion-level data
- Extend analysis beyond the first 10 minutes
- Compare additional models (Random Forest, XGBoost)
