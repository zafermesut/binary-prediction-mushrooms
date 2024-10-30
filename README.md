# Mushroom Toxicity Prediction 🌲🍄

Welcome to the Mushroom Toxicity Prediction project! This project is part of the Kaggle Playground Series 2024 and aims to predict whether a mushroom is edible or poisonous based on its physical characteristics. The dataset offers a great opportunity to practice binary classification techniques using various machine learning algorithms.

## Project Overview

In this competition, the goal is to build a model capable of accurately predicting mushroom toxicity. Each mushroom is classified as either **edible** or **poisonous** based on a set of physical attributes. Given the simplicity yet usefulness of the dataset, this project is ideal for refining skills in classification and optimizing for specific evaluation metrics.

### Dataset

The dataset provided by Kaggle consists of various categorical features, each describing the physical properties of mushrooms. Some of these features include cap shape, color, odor, gill size, and more. For privacy and safety reasons, the dataset does not include actual mushroom species names.

### Evaluation Metric

The primary evaluation metric used in this competition is the **Matthews Correlation Coefficient (MCC)**. MCC is particularly effective in binary classification tasks with imbalanced classes, as it takes into account true and false positives and negatives, making it a robust measure of model performance. The best MCC score possible is 1, indicating a perfect prediction, while 0 indicates random performance.

## Model Selection and Approach

Several algorithms were evaluated for this project, with the **RandomForestClassifier** achieving the highest scores:

- **Random Forest Classifier**: This model achieved a public MCC score of **0.98439** and a private score of **0.98442**. Random Forest was chosen for its ability to handle categorical data effectively, as well as its robustness in providing high-quality predictions with limited hyperparameter tuning.

- **LightGBM**: Although initially considered, LightGBM required more memory than available on free Google Colab sessions, leading to a pivot towards Random Forest. However, LightGBM remains an ideal candidate for future improvement on a more powerful machine.

### Feature Engineering and Processing

Key steps involved in data preprocessing and feature engineering include:

1. **Encoding Categorical Variables**: All categorical features were encoded to numeric values suitable for model input.
2. **Hyperparameter Tuning**: Grid search and cross-validation were used to fine-tune model parameters for optimal performance.
3. **Class Balancing**: MCC's robustness allowed the model to perform effectively without additional balancing steps.

## Results

The Random Forest model's high MCC scores demonstrate its effectiveness in accurately distinguishing between edible and poisonous mushrooms based on physical characteristics alone.

| Metric | Public Score | Private Score |
| ------ | ------------ | ------------- |
| MCC    | 0.98439      | 0.98442       |

These results reflect the model’s strong ability to generalize well on unseen data and highlight the robustness of ensemble methods in categorical classification tasks.

## Future Work

Potential improvements for the project include:

- **Exploring Advanced Models**: With access to higher RAM, training with **LightGBM** and **XGBoost** may yield even better results.
- **Feature Importance Analysis**: Identifying the most influential features could provide insights into the physical traits most strongly associated with toxicity.
- **Deployment Considerations**: The model could be refined for real-world applications, possibly as a tool for educational purposes in identifying mushroom toxicity risks.

Thank you for exploring this project, and happy coding!
