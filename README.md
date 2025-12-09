Global Housing Price Prediction using Advanced Regression Models

This project develops machine learning models to estimate housing prices across multiple global cities. It includes data preprocessing, model benchmarking across seven regression algorithms, and deployment of an interactive prediction interface using Gradio.

Project Objectives

Analyze housing markets across varied geographical regions

Build and evaluate regression models using standardized ML pipelines

Deploy a user-friendly interface for price prediction

Compare model behavior and generalizability across datasets

Datasets Used

Ames Housing (Kaggle): Sale price prediction for residential properties in Ames, Iowa

Bengaluru Housing (Public dataset): Property price estimation in Bengaluru, India

King County Housing (Kaggle): Housing prices in the Seattle–Tacoma region, USA

Melbourne Housing (Kaggle): Residential property sale prices in Melbourne, Australia

California Housing (StatLib / sklearn): Median house value based on census data

Each dataset required individual preprocessing due to feature differences, data quality variability, and location-specific attributes.

Machine Learning Approach

Models investigated:

Linear Regression

Ridge Regression

Lasso Regression

Elastic Net

Random Forest Regressor

XGBoost Regressor

LightGBM Regressor

Evaluation metrics used:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² Score

Pipeline components:

Numerical imputation and scaling

One-hot encoding for categorical variables

Outlier handling and feature selection

Cross-validation for model assessment

Best Performing Models by Dataset

Ames Housing: XGBoost demonstrated best performance with high generalization

Bengaluru Housing: XGBoost delivered the most reliable results given high variability

King County Housing: LightGBM achieved highest accuracy on a complex dataset

Melbourne Housing: LightGBM showed consistent performance across diverse property features

California Housing: LightGBM provided the strongest predictive capability on large-scale data

Tree-based boosting methods consistently outperformed linear models in capturing non-linear pricing patterns.

Gradio Prediction Interface

A Gradio dashboard is included for interactive house price estimation using the Ames dataset.
Users input key structural and location features, and the model returns the predicted sale price.

Dashboard Screenshots
Price Prediction Interface

Model Benchmark Display

Repository Structure
/data                        - (Optional) dataset storage
/notebooks                   - EDA and model development notebooks
/models                      - Serialized ML models if saved
/screenshots                 - Interface preview assets
gradio_app.ipynb             - Dashboard deployment code
README.md
requirements.txt

How to Run

Install required dependencies:

pip install -r requirements.txt


Run the Gradio app:

python gradio_app.ipynb


(Recommended through Jupyter or Google Colab)

Key Insights

Diverse housing markets require adaptable regression strategies

Ensembles like XGBoost and LightGBM handle economic and spatial variability effectively

Model performance varies significantly by geography and feature availability

Real-time prediction deployment improves practical usability of ML models

Future Enhancements

Feature importance and SHAP explainability

Deployment to Hugging Face Spaces or other cloud platforms

Multi-city prediction interface within the same dashboard

Integration of geospatial coordinates for location-aware modeling
