# Housing Price Prediction - Linear Regression Analysis

A comprehensive exploratory data analysis and linear regression implementation for predicting housing prices using machine learning techniques.

## 🎯 Project Overview

This project implements simple and multiple linear regression to predict housing prices based on various property features. The analysis includes data preprocessing, model training, evaluation, and interpretation of results.

## 📊 Dataset

- **Source**: Kaggle Housing Dataset
- **Size**: 545 houses with 13 features
- **Target Variable**: House price (₹)
- **Features**: Mix of numerical (area, bedrooms, bathrooms) and categorical (amenities, location) variables

### Key Features:
- **Numerical**: area, bedrooms, bathrooms, stories, parking
- **Categorical**: mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishingstatus

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib & Seaborn** - Data visualization
- **Jupyter Notebook** - Development environment

## 📋 Project Structure

```
housing-price-prediction/
│
├── Housing.csv                 # Dataset file
├── Task_3.ipynb                # Main Jupyter notebook
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/housing-price-prediction.git
cd housing-price-prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook housing_analysis.ipynb
```

## 📈 Methodology

### 1. Data Preprocessing
- **Data Loading**: Imported CSV dataset with 545 records
- **Exploratory Analysis**: Examined data types, distributions, and missing values
- **Feature Engineering**: 
  - Binary encoding for yes/no variables (1/0)
  - One-hot encoding for categorical variables (furnishing status)

### 2. Model Development
- **Data Split**: 80% training, 20% testing
- **Algorithm**: Multiple Linear Regression
- **Features**: 14 processed features after encoding

### 3. Model Evaluation
- **Mean Absolute Error (MAE)**: ₹970,043
- **Root Mean Square Error (RMSE)**: ₹1,324,507
- **R² Score**: 0.653 (explains 65.3% of price variance)

## 📊 Key Findings

### Most Influential Price Factors:
1. **Bathrooms** (+₹1,094,445 per additional bathroom)
2. **Air Conditioning** (+₹791,427)
3. **Hot Water Heating** (+₹684,650)
4. **Preferred Area** (+₹629,891)
5. **Number of Stories** (+₹407,477)

### Business Insights:
- Luxury amenities (bathrooms, AC) drive the highest price premiums
- Location (preferred area) significantly impacts pricing
- House area has surprisingly low per-unit impact
- Unfurnished properties command lower prices (-₹233,469)

## 📉 Model Performance

- **Training R²**: 0.686
- **Testing R²**: 0.653
- **Performance**: Good generalization with minimal overfitting
- **Prediction Accuracy**: Average error of ~₹970K on properties worth ₹4.77M average

## 🔄 Future Improvements

- [ ] Implement polynomial features for non-linear relationships
- [ ] Compare with ensemble methods (Random Forest, Gradient Boosting)
- [ ] Feature engineering (price per sq ft, interaction terms)
- [ ] Cross-validation for robust model evaluation
- [ ] Hyperparameter tuning for optimization

## 📁 Files Description

- `Task_3.ipynb`: Complete step-by-step analysis with visualizations
- `Housing.csv`: Raw dataset from Kaggle
- `README.md`: Project documentation
- `requirements.txt`: Python package dependencies

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- Kaggle for providing the housing dataset
- Scikit-learn community for excellent documentation

---

⭐ **Star this repository if you found it helpful!**
