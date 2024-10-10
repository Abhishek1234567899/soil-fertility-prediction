# Soil Fertility Prediction

This project aims to predict soil fertility based on elemental soil analysis data. The notebook demonstrates how various soil parameters influence fertility, using machine learning techniques to classify soil into three categories: Less Fertile, Fertile, and Highly Fertile.

## Project Overview

This project uses soil data with features representing the chemical composition and properties of the soil to predict its fertility level. The goal is to build a model that can accurately classify soil fertility based on input features like Nitrogen, Phosphorous, Potassium levels, pH value, and other minerals.

### Dataset

The dataset includes the following features:

- **N**: Nitrogen content in soil
- **P**: Phosphorous content in soil
- **K**: Potassium content in soil
- **pH**: Soil acidity
- **EC**: Electrical conductivity
- **OC**: Organic carbon
- **S**: Sulfur content
- **Zn**: Zinc content
- **Fe**: Iron content
- **Cu**: Copper content
- **Mn**: Manganese content
- **B**: Boron content

### Target Variable

- **Fertility Class**: The fertility level of the soil, classified as:
  - 0: Less Fertile
  - 1: Fertile
  - 2: Highly Fertile

## Models and Methods

The project utilizes the following machine learning algorithms:

1. **Random Forest Classifier**: Tuned using Grid Search for optimal hyperparameters.
2. **Support Vector Classifier (SVC)**
3. **Decesion Tree

The `RandomForestClassifier` was fine-tuned using `GridSearchCV` with the following parameters:
- `n_estimators`: Number of trees in the forest (200, 300, 500).
- `max_features`: Maximum number of features considered for splitting (`sqrt`, `log2`).
- `max_depth`: Maximum depth of each tree (4 to 10).
- `criterion`: Function to measure the quality of a split (`gini`, `entropy`).

## Results

The best parameters were selected using cross-validation, and the model was evaluated based on its accuracy score and classification report. Confusion matrices were also visualized to understand the model's performance better.

### Model Evaluation Metrics

- **Accuracy Score**: The overall accuracy of the model on the validation set.
- **Classification Report**: Provides precision, recall, and F1-score for each class.

## Installation and Requirements

To run the notebook and reproduce the results, you need to install the following libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
