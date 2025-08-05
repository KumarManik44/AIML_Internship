# 🚢 Titanic Dataset - Exploratory Data Analysis

A comprehensive exploratory data analysis of the famous Titanic dataset, uncovering survival patterns and insights from one of history's most tragic maritime disasters.

## 📊 Project Overview

This project performs a detailed statistical and visual analysis of passenger data from the RMS Titanic to understand the factors that influenced survival rates during the disaster of April 15, 1912.

## 🎯 Objectives

- Generate comprehensive summary statistics for all features
- Create informative visualizations (histograms, boxplots, correlation matrices)
- Identify survival patterns across different passenger demographics
- Analyze feature relationships and correlations
- Provide actionable insights for future machine learning modeling

## 📈 Key Findings

### Survival Statistics
- **Overall Survival Rate**: 38.4%
- **Gender Impact**: 
  - Female survival: 74.2%
  - Male survival: 18.9%
- **Class Disparity**:
  - 1st Class: 63.0% survival rate
  - 2nd Class: 47.3% survival rate  
  - 3rd Class: 24.2% survival rate

### Economic Factors
- Survivors paid significantly higher fares (£48.40 vs £22.12 average)
- Strong correlation between passenger class and fare (-0.549)
- Clear evidence that wealth influenced survival chances

### Demographic Insights
- Younger passengers had slightly better survival odds (28.3 vs 30.6 avg age)
- "Women and children first" evacuation protocol clearly evident in data
- Family size showed mixed impact on survival rates

## 🔍 Data Quality Assessment

| Feature | Missing Values | Percentage | Status |
|---------|---------------|------------|---------|
| Age | 177 | 19.9% | Requires imputation |
| Cabin | 687 | 77.1% | Consider dropping |
| Embarked | 2 | 0.2% | Easy to handle |

## 📊 Dataset Information

- **Total Passengers**: 891
- **Features**: 12 columns
- **Target Variable**: Survived (0/1)
- **Data Types**: Mixed (numerical and categorical)

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Static visualizations
- **Seaborn** - Statistical data visualization

## 📁 Project Structure

```
titanic-eda/
│
├── Task_2.ipynb               # Main Jupyter notebook with complete analysis
├── Titanic_Dataset.csv        # Dataset file
├── README.md                  # Project documentation
└── requirements.txt           # Python dependencies
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Analysis

1. Clone this repository:
```bash
git clone https://github.com/yourusername/titanic-eda.git
cd titanic-eda
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook titanic_eda.ipynb
```

3. Run all cells sequentially to reproduce the complete analysis

## 📋 Analysis Workflow

1. **Data Loading & Initial Inspection**
   - Dataset structure and dimensions
   - First look at the data

2. **Data Quality Assessment**
   - Missing value analysis
   - Data type validation
   - Memory usage optimization

3. **Statistical Summary**
   - Descriptive statistics for numerical features
   - Frequency distributions for categorical features

4. **Survival Analysis**
   - Target variable distribution
   - Survival rates by demographics

5. **Feature Relationships**
   - Correlation analysis
   - Pairwise feature exploration
   - Pattern identification

6. **Advanced Insights**
   - Feature engineering opportunities
   - Model preparation recommendations

## 🎨 Visualizations Include

- Survival distribution charts
- Demographic breakdown plots
- Age and fare distribution histograms
- Correlation heatmaps
- Comprehensive pairplots
- Class-based survival analysis

## 🔮 Future Work & ML Recommendations

### Feature Engineering Opportunities
- Create `FamilySize` = SibSp + Parch + 1
- Extract passenger titles from names
- Bin age into categorical groups
- Create `IsAlone` binary feature

### Modeling Considerations
- Address 61.6% class imbalance in target variable
- Implement age imputation strategy
- Apply feature scaling for fare ranges
- Consider ensemble methods for best performance

## 📚 Key Insights for Historical Context

- **Social Protocol**: Clear evidence of "women and children first" evacuation
- **Economic Disparity**: Wealth directly correlated with survival chances
- **Infrastructure Impact**: Passenger class determined deck level and lifeboat access
- **Family Dynamics**: Small family groups showed slight survival advantages

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements or additional analysis techniques.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Kaggle for providing the Titanic dataset
- The pandas and matplotlib communities for excellent documentation
- Historical records that make this analysis possible

---

⭐ **If you found this analysis helpful, please consider giving it a star!**

📧 **Questions?** Feel free to reach out or open an issue!
