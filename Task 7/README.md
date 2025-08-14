# 🎯 Support Vector Machine (SVM) for Breast Cancer Classification

A comprehensive implementation of Support Vector Machines for binary classification of breast cancer diagnosis using the Wisconsin Breast Cancer Dataset.

## 📋 Project Overview

This project demonstrates the application of both linear and non-linear SVM kernels for medical diagnosis classification, achieving **98.25% accuracy** on the test dataset. The implementation includes thorough data preprocessing, hyperparameter optimization, cross-validation, and decision boundary visualization.

## 🚀 Key Features

- **Dual Kernel Implementation**: Linear and RBF (Radial Basis Function) kernels
- **Interactive Visualizations**: 2D decision boundary plots with support vectors
- **Hyperparameter Optimization**: Grid search with 5-fold cross-validation
- **Comprehensive Evaluation**: Confusion matrices, classification reports, and statistical analysis
- **Medical Context**: Optimized for minimizing false negatives in cancer diagnosis

## 📊 Results Summary

| Model | Test Accuracy | CV Score | Key Characteristics |
|-------|---------------|----------|-------------------|
| **Linear SVM (Optimized)** | **98.25%** | 96.70 ± 0.70% | Highest accuracy, C=0.1 |
| **RBF SVM (Optimized)** | 97.37% | 97.14 ± 0.54% | Most consistent, C=1, γ=scale |
| Linear SVM (2D) | 95.61% | - | Visualization purpose |
| RBF SVM (2D) | 95.61% | - | Visualization purpose |

## 🛠️ Technologies Used

- **Python 3.8+**
- **Scikit-learn**: SVM implementation and model evaluation
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development environment

## 📁 Project Structure

```
svm-breast-cancer-classification/
│
├── README.md                     # Project documentation
├── requirements.txt              # Python dependencies
├── Task_7.ipynb                  # Main Jupyter notebook
├── breast_cancer.csv             # Dataset

```

## 🔧 Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/svm-breast-cancer-classification.git
cd svm-breast-cancer-classification
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Download the dataset:**
   - Download the Wisconsin Breast Cancer Dataset from [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
   - Place `breast_cancer.csv` in the `data/` directory

4. **Run the notebook:**
```bash
jupyter notebook SVM_Breast_Cancer_Classification.ipynb
```

## 📈 Key Methodologies

### Data Preprocessing
- **Feature Selection**: Identified top 2 most correlated features for visualization
- **Standardization**: Applied StandardScaler for optimal SVM performance
- **Train-Test Split**: 80-20 stratified split maintaining class balance

### Model Training
- **Linear Kernel**: Optimal hyperparameter C=0.1
- **RBF Kernel**: Optimal hyperparameters C=1, gamma='scale'
- **Cross-Validation**: 5-fold stratified validation for robust evaluation

### Evaluation Metrics
- **Accuracy**: Primary metric for model comparison
- **Precision/Recall**: Critical for medical diagnosis applications
- **Confusion Matrix**: Detailed error analysis
- **Support Vector Analysis**: Model complexity assessment

## 🎯 Business Impact

- **Clinical Relevance**: 98%+ accuracy suitable for clinical decision support
- **False Negative Minimization**: Only 2 false negatives in optimized linear model
- **Interpretability**: Linear kernel provides clear feature importance insights
- **Scalability**: Efficient implementation suitable for real-time diagnosis

## 📊 Visualizations

The project includes comprehensive visualizations:

1. **Decision Boundaries**: 2D plots showing linear vs non-linear classification boundaries
2. **Support Vectors**: Visual identification of critical data points
3. **Performance Metrics**: Confusion matrices and classification reports
4. **Feature Analysis**: Correlation analysis and feature importance

## 🏆 Key Insights

- **Linear SVM Excellence**: Achieved highest test accuracy on this linearly separable problem
- **Feature Scaling Importance**: Standardization crucial for optimal SVM performance
- **Medical Applications**: Demonstrated excellent performance for binary medical classification
- **Model Interpretability**: Linear kernel provides better explainability for medical professionals

## 📝 Future Enhancements

- [ ] Implementation of polynomial kernel
- [ ] Feature importance analysis using SHAP values
- [ ] Ensemble methods combining multiple kernels
- [ ] Real-time prediction API development
- [ ] Integration with medical imaging data

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.


## 🙏 Acknowledgments

- UCI Machine Learning Repository for the Wisconsin Breast Cancer Dataset
- Scikit-learn community for excellent documentation and tools
- Kaggle for hosting the dataset and providing a collaborative platform

## 📚 References

1. Dua, D. and Graff, C. (2019). UCI Machine Learning Repository. University of California, Irvine, School of Information and Computer Sciences.
2. Cortes, C., & Vapnik, V. (1995). Support-vector networks. Machine learning, 20(3), 273-297.
3. Scikit-learn: Machine Learning in Python, Pedregosa et al., JMLR 12, pp. 2825-2830, 2011.

---

⭐ If you found this project helpful, please consider giving it a star!
