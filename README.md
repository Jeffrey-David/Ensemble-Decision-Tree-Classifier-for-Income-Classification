# Ensemble Decision Tree Classifier for Income Classification
## Introduction

This repository contains the implementation and evaluation of an ensemble decision tree classifier for income classification. The goal is to determine whether a person's income exceeds a certain threshold. The classifier utilizes decision tree-based machine learning algorithms, considering aspects such as performance, time, and data preprocessing.
## Methods and Procedures
### 1. Data Pre-processing

    Handling Missing Values: 2399 rows with missing values (5% of the dataset) were removed to maintain data integrity.

    Balancing the Dataset: The dataset was imbalanced, so 2000 samples from each class were used for training each Decision Tree Classifier.

### 2. Decision Tree Classifier Implementation

    Similarity Measure: Gini impurity was chosen as the similarity metric to assess the quality of splits during the tree-building process.

    Stopping Criterion: The tree construction stops based on maximum tree depth, purity, and minimum samples per leaf to control the tree's growth and complexity.

### 3. Ensemble Model Implementation

    DecisionTreeClassifierHunt: Created multiple times, each trained on a randomly selected part of the training data with replacement, producing a variety of base models.

    Ensemble Voting: Predictions from all base models are combined using majority voting to enhance generalization and reduce overfitting.

### 4. Hyperparameters

    Number of Base Models: Ten base models were trained for the ensemble.

    Max Depth and Min Samples per Leaf: Each base model was set to a maximum depth of 10 and a minimum of 5 samples per leaf.

### 5. Model Training

    Random Sampling: 4000 samples from the training data were randomly selected for each base model to ensure variability in training subsets.

    Training Time: Recorded the training time for each base model.

### 6. Performance and Speed Metrics

    Performance Metrics: Calculated accuracy, precision, recall, and F1-score for the final model.

    Confusion Matrix: Generated to analyze true positives, false positives, true negatives, and false negatives.

    Speed Metrics: Recorded the time taken to train each base model.

## Results

    Confusion Matrix:

    yaml

    Predicted 0   Predicted 1
    Actual 0      10403          957
    Actual 1      1494           2206

    Performance Metrics:
        Accuracy: 0.837
        Precision: 0.697
        Recall: 0.596
        F1-Score: 0.642

    Speed Metrics:
        Final model training time: 29.80 seconds
        Each decision tree classifier training time: about 3 seconds

## Discussion

The results demonstrate the effectiveness of ensemble approaches and decision tree-based classifiers for challenging classification tasks. The methodology supports future developments and applications in fields where precise classification is crucial.
Conclusion

In conclusion, this work successfully implements a Decision Tree Classifier using Hunt's approach and improves classification performance through ensemble learning. Careful data preprocessing and model parameter adjustment, along with the potency of ensemble learning, contribute to impressive outcomes. The accuracy, precision, recall, and F1-Score metrics highlight the significance of data pretreatment and the ensemble learning technique.
