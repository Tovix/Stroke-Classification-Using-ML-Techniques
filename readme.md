# Stroke Classification Using ML Techniques

## Overview

This project analyzes the [healthcare-dataset-stroke-data.csv](healthcare-dataset-stroke-data.csv) to predict the likelihood of stroke occurrence using machine learning techniques. The notebook covers data exploration, preprocessing, feature engineering, model training, evaluation, and insights.

---

## Table of Contents

- [Project Structure](#project-structure)
- [Setup & Requirements](#setup--requirements)
- [Data Exploration](#data-exploration)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results & Findings](#results--findings)
- [Conclusion](#conclusion)
- [Visualizations](#visualizations)

---

## Project Structure

- `strokeProject.ipynb` — Main analysis notebook
- `healthcare-dataset-stroke-data.csv` — Dataset file

---

## Setup & Requirements

Install the required Python libraries:

```sh
pip install numpy pandas seaborn matplotlib scikit-learn plotly tabulate
```

---

## Data Exploration

- Loaded the dataset and checked for missing values and duplicates.
- Explored data types and descriptive statistics.
- Key columns: `gender`, `age`, `hypertension`, `heart_disease`, `ever_married`, `work_type`, `Residence_type`, `avg_glucose_level`, `bmi`, `smoking_status`, `stroke`.

---

## Data Preprocessing

- Filled missing BMI values with the column mean.
- Encoded categorical variables (`gender`, `ever_married`, `work_type`, `Residence_type`, `smoking_status`) using custom label encoding.
- Normalized `avg_glucose_level` and `bmi` columns using min-max normalization.

---

## Feature Engineering

Created new features for analysis:
- **Sex**: Simplified gender.
- **Age Group**: Categorized into Child, Young, Adult, Old Person.
- **Tension**: Based on hypertension.
- **Heart Disease**: Patient/non-patient.
- **Marital Status**: Married/Single.
- **Glucose**: Normal, Pre-Diabetic, Diabetic.
- **BMI Group**: Underweight, Healthy Weight, Overweight, Obese.

---

## Modeling

- **Logistic Regression** and **Random Forest Classifier** were trained to predict the `stroke` outcome.
- Used a train-test split (80/20) without shuffling for reproducibility.
- Evaluated models using Training Score, Test Score, and Mean Square Error (MSE).

---

## Results & Findings

### Model Performance

| Name                | Training Score | Test Score | Mean Square Error [MSE] |
|---------------------|:-------------:|:----------:|:----------------------:|
| Logistic Regression |    93.91%     |  100.00%   |         0.00%          |
| Random Forest       |   100.00%     |   97.36%   |        2.64%           |

### Key Insights

- **Gender**: Males are more likely to have strokes than females.
- **Age**: Old people are at higher risk; young people are at lower risk.
- **Hypertension**: High tension increases stroke risk.
- **Heart Disease**: Patients are more likely to have strokes.
- **Marital Status**: Married people have a higher risk.
- **Residence**: Urban residents are more likely to have strokes.
- **Glucose Level**: Higher glucose increases risk.
- **BMI**: Higher fat percentage increases risk.
- **Smoking**: Smokers are more likely to have strokes.
- **Work Type**: Self-employed individuals have the highest risk.

#### Summary Table

| Most Likely to Have a Stroke           | Least likely to Have a Stroke         |
|----------------------------------------|---------------------------------------|
| Males                                 | Females                              |
| Old people                            | Young People                         |
| People with high tension              | People having normal blood pressure   |
| People with Heart disease             | People with Healthy Heart             |
| Married People                        | Single People                        |
| People living in urban environment    | People living in rural environment    |
| People having high level of glucose   | People having normal level of glucose |
| People with high fat rate             | People with normal fat rate           |
| Smokers                               | Non-smokers                          |
| Self-employment work system           | Other work systems                    |

---


## Conclusion

- Logistic Regression and Random Forest both performed well, with Random Forest achieving perfect training accuracy but slightly lower test accuracy, indicating possible overfitting.
- The analysis identified key demographic and health factors associated with stroke risk.
- The project demonstrates a full ML workflow from data exploration to model evaluation and interpretation.

---

## How to Run

1. Place the dataset (`healthcare-dataset-stroke-data.csv`) in the same directory as the notebook.
2. Open `strokeProject.ipynb` in Jupyter or VS Code.
3. Run all cells to reproduce the analysis and results.

---

## License

This notebook is prepared by ApplAi's Technical And Training Department. Please do not use it outside the training without permission.
