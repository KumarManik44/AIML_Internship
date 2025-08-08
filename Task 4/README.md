# 🩺 Breast Cancer Classification with Logistic Regression

A comprehensive binary classification project using logistic regression to predict breast cancer diagnosis (malignant vs benign) with **96.49% accuracy** and **ROC-AUC of 0.9960**.

## 📊 Project Overview

This project implements a complete machine learning pipeline for breast cancer classification using the Wisconsin Breast Cancer Dataset. The model demonstrates excellent performance with practical medical applications.

### 🎯 Key Results
- **Test Accuracy**: 96.49%
- **ROC-AUC Score**: 0.9960 (Near Perfect)
- **Precision**: 97.50%
- **Recall**: 92.86%
- **Clinical Performance**: Only 1 missed cancer case with optimized threshold

## 🔬 Dataset Information

- **Source**: Wisconsin Breast Cancer Dataset (Kaggle)
- **Samples**: 569 patients
- **Features**: 30 numerical features (mean, standard error, and worst values)
- **Target**: Binary classification (Malignant=1, Benign=0)
- **Class Distribution**: 62.7% Benign, 37.3% Malignant

### Most Predictive Features
1. Concave points (worst)
2. Perimeter (worst)  
3. Concave points (mean)
4. Radius (worst)
5. Perimeter (mean)

## 🛠️ Technical Implementation

### Data Preprocessing
- ✅ Removed unnecessary columns (ID, empty columns)
- ✅ Converted categorical target to binary (M→1, B→0)
- ✅ Train-test split (80-20) with stratification
- ✅ Feature standardization using StandardScaler

### Model Architecture
- **Algorithm**: Logistic Regression
- **Regularization**: Default L2 regularization
- **Solver**: lbfgs (default)
- **Max Iterations**: 1000

### Advanced Analysis
- **ROC Curve Analysis**: Visualized model performance
- **Sigmoid Function Explanation**: Mathematical interpretation
- **Threshold Tuning**: Optimized for medical applications (0.3 threshold)
- **Feature Correlation Analysis**: Identified most predictive biomarkers

## 📈 Model Performance

| Metric | Score |
|--------|--------|
| Accuracy | 96.49% |
| Precision | 97.50% |
| Recall | 92.86% |
| F1-Score | 95.12% |
| ROC-AUC | 0.9960 |
| Specificity | 98.61% |

### Confusion Matrix (Test Set)
```
                 Predicted
                 Benign  Malignant
Actual Benign      71       1
       Malignant    3      39
```

## 🔍 Threshold Analysis

| Threshold | Precision | Recall | F1-Score | Missed Cancer Cases |
|-----------|-----------|---------|----------|-------------------|
| 0.3 | 97.6% | 97.6% | **97.6%** | **1** ⭐ |
| 0.4 | 97.6% | 95.2% | 96.4% | 2 |
| 0.5 | 97.5% | 92.9% | 95.1% | 3 |
| 0.6 | 100.0% | 90.5% | 95.0% | 4 |
| 0.7 | 100.0% | 90.5% | 95.0% | 4 |

**Optimal Threshold**: 0.3 (minimizes false negatives for medical safety)

## 📁 Project Structure

```
breast-cancer-classification/
├── Task_4.ipynb
├── data.csv
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- Jupyter Notebook

### Installation

1. Clone the repository:
```bash
git clone https://github.com/kumarmanik44/Task_4.git
cd breast-cancer-classification
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the dataset:
   - Download `data.csv` from Kaggle: Wisconsin Breast Cancer Dataset

4. Run the notebook:
```bash
jupyter notebook notebook/breast_cancer_classification.ipynb
```

## 💡 Key Insights

### Medical Significance
- **Early Detection**: Model achieves high recall (92.86%) for cancer detection
- **False Negatives**: Minimized through threshold optimization (critical in medical diagnosis)
- **Feature Importance**: Concave points and perimeter measurements are strongest predictors

### Technical Insights
- **Sigmoid Function**: Converts linear combinations to probabilities [0,1]
- **Feature Scaling**: Critical for logistic regression performance
- **Threshold Tuning**: Can optimize for specific medical priorities (sensitivity vs specificity)

## 📊 Visualizations

The project includes comprehensive visualizations:
- ROC Curve demonstrating near-perfect performance
- Sigmoid function explanation for logistic regression
- Feature correlation heatmap
- Confusion matrix analysis
- Threshold optimization charts

## 🔄 Future Improvements

- [ ] Implement cross-validation for more robust evaluation
- [ ] Feature selection techniques (Recursive Feature Elimination)
- [ ] Ensemble methods (Random Forest, Gradient Boosting)
- [ ] Deep learning approaches
- [ ] Hyperparameter tuning with GridSearchCV

## 📖 References

1. Wisconsin Breast Cancer Dataset - UCI Machine Learning Repository
2. Scikit-learn Documentation
3. "Logistic Regression for Medical Data" - Medical ML Best Practices


## 🙏 Acknowledgments

- Wisconsin Breast Cancer Dataset contributors
- Scikit-learn community
- Kaggle for hosting the dataset

---

⭐ **If you found this project helpful, please consider giving it a star!**
