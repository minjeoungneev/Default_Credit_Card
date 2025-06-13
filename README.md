# Prediction on Credit Card Default

This project applies a **tree based algorithms** to correctly predict whether a credit card customer will default or not in the 7th month of the given dataset, **Default Credit Card dataset**. 

## 🧠 Objective

Credit cards are one of the most popular loan products. Accurately predicting credit card holder's behavior could mitigate several risks such as asset losses, reputation, and operational risk. In this project, given six months of client's payment behavior, the goal is to build a predictive model to correctly classify the next month's payment status, whether the loan will default or not. 

In classification problem, we consider confusion matrix. The components are 
* True Positive: model predicts default when customer defaults.
* True Negative: model predicts non-default when customer does not default.
* False Positive: model predicts default when customer does not default.
* False Negative: model predicts non-default when customer defaults.

From a financial institution's perspective, catching false negative is important, because we don't want to miss monitoring defaulting customers, causing risk in financial losses. False positive becomes more relevant with the bank's goal to invest limited resources to prevent defaults. Like this, the cost function of a model can vary depending on the problem context. In this case, the latter assumption is applied.

---

## 📊 Dataset

- **Dataset:** [Default of Credit Card Clients Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset/data)
- **Description:** 30,000 rows of information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

---

## 🧪 Experiments

The following models were tested:

- **Random Forest:** 
- **AdaBoost:** 
- **XGBoost:** 
- **CatBoost:** 
- **LightGBM:**


Each model was evaluated based on ___.

---

## 🧰 Tools & Libraries

- Python 3.13.3
-   
- NumPy, Matplotlib for visualization  

---

## 📈 Results Summary

- Best performance achieved with:
  - **256 hidden neurons**


> Final test accuracy: **0.**

Visualizations include training/validation accuracy plots and confusion matrix of final predictions.

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

