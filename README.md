# Regression-based-Particle-Position-Detection
Regression-Based Particle Position Detection in Resistive Silicon Detectors

Overview

This project addresses the problem of predicting the position of particles passing through a Resistive Silicon Detector (RSD). Using features extracted from signals recorded by RSD sensors, we develop regression models to determine particle positions in two-dimensional space.

Problem Description
	•	Goal: Predict the x and y positions of particles passing through the sensor.
	•	Dataset:
	•	Training set with 385,500 events, including features such as peak magnitudes, delays, signal areas, and RMS values.
	•	Evaluation set with 128,500 events (target positions are not included).

The features are recorded by 12 pads on the sensor, with 18 readings for each feature (some of which are noisy).
