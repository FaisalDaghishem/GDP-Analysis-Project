# GDP-Analysis-Project

This project analyzes GDP per capita across countries using World Development Indicators (WDI) from the World Bank.  
The focus is on understanding how **life expectancy** and **population growth** relate to GDP per capita, and whether simple models can predict economic differences across countries.

---

## 1. Project Purpose

The goal of this project is to answer a set of clear questions:

1. How does GDP per capita differ across countries and years?
2. Does higher life expectancy relate to higher GDP per capita?
3. Is population growth linked to economic performance?
4. Can we build a model that predicts GDP per capita using only these indicators?
5. Do non-linear machine learning models perform better than standard linear models?

The project follows the main steps of the **CRISP-DM** process:  
Understanding the questions → Preparing the data → Modeling → Evaluating results → Communicating findings.

---

## 2. Data Summary

- **Source:** World Bank – World Development Indicators.  
- **Key indicators used:**
  - GDP per capita (current US$)
  - Life expectancy at birth (years)
  - Population growth (%)

Data preparation included:
- Converting the WDI dataset from wide to long format.
- Selecting only the indicators needed for the analysis.
- Dropping rows with missing target values.
- Imputing missing values in features.
- Removing indicators that had no usable observations.

---

## 3. Business Questions Answered in the Notebook

The notebook answers these questions with visualizations and statistics:

- General trends in GDP per capita.
- How life expectancy relates to economic performance.
- How population growth trends differ across countries.
- Whether a prediction model can estimate GDP per capita.
- Comparing linear and non-linear models to see which works best.

---

## 4. Modeling Approach

Two modeling stages were used:

### Linear Models (with log-transformed GDP):
- Linear Regression  
- Ridge Regression  
- Lasso Regression  

### Non-Linear Models:
- Decision Tree  
- Random Forest  
- Gradient Boosting  

**Evaluation metrics:**
- MAE (Mean Absolute Error) on log scale  
- R² score  

---

## 5. Key Results

- GDP per capita is highly skewed, so log-transforming the target improved model stability.
- Life expectancy showed a **positive** relationship with GDP per capita.
- Population growth showed a **negative** relationship.
- Linear models reached an R² of about **0.04**.
- Non-linear models performed noticeably better:
  - Random Forest and Gradient Boosting reached **R² ≈ 0.33** with lower MAE.
- Feature importance (Random Forest) shows life expectancy contributes more than population growth.

---

## 6. Repository Structure

- `GDP_Analysis_Project.ipynb` — main notebook with all steps.
- `README.md` — project overview and documentation.

The dataset itself is not uploaded due to size, but the notebook explains how it was obtained from the World Bank.

---

## 7. Tools and Libraries

- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn (regression models, tree-based models, evaluation metrics)




