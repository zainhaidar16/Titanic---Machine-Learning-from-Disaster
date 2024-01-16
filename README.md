# Titanic Dataset Analysis

This repository contains code and documentation for the analysis of the Titanic dataset. The goal is to build a predictive model to determine whether a passenger survived or not during the infamous Titanic shipwreck.

## Dataset

The dataset consists of two CSV files:
- `train.csv`: Contains details of a subset of passengers with ground truth on survival.
- `test.csv`: Similar information but without disclosing the ground truth for each passenger.

## Steps

### 1. Feature Engineering

- Added a new feature, `FamilySize`, which represents the total family size on board (Siblings/Spouses + Parents/Children + 1).
- Handled missing values for 'Age', 'Embarked', and 'Fare'.
- Encoded categorical features ('Sex' and 'Embarked') using Label Encoding.

### 2. Data Splitting

- Split the training data into training and validation sets using the `train_test_split` function.

### 3. Model Training

- Used a Decision Tree Classifier for the initial model.
- Employed hyperparameter tuning using GridSearchCV.

### 4. Hyperparameter Tuning

- For Decision Tree:
  - Tuned the 'max_depth' hyperparameter using GridSearchCV.
- For Random Forest:
  - Defined the parameter distribution for 'max_depth' and 'n_estimators'.
  - Utilized RandomizedSearchCV for hyperparameter tuning.
  
### 5. Assess Model Performance

- Evaluated the model(s) on the validation set.
- Calculated accuracy, confusion matrix, and classification report.

### 6. Tree Visualization

- Visualized a decision tree from the Random Forest.
- Saved the visualization as a PNG file.

## Usage

1. Ensure you have Python installed along with the required libraries listed in `requirements.txt`.
2. Run the Jupyter Notebook or Python script (`titanic_analysis.py`) to execute the analysis.
3. Review the results and model performance metrics.
4. Optionally, modify parameters, features, or algorithms for further experimentation.

## Files

- `titanic_analysis.py`: Python script containing the complete analysis code.
- `random_forest_decision_tree.png`: Visualization of a decision tree from the Random Forest.

## Author

Zain Haidar

## Acknowledgments

- The Titanic dataset is sourced from Kaggle.
- This analysis is for educational purposes and to showcase data analysis and machine learning skills.
