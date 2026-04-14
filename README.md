# 🩺 Diabetes Risk Prediction using Machine Learning

A high-performance machine learning model to predict diabetes risk using clinical data from **100,000 patients**, with a strong focus on **feature engineering and real-world evaluation metrics**.

---

## 🚀 Key Results

* **ROC-AUC:** 0.98
* 
* **PR-AUC:** 0.89
* 
* **F1-Score:** 0.78
* 
* **Generalization Gap:** ~0.003

* **Precision:** 0.76

* **Recall:** 0.80

---

## 📂 Dataset

* **Size:** 100,000 patient records
* **Type:** Structured clinical dataset
* **Target:**

  * `0` → Non-diabetic
  * `1` → Diabetic

---

## 🛠️ Methodology

### Feature Engineering (Core Contribution)

* **Risk_Score:** Composite index combining BMI, Age, and Glucose
* **GlucoseAge:** Interaction feature capturing compounded risk effects

---

### Handling Class Imbalance

Two approaches were evaluated:

* **Version-A : SMOTE / SMOTE-NC (Synthetic Oversampling)**

* **Version-B : Cost-Sensitive Learning or without SMOTE / SMOTE-NC (Preferred)**


**Key Insight:**
Synthetic balancing improved class symmetry and precision, but **reduced recall for the minority class (diabetic patients)**—which is more critical in healthcare settings where missing positive cases is costly.

---

## 📊 Best Model Configurations

| Configuration | Precision | Recall   | F1-Score |
| ------------- | --------- | -------- | -------- |
| **Version A** | **0.92**     | **0.71** | **0.81**    |
| **Version B** | **0.76**  | **0.80**    | **0.78** |

---

## 🧪 Tech Stack

* **Language:** Python
  
* **Libraries:** Scikit-learn, Pandas, NumPy, Seaborn, Matplotlib, XGBoost 
  
* **Optimization:** RandomizedSearchCV with regularization tuning (Gamma, Alpha, Lambda)

---

## 🔍 Key Insights

* **Feature Engineering > Synthetic Data** for preserving meaningful clinical patterns
  
* **High PR-AUC (0.89)** indicates strong performance under class imbalance
  
* **Low generalization gap (~0.003)** suggests robust performance on unseen data

* **High Recall(0.80) (High Sensitivity)** indicates model is effective at identifying most of the actual positive cases, resulting in very few false negatives

---

## 🏥 Practical Impact

* Supports **early screening** of high-risk patients
  
* Helps reduce **false negatives**, critical in medical diagnosis
  
* Can assist clinicians in **prioritizing further testing**

---

## ⭐ Conclusion

This project demonstrates that **domain-driven feature engineering combined with cost-sensitive learning** can deliver reliable and clinically meaningful performance in imbalanced healthcare datasets.
