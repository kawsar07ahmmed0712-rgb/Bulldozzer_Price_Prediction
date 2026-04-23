# Numeric 

| Column Name                     | কেন দরকার                                      |
| ------------------------------- | ---------------------------------------------- |
| `Feature_Name`                  | feature identify করার জন্য                     |
| `Dtype`                         | actual storage type বোঝার জন্য                 |
| `Primary_Feature_Type`          | numeric / maybe category-like 
বোঝার জন্য       |

| `Missing_Count`                 | missing burden                                 |
| `Missing_Percentage`            | missing severity                               |
| `Non_Null_Count`                | usable data count                              |

| `Unique_Count`                  | continuous না coded-category-like বুঝতে        |
| `Unique_Ratio`                  | low-card numeric detect করতে                   |
| `Mean`                          | central tendency                               |
| `Median`                        | skew বুঝতে                                     |
| `Mode`                          | dominant value বুঝতে                           |
| `Std`                           | spread                                         |
| `Min`                           | lower boundary                                 |
| `Max`                           | upper boundary                                 |
| `Range`                         | spread quick view                              |
| `Q1 (25%)`                      | quartile                                       |
| `Q3 (75%)`                      | quartile                                       |
| `IQR`                           | spread + outlier base                          |
| `P01`                           | extreme low percentile                         |
| `P05`                           | lower tail                                     |
| `P95`                           | upper tail                                     |
| `P99`                           | extreme high percentile                        |
| `Skewness`                      | asymmetry                                      |
| `Skewness_Level`                | human-readable skew label                      |
| `Kurtosis`                      | tail heaviness                                 |
| `Distribution_Shape`            | symmetric / right-skew / left-skew             |
| `Zero_Count`                    | zero-heavy feature detect                      |
| `Zero_Percentage`               | zero inflation                                 |
| `Negative_Count`                | negative values আছে কি না                      |
| `Negative_Percentage`           | sign issue / business logic                    |
| `IQR_Outlier_Count`             | outlier burden                                 |
| `IQR_Outlier_Percentage`        | outlier severity                               |
| `Lower_Bound_IQR`               | outlier lower threshold                        |
| `Upper_Bound_IQR`               | outlier upper threshold                        |
| `Constant_Flag`                 | same value everywhere?                         |
| `Near_Constant_Flag`            | almost same value?                             |
| `Looks_Like_Categorical_Flag`   | numeric হলেও category-like?                    |
| `Suggested_Base_Imputation`     | mean / median / custom hint                    |
| `Suggested_Base_Transformation` | none / log1p candidate / yeo-johnson candidate |
| `Suggested_Base_Outlier_Action` | keep / review / cap candidate                  |
| `Data_Quality_Issues`           | invalid values / weird pattern                 |
| `Cleaning_Action`               | short plain-English action                     |

# categorical
| Column Name                            | কেন দরকার                                    |
| -------------------------------------- | -------------------------------------------- |
| `Feature_Name`                         | identify                                     |
| `Dtype`                                | actual storage type                          |
| `Primary_Feature_Type`                 | categorical class                            |
| `Missing_Count`                        | missing burden                               |
| `Missing_Percentage`                   | missing severity                             |
| `Non_Null_Count`                       | usable count                                 |
| `Unique_Count`                         | cardinality                                  |
| `Unique_Ratio`                         | uniqueness density                           |
| `Top_Category`                         | dominant label                               |
| `Top_Count`                            | dominant frequency                           |
| `Top_Percentage`                       | dominance strength                           |
| `Second_Category`                      | second biggest label                         |
| `Second_Count`                         | second category count                        |
| `Second_Percentage`                    | second dominance                             |
| `Entropy`                              | label diversity                              |
| `Cardinality_Level`                    | low / medium / high / very high              |
| `Is_High_Cardinality`                  | direct flag                                  |
| `Rare_Threshold_Count`                 | rare cutoff used                             |
| `Rare_Category_Count`                  | কত rare labels আছে                           |
| `Rare_Row_Count`                       | rare rows কত                                 |
| `Rare_Row_Percentage`                  | rare burden                                  |
| `Single_Dominant_Label_Flag`           | এক label dominant কি না                      |
| `Constant_Flag`                        | one-category only কি না                      |
| `Near_Constant_Flag`                   | almost one-category?                         |
| `Has_Whitespace_Issue_Flag`            | leading/trailing spaces issue                |
| `Has_Case_Inconsistency_Flag`          | `Male`, `male`, `MALE` type issue            |
| `Has_Special_Character_Variation_Flag` | formatting inconsistency                     |
| `Average_Label_Length`                 | free-text-ish category detect                |
| `Max_Label_Length`                     | suspicious long category detect              |
| `Looks_Like_Text_Flag`                 | text-like feature কি না                      |
| `Looks_Like_ID_Flag`                   | ID-like label কি না                          |
| `Is_Consistent_Binary_Format`          | yes/no, y/n, true/false consistency          |
| `Suggested_Base_Missing_Action`        | Missing label / mode                         |
| `Suggested_Base_Rare_Action`           | keep / group Other                           |
| `Suggested_Base_Encoding_Family`       | one-hot / freq / target-safe later / raw-cat |
| `Data_Quality_Issues`                  | formatting/spelling/etc                      |
| `Cleaning_Action`                      | plain-English action                         |


# datetime 
| Column Name                     | কেন দরকার                                  |
| ------------------------------- | ------------------------------------------ |
| `Feature_Name`                  | identify                                   |
| `Primary_Feature_Type`          | datetime class                             |
| `Dtype`                         | actual type                                |
| `Missing_Count`                 | missing burden                             |
| `Missing_Percentage`            | missing severity                           |
| `Is_Datetime_Parsed`            | parse success                              |
| `Minimum_Date`                  | start point                                |
| `Maximum_Date`                  | end point                                  |
| `Date_Span_Days`                | total span                                 |
| `Date_Span_Years_Approx`        | long-term span                             |
| `Unique_Date_Count`             | temporal diversity                         |
| `Duplicate_Date_Percentage`     | repeated dates কত                          |
| `Most_Frequent_Date`            | dominant date                              |
| `Most_Frequent_Date_Percentage` | dominant date strength                     |
| `Future_Date_Count`             | impossible future values                   |
| `Suspiciously_Old_Date_Count`   | old invalid values                         |
| `Null_Parse_Count`              | failed parse count                         |
| `Has_Time_Component_Flag`       | datetime না date-only?                     |
| `Year_Range`                    | year coverage                              |
| `Month_Coverage_Count`          | কত মাস cover হয়েছে                         |
| `DayOfWeek_Coverage_Count`      | weekday diversity                          |
| `Is_Monotonic_Flag`             | sorted/time-series-ish?                    |
| `Potential_Leakage_Risk_Note`   | post-event date risk আছে কি না             |
| `Suggested_FE_List`             | year/month/quarter/dayofweek/dayofyear/... |
| `Datetime_FE_Action`            | create datetime-derived features           |
| `Data_Quality_Issues`           | parse/future/old issues                    |
| `Cleaning_Action`               | plain-English action                       |
