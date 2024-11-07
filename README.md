# Attrition Prediction with Neural Networks

This project aims to predict employee attrition and department assignment using a neural network with dual output branches. The model uses various features from employee data to understand the factors that contribute to attrition and to categorize employees based on their department.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Model Structure](#model-structure)
4. [Setup and Requirements](#setup-and-requirements)
5. [Running the Code](#running-the-code)
6. [Evaluation](#evaluation)
7. [Future Improvements](#future-improvements)

## Project Overview
This project is designed to:
- **Predict employee attrition** (binary classification).
- **Predict employee department** (multi-class classification).

The model leverages multiple predictors such as job satisfaction, job involvement, and various demographic factors, aiming to reveal potential patterns or signals associated with employee attrition.

## Data Description
The dataset includes information on employee demographics, job satisfaction, and other relevant factors. Here are some key columns used in this model:

- **Age**: Employee's age.
- **HourlyRate**: Employee's hourly pay rate.
- **DistanceFromHome**: Distance between the employee’s home and workplace.
- **JobSatisfaction**: Self-reported job satisfaction rating.
- **TotalWorkingYears**: Total years the employee has been working.
- **NumCompaniesWorked**: Number of previous companies the employee has worked for.

The target columns are:
- **Attrition**: Indicates if an employee left the company.
- **Department**: Employee's department within the company.

## Model Structure
This project uses a neural network with two output branches:
1. **Attrition Output**: Uses a sigmoid activation for binary classification (attrition prediction).
2. **Department Output**: Uses a softmax activation for multi-class classification (department prediction).

The architecture includes:
- Input layer to take in standardized features.
- Two shared hidden layers for capturing general patterns.
- Two branch-specific layers for each output.

## Setup and Requirements
### Prerequisites
- Python 3.6 or later
- Required libraries (install using pip):
  ```bash
  pip install pandas numpy scikit-learn tensorflow

## Files
- **attrition.csv**: Dataset used for training and testing.

## Running the Code
1. Clone or download this repository.
2. Ensure `attrition.csv` is in the same directory as the code file.
3. Run the script to train and evaluate the model.

### Example Code Execution
To run in a Jupyter Notebook or Google Colab, execute each cell as shown in the script. For standalone execution, run the following command:

    python attrition_prediction.py

## Evaluation
The model is evaluated on two metrics:
- **Department Prediction Accuracy**: Measures accuracy in correctly classifying departments.
- **Attrition Prediction Accuracy**: Measures accuracy in predicting whether an employee will leave.

Due to potential class imbalances in the attrition data, consider using precision, recall, and F1-score for a more comprehensive performance evaluation.

## Future Improvements
Potential improvements include:
- **Additional Feature Engineering**: Adding interaction terms or other important features, such as `WorkLifeBalance` and `YearsSinceLastPromotion`.
- **Hyperparameter Tuning**: Experiment with different architectures, layer sizes, and dropout rates to improve model performance.
- **Alternative Models**: Implementing ensemble methods or more complex architectures like recurrent layers to capture temporal patterns (if time-series data is available).

## Summary
This project provides an introductory approach to predicting employee attrition and categorizing employees by department using neural networks. The dual-output architecture allows simultaneous multi-task learning, aiming to help organizations understand and address attrition factors effectively.
