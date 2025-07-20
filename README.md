# Predicting Music Track Popularity: Miniproject

This repository presents the codebase for predicting music track popularity as part of a machine learning miniproject. The project utilizes a real-world music 
dataset provided by Kaggle as part of the **MLX 2.0 Regression Competition**.

---

## Project Overview

Forecasting music track popularity is a challenging regression task of importance to streaming platforms and music industry professionals. This miniproject explores 
a variety of machine learning methods—including tree-based ensembles and gradient boosting—to predict track popularity using a range of audio features and metadata from the Kaggle competition dataset.

---

## Dataset

- **Source**: Kaggle MLX 2.0 Regression Competition  
- **Link**: https://www.kaggle.com/competitions/mlx-2-0-regression/data 
- **Format**: CSV files containing:
  - `train.csv` (with target)
  - `test.csv` (without target)
  - Metadata describing various audio and categorical features for each music track.

---

## Experimental Setup
We have experimented with numerous approaches to predict the popularity of music tracks, each leveraging distinct machine learning methodologies. These include 
various ensemble techniques, boosting models, and baseline regressors. The repository is organized such that each folder contains Jupyter notebooks relevant to a 
specific modeling strategy, allowing for modular analysis and easy comparison. Additionally, a detailed report summarizing these experiments and insights is 
included in the root directory. <br>
Given below are the approaches used for this project.
- Method A: Sequential Feature Pruning with Linear Regression and Optimized Ensemble Regression
- Method B: Hybrid Ensemble Regression and Feature Selection
- Method C: Iterative Optimization with Advanced Feature Engineering and Model Simplification
- Method D: Hybrid Ensemble Regression and Feature Engineering
- Method E: RegressionModel Implementation
- Method F: Dual-Strategy Analysis: Retained Feature Space vs. PCA Optimized Regression


---

## Repository Structure
. <br>
├── Dataset/ <br>
│   ├── train.csv <br>
│   └── test.csv <br>
├── Method A/ <br>
├── Method B/ <br>
├── Method C/ <br>
├── Method D/ <br>
├── Method E/ <br>
├── Method F/ <br>
├── Predicting Music Track Popularity.pdf <br>
└── README.md <br>
Note: Each "Method" folder contains the notebooks relevant to the implementation of the method.

---

## Future Work
- Integrate real-time streaming metrics (e.g., skip rates, playlist retention).
- Use deep learning audio embeddings (e.g., CNN-based features).
- Apply model interpretability techniques (e.g., SHAP values).
- Test model generalizability across genres and time periods.

## References
- Kaggle MLX 2.0 Regression Competition Dataset
- A. Smith and B. Jones, “Hit Song Science: Regression on Spotify Features,” Proc. ISMIR, 2015.
- L. Breiman, “Random Forests,” Machine Learning, vol. 45, no. 1, pp. 5–32, 2001.
- T. Chen and C. Guestrin, “XGBoost: A Scalable Tree Boosting System,” KDD, 2016.
- G. Ke et al., “LightGBM: A Highly Efficient Gradient Boosting Decision Tree,” NeurIPS, 2017.
- K. Li, J. Wang, and S. Liu, “Enhanced Popularity Prediction with XGBoost on Spotify Data,” J. Audio Eng. Soc., 2022.
- I. T. Jolliffe, Principal Component Analysis, 2nd ed., Springer, 2002.
- H. Peng, F. Long, and C. Ding, “Feature Selection Based on Mutual Information: Criteria of Max-Dependency, Max-Relevance, and Min Redundancy,” IEEE Trans. PAMI, vol. 27, no. 8, pp. 1226–1238, 2005.
- Y. Park, H. Kim, and D. Lee, “Stacked Ensemble for Hit Song Prediction,” Kaggle Days, 2019.
- J. Lee and K. Nam, “Convolutional Neural Networks for Music Classification,” ISMIR, 2017.
- S. Dieleman and B. Schrauwen, “End-to-end Learning for Music Audio,” ICASSP, 2014.

---

## Authors

- **Dineth Randula**  
  [LinkedIn](linkedin.com/in/dineth-randula-11814b283)
- **Thimira Sahan**  
  [LinkedIn](linkedin.com/in/thimira-sahan)
- **Madhushankha de Silva**  
  [LinkedIn](https://www.linkedin.com/in/madhushankha-de-silva-5bb58129a/))
- **Anas Hussaindeen**  
  [LinkedIn](linkedin.com/in/anas-hussaindeen)
- **Vihnaga Muthumala**  
  [LinkedIn](linkedin.com/in/vihanga-muthumala-678451277)
- **Dilanka Heshan**  
  [LinkedIn](linkedin.com/in/dilanka-heshan-93935b219)
