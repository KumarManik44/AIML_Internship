# K-Nearest Neighbors (KNN) Classification on Iris Dataset

A comprehensive implementation of K-Nearest Neighbors classification algorithm with systematic hyperparameter tuning, detailed evaluation, and beautiful visualizations.

## 🎯 Project Overview

This project demonstrates a complete machine learning pipeline for classification using KNN algorithm on the classic Iris dataset. The implementation includes feature normalization, systematic K-value optimization, comprehensive model evaluation, and stunning decision boundary visualizations.

## 📊 Key Results

- **Best Test Accuracy**: 96.67% (K=7)
- **Perfect Classification**: Iris-setosa (100% accuracy)
- **Strong Performance**: Iris-versicolor and Iris-virginica (90-100% accuracy)
- **Feature Insight**: Petal measurements alone achieve 93.3% accuracy

## 🔧 Features

- ✅ Systematic K-value optimization (K=1 to K=20)
- ✅ Proper feature normalization using StandardScaler
- ✅ Comprehensive model evaluation (accuracy, precision, recall, F1-score)
- ✅ Beautiful confusion matrix visualization
- ✅ Decision boundary visualization in 2D space
- ✅ Detailed error analysis of misclassified samples
- ✅ Professional-quality plots and charts

## 📁 Project Structure

```
knn-iris-classification/
│
├── Task_6.ipynb              # Main Jupyter notebook with complete implementation
├── iris.csv                  # Iris dataset
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies

```

## 🚀 Quick Start

### Prerequisites

- Python 3.7+
- Jupyter Notebook

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/knn-iris-classification.git
cd knn-iris-classification
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```

4. Open `Task_6.ipynb` and run all cells step by step.

### Dataset

The project uses the famous Iris dataset containing:
- **150 samples** of iris flowers
- **4 features**: Sepal Length, Sepal Width, Petal Length, Petal Width
- **3 classes**: Iris-setosa, Iris-versicolor, Iris-virginica
- **Balanced dataset**: 50 samples per class

## 📈 Implementation Highlights

### 1. Data Preprocessing
- Feature normalization using StandardScaler (mean=0, std=1)
- Stratified train-test split (80-20) maintaining class balance
- No missing values handling required (clean dataset)

### 2. Model Optimization
- Systematic testing of K values from 1 to 20
- Identification of overfitting at K=1 (100% train, 96.67% test)
- Optimal K=7 selected based on test performance

### 3. Evaluation Metrics
- **Accuracy**: Overall classification performance
- **Precision**: Class-wise prediction accuracy
- **Recall**: Class-wise detection rate
- **F1-Score**: Balanced precision-recall metric
- **Confusion Matrix**: Detailed misclassification analysis

### 4. Visualizations
- K-value performance curves showing bias-variance tradeoff
- Heatmap confusion matrix with class-wise breakdown
- 2D decision boundaries using most discriminative features
- Training vs test data comparison

## 🔍 Key Insights

1. **Feature Importance**: Petal measurements (length and width) are highly discriminative
2. **Class Separability**: Iris-setosa is linearly separable, while Iris-versicolor and Iris-virginica overlap
3. **Optimal Complexity**: K=7 provides the best balance between bias and variance
4. **Normalization Impact**: Feature scaling crucial for distance-based algorithms like KNN

## 📊 Model Performance

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Iris-setosa | 1.00 | 1.00 | 1.00 | 10 |
| Iris-versicolor | 0.91 | 1.00 | 0.95 | 10 |
| Iris-virginica | 1.00 | 0.90 | 0.95 | 10 |
| **Overall** | **0.97** | **0.97** | **0.97** | **30** |

## 🛠️ Technologies Used

- **Python 3.x**: Programming language
- **scikit-learn**: Machine learning library
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Static plotting
- **seaborn**: Statistical data visualization
- **Jupyter Notebook**: Interactive development environment

## 📝 Usage Examples

### Basic KNN Implementation
```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.preprocessing import StandardScaler

# Normalize features
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_train)

# Train KNN
knn = KNeighborsClassifier(n_neighbors=7)
knn.fit(X_scaled, y_train)

# Make predictions
predictions = knn.predict(X_test_scaled)
```

### K-Value Optimization
```python
k_values = range(1, 21)
accuracies = []

for k in k_values:
    knn = KNeighborsClassifier(n_neighbors=k)
    knn.fit(X_train_scaled, y_train)
    accuracy = knn.score(X_test_scaled, y_test)
    accuracies.append(accuracy)

optimal_k = k_values[np.argmax(accuracies)]
```

## 🙏 Acknowledgments

- UCI Machine Learning Repository for the Iris dataset
- scikit-learn community for excellent documentation
- Matplotlib and Seaborn for visualization capabilities

---

⭐ **If you found this project helpful, please give it a star!** ⭐
