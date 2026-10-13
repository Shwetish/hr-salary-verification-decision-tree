# HR Candidate Salary Verification & Prediction Suite
Verifying candidate salary claims and predicting monthly income in the recruitment domain using Decision Tree and Random Forest models.



## 1. Business Problem
### 1.1. What is the business objective?
In recruitment, HR faces challenges verifying candidate salary claims (e.g., verifying if a candidate with X years of experience and specific role truly earns a claimed monthly income). The objective is to build a predictive model using monthly income as the target variable to benchmark and verify candidate salary expectations against market standards.
### 1.2. Are there any constraints?
* Sensitivity to outlier compensation packages across different industries and job levels.
* Ensuring fairness and transparency in automated hiring recommendations.

---

## 2. Data Dictionary
| Feature Name | Data Type | Relevance to Model Building | Description & Reason for Inclusion/Exclusion |
| :--- | :--- | :--- | :--- |
| `Experience` | Numerical (Float/Int) | Highly Relevant | Years of professional work experience. |
| `Job_Role` | Categorical | Relevant | Designation or managerial level (e.g., Regional Manager, Analyst). |
| `Education_Level` | Categorical | Relevant | Highest degree or qualification attained. |
| `Location` | Categorical | Relevant | Work geography / city tier affecting cost of living adjustments. |
| `Monthly_Income` | Numerical (Float) | **Target Variable** | Candidate's monthly salary / CTC used for verification benchmarks. |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1 Summary:** Statistical breakdown of candidate experience levels and salary distributions.
* **3.2 Univariate Analysis:** Histograms of monthly income and experience spreads.
* **3.3 Bivariate Analysis:** Scatter plots of experience vs. monthly income grouped by job role to identify anomalies or inflated claims.

---

## 4. Data Pre-processing
* **4.1 Data Cleaning & Feature Engineering:** Cleaned missing entries, encoded categorical designations, and handled outlier salaries using interquartile range (IQR) capping.

---

## 5. Model Building
* **5.1 Scaling:** Normalized numerical attributes for regression/classification stability.
* **5.2 Model Training:** Built Decision Tree and Random Forest models to predict expected monthly income based on candidate attributes.
* **5.3 Evaluation & Cross-Validation:** Performed train-test splits and cross-validation, evaluating accuracy, mean squared error, and classification metrics when thresholding salary brackets.
* **5.4 Model Output Explanation:** Highlighted how experience and job role split the decision nodes to justify predicted salary benchmarks.

---

## 6. Business Benefits & Impact
* Streamlines HR verification processes, preventing fraudulent salary inflation during recruitment negotiations.
* Ensures fair, market-aligned compensation offers.
