# ML_Course_Project - Diabetes & Divorce Prediction

A comparative study of **Logistic Regression** and **Random Forest** applied to two binary classification datasets.

---

## Project Structure

```
project/
│
├── data/
│   ├── diabetes.csv          # Diabetes dataset (768 samples, 8 features)
│   ├── divorce_data.csv      # Divorce dataset (170 samples, 54 features)
│   └── reference.tsv         # Divorce questions refrence 
│
├── diabetes.ipynb   # Diabetes model code
├── divorce.ipynb    # Divorce model code
├── .gitignore       # Ignores all the data files 
└── README.md
```

---

## Requirements

- Python 3.8+
- pip

### Install Dependencies

Run this command in your terminal inside the project folder:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

## Dataset Setup

Download the datasets and place them in a folder called `data/` in the same directory as your scripts.

- **Diabetes dataset:** https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset
  - Save as `data/diabetes.csv`
- **Divorce dataset:** https://www.kaggle.com/datasets/andrewmvd/divorce-prediction
  - Save as `data/divorce_data.csv`

> The divorce dataset uses semicolons (`;`) as delimiters — the code handles this automatically with `delimiter=';'`.

---

## Running the Code

### Diabetes Classification

```bash
python diabetes.ipynb
```

This will:
1. Load and preview the dataset
2. Display a class distribution plot (Outcome 0 vs 1)
3. Display a feature correlation heatmap
4. Replace zero values in physiological columns with column medians
5. Scale features and split into 80/20 train/test
6. Train Logistic Regression and Random Forest
7. Print accuracy, classification report, and confusion matrix for each model
8. Display feature importance plot for Random Forest
9. Print a final model comparison summary

### Divorce Classification

```bash
python divorce.ipynb
```

This will:
1. Load the dataset
2. Display a correlation heatmap (lower triangle)
3. Display histogram distributions for all 54 features grouped by divorce outcome
4. Scale features and split into 80/20 train/test
5. Train Logistic Regression and Random Forest
6. Print accuracy, classification report, and normalized confusion matrix for each model
7. Display feature importance plot for Random Forest
8. Print a final model comparison summary

---

## Expected Output

### Diabetes

```
--- Final Model Comparison ---
Logistic Regression: 75.32%
Random Forest: 74.03%
```

### Divorce

```
--- Final Model Comparison ---
Logistic Regression: 94.12%
Random Forest: 94.12%
```
