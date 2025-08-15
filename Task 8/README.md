# Customer Segmentation using K-Means Clustering

A comprehensive machine learning project that performs customer segmentation analysis on mall customer data using K-Means clustering algorithm to identify distinct customer groups and provide actionable business insights.

## 🎯 Project Overview

This project analyzes customer behavior patterns using unsupervised machine learning techniques to segment customers into distinct groups based on their age, annual income, and spending score. The analysis helps businesses understand their customer base and develop targeted marketing strategies.

## 📊 Dataset

- **Source**: Mall Customer Segmentation Data (Kaggle)
- **Size**: 200 customers
- **Features**: 
  - CustomerID
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1-100)

## 🔧 Technologies Used

- **Python 3.8+**
- **Libraries**:
  - pandas - Data manipulation and analysis
  - numpy - Numerical computations
  - matplotlib - Data visualization
  - seaborn - Statistical data visualization
  - scikit-learn - Machine learning algorithms
  - scipy - Scientific computing

## 🚀 Features

- **Data Exploration**: Comprehensive statistical analysis and visualization
- **Data Preprocessing**: Feature scaling using StandardScaler
- **Optimal K Selection**: Elbow Method implementation for determining optimal number of clusters
- **K-Means Clustering**: Customer segmentation with detailed cluster analysis
- **Performance Evaluation**: Silhouette Score analysis for cluster quality assessment
- **Business Insights**: Actionable recommendations for each customer segment

## 📈 Key Results

### Clustering Performance
- **Optimal K**: 5 clusters
- **Silhouette Score**: 0.417 (Fair clustering quality)
- **WCSS**: 168.25

### Customer Segments Identified

| Cluster | Segment Name | Size | Avg Age | Avg Income | Avg Spending | Business Strategy |
|---------|--------------|------|---------|------------|--------------|-------------------|
| 0 | Premium Young | 40 | 32.9 | $86.1k | 81.5/100 | Premium products & exclusive offers |
| 1 | Young Spenders | 54 | 25.2 | $41.1k | 62.2/100 | Affordable luxury & payment plans |
| 2 | Budget Conscious | 20 | 46.2 | $26.7k | 18.3/100 | Value-for-money & discounts |
| 3 | Conservative High Earners | 39 | 39.9 | $86.1k | 19.4/100 | Quality practical products |
| 4 | Moderate Seniors | 47 | 55.6 | $54.4k | 48.9/100 | Comfortable reliable products |

## 🔍 Analysis Workflow

1. **Data Loading & Exploration**
   - Load dataset and examine structure
   - Statistical summary and data quality check

2. **Data Visualization**
   - Distribution analysis of key features
   - Correlation exploration through scatter plots

3. **Data Preprocessing**
   - Feature selection (Age, Income, Spending Score)
   - Standardization using StandardScaler

4. **Optimal K Determination**
   - Elbow Method implementation
   - WCSS calculation for K=1 to K=10

5. **K-Means Clustering**
   - Apply K-Means with optimal K=5
   - Generate cluster labels and centroids

6. **Cluster Visualization**
   - Multi-dimensional scatter plots
   - Color-coded cluster visualization
   - Centroid identification

7. **Performance Evaluation**
   - Silhouette Score analysis
   - Per-cluster performance metrics

8. **Business Insights**
   - Customer segment profiling
   - Strategic recommendations

## 📁 Project Structure

```
Task 8/
├── Mall_Customers.csv
├── Task_8.ipynb
├── requirements.txt
├── README.md
```

## 🛠️ Installation & Usage

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/customer-segmentation-kmeans.git
cd customer-segmentation-kmeans
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the Jupyter notebook**
```bash
jupyter notebook notebooks/Customer_Segmentation_Analysis.ipynb
```

4. **Or run the Python script**
```bash
python src/kmeans_clustering.py
```

## 📊 Visualizations

The project includes comprehensive visualizations:
- Feature distribution histograms
- Elbow curve for optimal K selection
- Multi-dimensional cluster scatter plots
- Silhouette analysis plots
- Cluster comparison charts

## 💡 Business Impact

### Marketing Strategy Recommendations:

- **Cluster 0 (Premium Young)**: Focus on luxury products, exclusive memberships, and premium services
- **Cluster 1 (Young Spenders)**: Implement installment plans, student discounts, and trendy affordable items
- **Cluster 2 (Budget Conscious)**: Emphasize value deals, bulk discounts, and essential items
- **Cluster 3 (Conservative High Earners)**: Market high-quality, durable products with proven value
- **Cluster 4 (Moderate Seniors)**: Prioritize customer service, comfort, and reliability

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- Dataset source: Kaggle Mall Customer Segmentation Data
- Inspiration from various customer analytics case studies
- Thanks to the open-source community for the amazing tools and libraries

---

⭐ If you found this project helpful, please give it a star!
