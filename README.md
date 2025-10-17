## From Data to Decisions: Machine Learning for Formula One Race Strategy Optimization
# Team Members
Ameer Al Bitar – ama281@mail.aub.edu
Nagi Labaki – nsl03@mail.aub.edu
Nancy Fayad – nhf14@mail.aub.edu

Submitted to Dr. Joseph Bakarji – MECH 534

# Overview

This project applies machine learning to optimize Formula One race strategy by predicting lap times under varying conditions. Strategy decisions—when to pit, which tire compound to select, and how to respond to race events—can determine the outcome of a race.
Using real-world data from the Kaggle Formula 1 World Championship dataset and the FastF1 telemetry library, we build models that estimate lap times based on race, driver, and tire characteristics.

# Motivation

Formula 1 races rely heavily on strategic decisions that balance tire wear, fuel load, and driver pace. With teams increasingly integrating AI and ML into decision-making, our project explores how machine learning can improve lap-time forecasting, forming the foundation for automated strategy optimization.

# Datasets
1. Kaggle – Formula 1 World Championship (1950–2024)

Dataset Link

This dataset includes historical F1 data such as races, results, lap times, pit stops, qualifying sessions, and constructors.

~589,000 lap-time records

14–18 features across linked tables

Covers 1950–2024 seasons

Ideal for large-scale trend and statistical modeling

2. FastF1 – FIA Telemetry API (2018–present)

FastF1 on GitHub

This dataset provides modern telemetry and weather information, including:

Tire compound and tire life

Track and air temperature

Stint and lap-by-lap data

Ideal for detailed analysis of tire degradation and environmental effects

These datasets were merged using race and circuit identifiers to form a unified data source linking long-term performance data with modern telemetry.

# Methods and Models

We implemented multiple supervised learning models to predict lap times as continuous values.

Linear Regression (Baseline): interpretable model to estimate feature influence on lap time.

Neural Networks: capture nonlinear dependencies between features (lap evolution, tire wear, etc.).

Tree-Based Models (Random Forests): learn feature interactions and rank variable importance.

Derived Features

FuelLoadProxy – proportion of remaining fuel per lap.

LapsBeforePit – average laps per tire stint.

LapNumber² – captures nonlinear performance drop due to tire degradation.

Initial experiments using linear regression achieved R² ≈ 0.67, capturing much of the lap-time variability while highlighting areas for model improvement.
