# Clustering Analysis on Wine Dataset

## Overview

This project explores two clustering techniques—**Hierarchical Clustering** and **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**—applied to the **Wine dataset** from Scikit-learn. The objective is to identify patterns in unlabeled data and compare how each algorithm performs in grouping similar wine samples based on their chemical attributes.

## Dataset

The **Wine dataset** consists of 178 samples with 13 numerical features representing different chemical properties of wines from three cultivars. These include:
- Alcohol
- Malic acid
- Ash
- Alcalinity of ash
- Magnesium
- Total phenols
- Flavanoids
- Nonflavanoid phenols
- Proanthocyanins
- Color intensity
- Hue
- OD280/OD315 of diluted wines
- Proline

There are no missing values, and all data is numeric, making it ideal for clustering.

## Tools and Libraries

The project was implemented in Python using the following libraries:
- `scikit-learn` – for clustering models and dataset
- `matplotlib` & `seaborn` – for visualizations
- `scipy` – for generating dendrograms
- `numpy` – for array operations
- `pandas` – for data exploration and handling

## Steps Performed

1. **Data Loading and Preprocessing**:
   - Loaded the Wine dataset from Scikit-learn.
   - Scaled the data using `StandardScaler` to ensure equal weight for all features.

2. **Hierarchical Clustering**:
   - Applied Agglomerative Clustering with varying cluster sizes (2, 3, and 4).
   - Visualized the results using scatter plots.
   - Generated a dendrogram using SciPy to interpret hierarchical cluster relationships.

3. **DBSCAN Clustering**:
   - Tested multiple configurations of `eps` and `min_samples`.
   - Found only one configuration that resulted in multiple clusters.
   - Evaluated clustering performance using silhouette score, homogeneity, and completeness.

4. **Analysis and Comparison**:
   - Compared both algorithms based on visual and metric-based performance.
   - Hierarchical clustering produced clearer and more consistent results.
   - DBSCAN struggled due to the dataset's lack of density-separated clusters.

## Results Summary

- **Hierarchical Clustering** was effective in grouping similar wine types, with interpretable dendrograms and clean visual separation.
- **DBSCAN** failed to find meaningful clusters except for one configuration, and even then, it marked the majority of samples as noise.

## Conclusion

This project highlights the strengths of hierarchical clustering when working with moderately structured datasets like the Wine data. It also demonstrates the importance of choosing the right algorithm based on data distribution and the need for visualization to support clustering decisions.

## How to Run

1. Clone this repository or copy the code files.
2. Ensure Python 3.8+ and pip are installed.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
