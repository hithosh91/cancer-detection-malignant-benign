
# Project Overview
This repository contains a machine learning project for predicting breast cancer diagnoses (Malignant or Benign) using a Decision Tree Classifier. The code processes a dataset, visualizes the diagnosis distribution, trains a model, and evaluates its performance across various tree depths. The project uses Python with libraries like pandas, numpy, seaborn, matplotlib, and scikit-learn.
# Dataset
Features: 30 numerical attributes (e.g., radius, texture, perimeter) from fine needle aspirate (FNA) images.
Target: A diagnosis column with values 'M' (Malignant) or 'B' (Benign).
ID Column: An identifier column dropped during preprocessing.


# Prerequisites

Python 3.8 or higher
Required libraries:
pandas
numpy
seaborn
matplotlib
scikit-learn







# workflow
Loads and preprocesses data.csv (maps 'M'→1, 'B'→0; drops 'id' column).
Displays a bar plot of diagnosis distribution using seaborn.
Splits data into training (80%) and testing (20%) sets.
Trains a Decision Tree Classifier and outputs the test set accuracy.
Evaluates model performance for tree depths 1 to 20, printing training accuracy and 10-fold cross-validation scores.


# WorkFlowStructure

# 1.Data Preprocessing:
Loads data.csv using pandas.
Checks for missing values using isnull().sum().
Maps diagnosis labels: 'M' → 1, 'B' → 0.
Removes the id column.


# 2.Visualization:
Generates a bar plot of diagnosis counts using seaborn.


# Model Training:
Splits data into training (80%) and testing (20%) sets with train_test_split.
Trains a Decision Tree Classifier and computes test set accuracy.


# Hyperparameter Tuning:
Tests tree depths from 1 to 20.
For each depth:
Calculates training accuracy.
Computes mean 10-fold cross-validation score.





# Example Output

Test set accuracy (example):0.9473684210526315


# Hyperparameter tuning results (example):Depth  : 1  Training Accuracy : 0.8505494505494505  Cross val score : 0.8989010989010989
Depth  : 2  Training Accuracy : 0.9164835164835164  Cross val score : 0.9164835164835164
...
Depth  : 20 Training Accuracy : 1.0  Cross val score : 0.9252747252747253



Results

The Decision Tree Classifier typically achieves ~90–95% accuracy on the test set, depending on the data split.
Cross-validation scores indicate the model’s generalization performance, with higher depths potentially causing overfitting (e.g., training accuracy of 1.0 but lower cross-validation scores).

Repository Details
The repository has been created and includes:

breast_cancer_prediction.py: The core script.
README.md: This documentation.
.gitignore: Excludes unnecessary files (e.g., __pycache__, data.csv).

To update the repository with this README:

Replace the existing README.md with this content.
Commit and push changes:git add README.md
git commit -m "Update README with detailed project information"
git push origin main



.gitignore
The .gitignore file contains:
__pycache__/
*.pyc
venv/
data.csv

License
This project is licensed under the MIT License.
Contributing
Contributions are welcome! Please open an issue or submit a pull request for bug fixes, improvements, or new features.
Contact
For questions or feedback, contact the repository owner via GitHub.
