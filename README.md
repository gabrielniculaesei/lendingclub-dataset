# LendingClub Credit Risk Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabrielniculaesei/lendingclub-dataset/blob/colab/FAD.ipynb)

## Overview

This project performs a comprehensive credit risk analysis on the LendingClub dataset, an American peer-to-peer lending platform. The analysis spans from exploratory data analysis to predictive modeling.

## Objectives

- Analyze borrower characteristics and loan conditions
- Identify factors associated with loan defaults
- Build predictive models for credit risk assessment
- Provide economic analysis of model performance

## Project Structure

```
lendingclub-dataset/
├── faad.ipynb          # Main analysis notebook
├── Presentation.pdf    # Project presentation
├── loans.csv           # Dataset
└── README.md           # This file
```

## Dataset

The dataset contains information on thousands of loans including:

| Variable | Description |
|----------|-------------|
| `credit_policy` | Whether the customer meets credit criteria (1=yes, 0=no) |
| `purpose` | Purpose of the loan |
| `interest_rate` | Interest rate applied to the loan |
| `installment` | Monthly payment amount |
| `log_annual_income` | Natural log of annual income |
| `dti` | Debt-to-Income ratio |
| `fico_score` | FICO credit score (300-850) |
| `credit_history_days` | Length of credit history in days |
| `revolving_balance` | Current balance on revolving credit |
| `revolving_util` | Percentage of available credit used |
| `inquiries_last_6m` | Credit inquiries in last 6 months |
| `delinquencies_2y` | Late payments in last 2 years |
| `public_records` | Negative public records (bankruptcies, etc.) |
| `not_fully_paid` |  Whether loan was not fully repaid |

## Analysis Structure

### Part 1 - Data Preparation
- Dataset loading and initial exploration
- Variable renaming for readability
- Data type conversion and missing value handling

### Part 2 - Exploratory Data Analysis
- Distribution analysis for all variables
- Outlier detection and treatment
- Individual feature deep-dives (Interest Rate, FICO Score, DTI, etc.)

### Part 3 - Multivariate Analysis
- Correlation and covariance matrices
- Cross-variable relationships
- Default rate analysis by categories

### Part 4 - Statistical Testing
- Shapiro-Wilk normality tests
- Chi-Square tests (Purpose vs Default)
- Independent samples t-tests

### Part 5 - Clustering & Segmentation
- K-Means clustering
- Elbow method and Silhouette analysis
- Risk profile identification
- PCA visualization

### Part 6 - Predictive Models

#### 6.1 Credit Policy Prediction
- Feature selection and correlation analysis
- Logistic Regression with GridSearch
- Bootstrap validation
- Selection bias handling

#### 6.2 Default Prediction
- Feature engineering
- Class imbalance handling
- **Models implemented:**
  - Logistic Regression
  - Decision Tree 
  - Random Forest
- Model comparison (ROC curves, Precision-Recall)
- Threshold optimization
- Economic impact analysis

## Requirements

This project was developed using Anaconda Python distribution. The following packages are required:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy
- graphviz

### Installation

If you have Anaconda installed, most packages are included by default. You may need to install graphviz separately:

```bash
pip install graphviz
```

For a fresh Python installation, install all dependencies with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy graphviz
```

## Getting Started

### Option 1: Google Colab (Recommended)
Click the "Open in Colab" badge at the top of this README.

### Option 2: Local Installation

1. Clone the repository:
```bash
git clone https://github.com/gabrielniculaesei/lendingclub-dataset.git
cd lendingclub-dataset
```

2. Open the notebook:
```bash
jupyter notebook faad.ipynb
```

## Key Findings

The analysis reveals:
- Strong correlation between FICO score and default probability
- DTI ratio as a significant predictor of loan repayment
- Clustering identifies distinct risk profiles among borrowers
- Random Forest achieves best performance for default prediction
- Economic analysis demonstrates model value in lending decisions

