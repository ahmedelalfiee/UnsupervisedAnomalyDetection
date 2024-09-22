<p align="center">
  <img src="https://github.com/user-attachments/assets/8c89a5da-4367-4514-a277-c8d9cb5f6ab4" width="500" />
</p>

## Problem
- This project introduces an unsupervised approach to anomaly detection of a Hypothyroidism dataset (without domain knowledge) using different outlier detection methods and techniques. We will
compare their results and conclude the most effective method.  
- The probability of each data point being an outlier will be recorded in the 'Data_with_anomalies_and_probabilities' csv file based on the chosen method.

## Dataset
The dataset details: 21 attributes, 15 binary, 6 continuous, 7200 objects. (No information on attribute significance)

## Pre-Processing
Normalization using Z-score standardization for consistent data ranges.
<p align="center">
  <b>Z = (x - μ)/std</b>
</p>

## Anomaly Detection Methods
Different methods were divided as follows:
- **Binary Attributes**: Mahalanobis Distance, Isolation Forest.
- **Continuous Attributes**: PCA, Isolation Forest, LOF.
- **Mixed Attributes**: Hierarchical Clustering, Isolation Forest, VAE.

## Binary Attributes Analysis
- **Mahalanobis Distance**: 90 outliers detected.
- **Isolation Forest**: 36 outliers detected.
Common outliers between methods: 14.
  
## Continuous Attributes Analysis
- **PCA**: 15 outliers detected.
- **Isolation Forest**: 36 outliers detected.
- **LOF**: 36 outliers detected.
Common outliers between methods: 13.

<p align="center">
  <img src="https://github.com/user-attachments/assets/9a27929e-3339-42c7-9bd4-7e8b044f993b" width="500" />
</p>

## Mixed Attributes
- **Hierarchical Clustering**: 11 clusters
  Agglomerative clustering using Ward as the linkage method. 
- **Isolation Forest**: showed limited success.
- **Variational AutoEncoder (VAE)**: Effective, 72 outliers detected.

## Conclusion
Variational AutoEncoder was the final decision after showing great effectiveness in outlier detection.

<p align="center">
  <img src="https://github.com/user-attachments/assets/eae0940a-ea0f-44b2-8ebe-7f02d4798e3d" width="500" />
</p>






