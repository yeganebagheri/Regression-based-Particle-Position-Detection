🎯 Regression-Based Particle Position Detection

In Resistive Silicon Detectors

🛠️ Overview

This project focuses on predicting the position of particles passing through a Resistive Silicon Detector (RSD). By extracting relevant features from signal data, we implemented regression models to accurately determine particle positions. 🧬✨

📂 Problem Description

The dataset consists of:
	•	🗂️ Training Set: 385,500 events with features:
	•	Peak magnitudes (pmax), negative peaks (negpmax), delays (tmax), signal areas (area), and RMS values (rms).
	•	📊 Evaluation Set: 128,500 events without target features (x, y).

The goal 🎯: Predict the particle’s x and y positions using the training data.

🚀 Approach

🧹 1. Preprocessing
	•	🧪 Noise Identification:
	•	Analyzed statistical properties to detect noisy features.
	•	Dropped noisy columns and rare event rows.
	•	🏗️ Feature Selection:
	•	Removed less relevant features (e.g., RMS values) to enhance model performance.

🤖 2. Modeling
	•	Models Used:
	•	🟦 Ridge Regression: Baseline linear model.
	•	🌲 Random Forest Regression: Ensemble tree-based model.
	•	🐍 XGBoost Regression: Gradient boosting algorithm optimized for speed and accuracy.
	•	Metric:
📐 Euclidean Distance between actual and predicted particle positions.

🎛️ 3. Hyperparameter Tuning
	•	🎯 Ridge & Random Forest: Tuned using GridSearchCV.
	•	⚡ XGBoost: Tuned using Optuna for efficient parameter optimization.

📈 Results
	•	Ridge Regression: 🎯 Score = 18.157 (Baseline)
	•	Random Forest Regression: 🌟 Score = 5.170
	•	XGBoost Regression: 🏆 Best Score = 4.959

🔍 Key Insights
	•	🥇 XGBoost provided the best performance due to its adaptability and efficiency.
	•	✨ Preprocessing played a critical role in boosting model accuracy.
	•	💡 Future improvements could involve advanced noise handling and additional optimization techniques.

⚙️ Requirements
	•	Python 3.8+ 🐍
	•	Required libraries:
numpy, pandas, scikit-learn, xgboost, optuna, matplotlib


👥 Authors
	•	🧑‍🔬 Chiara Roberta Casale
✉️ Email: s322574@studenti.polito.it
	•	🧑‍🔬 Yegane Bagheri
✉️ Email: s327779@studenti.polito.it

📚 References
	1.	📄 Tornago et al., “Silicon sensors with resistive read-out: Machine learning techniques for ultimate spatial resolution,” Nuclear Instruments and Methods in Physics Research Section A, 2023.
	2.	📘 James et al., An Introduction to Statistical Learning, Springer, 2013.
	3.	📊 Béntéjac et al., “A comparative analysis of gradient boosting algorithms,” Artificial Intelligence Review, 2021.
	4.	🔍 Akiba et al., “Optuna: A next-generation hyperparameter optimization framework,” Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, 2019.
