# 🌟 Customer Satisfaction Prediction with Decision Tree Models

## 📁 Project Overview

This project applies decision tree classifiers to predict customer satisfaction using the **Santander Customer Satisfaction** dataset from Kaggle. The goal is to build, evaluate, and fine-tune decision tree models for classification tasks, optimizing their performance using metrics like ROC AUC, F1 score, and accuracy.

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

## 📂 Dataset Information

The dataset used in this project was obtained from the **Santander Customer Satisfaction** competition hosted on Kaggle.

### 📌 Dataset Overview

This dataset was provided by **Banco Santander**, a global financial institution, to help build models that identify dissatisfied customers. The challenge is a **binary classification** problem, where the goal is to predict the likelihood of customer dissatisfaction based on anonymized customer data.

- **Training Set**: Contains ~76,000 rows with 370+ anonymized numerical features and a target column.
- **Test Set**: Contains ~76,000 rows (same structure as training, but without the target column).
- **Target Variable**:  
  - `TARGET = 0`: Satisfied customer  
  - `TARGET = 1`: Unsatisfied customer (minority class)

### 🔍 Feature Structure

- All features are named generically (e.g., `var15`, `imp_ent_var16_ult1`), and no business meaning is provided for them.
- All values are numeric — no categorical or textual features.
- The dataset is highly **imbalanced**, with fewer than 5% of customers labeled as dissatisfied. This introduces a challenge in model evaluation and optimization.

### 🧪 Modeling Considerations

- **Class Imbalance**: Since the target class (dissatisfied customers) is rare, metrics like **ROC AUC** and **F1-score** are more informative than accuracy.
- **Feature Engineering**: No explicit feature names means that feature selection must rely entirely on data-driven methods like correlation, variance, and model-based importance.
- **Anonymized Data**: Limits the use of domain knowledge — forces the model to purely learn patterns from statistical behavior.

### ✅ Why This Dataset?

- Ideal for practicing **classification**, **hyperparameter tuning**, **model evaluation**, and **handling imbalanced data**.
- Common benchmark dataset for decision trees, ensemble models (Random Forest, XGBoost), and logistic regression.

---

## 🧠 Workflow Summary

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

## 🛠️ Tools & Technologies

- **Python**  
- **Pandas, NumPy** for data manipulation  
- **Scikit-learn** for modeling and metrics  
- **Matplotlib, Seaborn** for visualizations  
- **GridSearchCV** for model optimization  
- **Jupyter Notebook** for analysis

---

## 👤 About Me

Hi, I'm **Balbir Singh**, and I recently completed my Master’s in Business Analytics from Arizona State University in May 2025. I was awarded a **$5,000 International Scholarship** from ASU before starting the program.

During the program, I worked on projects involving forecasting, unstructured data, and decision modeling. I gained experience with tools like Python, SQL, Power BI, Tableau, and Excel, and I enjoy solving real-world problems using analytics and machine learning. Outside of work, I love swimming, sketching, volleyball, and exploring new places.

---

## 📝 Acknowledgment

Special thanks to **Kaggle** and **Banco Santander** for providing the dataset, and to **ASU W. P. Carey School of Business** for supporting this academic project.
