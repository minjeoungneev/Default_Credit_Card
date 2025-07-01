# Prediction on Credit Card Default

This project applies a **tree based algorithms** to predict a class label and compare performances, using **Default Credit Card dataset**. 

## 🧠 Background & Objective

Credit cards are one of the most popular loan products. Accurately predicting credit card holder's behavior could mitigate several risks such as asset losses, reputation, and operational risk. In this project, given six months of client's payment behavior, the goal is to build a predictive model to correctly classify the next month's payment status, whether the loan will default or not. 

In classification problem, we consider the confusion matrix. The components are 
* True Positive: model predicts default when customer defaults.
* True Negative: model predicts non-default when customer does not default.
* False Positive: model predicts default when customer does not default.
* False Negative: model predicts non-default when customer defaults.

From a financial institution's perspective, catching false negative is important, because the bank doesn't want to miss monitoring defaulting customers, causing risk in financial losses. False positive becomes more relevant with the bank's goal to invest limited resources to prevent defaults. Like this, the cost function of a model can vary depending on the context of the problem. In this case, the latter assumption is applied.

---

## 📊 Dataset

- **Dataset:** [Default of Credit Card Clients Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset/data)
- **Description:** 30,000 rows of information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

---

## 🧪 Procedure

- **1. Data Cleaning:**
  1. Removed 35 duplicated values.
  2. Regrouped mislabeled categorical variables.
  3. Fixed a variable name for consistency.

- **2. EDA:** explored features in relation to default status by bar plots, KDE plots, and correlation analysis.
  Findings include
  1. Target (default 22% /non-default 78%) is highly imbalanced -> I will perform various sampling techniques.
  2. People who are delayed in payment for 2+ months have higher default %.
  3. Male, lower education, and the married have higher default %
  4. Early 20s' have higher default %.
  5. Lower credit limit has higher default %.
  
- **3. Feature Engineering:**
  1. Created 'SEX_MAR' by combining SEX and MARRIAGE.
  2. Created 'PAY_RATIO_i' by dividing PAY_AMTi by BILL_AMTi.
  3. Created 'CREDIT_UTILIZATION_i' by dividing BILL_AMTi by LIMIT_BAL.
  4. Created 'AVG_EXP_i' by calculating average expense in proportion to LIMIT_BAL.
     --> Total 41 independent variables.
     
- **4. Feature Selection:**
  1. Feature importance using random forest classifier --> Total 33 independent variables selected.
 
- **5. Data Preprocessing:**
  1. Sampling
  2. Sampling - oversampling minority
  3. Sampling - undersampling majority
  4. SMOTE
  5. Scaling
     
- **6. Model Building:**
  1. **Bagging**: Random Forest Classifier
  2. **Boosting**: AdaBoost, Gradient Boosting Machine (GBM), Light GBM

- **7. Performance Metric:**
Each model was evaluated based on F1 Score, Accuracy, Precision, Recall, and Miss Rate (1 - Recall).

---

## 🧰 Tools & Libraries

- Python 3.13.3
- Numpy, Pandas for data manipulation
- Seaborn, Matplotlib for visualization  
- Sklearn for data preprocessing and modeling
---

## 📈 Results Summary

- Best performance achieved with: LightGBM model trained on SMOTE processed data.
> F1 score: **0.75**
> Test accuracy: **0.72**
> Precision: **0.68**
> Recall: **0.84**
> Miss Rate: **0.16**



---

---

## 🚀 How to Run

You can run the notebook directly in **[Google Colab](https://colab.research.google.com/)** or locally:

1. Clone the repo  
   `git clone https://github.com/yourusername/MNST-Classification.git`

2. Open `DNN_MNST_Classification.ipynb` in Jupyter or Colab

3. Run all cells to train the model

---

## 📌 Learnings

- Importance of tuning hidden units and optimizers for faster convergence
- Impact of activation functions on performance and training stability
- How batch size affects noise vs. convergence speed

---

## 🧠 Author

**Minjeoung Neev**  
Graduate student passionate about machine learning & data science  
📧 laminjon@gmail.com

---

## 📜 License

This project is under the MIT License. Feel free to fork and experiment!

