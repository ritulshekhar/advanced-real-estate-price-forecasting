Global Housing Price Prediction using Advanced Regression Models

This project implements and benchmarks multiple regression algorithms to predict housing prices across diverse geographical regions. Five real-world datasets are explored with a standardized machine learning pipeline, and the final model is deployed through a Gradio-based web interface for interactive predictions.

Project Overview

Housing price estimation involves non-linear and region-specific patterns influenced by property characteristics, location, and socio-economic factors. The purpose of this project is to:

Analyze housing datasets from different cities and countries

Develop regression models suited for each market

Compare model performance across datasets

Deploy an end-to-end solution for practical use

The project follows a structured workflow including preprocessing, model evaluation, visualization, and deployment.

Datasets Used

Ames Housing (Kaggle): Predicting sale price of residential properties in Ames, Iowa

Bengaluru Housing (Public dataset): Residential property price prediction in Bengaluru, India

King County Housing (Kaggle): House prices in the Seattle–Tacoma region, USA

Melbourne Housing (Kaggle): Property sale prices in Melbourne, Australia

California Housing (StatLib / sklearn): Median house value prediction across California census tracts

Methods and Models

Algorithms evaluated:

Linear Regression

Ridge Regression

Lasso Regression

Elastic Net

Random Forest Regressor

XGBoost Regressor

LightGBM Regressor

Core processing pipeline:

Handling missing values and structural inconsistencies

Outlier treatment and feature engineering

One-hot encoding for categorical data

Scaling and normalization for numeric variables

Train-test splits and cross-validation scoring

Evaluation metrics used:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² Score

Best Performing Models by Dataset

Ames Housing → XGBoost demonstrated the strongest generalization capability

Bengaluru Housing → XGBoost achieved highest predictive accuracy given high price variability

King County Housing → LightGBM performed best on a larger and more complex dataset

Melbourne Housing → LightGBM delivered consistent performance across diverse property features

California Housing → LightGBM achieved the best generalization on population-scale data

These results emphasize that tree-based boosting methods provide the most reliable performance for real estate valuation problems.

Deployment Interface

A Gradio dashboard is developed for interactive real-time predictions.
Users can input key features such as:

Overall construction quality

Living area and lot area

Basement size and number of bathrooms

Garage capacity

Year built

Neighborhood category

The dashboard returns an estimated selling price based on the trained model.

Screenshots are included inside the screenshots/ directory.

Repository Structure
/data                         - datasets used in model development
/notebooks                    - model training, evaluation, and EDA files
/gradio_app.ipynb             - deployed prediction interface
/screenshots                  - UI screenshots for documentation
/models (optional)            - serialized ML pipelines
requirements.txt
README.md

How to Run

Install required packages:

pip install -r requirements.txt


Open and execute the Gradio application in Google Colab or a local environment:

python gradio_app.ipynb


(Gradio will generate a shareable link for the interface.)

Key Learning Outcomes

Comparative analysis of regression algorithms across five distinct real-estate markets

Techniques for data preprocessing in heterogeneous environments

Hyperparameter tuning for ensemble methods

Deployment of ML solutions for end-user interaction

Interpretation of performance metrics for decision-driven insights

Future Enhancements

SHAP-based explainability for feature impact analysis

Integration of geographic and economic indicators

Public deployment on Hugging Face Spaces or Streamlit Community Cloud

Dataset expansion to additional cities for broader generalization
