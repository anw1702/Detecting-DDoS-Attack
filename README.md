# Network Activity Classification

## Problem Description

The goal of this project is to classify network activities as either normal or a specific type of attack known as "Neptune." The dataset contains detailed records of network connections, with various attributes associated with each connection. Each record is labeled to indicate whether the activity is normal (no attack) or a Neptune attack.

### Dataset Details

- **Training Set:**
    - Contains 86,845 rows.
    - Columns include features related to network activities.
    - Target variable: "Attack" (0 for normal, 1 for Neptune).
- **Test Set:**
    - Contains 21,712 entries.

## Steps to Solve the Problem

### 1. Data Preprocessing

#### Handling Missing Values
Check for missing values in the dataset. Decide how to handle them:
- Impute missing values (using mean, median, or mode).
- Remove rows with missing values.

#### Encoding Categorical Features
Since machine learning models require numerical input, encode categorical features:
- One-Hot Encoding: Create binary columns for each category.
- Label Encoding: Assign a unique integer to each category.

### 2. Model Training

Choose a suitable classification algorithm (e.g., Logistic Regression, Random Forest, or Gradient Boosting). Follow these steps:
1. Split the data into training and validation sets.
2. Train the model using the training data.

### 3. Evaluation

Evaluate the model's performance using the validation set:
- Calculate precision, recall, and F1 score:
    - **Precision**: Proportion of true positive predictions among all positive predictions.
    - **Recall**: Proportion of true positive predictions among all actual positive instances.
    - **F1 Score**: Harmonic mean of precision and recall.

Fine-tune hyperparameters and validate the model thoroughly. Finally, use the trained model to predict labels for the test set.
