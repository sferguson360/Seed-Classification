# 🌾 Seed Classification using OLS Regression

## 📌 Overview  
This project explores the use of **Ordinary Least Squares (OLS)** regression to classify three varieties of wheat seeds using a subset of features from the UCI Seeds dataset. While OLS is traditionally a regression method, it is evaluated here for its interpretability and statistical significance in feature selection for classification tasks.

---

## 🎓 Academic Context  
This project was completed as part of the **Statistical Learning** course in the **Master of Data Science** program at the **Illinois Institute of Technology**. It demonstrates foundational modeling, hypothesis testing, and analysis techniques for supervised learning using real-world datasets.

---

## 📊 Dataset  
- **Source**: [UCI Machine Learning Repository – Seeds Dataset](https://doi.org/10.24432/C5H30K)  
- **Samples**: 210 seed observations  
- **Target Classes**: Kama, Rosa, Canadian  
- **Original Features**: 7 geometrically derived attributes (e.g., area, length, compactness, groove length)

---

## 🎯 Objective  
To assess the predictive power of two selected features—**length of kernel groove** and **area**—in classifying seed varieties using OLS regression, and to evaluate the trade-offs between model simplicity and performance.

---

## 🛠 Tools & Environment  
- **Language**: Python  
- **IDE**: JupyterLab (with Spellcheck & Variable Inspector extensions)  
- **Libraries**:  
  - `pandas`, `numpy` – data wrangling  
  - `matplotlib`, `seaborn` – visualization  
  - `sklearn`, `statsmodels` – modeling and statistical inference  

---

## 🔍 Methodology  
- **Feature Selection**: Based on significance (p-values) and coefficient magnitude  
- **Modeling**: OLS Regression used for interpretability  
- **Classification Evaluation**:  
  - Accuracy  
  - Precision, Recall (Macro, Micro, Weighted)  
  - Confusion Matrix Analysis  

---

## ✅ Results  
- **Accuracy**: 92.06%  
- **Key Coefficients**:  
  - `length_of_kernel_groove`: **2.172**  
  - `area`: **0.4126**  
- **Precision & Recall**:  
  - Rosa: Precision = 1.00, Recall = 0.96  
  - Kama: Precision = 0.85, Recall = 0.89  
- **Statistical Significance**:  
  - All predictors used had near-zero p-values  
  - Model F-statistic p-value: **1.32e-22**

---

## 💡 Insights  
- **Interpretability**: Length of kernel groove was more influential than area  
- **Model Fairness**: Similar macro/micro/weighted scores suggest balanced class performance  
- **Performance Caveat**: OLS R² value of 0.504 is less relevant for classification accuracy, highlighting the importance of using proper classification metrics  

---

## ⚠️ Limitations  
- Small dataset (210 samples)  
- Only 2 features used in main model; full 7-feature OLS achieved 100% accuracy  
- OLS is not a classification model; **logistic regression** would be more appropriate in practice  

---

## 🚀 Future Improvements  
- Use **logistic regression** or ensemble methods (e.g., random forest)  
- Implement **cross-validation**  
- Expand feature set to 3–4 variables for balance between performance and complexity  

---

## 💬 Reflections  
> This project taught me the real challenge isn't writing the code — it's explaining it clearly. I initially underestimated the effort required to structure and write the report. Using JupyterLab with helpful extensions like Spellcheck and Variable Inspector helped me stay organized.  
>  
> I also learned the importance of variable naming, reproducibility, error handling, and documentation. Although I had the analysis done early, the reporting process forced me to truly understand each step, making this a valuable learning experience.  

---

## 🧠 How to Run This Project  
1. Clone the repo  
2. Open the `.ipynb` file in JupyterLab or Jupyter Notebook  
3. Install required libraries via `pip install -r requirements.txt`  
4. Run cells sequentially  

---

## 📚 Citation  
Charytanowicz, M., Niewczas, J., Kulczycki, P., Kowalski, P., & Łukasik, S. (2010). *Seeds Dataset*. UCI Machine Learning Repository. https://doi.org/10.24432/C5H30K

---

