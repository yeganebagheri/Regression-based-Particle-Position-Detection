Regression-Based Particle Position Detection in Resistive Silicon Detectors

Overview

This project focuses on predicting the position of particles passing through a Resistive Silicon Detector (RSD). By extracting relevant features from signal data, we implement regression models to accurately determine particle positions.

Problem Description

The dataset consists of:
	•	Training Set: 385,500 events with features like peak magnitudes (pmax), negative peaks (negpmax), delays (tmax), signal areas (area), and RMS values.
	•	Evaluation Set: 128,500 events without target features.

The features are recorded by 12 pads, with 18 readings per feature, some of which include noise. The target values are the x and y positions of the particles.

Approach

1. Preprocessing
	•	Noise Identification:
	•	Analyzed statistical properties to detect noisy columns.
	•	Dropped noisy features and infrequent event rows.
	•	Feature Selection:
	•	Removed less relevant features (e.g., RMS values) to improve model performance.

2. Modeling
	•	Models:
	•	Ridge Regression: Baseline linear model.
	•	Random Forest Regression: Ensemble tree-based model.
	•	XGBoost Regression: Gradient boosting algorithm optimized for speed and performance.
	•	Evaluation Metric: Euclidean distance between actual and predicted particle positions.

3. Hyperparameter Tuning
	•	Ridge and Random Forest models tuned with GridSearchCV.
	•	XGBoost tuned with Optuna for efficient exploration of hyperparameter space.

Results
	•	Ridge Regression: Score = 18.157 (baseline).
	•	Random Forest Regression: Score = 5.170.
	•	XGBoost Regression: Score = 4.959 (best-performing model).

Key Insights
	•	XGBoost outperformed other models due to its flexibility and efficiency.
	•	Preprocessing and feature selection significantly improved model accuracy.
	•	Future work could include advanced preprocessing techniques and additional hyperparameter optimization.

How to Run

Requirements
	•	Python 3.8+
	•	Libraries: numpy, pandas, scikit-learn, xgboost, optuna, matplotlib
