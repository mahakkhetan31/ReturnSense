# ReturnSense – E-Commerce Return Risk Prediction

A machine learning project that predicts the likelihood of e-commerce product returns using **PySpark and Machine Learning**.

## About the Project

ReturnSense analyses customer behaviour, purchase history, product details, discounts, payment methods, and shipping preferences to identify patterns associated with product returns.

The objective is to help e-commerce businesses understand return behaviour and prioritise potentially high-risk orders.

## Tech Stack

- Python
- PySpark & Apache Spark
- Spark MLlib
- Pandas & NumPy
- Matplotlib
- Kaggle Notebook

## Project Workflow

1. Data Cleaning and Preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Model Building and Evaluation
5. Return Risk Segmentation
6. Final Test Predictions

## Research Findings & Business Insights

The analysis revealed several patterns in e-commerce return behaviour:

- **Product Category:** Clothing recorded the highest return rate at 53.05%.
- **Shipping Method:** Express shipping had a return rate of 53.22%, compared with 45.51% for standard shipping.
- **Payment Method:** Apple Pay orders showed a return rate of 52.17%.
- **Coupon Usage:** Orders using coupons had a higher return rate (49.63%) than orders without coupons (43.99%).
- **Risk Prioritisation:** Reviewing the top 20% highest-risk orders captured 24.88% of all actual returns in the validation dataset.

These findings indicate associations between transaction characteristics and return behaviour, not necessarily causal relationships.

## Model Performance

Three classification models were evaluated using validation ROC-AUC.

| Model | ROC-AUC |
|---|---:|
| Logistic Regression | 0.5897 |
| Random Forest | 0.5923 |
| **Gradient-Boosted Trees** | **0.5928** |

Gradient-Boosted Trees achieved the highest ROC-AUC and was selected for final model training.

## Key Results

- Analysed **200,000 training records**.
- Generated predictions for **50,000 test records**.
- Identified important return-related patterns across customer behaviour and transaction characteristics.
- Developed a three-level return risk segmentation: Low, Medium, and High.
- Captured 24.88% of actual returns within the top 20% highest-risk validation orders.

## Project Structure

```text
ReturnSense/
│
├── e-commerce-return-prediction.ipynb
├── returnsense/
│   ├── Model Outputs
│   ├── Prediction Files
│   ├── Analysis CSVs
│   └── Visualisations
│
├── returnsense_submission.csv
└── README.md
```

## Conclusion

ReturnSense demonstrates an end-to-end data science workflow combining big data processing, exploratory analysis, feature engineering, and machine learning to analyse and predict e-commerce return risks.

The findings highlight opportunities for data-driven return management, while the modest model performance leaves scope for further improvement through advanced features and modelling techniques.
