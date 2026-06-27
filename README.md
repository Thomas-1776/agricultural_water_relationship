# Water Quality Index (WQI) & Agricultural Suitability Pipeline

##  Project Overview
[cite_start]This project focuses on leveraging predictive modeling to analyze environmental data parameters for both agricultural use and drinking water safety. [cite_start]Using a validated machine learning pipeline, we successfully mapped out the underlying relationships between various environmental variables to understand how they influence one another over time[cite: 2]. 

[cite_start]By analyzing feature weights and model performance across multiple algorithms, this repository provides data-driven insights into resource management and sustainability[cite: 2, 3].

##  Methodology & Performance

### 1. Predictive Modeling (Regression)
We implemented a 70/30 train-test split to evaluate 5 distinct regression models for predicting the relationship between parameters:
* **Support Vector Regressor (Optimized):** achieved the highest accuracy with an **R^2 score of 0.94** and an RMSE of 2.53.
* **Random Forest Regressor:** performed strongly with an **R^2 score of 0.91** and an RMSE of 3.14.
* **Linear Regression & Bayesian Ridge:** tied with an **R^2 score of 0.77**.
* **Gaussian Process Regressor:** yielded an **R^2 score of 0.76**.

### 2. Feature Importance Analysis
[cite_start]By evaluating permutation importance and absolute coefficients across our top models, we identified that **RSC** (Residual Sodium Carbonate), **SAR** (Sodium Adsorption Ratio), and **EC** (Electrical Conductivity) serve as the dominant drivers determining water suitability for agriculture[cite: 3]. [cite_start]The models heavily indicate that these three key parameters vary in a highly non-linear fashion[cite: 4].

### 3. Safety Classification
[cite_start]In addition to continuous predictions, classification techniques were applied to our drinking water parameters to categorize and tier water safety levels effectively[cite: 2].

##  Future Scope
* **Interactive Web Deployment:** Develop a frontend interface (via Streamlit or Flask) where users can manually input localized environmental metrics to get real-time agricultural and drinking water safety predictions.
