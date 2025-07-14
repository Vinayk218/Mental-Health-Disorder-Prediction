
# 🧠 Mental Health Disorder Prediction System

This system predicts mental health conditions and their severity based on user responses to a structured questionnaire. It uses a **stacked ensemble** model combining TabNet, LightGBM, and Logistic Regression, deployed via a Flask-based web application with an interactive UI. The goal is to assist early detection and offer personalized recommendations.

---

## 🚀 Features

- Predicts mental health treatment need
- Classifies disorders: **Depression, Anxiety, Bipolar Disorder, OCD**
- Outputs **Risk Level**: Low / Medium / High
- Personalized suggestions for high-risk individuals
- Result retrieval using a unique submission ID
- Stores results securely in a local SQLite database

---

## 🛠 Technologies Used

- **Frontend**: HTML, Jinja2 (Flask templates)
- **Backend**: Python 3.x, Flask, SQLAlchemy
- **ML Models**:
  - TabNet (PyTorch)
  - LightGBM
  - Logistic Regression (meta-classifier)
- **Libraries**: pandas, numpy, scikit-learn, joblib

---

## 📈 Model Performance

| Model               | Accuracy | Strengths                                       |
|--------------------|----------|--------------------------------------------------|
| TabNet             | ~88%     | Deep learning with feature-level interpretability |
| LightGBM           | ~85%     | Fast, scalable, handles missing values well      |
| Logistic Regression| Meta     | Used as meta-model for final decision making     |
| **Hybrid Ensemble**| **89–92%** | Combines both models to improve prediction power |

- **F1-Score**: 0.87 for positive (treatment needed) class  
- **ROC-AUC**: 0.902  
- **Cross-Validation**: Stratified K-Fold (5–10 splits)

---

## ⚙️ How to Run

1. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Start the server**:
   ```bash
   python app.py
   ```

3. **Use in browser**:  
   Navigate to [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 📊 Prediction Output

- **Disorder Classification**: One or more from Depression, Anxiety, OCD, Bipolar
- **Risk Level**:
  - High Risk: ≥ 80% → Immediate attention recommended
  - Medium Risk: 50–79% → Monitoring and check-ins
  - Low Risk: < 50% → Preventive care

---

## 🔐 Data Ethics

- Uses anonymized survey data (5,000 entries)
- Models trained with SMOTE to balance class distribution
- Designed for explainability and fairness
- Not a diagnostic tool — **supports, not replaces, clinicians**

---

## 📌 Future Enhancements

- Admin dashboard with analytics
- User login/authentication
- Deployment on cloud (AWS, Azure)
- Real-time chat support for recommendations

---

## 👤 Author

**Vinay K.**  
B.E. Final Year – JSS Science and Technology University, Mysuru  
[GitHub: Vinayk218](https://github.com/Vinayk218)

---
