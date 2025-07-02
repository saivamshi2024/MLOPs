# 🛠️ MLOps: Binary Classification with Model Registration & Version Control

This project demonstrates a full **MLOps pipeline** built around a **binary classification model**. It includes model training, version control, and registration using tools suitable for **production-level deployment** and monitoring.

---

## 🎯 Project Goals

- ✅ Train a binary classification model using Scikit-learn
- 🔁 Automate model registration with versioning
- 🔍 Track experiments, hyperparameters, metrics
- 🚀 Simulate how model versions are used in production
- 🛠 Use MLOps tools to ensure **reproducibility**, **traceability**, and **consistency**

---

## 🧰 Tech Stack & Tools

| Tool / Library     | Purpose                                     |
|--------------------|---------------------------------------------|
| **Python**         | Programming Language                        |
| **Scikit-learn**   | Model building (binary classification)      |
| **MLflow**         | Model tracking, versioning, registration    |
| **Streamlit** (optional) | Visual dashboard (frontend UI)        |
| **Joblib / Pickle**| Model saving/loading                        |
| **Git**            | Source code version control                 |

---

## 🧠 How Model Registration & Versioning Works
Each time you train a model, MLflow tracks:

- Parameters
- Accuracy, precision, recall, ROC AUC
- Confusion matrix
- Timestamp and version ID
  
After training:

- The model is registered in the MLflow Model Registry
- Assigned a unique version number (e.g., ModelName/Version 1, Version 2)
- You can promote a version to "Staging" or "Production" manually or via CI/CD

In production:

- The predict.py script loads the latest production version of the model
- Ensures consistency between training and inference environments

  ![Image](https://github.com/user-attachments/assets/15ba0030-0c82-4318-a5e6-078eaa3046c8)
![Image](https://github.com/user-attachments/assets/4efc3578-b3f8-4374-b465-ae87d2a43ae1)
![Image](https://github.com/user-attachments/assets/b5399dd9-f526-4eb2-b6e3-0e927633231d)
![Image](https://github.com/user-attachments/assets/236d3521-01e3-4fbd-82dd-9d71a2057334)
![Image](https://github.com/user-attachments/assets/67b78938-ab6c-4bdd-aff4-35dcfbba9a8a)
![Image](https://github.com/user-attachments/assets/4d87036e-b564-4761-bb87-86936946827f)

---

## 🔍 Sample Output
- ✅ MLflow UI displays experiment logs
- 📈 ROC Curve and metrics visualization
- 🔄 Predict script uses mlflow.pyfunc.load_model("models:/ModelName/Production")

---

## 🏗️ Production-Ready Benefits
- 🔐 Version control ensures traceability
- 📦 Easy rollback to previous working models
- 📊 Real-time model monitoring and auditing
- ⚙️ Integration-ready for CI/CD pipelines (e.g., GitHub Actions, Jenkins)

---

## 📌 Future Scope
- Integrate with DVC or Kubeflow
- Add Streamlit or FastAPI frontend for live predictions
- Setup automated model retraining and deployment

