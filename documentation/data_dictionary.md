# Data Dictionary

## Dataset Overview

The HR Workforce Analytics project uses a synthetic employee-level workforce dataset containing **100,000 employee records**.

The intended analytical grain of the dataset is:

> **One row = one employee**

The final analysis-ready Excel table is:

`tblEmployees`

The dataset contains information covering employee demographics, employment characteristics, compensation, performance, workload, development, employee experience and resignation.

This document defines the original dataset fields and the derived analytical fields created during data preparation.

---

# Original Fields

| Field | Description | Analytical Role |
|---|---|---|
| `Employee_ID` | Unique identifier assigned to each employee | Employee identification |
| `Department` | Employee's organisational department | Workforce segmentation |
| `Gender` | Employee gender category | Demographic analysis |
| `Age` | Employee age | Demographic analysis |
| `Job_Title` | Employee's job role or title | Workforce structure |
| `Hire_Date` | Date the employee joined the organisation | Employment history |
| `Years_At_Company` | Number of years the employee has been with the organisation | Tenure and retention analysis |
| `Education_Level` | Employee's education level | Workforce demographics |
| `Performance_Score` | Employee performance score | Performance analysis |
| `Monthly_Salary` | Employee monthly salary | Compensation analysis |
| `Work_Hours_Per_Week` | Average number of hours worked per week | Workload analysis |
| `Projects_Handled` | Number of projects handled by the employee | Productivity analysis |
| `Overtime_Hours` | Number of overtime hours worked | Workload analysis |
| `Sick_Days` | Number of sick days recorded | Workforce experience and workload analysis |
| `Remote_Work_Frequency` | Frequency of remote work | Work arrangement analysis |
| `Team_Size` | Number of employees within the employee's team | Organisational analysis |
| `Training_Hours` | Number of training hours received | Employee development analysis |
| `Promotions` | Number of promotions received | Career progression analysis |
| `Employee_Satisfaction_Score` | Employee satisfaction score | Employee experience analysis |
| `Resigned` | Indicates whether the employee has resigned | Retention analysis |

---

# Derived Analytical Fields

The following fields were created during Phase 2 to support standardised workforce analysis.

| Field | Description | Purpose |
|---|---|---|
| `Duplicate_ID_Check` | Helper field used to identify potential duplicate Employee IDs | Data-quality validation |
| `Age_Group` | Categorises employees into age bands | Demographic segmentation |
| `Tenure_Group` | Categorises employees according to years at the company | Tenure and retention segmentation |
| `Salary_Band` | Categorises employees according to monthly salary ranges | Compensation segmentation |
| `Performance_Category` | Converts the numerical performance score into descriptive categories | Performance segmentation |
| `Promotion_Flag` | Binary indicator identifying employees with one or more recorded promotions | Promotion analysis |
| `Resignation_Flag` | Binary indicator derived from the `Resigned` field | Retention analysis |

---

# Derived Field Definitions

## Age Group

Employees are grouped into:

- `22-29`
- `30-39`
- `40-49`
- `50+`

Validation result:

**100,000 employees**

---

## Tenure Group

Employees are grouped into:

- `0-2 Years`
- `3-5 Years`
- `6-10 Years`
- `11+ Years`

Validation results:

| Tenure Group | Employees |
|---|---:|
| 0-2 Years | 30,373 |
| 3-5 Years | 29,930 |
| 6-10 Years | 39,697 |
| 11+ Years | 0 |
| **Total** | **100,000** |

The absence of employees in the `11+ Years` category reflects the distribution of the source dataset rather than a formula error.

---

## Salary Band

Employees are grouped into:

- `Lower`
- `Lower-Middle`
- `Middle`
- `Upper-Middle`
- `Higher`

Validation results:

| Salary Band | Employees |
|---|---:|
| Lower | 14,289 |
| Lower-Middle | 20,129 |
| Middle | 17,151 |
| Upper-Middle | 25,783 |
| Higher | 22,648 |
| **Total** | **100,000** |

---

## Performance Category

The numerical performance score is converted into descriptive categories:

| Performance Score | Performance Category |
|---:|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Moderate |
| 4 | High |
| 5 | Very High |

Validation results:

| Performance Category | Employees |
|---|---:|
| Very Low | 19,940 |
| Low | 20,013 |
| Moderate | 19,999 |
| High | 19,928 |
| Very High | 20,120 |
| **Total** | **100,000** |

---

## Promotion Flag

`Promotion_Flag` provides a binary indicator based on whether an employee has recorded promotions.

| Promotion Flag | Employees |
|---|---:|
| 0 | 33,296 |
| 1 | 66,704 |
| **Total** | **100,000** |

---

## Resignation Flag

`Resignation_Flag` provides a binary indicator derived from the original `Resigned` field.

| Resignation Flag | Employees |
|---|---:|
| 0 | 89,990 |
| 1 | 10,010 |
| **Total** | **100,000** |

---

# Salary Validation

The monthly salary field was validated during Phase 2.

| Metric | Result |
|---|---:|
| Minimum Monthly Salary | 3,850 |
| Maximum Monthly Salary | 9,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary | 6,500 |

---

# Field Groupings

The dataset can be broadly organised into the following analytical areas.

### Employee Identification

- `Employee_ID`

### Demographics

- `Gender`
- `Age`
- `Age_Group`
- `Education_Level`

### Employment & Organisation

- `Department`
- `Job_Title`
- `Hire_Date`
- `Years_At_Company`
- `Tenure_Group`
- `Team_Size`

### Compensation

- `Monthly_Salary`
- `Salary_Band`

### Performance & Productivity

- `Performance_Score`
- `Performance_Category`
- `Projects_Handled`

### Workload

- `Work_Hours_Per_Week`
- `Overtime_Hours`
- `Sick_Days`

### Work Arrangement

- `Remote_Work_Frequency`

### Development & Career Progression

- `Training_Hours`
- `Promotions`
- `Promotion_Flag`

### Employee Experience

- `Employee_Satisfaction_Score`

### Retention

- `Resigned`
- `Resignation_Flag`

### Data Quality

- `Duplicate_ID_Check`

---

# Data Quality Validation

Phase 2 included validation of:

- Employee ID uniqueness.
- Duplicate records.
- Missing values.
- Categorical consistency.
- Numerical values.
- Dates.
- Formatting and text consistency.

The final analytical population remained:

**100,000 employees**

Three final population QA checks each reconciled to **100,000**, confirming that the employee population remained unchanged during preparation.

No meaningful duplicate, missing-value or categorical/numerical consistency issues were identified during the validation process.

---

# Data Dictionary Status

**Current status: Phase 2 Complete**

The dictionary now documents:

- The original dataset fields.
- The derived analytical fields created during preparation.
- Derived field definitions.
- Validation results.
- Salary validation results.
- Data-quality validation results.

The data dictionary will be updated again if additional analytical fields are created during later project phases.