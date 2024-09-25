# Defect Analysis in Manufacturing

## Overview

This project focuses on predicting defect occurrences in a manufacturing environment using a Random Forest model. The project explores various factors like production volume, quality control metrics, energy consumption, and workforce productivity to forecast defect status (low or high).

The analysis includes:
- Exploratory Data Analysis (EDA)
- Feature Importance Analysis
- Model Training using Random Forest
- Model Optimization with Hyperparameter Tuning
- Comparison with other models (XGBoost, Gradient Boosting)

## Dataset

The dataset used in this project simulates a manufacturing defect prediction problem with various features:

- **ProductionVolume**: Number of units produced per day
- **ProductionCost**: Cost incurred for production per day
- **SupplierQuality**: Supplier quality ratings
- **DefectRate**: Defects per thousand units produced
- **MaintenanceHours**: Hours spent on maintenance per week
- ... and more.

Target variable:
- **DefectStatus**: (0 for Low Defects, 1 for High Defects)

## File Descriptions

- `Defect_analysis.ipynb`: Jupyter notebook containing the entire analysis, including data visualization, model training, and evaluation.
- `manufacturing_defect_dataset.csv`: The dataset used for training and evaluating the model.
- `best_random_forest_model.pkl`: The trained Random Forest model saved for future predictions.

## Installation

To run the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/mkim1234/Defect_analysis_project.git
   cd Defect_analysis_project

## Usage

1. **Run the notebook**: Open the `Defect_analysis.ipynb` file and run all cells to execute the data analysis and model training.
2. **Model Testing**: Load the pre-trained model from `best_random_forest_model.pkl` and test it on new data.

```python
import pickle

# Load the trained model
with open('models/best_random_forest_model.pkl', 'rb') as file:
    model = pickle.load(file)

# Predict on new data
predictions = model.predict(new_data)
print(predictions)

