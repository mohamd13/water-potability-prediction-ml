# Water Potability Prediction using Machine Learning

A comparative study of supervised machine learning algorithms for drinking water potability prediction, including feature importance analysis, hyperparameter optimization, and exhaustive feature ablation.

> This repository accompanies the paper:
>
> **Machine Learning-Based Drinking Water Potability Prediction: A Comparative Study of Classification Models with Feature Importance Analysis**

---

## Overview

Access to safe drinking water is a critical global challenge. Traditional laboratory testing is accurate but often expensive and unsuitable for real-time monitoring.

This project investigates whether machine learning models can accurately predict drinking water potability using physicochemical measurements.

Five supervised learning algorithms are compared under a rigorous experimental protocol, including:

- Random Forest
- Decision Tree
- Support Vector Machine (SVM)
- Logistic Regression
- K-Nearest Neighbors (KNN)

The study also includes:

- Hyperparameter optimization using GridSearchCV
- 10-fold cross-validation
- Feature importance analysis (MDI vs. Permutation Importance)
- Leave-One-Out feature analysis
- Exhaustive evaluation of all 63 possible feature subsets

---

## Dataset

**Dataset:** `water_potability.csv`

The dataset contains:

- **4,011 samples**
- **6 physicochemical features**
- Binary target:
  - `1` → Potable
  - `0` → Non-potable

### Features

- pH
- Solids (TDS)
- Chloramines
- Sulfate
- Trihalomethanes
- Turbidity

---

## Repository Structure

```
.
├── water_potability_complete.ipynb   # Complete implementation
├── water_potability.csv              # Dataset
├── README.md
└── paper/                            # (optional) Research paper
```

---

## Experimental Pipeline

1. Data loading
2. Exploratory Data Analysis (EDA)
3. Train/Test Split (80/20)
4. Model Training
5. Hyperparameter Optimization
6. Cross Validation
7. Model Evaluation
8. Feature Importance Analysis
9. Feature Ablation Study

---

## Models Evaluated

| Model | Accuracy | F1-score | AUC |
|--------|---------:|---------:|---------:|
| Random Forest | **89.91%** | **0.8991** | **0.9172** |
| Decision Tree | 81.07% | 0.8107 | 0.8107 |
| Logistic Regression | 79.33% | 0.7931 | 0.8659 |
| SVM | 75.34% | 0.7441 | 0.7995 |
| KNN | 72.85% | 0.7259 | 0.7688 |

Random Forest achieved the best overall performance after hyperparameter optimization.

---

## Feature Importance

Two complementary feature importance methods were investigated:

- Mean Decrease in Impurity (MDI)
- Permutation Importance (PI)

The analysis shows that MDI underestimates the importance of **pH** and **Turbidity**, while Permutation Importance identifies them as among the most informative predictors.

---

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/mohamd13/water-potability-prediction-ml.git
```

Move into the project directory:

```bash
cd water-potability-prediction-ml
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
water_potability_complete.ipynb
```

---

## Reproducibility

The experiments were performed using:

- Train/Test split: 80/20
- Stratified sampling
- Random seed: 42
- GridSearchCV (5-fold)
- 10-fold Stratified Cross Validation

Evaluation metrics:

- Accuracy
- F1-score (Macro)
- ROC-AUC

---

## Citation

If you use this repository, please cite:

```bibtex
@article{bentahrour2025water,
  title={Machine Learning-Based Drinking Water Potability Prediction: A Comparative Study of Classification Models with Feature Importance Analysis},
  author={Bentahrour, Abir and Djeghaba, Mohammed Baha Eddine},
  year={2025}
}
```

---

## Authors

**Abir Bentahrour**

Department of Computer Science

University of Bari Aldo Moro

---

**Mohammed Baha Eddine Djeghaba**

Department of Computer Science

University of Bari Aldo Moro

GitHub: https://github.com/mohamd13

---

## License

This project is released under the MIT License.

---

## Acknowledgements

This work was developed as part of the Machine Learning course at the University of Bari Aldo Moro (Academic Year 2025–2026).
