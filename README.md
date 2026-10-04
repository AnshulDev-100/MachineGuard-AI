# 🔧 MachineGuard-AI: Predictive Maintenance for Industrial Machines

> **Industrial IoT Analytics** • **Machine Learning** • **MLOps** • **REST API**

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikitlearn)
![MLflow](https://img.shields.io/badge/MLflow-Experiment_Tracking-blue?logo=mlflow)
![FastAPI](https://img.shields.io/badge/FastAPI-REST_API-green?logo=fastapi)

An ML system that **predicts equipment failures from sensor readings before they occur**. It covers the full workflow: data preprocessing, class balancing, model comparison with experiment tracking, and serving the best model through a REST API.

---

## 🎯 Key Highlights

* **91.2% accuracy** (90.7% F1) with Random Forest, the best of 4 models compared
* **End-to-end pipeline**: data ingestion → preprocessing → model training → experiment tracking → API serving
* **Class imbalance handled** with SMOTE, since machine failures are rare events
* **FastAPI prediction service** with Pydantic input validation and health checks
* **MLflow** experiment tracking and model registry for reproducible runs

---

## 📊 Project Overview

Predictive maintenance helps manufacturers **anticipate machine breakdowns**, reducing unplanned downtime and maintenance cost.
This system ingests **sensor data** (temperature, torque, rotational speed, tool wear), trains and compares ML models, and serves failure predictions through an API.

---

## 🛠 Technical Stack

| Area | Tools |
| --- | --- |
| Machine Learning & Data | scikit-learn, pandas, numpy, SMOTE |
| API & Validation | FastAPI, Pydantic |
| Experiment Tracking | MLflow (experiments & model registry) |

---

## 🏗 Architecture

```
Data → Preprocessing (SMOTE) → Model Training & Comparison (MLflow) → Model Registry → FastAPI Prediction Service
```

---

## 📸 Screenshots

## 📸 Screenshots

![Capture](https://github.com/user-attachments/assets/b5ea1ab5-03d2-44e6-8820-187a19caeaef)

![Capture1](https://github.com/user-attachments/assets/f26830f7-deff-475a-bfeb-f62a10ef6608)

![Capture3](https://github.com/user-attachments/assets/31c9f394-42b5-43dd-a88c-2dd433af423d)

![Capture4](https://github.com/user-attachments/assets/d0772238-2de6-4264-ac18-958c9dec3bc4)

![Capture5](https://github.com/user-attachments/assets/9dbe47c1-21b9-4ef9-8144-6cafc4130858)

![Capture6](https://github.com/user-attachments/assets/6bc82e51-f6ae-40f0-b5e4-0aeee2da48ce) <img width="1878" height="693" alt="Screenshot 2025-08-15 120611" src="https://github.com/user-attachments/assets/afe3a0b4-9599-4a5a-8eb8-fd2dac558420" />

---

## 📈 Model Performance

| Model               | Accuracy  | Precision | Recall | F1-Score |
| ------------------- | --------- | --------- | ------ | -------- |
| Random Forest       | **91.2%** | 89.4%     | 92.1%  | 90.7%    |
| Gradient Boosting   | 89.8%     | 87.3%     | 91.5%  | 89.3%    |
| Logistic Regression | 86.4%     | 84.1%     | 88.7%  | 86.3%    |
| SVM                 | 88.1%     | 85.9%     | 90.2%  | 88.0%    |

**Feature Importance (Random Forest):**

1. Tool Wear (32%)
2. Temperature Differential (24%)
3. Torque Variance (21%)
4. Rotational Speed (15%)
5. Equipment Type (8%)

---

## 🚀 Quick Start

**Clone & Setup**

```bash
git clone https://github.com/AnshulDev-100/MachineGuard-AI.git
cd MachineGuard-AI

python -m venv venv
venv\Scripts\activate  # Windows
pip install -r requirements.txt
```

**Run Pipeline**

```bash
# Train and compare models
python run_pipeline.py --mode train

# Start the prediction API
python app.py
```

---

## 🔮 Future Enhancements

* **Advanced feature engineering:** rolling statistics, lag features
* **Ensemble/stacking models** for higher accuracy
* **Containerized deployment and CI/CD** for automated builds and releases
* **Real-time data** with automated retraining
* **Monitoring & observability:** drift detection, dashboards, alerting

---
