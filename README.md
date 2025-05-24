# 🌾 Seed Classification using OLS Regression

## 📌 Overview

This project explores the use of **Ordinary Least Squares (OLS)** regression to classify three varieties of wheat seeds using a subset of features from the UCI Seeds dataset. While OLS is traditionally a regression method, it is evaluated here for its interpretability and statistical significance in feature selection for classification tasks.

---

## 🎓 Academic Context

This project was completed as part of the **Statistical Learning** course in the **Master of Data Science** program at the **Illinois Institute of Technology**. It demonstrates foundational modeling, hypothesis testing, and analysis techniques for supervised learning using real-world datasets.

---

## 📊 Dataset

* **Source**: [UCI Machine Learning Repository – Seeds Dataset](https://doi.org/10.24432/C5H30K)
* **Samples**: 210 seed observations (70 per class)
* **Classes**: Kama, Rosa, Canadian
* **Features**:

  * Area (A)
  * Perimeter (P)
  * Compactness (C) = 4πA / P²
  * Length of Kernel
  * Width of Kernel
  * Asymmetry Coefficient
  * Length of Kernel Groove

The original labels (1 = Kama, 2 = Rosa, 3 = Canadian) were mapped to species names and one-hot encoded for regression-based classification.

---

## 📓 Dataset Preparation

* **Header Fix**: Dataset lacked headers; corrected using `header=None`
* **Delimiter Issue**: Corrected tab misalignment using `delim_whitespace=True`
* **Target Encoding**: Integer labels were mapped to class names, then one-hot encoded
* **Train/Test Split**: 70/30 split using `train_test_split` from scikit-learn

---

## 🤹 Feature Selection

Feature importance was first evaluated using a **Random Forest** model. Pairwise plots were also created to visually inspect class separability. Based on these, the two most influential features—**Area** and **Length of Kernel Groove**—were selected for the primary OLS model.

---

## 🚀 Model Implementation

* **One-hot Encoding**: Converted categorical target into 3 binary columns
* **OLS Regression**: Built using `LinearRegression()` from scikit-learn
* **Prediction Logic**: The class with the highest predicted value among the three regression outputs was selected as the final class

---

## ✅ Results

* **Accuracy**: 92.06%
* **Coefficients**:

  * Length of Kernel Groove: **2.172**
  * Area: **0.4126**
* **Rosa**: Easiest to classify (Precision = 1.00, Recall = 0.96)
* **Kama**: Most misclassifications (Precision = 0.85, Recall = 0.89)
* **Statistical Significance**: p-values near zero for predictors; F-statistic p = **1.32e-22**

---

## 🔍 Evaluation Insights

* OLS R² value = 0.504 (low due to categorical output)
* Accuracy, precision, recall better indicators for this classification task
* Macro, micro, and weighted metrics were similar, showing no class imbalance bias

---

## ⚠️ Limitations

* Small dataset (210 observations)
* Only two predictors used in main model
* Logistic regression would be more appropriate for classification
* Full 7-feature model (in code only) achieved 100% accuracy but lacks generalizability

---

## 🚀 Future Improvements

* Apply logistic regression or ensemble classifiers
* Use cross-validation
* Try 3–4 best predictors to balance simplicity and performance

---

## 💬 Reflections

> I initially underestimated how much effort the written report would take, even though the code was completed weeks earlier. This project pushed me to think more critically about model interpretation and report clarity. Using JupyterLab with extensions like Spellcheck and Variable Inspector helped manage variables and structure. I also learned a lot about data cleaning (e.g., fixing misaligned tabs), one-hot encoding, and the importance of understanding dimensionality and formatting.

> This wasn’t just about getting a working model, but about clearly communicating what the model means and how to assess its performance. That shift in mindset was a major learning moment for me.

---

## 🚧 How to Run This Project

1. Clone the repository
2. Open the `.ipynb` file in JupyterLab or Jupyter Notebook
3. Install dependencies via `pip install -r requirements.txt`
4. Run cells sequentially

---

## 📚 Citation

Charytanowicz, M., Niewczas, J., Kulczycki, P., Kowalski, P., & Łukasik, S. (2010). *Seeds Dataset*. UCI Machine Learning Repository. [https://doi.org/10.24432/C5H30K](https://doi.org/10.24432/C5H30K)

---
Repository. https://doi.org/10.24432/C5H30K

---

