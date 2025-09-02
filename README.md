Absolutely, Prafful! Here's a clean, professional README tailored for your project, ideal for GitHub and portfolio visibility:

---

# 🎓 Student Performance Prediction – Azure Web App Deployment

This project is a production-grade machine learning web application that predicts student performance using a CatBoost model. The app is containerized with Docker and deployed to Azure using GitHub Actions and Azure Container Apps.

---

## 🚀 Features

- 🧠 ML model trained with CatBoost and scikit-learn
- 🌐 Flask-based web interface for predictions
- 📦 Dockerized for reproducible builds
- 🔄 CI/CD pipeline with GitHub Actions
- ☁️ Deployed to Azure Container Registry and Azure Container Apps
- 🔐 Secure ingress and environment configuration

---

## 🛠️ Tech Stack

- Python, Flask, CatBoost, scikit-learn
- Docker, GitHub Actions
- Azure Container Registry (ACR)
- Azure Container Apps
- CI/CD with OIDC-based authentication

---

## 📦 Setup & Deployment

### 1. Clone the Repository
```bash
git clone https://github.com/Prafful-Vyas/Student-Performance-Azure-Web-App.git
cd Student-Performance-Azure-Web-App
```

### 2. Build Docker Image
```bash
docker build -t pvreg.azurecr.io/student_performance:latest .
```

### 3. Push to Azure Container Registry
```bash
docker login pvreg.azurecr.io
docker push pvreg.azurecr.io/student_performance:latest
```

### 4. Deploy via GitHub Actions
CI/CD is triggered on every push to `main` using the workflow:
```
.github/workflows/azure-web-app-AutoDeployTrigger.yml
```

---

## 🔐 Secrets Required (GitHub → Settings → Secrets)

| Secret Name                          | Description                      |
|-------------------------------------|----------------------------------|
| `AZUREWEBAPP_AZURE_CLIENT_ID`       | Azure AD App Client ID           |
| `AZUREWEBAPP_AZURE_TENANT_ID`       | Azure Tenant ID                  |
| `AZUREWEBAPP_AZURE_SUBSCRIPTION_ID` | Azure Subscription ID            |

---

## 📊 Model Overview

- Input features: Student demographics, academic scores, and behavioral metrics
- Output: Predicted performance category (e.g., Pass/Fail or Grade)
- Model: CatBoostClassifier with hyperparameter tuning

---


