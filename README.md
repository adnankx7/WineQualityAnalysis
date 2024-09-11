# Red Wine Quality Prediction - Exploratory Data Analysis (EDA) and Classification

This project focuses on analyzing the red wine dataset from the Portuguese "Vinho Verde" wines. The dataset contains physicochemical properties and sensory data, with the goal of predicting the quality of wine using machine learning techniques.

## Dataset

The dataset includes measurements of various properties of red wine, such as acidity, alcohol content, and sulfur dioxide levels. The output variable, `quality`, is a score between 0 and 10 based on sensory data.

### Input Variables (Physicochemical Tests)
1. `fixed acidity`
2. `volatile acidity`
3. `citric acid`
4. `residual sugar`
5. `chlorides`
6. `free sulfur dioxide`
7. `total sulfur dioxide`
8. `density`
9. `pH`
10. `sulphates`
11. `alcohol`

### Output Variable
- `quality` (wine quality score between 0 and 10)

## Project Steps

### 1. Data Loading and Initial Exploration
- Loaded the red wine dataset using `pandas`.
- Displayed dataset structure using `df.info()` and generated descriptive statistics with `df.describe()`.
- Checked for duplicate values and dropped them to clean the dataset.

### 2. Exploratory Data Analysis (EDA)
- Visualized correlations between variables using a heatmap (`seaborn` heatmap).
- Explored the distribution of wine quality scores with a bar chart.
- Plotted histograms for each feature to understand their distributions.
- Used pairplots to explore relationships between features.

### 3. Addressing Class Imbalance
- The quality scores were imbalanced, with some ratings more frequent than others.
- Applied **upsampling** using `sklearn.utils.resample()` to balance the dataset by increasing the number of samples in minority classes.

### 4. Model Training and Evaluation
- Split the dataset into training and testing sets using `train_test_split()`.
- Built a **Random Forest Classifier** to predict wine quality.
- Evaluated the model using:
  - **Accuracy Score**
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-Score)

### 5. Visualization of Results
- Displayed the distribution of wine quality before and after upsampling.
- Plotted histograms for each feature.
- Generated the confusion matrix and classification metrics.

## Technologies Used
- **Python**
- **pandas** for data manipulation
- **seaborn** and **matplotlib** for visualizations
- **scikit-learn** for machine learning models and evaluation
- **RandomForestClassifier** for classification

## Results
- The Random Forest Classifier achieved competitive accuracy in predicting wine quality.
- Visualization of the confusion matrix and classification report provides insight into the model's performance across different quality classes.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/adnankx7/WineQualityAnalysis.git
