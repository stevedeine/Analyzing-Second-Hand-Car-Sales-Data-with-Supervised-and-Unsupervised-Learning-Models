# Analyzing Second-Hand Car Sales Data with Supervised and Unsupervised Learning Models

## 1.0 Abstract
This report presents an analysis of a mock dataset containing over 50,000 used car sales information. The objective is to predict used car prices using various supervised learning models, including regression models and neural networks, and to identify patterns within the dataset using unsupervised learning models such as k-means, Agglomerative Clustering, and DBSCAN. The effectiveness of each approach is evaluated to provide insight into their performance. The Artificial Neural Network produced the best predictive model based on the evaluation metrics used, while Agglomerative clustering produced the best clustering pattern. Overall, this report aims to contribute to the understanding of how second-hand car sales prices can be predicted and provides insight into clustering identification within the automotive industry.

## 2.0 Introduction
There has been a significant increase in the market for used cars, driven by factors such as a ban on petrol and diesel cars by 2030. Predicting used car prices is crucial for fair transactions, market efficiency, and customer satisfaction. This report aims to predict used car prices and identify patterns using various machine learning techniques.

## 3.0 Project Plan

| Phase                    | Timeline | Milestones                                                                  |
|--------------------------|----------|-----------------------------------------------------------------------------|
| Data Collection          | Week 1   | Collect dataset and assess its structure                                    |
| Data Preprocessing       | Week 2-3 | Clean and preprocess data, handle missing values, normalize features        |
| Exploratory Data Analysis| Week 4   | Generate correlation heatmaps and visualize data                            |
| Supervised ML Models     | Week 5-6 | Train and evaluate Linear, Polynomial, Multiple Linear Regression, and Random Forest models |
| Deep Learning Models     | Week 7-8 | Train and evaluate Artificial Neural Network (ANN)                          |
| Model Fine-Tuning        | Week 9   | Apply hyperparameter tuning and regularization                              |
| Unsupervised Learning Models | Week 10-11 | Train and evaluate K-Means, Agglomerative Clustering, and DBSCAN models      |
| Final Evaluation         | Week 12  | Compare models, finalize best-performing models                             |
| Visualization & Reporting| Week 13  | Generate final plots and report                                             |

## 4.0 Methodology

### Dataset
- **Source:** Mock dataset
- **Size:** 50,000 rows
- **Features:** Numerical (Engine Size, Year of Manufacture, Mileage, Price), Categorical (Fuel Type, Model, Manufacturer)

### Data Preparation
- **Loading Data:** Remove unnecessary columns and handle missing data
- **Text Preprocessing:** Clean, normalize, and lemmatize text; remove stopwords and punctuation

### Exploratory Data Analysis
- **Visualizations:** Correlation heatmaps and other visualizations for numerical features

### Supervised Learning Methods
- **Models:** Linear Regression, Polynomial Regression, Multiple Linear Regression, Random Forest
- **Justifications:** Robustness, computational efficiency, handling imbalanced data

### Deep Learning Methods
- **Model:** Artificial Neural Network (ANN)
- **Justifications:** Handling complex patterns in data

### Unsupervised Learning Models
- **Models:** K-Means Clustering, Agglomerative Hierarchical Clustering, DBSCAN
- **Justifications:** Identifying patterns and clusters within the data

### Implementation
- **Libraries:** Pandas, Matplotlib, Seaborn, Scikit-learn, Tensorflow, Keras
- **Feature Engineering:** TF-IDF matrix for text features, computation of sentiment scores
- **Model Building and Training:** Train and evaluate supervised and unsupervised learning models
- **Model Evaluation:** Classification reports, confusion matrix, ROC-AUC scores

## 5.0 Results

### Visualizations
- **Heatmap:** Correlation between numerical features
- **Cluster Plots:** Distribution of features and cluster identification

### Model Evaluation

#### Supervised Learning Models

| Model                      | MAE      | MSE          | RMSE     | R2    |
|----------------------------|----------|--------------|----------|-------|
| Linear Regression          | 7,031.04 | 132,679,000  | 11,518.64| 0.51  |
| Polynomial Regression (D5) | 5,160.77 | 102,654,671.5| 10,131.86| 0.62  |
| Multiple Linear Regression | 6,091.46 | 89,158,615.76| 9,442.38 | 0.67  |
| Random Forest              | 287.69   | 401,091.51   | 633.32   | 1.00  |

#### Deep Learning Models

| Model                      | MAE      | MSE         | RMSE    | R2    |
|----------------------------|----------|-------------|---------|-------|
| Artificial Neural Network  | 213.98   | 142,055.88  | 376.9   | 1.00  |

#### Unsupervised Learning Models

| Model                              | Silhouette Score | Davies-Bouldin Index (DBI) |
|------------------------------------|------------------|----------------------------|
| K-Means Clustering                 | 0.51             | 0.69                       |
| Agglomerative Hierarchical Clustering (AHC) | 0.64             | 0.46                       |
| DBSCAN                             | 0.68             | 1.5                        |

## 6.0 Discussion
The Artificial Neural Network (ANN) model was the most effective for predicting used car prices, achieving an MAE of 213.98, MSE of 142,055.88, RMSE of 376.9, and an R-square score of 1.00. Among regression models, Random Forest performed best with an MAE of 287.69, MSE of 401,091.51, RMSE of 633.32, and an R-square score of 1.00.

For clustering, Agglomerative Hierarchical Clustering (AHC) provided the best results with a silhouette score of 0.64 and a Davies-Bouldin Index of 0.46. While DBSCAN showed a higher silhouette score, its DBI was significantly higher, indicating less distinct clusters compared to AHC.

These results demonstrate the effectiveness of advanced machine learning techniques in predicting prices and identifying patterns in used car sales data, which can help improve market efficiency, ensure fair transactions, and enhance customer satisfaction.

## 7.0 Conclusion
The ANN model outperformed all regression models with the best predictive accuracy. AHC was the best clustering method, providing the highest silhouette score and lowest Davies-Bouldin Index. This analysis highlights the effectiveness of ANN for predicting used car prices and AHC for clustering. Future studies should consider larger datasets to further improve prediction and clustering accuracy.
