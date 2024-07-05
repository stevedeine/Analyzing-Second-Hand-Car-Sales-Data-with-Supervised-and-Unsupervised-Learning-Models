# Analyzing Second-Hand Car Sales Data with Supervised and Unsupervised Learning Models

## 1.0 Abstract
This report analyzes over 50,000 instances of used car sales data to predict car prices using supervised learning models such as regression and neural networks, and to identify patterns using unsupervised learning models like k-means, Agglomerative Clustering, and DBSCAN. The Artificial Neural Network provided the most accurate predictions, while Agglomerative Clustering was most effective in pattern identification. The insights from this report enhance the understanding of price dynamics and pattern recognition in the used car market.

## 2.0 Introduction
The used car market has seen significant growth, highlighted by a 108.6% increase in sales year-on-year and a 6.6% increase over pre-COVID-19 levels, as reported by BBC (2021). Additionally, impending bans on petrol and diesel cars by 2030, as reported by The Telegraph (2022), are expected to boost the demand for used cars further, making price prediction increasingly relevant for ensuring fair transactions and market efficiency.

## 3.0 Literature Review
Research by Liu et al. (2021) utilized various regression techniques to predict used car prices, achieving an R-square score of up to 90%. Gegic et al. (2017) explored an ensemble model combining ANN, SVM, and Random Forest, reaching an accuracy of 87.38%. These studies highlight the potential of using diverse analytical techniques to enhance prediction accuracy, though they also indicate the need for larger datasets for robust model training.

## 4.0 Methodology

### 4.1 Data Description
The dataset comprises 50,000 entries with numerical and categorical features, including Engine Size, Year of Manufacture, Mileage, Price (target variable), Fuel Type, Model, and Manufacturer.

### 4.2 Supervised Learning Models
We implemented Linear, Polynomial, and Multiple Linear Regression models. Additionally, we used a Random Forest Regressor for its ability to handle both types of features effectively. The ANN was designed with a sequential model architecture to manage complexity and prevent overfitting, utilizing dropout and Adam’s optimizer.

### 4.3 Unsupervised Learning Models
We applied K-Means, Agglomerative Clustering, and DBSCAN for pattern identification, using techniques like the elbow method to determine the optimal number of clusters for K-Means.

### 4.4 Evaluation Metrics
We used MAE, MSE, RMSE, and R-square Score for regression models, and Silhouette Score and Davies Bouldin Index for clustering models.

## 5.0 Results

### 5.1 Supervised Learning Model Performance

| Model Type                  | MAE        | MSE             | RMSE      | R2    |
|-----------------------------|------------|-----------------|-----------|-------|
| Linear Regression           | 7,031.04   | 132,678,999.95  | 11,518.64 | 0.51  |
| Polynomial Regression       | 5,160.77   | 102,654,671.5   | 10,131.86 | 0.62  |
| Multiple Linear Regression  | 6,091.46   | 89,158,615.76   | 9,442.38  | 0.67  |
| Random Forest               | 287.69     | 401,091.51      | 633.32    | 1.00  |
| ANN                         | 213.98     | 142,055.88      | 376.9     | 1.00  |

### 5.2 Unsupervised Learning Model Performance

| Model                          | Silhouette Score | Davies-Bouldin Index |
|--------------------------------|------------------|----------------------|
| K-Means                        | 0.51             | 0.69                 |
| Agglomerative Clustering       | 0.64             | 0.46                 |
| DBSCAN                         | 0.68             | 1.5                  |

## 6.0 Discussion
The ANN outperformed all regression models, offering high precision in price prediction. Agglomerative Clustering was the superior method for identifying clusters, indicating distinct groupings within the data. This study underscores the efficacy of combining various machine learning approaches to improve predictive accuracy and data insight in the used car market.

## 7.0 Conclusion
The analysis demonstrated that ANN provides the most accurate predictions of used car prices, and Agglomerative Clustering is most effective for clustering tasks. These findings suggest a robust framework for enhancing transaction transparency and customer satisfaction in the used car industry. Future research could expand on dataset size and feature engineering to further refine the models.

## 8.0 References
1. BBC News (2021). "Second-hand car sales soar amid shortage of new models." Available at: [BBC News Article](https://www.bbc.co.uk/news/business-58150025).
2. The Telegraph (2022). "Future ban on petrol and diesel cars." Available at: [The Telegraph Article](https://www.telegraph.co.uk/cars/).
3. Liu, Y., Wang, J., & Zhang, Y. (2021). "Price Prediction of Used Cars Using Machine Learning." IEEE International Conference.
4. Gegic, E., Isakovic, B., Keco, D., Masetic, Z., & Kevric, J. (2017). "Car price prediction using machine learning techniques." IEEE IcETRAN Conference.
