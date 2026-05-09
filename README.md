# ❤️ Heart Stroke Prediction App

A machine learning web application that predicts the risk of heart disease based on clinical parameters, built with Python and deployed using Streamlit.

---

## 🔗 Live Demo
👉 [Click here to try the app](https://heart-stroke-prediction-app-pdlmfgfkonj2ftfcpsvxcx.streamlit.app/)

---

## 📌 Problem Statement
Heart disease is one of the leading causes of death globally. Early prediction using patient clinical data can help in timely diagnosis and intervention. This app allows users to input health parameters and instantly receive a risk prediction.

---

## 📊 Dataset
- Source: [Heart Failure Prediction Dataset – Kaggle](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- 918 patient records with 11 clinical features
- Target variable: `HeartDisease` (1 = High Risk, 0 = Low Risk)

---

## 🧬 Features Used

| Feature | Description |
|---|---|
| Age | Patient age in years |
| Sex | Gender (Male / Female) |
| ChestPainType | ATA, NAP, TA, or ASY |
| RestingBP | Resting blood pressure (mm/Hg) |
| Cholesterol | Serum cholesterol (mg/dL) |
| FastingBS | Fasting blood sugar > 120 mg/dL |
| RestingECG | Resting ECG results |
| MaxHR | Maximum heart rate achieved |
| ExerciseAngina | Exercise-induced angina |
| Oldpeak | ST depression (numeric) |
| ST_Slope | Slope of peak exercise ST segment |

---

## ⚙️ ML Pipeline

1. **Data Preprocessing** — One-hot encoding for categorical features, StandardScaler for numeric features
2. **Model Training** — K-Nearest Neighbors (KNN) classifier
3. **Serialization** — Model, scaler, and column list saved using `joblib`
4. **Deployment** — Streamlit web app hosted on Streamlit Cloud

---

## 🧠 Model Details
- **Algorithm:** K-Nearest Neighbors (KNN)
- **Why KNN:** Non-parametric, no assumptions about data distribution; works well for binary classification on tabular clinical data
- **Preprocessing:** StandardScaler (critical for KNN since it uses Euclidean distance)

---

## 🚀 Run Locally

```bash
git clone https://github.com/AnshPanwar17/Heart-Stroke-Prediction-App.git
cd Heart-Stroke-Prediction-App
pip install -r requirements.txt
streamlit run app.py
```

---

## 📁 Project Structure

```
├── app.py                        # Streamlit web app
├── Project2(heart disease).ipynb # Model training notebook
├── KNN_heart.pkl                 # Trained KNN model
├── scalar.pkl                    # Fitted StandardScaler
├── columns.pkl                   # Expected feature columns
├── heart.csv                     # Dataset
└── requirements.txt              # Dependencies
```

---

## 🔮 Future Improvements
- Compare KNN against Random Forest, XGBoost, and Logistic Regression
- Display prediction confidence/probability score
- Add SHAP values for model explainability
- Input validation for physiologically invalid values
- Convert to FastAPI backend for scalability

---

## 🛠️ Tech Stack
`Python` `Scikit-learn` `Pandas` `Streamlit` `Joblib`
