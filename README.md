# Housing Price Prediction API

An end-to-end machine learning application that predicts California housing prices using a Random Forest regression model and serves predictions through a FastAPI REST API.

---

## Overview

This project demonstrates the complete machine learning workflow from data preprocessing and model training to model deployment through a REST API.

The model is trained using the California Housing dataset provided by scikit-learn and predicts median housing values from demographic and geographic features. Rather than stopping at model development, the project focuses on building a deployable prediction service that can be integrated into larger applications.

---

## Dataset

**Source**
- California Housing Dataset (`sklearn.datasets.fetch_california_housing`)

**Dataset Size**
- 20,640 housing samples

**Input Features**

| Feature | Description |
|---------|-------------|
| MedInc | Median income |
| HouseAge | Median house age |
| AveRooms | Average rooms per household |
| AveBedrms | Average bedrooms per household |
| Population | Population of block group |
| AveOccup | Average household occupancy |
| Latitude | Latitude |
| Longitude | Longitude |

**Target**

- Median house value

---

## Machine Learning Pipeline

```text
California Housing Dataset
            │
            ▼
Data Preprocessing
            │
            ▼
Train/Test Split
            │
            ▼
Random Forest Regression
            │
            ▼
Model Evaluation
            │
            ▼
Serialize Model (.pkl)
            │
            ▼
FastAPI REST API
            │
            ▼
Prediction Endpoint
```

---

## Model

**Algorithm**

- Random Forest Regressor

**Train/Test Split**

- 80 / 20

**Hyperparameters**

- n_estimators = 100
- random_state = 42

---

## Performance

| Metric | Value |
|---------|------:|
| Mean Absolute Error (MAE) | 0.328 |
| R² Score | 0.804 |

The trained model explains approximately 80% of the variance in housing prices while maintaining a mean absolute error of approximately 0.33.

---

## Technologies

### Machine Learning

- Python
- Pandas
- NumPy
- Scikit-learn

### Backend

- FastAPI
- Uvicorn

### Development

- Git
- GitHub

---

## Project Structure

```text
housing-price-prediction-api/

├── notebooks/
│   └── train_model.ipynb
│
├── models/
│   └── house_price_model.pkl
│
├── api.py
├── requirements.txt
└── README.md
```

---

## API

The trained model is served through a FastAPI application.

Future versions will expose REST endpoints for real-time housing price prediction.

---

## Future Work

- Improve model performance through hyperparameter tuning
- Validate user input with Pydantic
- Dockerize the application
- Deploy to Microsoft Azure
- Implement GitHub Actions CI/CD
- Add model monitoring and logging

---

## Repository Status

This project is actively under development as part of my machine learning engineering portfolio, with a focus on production-ready deployment and cloud-based machine learning services.
