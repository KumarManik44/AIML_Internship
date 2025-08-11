# Heart Disease Prediction using Decision Trees and Random Forests

A comprehensive machine learning project analyzing heart disease prediction using tree-based models. This project demonstrates systematic model development, overfitting analysis, and ensemble methods.

## 🎯 Project Objectives

- Train and visualize Decision Tree classifiers
- Analyze overfitting behavior and control tree depth
- Implement Random Forest for improved performance
- Compare feature importances across models
- Evaluate models using cross-validation

## 📊 Dataset

- **Source**: Heart Disease Dataset (heart.csv) from Kaggle
- **Size**: 1,025 samples with 13 features
- **Target**: Binary classification (0: No Disease, 1: Disease)
- **Balance**: Well-balanced dataset (51.3% disease, 48.7% no disease)

### Features
- `age`: Age of the patient
- `sex`: Gender (1 = male, 0 = female)
- `cp`: Chest pain type (0-3)
- `trestbps`: Resting blood pressure
- `chol`: Cholesterol level
- `fbs`: Fasting blood sugar > 120 mg/dl
- `restecg`: Resting electrocardiographic results
- `thalach`: Maximum heart rate achieved
- `exang`: Exercise induced angina
- `oldpeak`: ST depression induced by exercise
- `slope`: Slope of peak exercise ST segment
- `ca`: Number of major vessels colored by fluoroscopy
- `thal`: Thalassemia type

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/heart-disease-prediction.git
cd heart-disease-prediction
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the dataset:
   - Download `heart.csv` from Kaggle
   - Place it in the project root directory

## 🚀 Usage

Run the Jupyter notebook step by step:

```bash
jupyter notebook Task_5.ipynb
```

The notebook is structured in 11 cells covering:
1. Library imports
2. Data loading and exploration
3. Target distribution analysis
4. Data preparation and train-test split
5. Initial Decision Tree training
6. Tree visualization
7. Overfitting analysis with different depths
8. Random Forest training
9. Feature importance comparison
10. Cross-validation evaluation
11. Final model evaluation

## 📈 Results

### Model Performance

| Model | Cross-Validation Accuracy | Test Accuracy | Overfitting Gap |
|-------|---------------------------|---------------|-----------------|
| Decision Tree (depth=3) | 82.93% ± 1.39% | - | Low |
| Decision Tree (depth=8) | 97.20% ± 1.26% | 97.56% | Moderate |
| Decision Tree (unlimited) | 98.05% ± 1.24% | 98.54% | Low |
| **Random Forest** | **97.93% ± 1.57%** | **99.02%** | **Minimal** |

### Key Findings

- **Best Model**: Random Forest achieved 99.02% test accuracy with minimal overfitting
- **Optimal Tree Depth**: Depth 8-9 provides best balance for single trees
- **Feature Importance**: `cp` (chest pain type) is the most predictive feature
- **Ensemble Advantage**: Random Forest shows better generalization than single trees

### Top 5 Most Important Features
1. **cp** (Chest Pain Type) - 15.25%
2. **ca** (Major Vessels) - 11.82%
3. **thalach** (Max Heart Rate) - 11.40%
4. **oldpeak** (ST Depression) - 10.58%
5. **thal** (Thalassemia) - 10.46%

## 📊 Visualizations

The project includes comprehensive visualizations:
- Target distribution analysis
- Decision tree structure visualization
- Overfitting analysis across tree depths
- Feature importance comparisons
- Cross-validation performance plots

## 🔍 Technical Highlights

- **Systematic Hyperparameter Tuning**: Analyzed tree depths from 1-10
- **Overfitting Detection**: Implemented gap analysis between train/test accuracy
- **Ensemble Methods**: Leveraged Random Forest for improved stability
- **Statistical Validation**: 5-fold stratified cross-validation
- **Feature Engineering**: Comprehensive importance analysis

## 📁 Project Structure

```
heart-disease-prediction/
│
├── Task_5.ipynb              # Main Jupyter notebook
├── heart.csv                 # Dataset
├── README.md                 # This file
├── requirements.txt          # Python dependencies
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- Dataset source: Kaggle Heart Disease Dataset
- Scikit-learn community for excellent documentation
- Matplotlib and Seaborn for visualization capabilities


---

⭐ **Star this repository if you found it helpful!**
