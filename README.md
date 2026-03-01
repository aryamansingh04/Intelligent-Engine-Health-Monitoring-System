# 🚗 Engine Health Prediction System

A Machine Learning-based system that predicts engine condition using sensor parameters such as RPM, pressure, and temperature.

The system uses a **Random Forest Classifier** to estimate failure probability and classify engine health status.

---

## 📊 Dataset Features

The dataset includes the following parameters:

| Feature | Description |
|----------|--------------|
| Engine rpm | Engine rotational speed |
| Lub oil pressure | Lubrication system pressure |
| Fuel pressure | Fuel injection pressure |
| Coolant pressure | Cooling system pressure |
| Lub oil temp | Lubrication oil temperature |
| Coolant temp | Engine coolant temperature |
| Engine Condition | Target variable (0 or 1) |

---

## 🧠 Model Details

- **Algorithm:** Random Forest Classifier  
- **Class Handling:** `class_weight="balanced"`  
- **Train/Test Split:** 80/20  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix  

---

## ⚙️ Model Workflow
Sensor Data → Preprocessing → Random Forest → Failure Probability → Health Classification

---

## 📈 Health Classification Logic

The model predicts the probability of failure (class 1).

Health status is determined as:

| Failure Probability | Status |
|---------------------|--------|
| < 0.30 | GOOD |
| 0.30 – 0.70 | WARNING |
| > 0.70 | CRITICAL |

---

## Project Structure
├── engine_data.csv
├── training_notebook.ipynb
└── README.md
