# Asthma Disease Prediction Using Machine Learning

## Project Overview

This project explores the application of machine learning algorithms for asthma disease classification. The objective is to develop and compare different classification models based on demographic, lifestyle, environmental, clinical, and respiratory features.

The project includes exploratory data analysis, data preprocessing, feature scaling, model development, and performance evaluation.

## Dataset

**Dataset:** Asthma Disease Dataset  
**Source:** Kaggle

The dataset contains patient information across 29 columns, including:

- Demographic features such as age, gender, and ethnicity
- Lifestyle factors such as smoking, physical activity, diet quality, and sleep quality
- Environmental exposures such as pollution, pollen, and dust
- Medical history, including allergies, eczema, and family history of asthma
- Lung function measurements, including FEV1 and FVC
- Respiratory symptoms such as wheezing, coughing, and shortness of breath
- Asthma diagnosis (target variable)

No missing values were identified during the initial data inspection.

## Methodology

### 1. Exploratory Data Analysis

Performed exploratory data analysis to understand the dataset and examine feature distributions.

- Age distribution using histograms and KDE curves
- Gender distribution using count plots
- Feature correlation analysis using a correlation heatmap

### 2. Data Preprocessing

- Removed `PatientID` and `DoctorInCharge` columns.
- Separated the independent variables and target variable (`Diagnosis`).
- Split the dataset into training (80%) and testing (20%) sets.
- Applied `StandardScaler` for feature standardization.

### 3. Machine Learning Models

Implemented and compared six classification algorithms:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. Support Vector Machine (SVM)
5. XGBoost
6. K-Nearest Neighbors (KNN)

### 4. Model Evaluation

Evaluated model performance using:

- Accuracy
- Receiver Operating Characteristic Area Under the Curve (ROC-AUC)

## Results

The following table presents the classification results obtained on the test dataset.

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 95.20% | 0.523 |
| Random Forest | 95.20% | 0.416 |
| Gradient Boosting | 94.99% | 0.440 |
| Support Vector Machine | 95.20% | 0.505 |
| XGBoost | 95.20% | 0.403 |
| K-Nearest Neighbors | 95.20% | 0.542 |

**Observation:** All six models achieved approximately 95% accuracy. However, their ROC-AUC scores remained relatively low, which indicates that accuracy alone does not adequately represent their classification performance. Further investigation of class distribution and class-specific prediction performance is necessary.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost



## Future Improvements

- Investigate class imbalance and its effect on model performance.
- Perform hyperparameter optimization using GridSearchCV.
- Evaluate models using precision, recall, F1-score, and confusion matrices.
- Analyze feature importance and the contribution of individual predictors.
- Explore techniques to improve the models' ability to identify asthma-positive cases.

## Disclaimer

This project is intended for educational and research purposes only. The models have not been clinically validated and should not be used for medical diagnosis or treatment decisions.
