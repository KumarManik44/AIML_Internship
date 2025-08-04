# Titanic Dataset Cleaning & Preprocessing

## Project Overview
This project focuses on cleaning and preprocessing the Titanic dataset for machine learning tasks as part of an AI/ML internship. The objective is to transform raw data into a clean, numerical format suitable for model training by handling missing values, encoding categorical features, standardizing numerical features, and removing outliers.

## Dataset
The dataset used is the **Titanic Dataset** (`Titanic_Dataset.csv`), containing 891 rows and 12 columns with passenger information such as `PassengerId`, `Survived`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, and `Embarked`.

## Tools Used
- **Python**: Programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib/Seaborn**: Data visualization (boxplots for outlier detection)
- **Scikit-learn**: Standardization of numerical features

## Preprocessing Steps
1. **Exploratory Data Analysis**:
   - Checked dataset shape, column names, data types, and missing values.
   - Identified missing values: `Age` (19.87%), `Cabin` (77.10%), `Embarked` (0.22%).

2. **Handling Missing Values**:
   - Filled `Embarked` missing values with the mode (`S`).
   - Created a binary `Has_Cabin` feature (1 for non-missing, 0 for missing) and dropped the original `Cabin` column due to high missingness.
   - Imputed missing `Age` values with median age per `Pclass` (24.0 for Pclass 3, 37.0 for Pclass 1, 29.0 for Pclass 2).

3. **Encoding Categorical Features**:
   - Binary encoded `Sex` (`male=1`, `female=0`) as `Sex_encoded`.
   - One-hot encoded `Embarked` into `Embarked_C`, `Embarked_Q`, `Embarked_S`.
   - Dropped original categorical columns (`Sex`, `Embarked`, `Name`, `Ticket`) and non-essential `PassengerId`.

4. **Standardization**:
   - Standardized numerical features (`Age`, `SibSp`, `Parch`, `Fare`) using `StandardScaler` to achieve zero mean and unit variance.
   - Kept binary/categorical columns (`Pclass`, `Has_Cabin`, `Sex_encoded`, `Embarked_C`, `Embarked_Q`, `Embarked_S`) unchanged.

5. **Outlier Detection and Removal**:
   - Visualized outliers using boxplots for standardized numerical features.
   - Removed rows with values beyond ±3 standard deviations in any numerical column (71 rows, 8% of data).
   - Final dataset shape: (820 rows, 11 columns).

## Final Dataset
The cleaned dataset contains 820 rows and 11 columns:
- **Target**: `Survived` (binary, 0 or 1)
- **Features**: `Pclass`, `Age`, `SibSp`, `Parch`, `Fare`, `Has_Cabin`, `Sex_encoded`, `Embarked_C`, `Embarked_Q`, `Embarked_S`

All features are numerical, with numerical columns standardized and no missing values.

## How to Run
1. **Prerequisites**:
   - Install required libraries: `pip install pandas numpy matplotlib seaborn scikit-learn`
   - Download the `Titanic_Dataset.csv` file (e.g., from Kaggle) and place it in the project directory.

2. **Running the Code**:
   - The preprocessing steps are implemented in a Jupyter Notebook or Python script.
   - Ensure the dataset file path is correctly specified in the `pd.read_csv()` function.
   - Run the code cells sequentially to perform data loading, cleaning, encoding, standardization, and outlier removal.

3. **Output**:
   - The final cleaned dataset (`X_clean` for features, `y_clean` for target) is ready for machine learning model training.
   - Boxplots are generated to visualize outliers before removal.

## Repository Structure
- `Titanic_Dataset.csv`: Input dataset
- `preprocessing.ipynb`: Jupyter Notebook with all preprocessing steps
- `README.md`: Project documentation

## Notes
- The `Name` and `Ticket` columns were dropped as they were deemed non-essential for ML in this context. Feature engineering (e.g., extracting titles from `Name`) could be explored for enhanced model performance.
- Outlier removal used a ±3 standard deviation threshold on standardized data. Adjust this threshold if a different sensitivity is desired.
- The code assumes the Titanic dataset is in CSV format with the same column structure as the standard Kaggle dataset.

## Author
Created as part of an AI/ML internship project.