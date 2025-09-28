# Breast Cancer Prediction using Linear Regression

This is my first Machine Learning project using the Breast Cancer dataset from **scikit-learn**.  
The goal of this project is to build a Linear Regression model, evaluate it using cross-validation, and analyze its performance.

---

## Project Workflow

### 1. Import Libraries
The following libraries are used in this project:
- **numpy** → for numerical computations  
- **pandas** → for handling tabular data  
- **matplotlib & seaborn** → for visualization  
- **scikit-learn** → for dataset, preprocessing, model training, and evaluation  

---

### 2. Load Dataset
- The dataset is loaded from `sklearn.datasets` using `load_breast_cancer()`.  
- It contains **569 samples** and **30 numerical features** describing breast cancer tumors.  
- Target variable (`y`) → `0 = malignant`, `1 = benign`.

---

### 3. Convert to DataFrame
- The dataset is converted into a Pandas DataFrame for better readability.  
- Feature names from the dataset are assigned as column names.  

---

### 4. Split Features and Target
- **X (features):** The 30 tumor characteristics.  
- **y (target):** The diagnosis (malignant/benign).  

---

### 5. Train-Test Split
- The dataset is split into:
  - **80% Training Data**
  - **20% Testing Data**  
- `random_state=42` is used for reproducibility (ensures same split every time).  

---

### 6. Feature Scaling
- Linear Regression is sensitive to feature scales.  
- **StandardScaler** is applied:
  - Mean = 0  
  - Standard Deviation = 1  
- Both training and testing data are scaled.  

---

### 7. Train Linear Regression Model
- A **Linear Regression** model is created and trained using training data (`x_train`, `y_train`).  

---

### 8. Cross Validation
- **10-Fold Cross Validation** is applied.  
- Metric: **Negative Mean Squared Error (MSE)**  
- The mean MSE gives an overall estimate of model performance.  

---

### 9. Predictions
- The trained model predicts the values on the **test dataset**.  
- Residuals (difference between actual and predicted values) are plotted using a distribution plot.  

---

### 10. Evaluation using R² Score
- **R² Score** is calculated to evaluate model performance.  
- Interpretation:
  - **R² = 1:** Perfect predictions  
  - **R² = 0:** Model does not explain any variance  
  - **R² < 0:** Model is worse than a baseline mean predictor  

---

### 11. Conclusion
- Linear Regression provides a **baseline model** for this dataset.  
- Since the target variable is categorical (classification problem), **Logistic Regression or classification models** would be more appropriate.  
- This project demonstrates the complete ML workflow:
  1. Data Loading  
  2. Preprocessing  
  3. Model Training  
  4. Cross Validation  
  5. Evaluation & Visualization  

---

## Future Improvements
- Try **Logistic Regression** for better classification performance.  
- Experiment with **SVM, Random Forest, and Gradient Boosting**.  
- Add more **visualizations** for feature importance and correlations.  

---

## Files in this Repository
- `BreastCancer_LinearRegression.ipynb` → Jupyter Notebook with code + explanations  
- `README.md` → Project documentation  

---

## Author
**Mohd Umair**  
- Beginner Data Scientist | Learning ML, Python, and Data Analysis  
