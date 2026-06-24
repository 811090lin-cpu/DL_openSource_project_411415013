# DL_openSource_project_411415013
Deep learning models for traffic volume prediction
# Traffic Flow Prediction: Feature Engineering Optimization

This project focuses on enhancing traffic flow prediction accuracy through advanced feature engineering and automated data preprocessing techniques.

---

## Table of Contents
1. [Project Goal](#project-goal)
2. [Data Pipeline & Structure](#data-pipeline--structure)
3. [Optimization Techniques](#optimization-techniques)
4. [Usage](#usage)
5. [Evaluation Metrics](#evaluation-metrics)
6. [Dependencies](#dependencies)

---

## Project Goal
This project aims to resolve data bottlenecks in traffic forecasting models, specifically addressing temporal dependency loss and high-dimensional noise. By implementing structured feature optimization, we achieve a more stable and accurate prediction system.

## Data Pipeline & Structure
Our pipeline transforms raw traffic and meteorological data into optimized input for the model.

* **Raw Data**: Includes real-time traffic volume, weather conditions (precipitation), and timestamps.
* **Feature Engineering**: 
    * **Temporal Injection**: Implementation of `lag_1` and `lag_24` features to capture cyclical traffic patterns.
    * **Dimensionality Reduction**: Replacing sparse One-hot weather encoding with weighted numerical values to reduce model complexity.
* **Preprocessing**: Application of `log1p` transformation on precipitation data to mitigate long-tail distribution impacts and improve data smoothness.



## Optimization Techniques

| Technique | Description | Impact |
| :--- | :--- | :--- |
| **Lag Features** | Explicit injection of historical temporal data | Captures cyclic traffic trends |
| **Weighted Encoding** | Replaces high-dimensional sparse One-hot vectors | Reduces noise and model complexity |
| **Log Scaling** | `log1p` transformation on skewed features | Improves training convergence stability |

## Usage

### 1. Installation
```bash
pip install -r requirements.txt
