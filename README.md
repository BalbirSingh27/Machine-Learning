
# 🌟 Customer Satisfaction Prediction with Decision Tree Models

## 📁 Project Overview

This project applies decision tree classifiers to predict customer satisfaction using the **Santander Customer Satisfaction dataset**. The goal is to build, evaluate, and fine-tune decision tree models for classification tasks, optimizing their performance using metrics like ROC AUC, F1 score, and accuracy.

---

## 🎯 Objectives

- Load and explore the dataset to understand its structure and quality.
- Select relevant features based on correlation with the target.
- Train decision tree models with various hyperparameters.
- Evaluate performance using confusion matrix, F1 score, ROC AUC, and accuracy.
- Use **GridSearchCV** for hyperparameter tuning.
- Compare results across multiple tuning iterations.
- Generate CSV submission files with predictions.

---

## 🛠️ Tools & Technologies

- **Python**  
- **Pandas, NumPy** for data manipulation  
- **Scikit-learn** for modeling and metrics  
- **Matplotlib, Seaborn** for visualizations  
- **GridSearchCV** for model optimization

---

## 🔍 Workflow Summary

1. **Data Loading**
   - Loaded training and test datasets using `pandas.read_csv()`.

2. **Exploratory Data Analysis (EDA)**
   - Checked for missing values.
   - Reviewed data types and summary stats.
   - Analyzed target variable distribution.
   - Computed feature correlations.

3. **Feature Selection**
   - Retained only features with strong correlation to the target.
   - Excluded noise features (correlation < 0.1).

4. **Model Training**
   - Trained multiple decision tree models using different hyperparameters.

5. **Model Evaluation**
   - Evaluated models using accuracy, F1 score, ROC AUC score, and confusion matrix.
   - Compared model performance in structured tables.

6. **Hyperparameter Tuning**
   - Applied GridSearchCV to find optimal parameters like `max_depth`, `criterion`, `class_weight`, and `min_samples_leaf`.
   - Re-trained models with tuned settings and re-evaluated.

7. **Result Comparison**
   - Compared performance between:
     - Initial models
     - First tuning
     - Second tuning
   - Exported results as CSV for documentation.

8. **Submission**
   - Created final `.csv` file for test set predictions (probabilities of satisfaction).

---

## 📈 Key Outcomes

- Significant improvement in model performance after tuning.
- ROC AUC used as the primary metric for hyperparameter optimization.
- Multiple CSV files generated to compare model iterations and prepare submission-ready outputs.

---

## 👨‍💻 Author

**Balbir Singh**  
MS Business Analytics – Arizona State University  
Email/contact optional here

---

## 📝 Acknowledgment

Thanks to Santander and ASU W. P. Carey School of Business for the data and opportunity to explore decision tree modeling techniques.
