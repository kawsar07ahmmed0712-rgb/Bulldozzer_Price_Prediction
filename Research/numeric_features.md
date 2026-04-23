# Numeric Raw Feature Report Structure

## 1. Feature Identity

| Column Name | Purpose |
|---|---|
| `Feature_Name` | Identify the feature |
| `Dtype` | Understand the actual storage type |
| `Primary_Feature_Type` | Understand whether the feature is truly numeric or maybe category-like |

---

## 2. Missing Value Summary

| Column Name | Purpose |
|---|---|
| `Missing_Count` | Show the total number of missing values |
| `Missing_Percentage` | Show the severity of missingness |
| `Non_Null_Count` | Show the usable number of observations |

---

## 3. Uniqueness and Feature Nature

| Column Name | Purpose |
|---|---|
| `Unique_Count` | Help detect whether the feature is continuous or coded-category-like |
| `Unique_Ratio` | Help identify low-cardinality numeric features |
| `Looks_Like_Categorical_Flag` | Indicate whether the numeric feature behaves like a categorical feature |

---

## 4. Central Tendency

| Column Name | Purpose |
|---|---|
| `Mean` | Show the average value |
| `Median` | Help understand skewness and robust center |
| `Mode` | Show the most frequent value |

---

## 5. Dispersion / Spread

| Column Name | Purpose |
|---|---|
| `Std` | Show the overall spread |
| `Min` | Show the lower boundary |
| `Max` | Show the upper boundary |
| `Range` | Provide a quick spread summary |
| `Q1 (25%)` | Show the first quartile |
| `Q3 (75%)` | Show the third quartile |
| `IQR` | Show spread and support outlier detection |

---

## 6. Percentile Summary

| Column Name | Purpose |
|---|---|
| `P01` | Show the extreme lower percentile |
| `P05` | Show the lower tail |
| `P95` | Show the upper tail |
| `P99` | Show the extreme upper percentile |

---

## 7. Distribution Shape

| Column Name | Purpose |
|---|---|
| `Skewness` | Measure asymmetry |
| `Skewness_Level` | Give a human-readable skewness label |
| `Kurtosis` | Measure tail heaviness |
| `Distribution_Shape` | Describe whether the distribution is symmetric, right-skewed, or left-skewed |

---

## 8. Special Value Pattern

| Column Name | Purpose |
|---|---|
| `Zero_Count` | Detect zero-heavy features |
| `Zero_Percentage` | Measure zero inflation |
| `Negative_Count` | Check whether negative values exist |
| `Negative_Percentage` | Detect possible sign issues or business-rule violations |

---

## 9. Outlier Summary

| Column Name | Purpose |
|---|---|
| `IQR_Outlier_Count` | Show the number of outliers |
| `IQR_Outlier_Percentage` | Show the severity of outliers |
| `Lower_Bound_IQR` | Show the lower outlier threshold |
| `Upper_Bound_IQR` | Show the upper outlier threshold |

---

## 10. Stability / Variability Flags

| Column Name | Purpose |
|---|---|
| `Constant_Flag` | Indicate whether the feature has the same value everywhere |
| `Near_Constant_Flag` | Indicate whether the feature is almost constant |

---

## 11. Base Feature Engineering Hints

| Column Name | Purpose |
|---|---|
| `Suggested_Base_Imputation` | Suggest a base missing-value handling strategy |
| `Suggested_Base_Transformation` | Suggest whether transformation may be useful |
| `Suggested_Base_Outlier_Action` | Suggest whether outlier review or capping may be needed |

---

## 12. Data Quality Notes

| Column Name | Purpose |
|---|---|
| `Data_Quality_Issues` | Highlight invalid values or unusual patterns |
| `Cleaning_Action` | Provide a short plain-English cleaning instruction |