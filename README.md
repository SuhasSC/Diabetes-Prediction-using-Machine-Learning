# 🩸 Diabetes Prediction using Machine Learning

This project uses various **machine learning algorithms** to predict whether a patient has diabetes based on medical diagnostic features.  
The dataset used is the **Pima Indians Diabetes Database** from the National Institute of Diabetes and Digestive and Kidney Diseases.



## 📌 Objective
To build a machine learning model that can **accurately predict diabetes** based on patient health data such as glucose level, BMI, insulin, age, and more.


## 📊 Dataset Details

| Feature | Description |
|----------|-------------|
| **Pregnancies** | Number of times pregnant |
| **Glucose** | Plasma glucose concentration after 2 hours |
| **BloodPressure** | Diastolic blood pressure (mm Hg) |
| **SkinThickness** | Triceps skinfold thickness (mm) |
| **Insulin** | 2-Hour serum insulin (mu U/ml) |
| **BMI** | Body mass index (kg/m²) |
| **DiabetesPedigreeFunction** | Diabetes pedigree function |
| **Age** | Age (years) |
| **Outcome** | 0 = Non-diabetic, 1 = Diabetic |

- **Total Records:** 768  
- **Target Variable:** Outcome  
- **Classes:** 0 (No Diabetes), 1 (Diabetes)



## ⚙️ Steps in the Project

1. **Exploratory Data Analysis (EDA):**
   - Distribution plots, correlation heatmap, outlier analysis  
   - Class balance visualization

2. **Data Preprocessing:**
   - Missing value handling (replaced with median by outcome)
   - Outlier removal using IQR and LOF
   - Feature scaling using RobustScaler

3. **Feature Engineering:**
   - New categorical features for BMI, Insulin, and Glucose
   - One-Hot Encoding for categorical variables

4. **Model Training and Comparison:**
   - Tested models:
     - Logistic Regression  
     - KNN  
     - SVM  
     - Decision Tree  
     - Random Forest  
     - XGBoost  
     - LightGBM  
   - Evaluated using **10-fold Cross Validation**

5. **Hyperparameter Tuning:**
   - GridSearchCV used for tuning Random Forest, XGBoost, and LightGBM  
   - Final best model achieved **~90% accuracy**

6. **Feature Importance Visualization:**
   - Bar plots showing the most influential medical parameters.



## 🧠 Best Model
- **Model:** XGBoost Classifier (after hyperparameter tuning)  
- **Cross Validation Score:** ~0.90  
- **Most Important Features:** Glucose, BMI, Age, Insulin


## 🧩 Requirements
Install the following Python libraries before running:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn lightgbm xgboost missingno
