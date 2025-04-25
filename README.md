# 🔍 Financial Fraud Detection in Mobile Payments

## 🧠 Project Overview
This project addresses the urgent need for reliable fraud detection in mobile transactions. Using a dataset of **6.3 million+ records**, we applied various machine learning and deep learning techniques to identify fraudulent transactions and reduce financial risk.

- 📌 **Course**: Data 606 – Capstone in Data Science  
- 🏛️ **Institution**: University of Maryland, Baltimore County (UMBC)  
- 👥 **Team**: Bala Sai Santhoshi, Revanth Kumar, Karthik Reddy  
- 🎓 **Instructor**: Prof. Unal Sakoglu  

## 🎯 Objective

- Identify and understand fraud patterns in mobile transactions  
- Apply classification models for fraud prediction  
- Use **SMOTE** and **downsampling** to handle class imbalance  
- Compare and tune multiple models for high-performance detection 

## 🗃️ Dataset

- **Source**: [Kaggle]
- **Size**: 6,362,620 records, 11 attributes  
- **Target**: `isFraud` (Binary: 0 = Non-fraud, 1 = Fraud)  
- **Note**: Only a **sample of the dataset** is uploaded due to GitHub's 100MB file limit. Full dataset available [here](#) or upon request.

## 📊 Exploratory Data Analysis (EDA)

- Most frequent transaction types: `CASH_OUT`, `PAYMENT`
- Fraud is most common in **low-amount transactions**
- High correlation between:
  - `oldbalanceDest` & `newbalanceDest` (0.97)
  - `amount` & `isFraud` (0.35)
- Applied both **univariate** and **bivariate** analysis for insights

## ⚙️ Data Preprocessing

- Dropped missing values  
- One-hot encoded categorical variables  
- Normalized numerical features  
- Tackled class imbalance using:
  - ✅ **SMOTE (Synthetic Oversampling)**
  - ✅ **Downsampling (100k samples from non-fraud class)**
 
## 🤖 Machine Learning Models

| Model                      | Key Points                                              |
|---------------------------|----------------------------------------------------------|
| Logistic Regression        | Baseline classifier, tuned using GridSearchCV           |
| Random Forest              | High performance with imbalanced data                   |
| XGBoost                    | Gradient boosting, handled class weights well           |
| Sequential Neural Network  | ⭐ Best model – high recall & accuracy                   |
| CatBoost / LightGBM        | Fast, scalable, good results with boosting              |
| Ensemble / Stacking        | Combined predictions from top-performing models         |
| Others Tested              | SVM, KNN, Naive Bayes, Extra Trees, MLP, AdaBoost    

## Visuals
<img width="453" alt="image" src="https://github.com/user-attachments/assets/d3376d93-fea6-4d4c-b4fd-95df91714daa" />
 ## 🧮 Confusion Matrix – Neural Network (Best Model)
This matrix shows the classification performance of your tuned Sequential Neural Network, specifically how well it identifies fraud:
✅ True Positives (Fraud detected): 45
❌ False Positives (Non-fraud flagged as fraud): 3,787
✅ True Negatives: 16,214
❌ False Negatives (Fraud missed): 4
This matrix emphasizes the model's high recall and minimal missed fraud cases — a key achievement!


## 📈 Performance Summary

- **🏆 Best Model**: Fine-tuned Sequential Neural Network
  - Accuracy: 96.5%
  - High Recall: Detected most fraudulent transactions
  - Minimal False Negatives
- **Random Forest**: F1-Score ~99.7%
- **XGBoost / CatBoost**: Robust and consistent with low overfitting

  ## 🧪 Evaluation Metrics
  
- ROC-AUC 📈  
- Confusion Matrix 📉

  ## 🔮 Key Insights

- **Fraudulent transactions** cluster around small transaction amounts
- **Time steps** (e.g., Step 212) show pattern concentration for fraud
- **SMOTE and downsampling** greatly improve model sensitivity
- **Ensemble methods** provide better generalization & robustness

## 👥 Team & Contributions

| Member               | Contributions                                 |
|----------------------|-----------------------------------------------|
| Bala Sai Santhoshi   | Data preprocessing, model training,EDA, reporting, visualizations,Feature engineering, evaluation metrics  |
| Revanth Kumar        
| Karthik Reddy        

