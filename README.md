# Heart Disease Analysis

This repository contains an analysis of the heart disease dataset from the UCI Machine Learning Repository. The goal is to identify patients with a high risk of developing heart disease using unsupervised learning techniques.

## Steps
1. Load and explore the dataset.
2. Preprocess the dataset.
3. Apply clustering algorithms (K-means, Hierarchical, DBSCAN).
4. Visualize the clusters using PCA and t-SNE.
5. Identify risk factors using Gaussian Mixture Models.
6. Evaluate clustering performance.
7. Compare clustering algorithms.

The Heart Disease dataset from the UCI Machine Learning Repository contains 303 instances and 13 features. Here’s a detailed summary of the dataset:

**Metadata:**
- **uci_id**: 45
- **name**: Heart Disease
- **repository_url**: [Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)
- **data_url**: [Data CSV](https://archive.ics.uci.edu/static/public/45/data.csv)
- **abstract**: The dataset comprises four databases: Cleveland, Hungary, Switzerland, and the VA Long Beach.
- **area**: Health and Medicine
- **tasks**: Classification
- **characteristics**: Multivariate
- **num_instances**: 303
- **num_features**: 13
- **feature_types**: Categorical, Integer, Real
- **demographics**: Age, Sex
- **target_col**: num
- **index_col**: None
- **has_missing_values**: yes
- **missing_values_symbol**: NaN
- **year_of_dataset_creation**: 1989
- **last_updated**: Fri Nov 03 2023
- **dataset_doi**: 10.24432/C52P4X
- **creators**: Andras Janosi, William Steinbrunn, Matthias Pfisterer, Robert Detrano
- **intro_paper**: ["International application of a new probability algorithm for the diagnosis of coronary artery disease." by R. Detrano et al.](https://www.semanticscholar.org/paper/a7d714f8f87bfc41351eb5ae1e5472f0ebbe0574)
- **additional_info**: This database contains 76 attributes, but all published experiments refer to using a subset of 14. The Cleveland database is the most used, focusing on distinguishing the presence (values 1,2,3,4) from absence (value 0) of heart disease.

**Variable Information:**

| Name     | Role    | Type        | Demographic | Description                                       | Units  | Missing Values |
|----------|---------|-------------|-------------|---------------------------------------------------|--------|----------------|
| age      | Feature | Integer     | Age         | None                                              | years  | no             |
| sex      | Feature | Categorical | Sex         | None                                              | None   | no             |
| cp       | Feature | Categorical | None        | None                                              | None   | no             |
| trestbps | Feature | Integer     | None        | Resting blood pressure (on admission to hospital) | mm Hg  | no             |
| chol     | Feature | Integer     | None        | Serum cholesterol                                 | mg/dl  | no             |
| fbs      | Feature | Categorical | None        | Fasting blood sugar > 120 mg/dl                   | None   | no             |
| restecg  | Feature | Categorical | None        | None                                              | None   | no             |
| thalach  | Feature | Integer     | None        | Maximum heart rate achieved                       | None   | no             |
| exang    | Feature | Categorical | None        | Exercise induced angina                           | None   | no             |
| oldpeak  | Feature | Integer     | None        | ST depression induced by exercise relative to rest| None   | no             |
| slope    | Feature | Categorical | None        | None                                              | None   | no             |
| ca       | Feature | Integer     | None        | Number of major vessels (0-3) colored by fluoroscopy| None  | yes            |
| thal     | Feature | Categorical | None        | None                                              | None   | yes            |
| num      | Target  | Integer     | None        | Diagnosis of heart disease                        | None   | no             |

**Key Points:**
- The target column `num` indicates the presence of heart disease, with values 1,2,3,4 indicating presence and 0 indicating absence.
- The dataset includes both categorical and numerical features.
- There are missing values in the `ca` and `thal` features.
- It is designed for classification tasks, primarily to distinguish the presence or absence of heart disease.

## Brief Description of Analysis.