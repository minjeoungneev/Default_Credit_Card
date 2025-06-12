# Prediction on Credit Card Default

This project applies a **tree based algorithms** to classify handwritten digits from the **Default Credit Card dataset**. 

## 🧠 Objective

To build and evaluate a basic deep learning model for digit recognition, while learning how a single layer activates neurons and a different number of features influences classification accuracy.

---

## 📊 Dataset

- **Dataset:** [Default of Credit Card Clients Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset/data)
- **Description:** 30,000 rows of information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

---

## 🧪 Experiments

The following model configurations were tested:

- **Hidden units:** 1, 2, 8, 16, 32, 64, 128, 256
- **Feature Selection:** PCA, Random Forest Classifier
- **Activation functions:** ReLU, Softmax 
- **Optimizers:** root mean squared propagation (rmsprop)
- **Batch sizes:** 32
- **Epochs:** Up to 50 (with early stopping)

Each configuration was evaluated based on validation accuracy and test accuracy.

---

## 🧰 Tools & Libraries

- Python 3.13.3
- TensorFlow / Keras  
- NumPy, Matplotlib for visualization  

---

## 📈 Results Summary

- Best performance achieved with:
  - **256 hidden neurons**
  - **ReLU activation**
  - **rmsprop optimizer**
  - **Batch size of 32**
  - **Full 784 Features**

> Final test accuracy: **0.9699**

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
Graduate student passionate about deep learning & data science  
📧 laminjon@gmail.com

---

## 📜 License

This project is under the MIT License. Feel free to fork and experiment!

