# Megaline — Mobile Plan Recommendation

**Author:** Ana Paula Takezawa   
**Program:** MBA in Data Science & Artificial Intelligence — TripleTen Brasil  
**Field:** Data Science | Machine Learning | Predictive Modeling  
**Technologies:** Python | Pandas | NumPy | Scikit-learn | Matplotlib | Seaborn  
**Project Type:** Supervised Learning | Classification | Model Evaluation

---

## Project Overview

This project develops a machine learning classification model to recommend the most suitable mobile plan — **Smart** or **Ultra** — to Megaline customers based on their monthly usage behavior.

The goal is to build a model that identifies the appropriate plan for each customer, achieving an accuracy of at least 75%.

## Business Problem

Megaline wants to improve its customer plan recommendation process by using behavioral data to identify which customers are more likely to benefit from the Smart or Ultra plan.

The classification model uses customer usage patterns to predict the recommended plan.

## Dataset

The project uses the `users_behavior.csv` dataset, containing monthly customer usage information.

| Feature | Description |
|---|---|
| `calls` | Number of calls |
| `minutes` | Total call duration in minutes |
| `messages` | Number of text messages |
| `mb_used` | Internet traffic used in megabytes |
| `is_ultra` | Target variable: 1 = Ultra, 0 = Smart |

The dataset contains **3,214 customer records** and five columns.

## Methodology

The project follows a supervised machine learning workflow:

1. Data loading and initial inspection.
2. Data preparation and validation.
3. Stratified division into training, validation, and test sets.
4. Training and comparison of classification models.
5. Hyperparameter tuning using the validation set.
6. Final evaluation using the independent test set.
7. Comparison against a Dummy Classifier baseline.

### Models Evaluated

- Decision Tree Classifier
- Random Forest Classifier
- Logistic Regression
- Dummy Classifier (baseline)

## Results

The Random Forest model achieved the best validation performance and was selected for final testing.

| Metric | Result |
|---|---:|
| Random Forest validation accuracy | 81.80% |
| Random Forest test accuracy | **82.43%** |
| Dummy Classifier test accuracy | 69.36% |
| Minimum required accuracy | 75.00% |

The final model exceeded the required accuracy threshold and outperformed the baseline model.

### Class-Level Performance

The model performed differently across the two customer segments:

- **Smart:** F1-score of 88.12%, with recall of 93.95%.
- **Ultra:** F1-score of 66.27%, with recall of 56.35%.

Although overall accuracy exceeded the project target, the lower recall for Ultra customers indicates that the model still misses a meaningful portion of customers who use the Ultra plan. This limitation is important when considering real-world deployment.

## Key Findings

- Random Forest delivered the strongest overall classification performance among the evaluated models.
- The final test accuracy was 82.43%, exceeding the required 75%.
- The model performed better at identifying Smart customers than Ultra customers.
- The Dummy Classifier baseline confirmed that the selected model provides predictive value beyond a simple baseline.

## Repository Structure

```text
megaline-machine-learning/
├── data/
│   ├── README.md
│   └── users_behavior.csv
├── megaline_mobile_plan_recommendation_ml.ipynb
└── README.md
```

## How to Run

1. Clone this repository.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Ensure the dataset is available in the `data/` directory.
4. Run the notebook cells sequentially.

## Conclusion

The project demonstrates how supervised machine learning can support customer segmentation and mobile plan recommendations.

The Random Forest model achieved 82.43% test accuracy, exceeding the required performance threshold. However, the difference in recall between Smart and Ultra customers highlights an opportunity for further model improvement, particularly in identifying Ultra customers.

---

**Skills Demonstrated:** Data Preparation | Exploratory Data Analysis | Classification | Hyperparameter Tuning | Model Evaluation | Machine Learning
