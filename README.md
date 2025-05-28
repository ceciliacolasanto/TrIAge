## 🏥 Project Summary: trIAge – AI-Powered Emergency Triage System

This project, **trIAge**, is an AI-based emergency triage system developed to support hospitals and healthcare providers in prioritizing emergency patients by predicting urgency levels and target medical areas based on initial symptoms and available health indicators.

### 📦 Data Ingestion & Storage

The dataset was stored in a **Google Cloud Platform (GCP) bucket** and accessed through **Google Colab** for processing and analysis.

### 🔄 Data Processing & Feature Engineering

We applied comprehensive **preprocessing steps** to prepare the data:

- **Outlier detection and treatment**, done in collaboration with medical professionals, to filter out biologically implausible values (e.g., unrealistic blood pressure or temperature readings).
- **Feature engineering** to create new variables and derive meaningful health signals.
- **Text preprocessing** on free-text symptom descriptions to apply NLP models.
- **Categorical simplification**, grouping rare values into "others" for model stability.
- Removal of variables that are the outcome of triage decisions to avoid data leakage.

### 🧠 AI Techniques & Modeling Approaches

We used a combination of classical machine learning and modern NLP techniques to handle two main triage scenarios:

#### 1. When health metrics are available (e.g., ambulance arrival):
- Predict **urgency level** and **medical area** using features like vital signs and symptoms.
- Models used: **K-Nearest Neighbors (KNN)**, **Random Forest**, **Gradient Boosting**, and **XGBoost**.
- Applied **zero-shot classification** on symptoms to complement traditional models.
- **Feature selection** techniques helped identify the most relevant predictors.

#### 2. When only symptoms are available (e.g., walk-ins):
- Applied **zero-shot classification** with **NLP models** to map free-text symptoms to predefined diagnosis categories and urgency levels.
- Combined with traditional models using vectorized symptom data.

### 🔐 Privacy & Testing

To ensure data privacy and ethical standards, we implemented **pseudo-anonymization**, allowing patient data to remain unlinkable to real identities while preserving the ability to group repeat entries.

To test usability and functionality, we created a **Google Forms-based simulation**, where users could input symptoms and health data, emulating patient entry in real time. The form dynamically triggers the appropriate model based on available information.

### 📈 Goals and Future Development

- Develop a **real-time triage app** for patients, companions, or ambulance staff to use before hospital arrival.
- Expand models with more labeled data and real hospital feedback.
- Integrate additional features like:
  - **Patient re-entry likelihood**
  - **Resource planning for emergency beds**
  - **Geolocation-aware triage**
  - **Interface with hospital systems and dashboards**

trIAge empowers healthcare institutions to optimize emergency response through intelligent, data-driven triage decisions.

📊 [Download the project presentation](https://www.canva.com/design/DAGXsipJG8s/kWYhsK0xrabG1XtUjTpllg/edit?utm_content=DAGXsipJG8s&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
