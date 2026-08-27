# Data Dictionary

## Dataset Overview

The HR Workforce Analytics project uses a synthetic employee-level workforce dataset containing **100,000 employee records**.

The analytical grain of the dataset is:

> **One row = one employee**

The dataset contains information covering employee demographics, employment characteristics, compensation, performance, workload, development, employee experience, and resignation.

This document defines the original dataset fields and the additional analytical fields created throughout the project.

---

# Original Fields

| Field                         | Description                                                 | Analytical Role                            |
| ----------------------------- | ----------------------------------------------------------- | ------------------------------------------ |
| `Employee_ID`                 | Unique identifier assigned to each employee                 | Employee identification                    |
| `Department`                  | Employee's organisational department                        | Workforce segmentation                     |
| `Gender`                      | Employee gender category                                    | Demographic analysis                       |
| `Age`                         | Employee age                                                | Demographic analysis                       |
| `Job_Title`                   | Employee's job role or title                                | Workforce structure                        |
| `Hire_Date`                   | Date the employee joined the organisation                   | Employment history                         |
| `Years_At_Company`            | Number of years the employee has been with the organisation | Tenure and retention analysis              |
| `Education_Level`             | Employee's education level                                  | Workforce demographics                     |
| `Performance_Score`           | Employee performance score                                  | Performance analysis                       |
| `Monthly_Salary`              | Employee monthly salary                                     | Compensation analysis                      |
| `Work_Hours_Per_Week`         | Average number of hours worked per week                     | Workload analysis                          |
| `Projects_Handled`            | Number of projects handled by the employee                  | Productivity analysis                      |
| `Overtime_Hours`              | Number of overtime hours worked                             | Workload analysis                          |
| `Sick_Days`                   | Number of sick days recorded                                | Workforce experience and workload analysis |
| `Remote_Work_Frequency`       | Frequency of remote work                                    | Work arrangement analysis                  |
| `Team_Size`                   | Number of employees within the employee's team              | Organisational analysis                    |
| `Training_Hours`              | Number of training hours received                           | Employee development analysis              |
| `Promotions`                  | Number of promotions received                               | Career progression analysis                |
| `Employee_Satisfaction_Score` | Employee satisfaction score                                 | Employee experience analysis               |
| `Resigned`                    | Indicates whether the employee has resigned                 | Retention analysis                         |

---

# Phase 2 Derived Fields

The following fields were created during **Phase 2 — Data Preparation & Excel Data Model**.

| Field                  | Purpose                                                                 |
| ---------------------- | ----------------------------------------------------------------------- |
| `Duplicate_ID_Check`   | Identifies potential duplicate Employee IDs for data-quality validation |
| `Age_Group`            | Groups employees into analytical age ranges                             |
| `Tenure_Group`         | Groups employees by length of service                                   |
| `Salary_Band`          | Groups monthly salaries into analytical compensation bands              |
| `Performance_Category` | Converts numerical performance scores into descriptive categories       |
| `Promotion_Flag`       | Indicates whether an employee has recorded at least one promotion       |
| `Resignation_Flag`     | Converts resignation status into a binary analytical flag               |

These fields were created to support validation, segmentation, and subsequent workforce analysis while preserving the original source fields.

---

# Phase 3 Analytical Grouping Fields

The following fields were created during **Phase 3 — Workforce Analysis**.

These fields were introduced to support descriptive analysis and business-friendly grouping of workforce measures.

| Field                | Source Field                  | Purpose                                                          |
| -------------------- | ----------------------------- | ---------------------------------------------------------------- |
| `Satisfaction_Group` | `Employee_Satisfaction_Score` | Groups satisfaction scores into five analytical levels           |
| `Work_Hours_Group`   | `Work_Hours_Per_Week`         | Groups weekly work hours into meaningful workload ranges         |
| `Overtime_Group`     | `Overtime_Hours`              | Groups overtime hours into business-friendly workload categories |

---

## Satisfaction_Group

**Purpose:** Convert employee satisfaction scores into five analytical levels.

**Formula:**

```excel
=ROUND([@[Employee_Satisfaction_Score]],0)
```

**Groups produced:**

| Satisfaction Score RangeGroup |   |
| ----------------------------- | - |
| 1.00–1.49                     | 1 |
| 1.50–2.49                     | 2 |
| 2.50–3.49                     | 3 |
| 3.50–4.49                     | 4 |
| 4.50–5.00                     | 5 |

The resulting group values correspond to the rounded satisfaction score and provide a simplified five-level satisfaction dimension for PivotTables and analysis.

---

## Work_Hours_Group

**Purpose:** Group weekly work hours into meaningful workload ranges.

**Formula:**

```
```

```text
=IF([@[Work_Hours_Per_Week]]<=34,"30-34 Hours",IF([@[Work_Hours_Per_Week]]<=39,"35-39 Hours",IF([@[Work_Hours_Per_Week]]<=44,"40-44 Hours",IF([@[Work_Hours_Per_Week]]<=49,"45-49 Hours",IF([@[Work_Hours_Per_Week]]<=54,"50-54 Hours","55-60 Hours")))))
```

**Groups produced:**

| Work Hours RangeGroup |             |
| --------------------- | ----------- |
| 30–34                 | 30-34 Hours |
| 35–39                 | 35-39 Hours |
| 40–44                 | 40-44 Hours |
| 45–49                 | 45-49 Hours |
| 50–54                 | 50-54 Hours |
| 55–60                 | 55-60 Hours |

These categories provide a business-friendly view of weekly workload patterns.

---

## Overtime_Group

**Purpose:** Group overtime hours into meaningful workload categories.

**Formula:**

```
```

```text
=IF([@[Overtime_Hours]]<=5,"Low Overtime",IF([@[Overtime_Hours]]<=10,"Moderate Overtime",IF([@[Overtime_Hours]]<=15,"High Overtime",IF([@[Overtime_Hours]]<=20,"Very High Overtime","Excessive Overtime"))))
```

**Groups produced:**

| Overtime Hours RangeGroup |                    |
| ------------------------- | ------------------ |
| 0–5                       | Low Overtime       |
| 6–10                      | Moderate Overtime  |
| 11–15                     | High Overtime      |
| 16–20                     | Very High Overtime |
| 21–29                     | Excessive Overtime |

These categories support workload analysis and allow overtime patterns to be compared across departments, performance categories, satisfaction levels, and resignation status.

---

# Field Groupings

The dataset can be broadly organised into the following analytical areas.

## Employee Identification

* `Employee_ID`

## Demographics

* `Gender`
* `Age`
* `Age_Group`
* `Education_Level`

## Employment & Organisation

* `Department`
* `Job_Title`
* `Hire_Date`
* `Years_At_Company`
* `Tenure_Group`
* `Team_Size`

## Compensation

* `Monthly_Salary`
* `Salary_Band`

## Performance & Productivity

* `Performance_Score`
* `Performance_Category`
* `Projects_Handled`

## Workload

* `Work_Hours_Per_Week`
* `Work_Hours_Group`
* `Overtime_Hours`
* `Overtime_Group`
* `Sick_Days`

## Work Arrangement

* `Remote_Work_Frequency`

## Development & Career Progression

* `Training_Hours`
* `Promotions`
* `Promotion_Flag`

## Employee Experience

* `Employee_Satisfaction_Score`
* `Satisfaction_Group`

## Retention

* `Resigned`
* `Resignation_Flag`

## Data Quality

* `Duplicate_ID_Check`

---

# Dashboard Usage

The **Phase 4 — HR Reporting & Dashboard** stage did not introduce additional analytical fields into the dataset.

Instead, the dashboard uses the validated analytical dataset together with:

* PivotTables
* PivotCharts
* Slicers
* KPI calculations
* Existing derived and analytical grouping fields

The dashboard provides an interactive reporting layer over the workforce analysis.

### Primary Dashboard Filtering Dimensions

The primary dashboard slicers include:

* `Department`
* `Gender`

Additional fields are used within dashboard KPIs, PivotTables, PivotCharts, and supporting analysis.

The dashboard calculations are based on the validated analytical dataset and its existing derived fields.

---

# Phase 5 Usage

The **Phase 5 — Insights & Business Recommendations** stage did not introduce additional dataset fields or transformations.

Phase 5 used the validated fields, metrics, analytical groupings and findings already established during Phases 2 through 4.

The phase focused on interpreting the existing analytical results and translating them into practical HR recommendations.

No new analytical fields were required.

---

# Analytical Table

The final analysis-ready dataset is stored in the Excel table:

```
```

```text
tblEmployees
```

This table contains the original dataset fields together with the validated derived and analytical grouping fields created throughout the project.

---

# Data Quality & Analytical Considerations

The dataset was validated during **Phase 2 — Data Preparation & Excel Data Model** before being used for workforce analysis.

Validation activities included:

* Employee record validation
* Employee ID uniqueness checks
* Duplicate identification
* Missing-value checks
* Categorical consistency checks
* Numerical validation
* Date validation
* Formatting standardisation
* Derived-field validation
* Final analytical quality assurance

The analytical population remains:

**100,000 employees**

The analytical grain remains:

> **One row = one employee**

---

# Analytical Interpretation

The derived and grouping fields in this dictionary are intended primarily for **descriptive and comparative workforce analysis**.

Observed relationships between variables should therefore be interpreted as **associations rather than causal relationships**, unless supported by an appropriate causal research design.

For example, an observed relationship between performance category and average monthly salary should be described as an **observed association** rather than evidence that performance directly causes salary differences.

This principle was maintained throughout the workforce analysis, dashboard reporting and Phase 5 recommendations.

---

# Data Dictionary Status

**Current status: Updated through Phase 5 — Insights & Business Recommendations**

This dictionary documents:

* The original dataset fields
* Phase 2 derived fields
* Phase 3 analytical grouping fields
* Phase 4 dashboard usage
* Phase 5 analytical usage
* The final analytical table
* Data-quality and analytical interpretation considerations

### Current Project Position

| PhaseStatus                                         |              |
| --------------------------------------------------- | ------------ |
| **Phase 1 — Project Setup & Analytical Framework**  | **COMPLETE** |
| **Phase 2 — Data Preparation & Excel Data Model**   | **COMPLETE** |
| **Phase 3 — Workforce Analysis**                    | **COMPLETE** |
| **Phase 4 — HR Reporting & Dashboard**              | **COMPLETE** |
| **Phase 5 — Insights & Business Recommendations**   | **COMPLETE** |
| **Phase 6 — Finalisation & Portfolio Presentation** | **NEXT**     |

---

## Dataset Summary

| AttributeDescription   |                                |
| ---------------------- | ------------------------------ |
| Dataset                | Synthetic HR workforce dataset |
| Analytical population  | 100,000 employees              |
| Analytical grain       | One row = one employee         |
| Primary tool           | Microsoft Excel 2016           |
| Final analytical table | `tblEmployees`                 |
| Documentation status   | Updated through Phase 5        |
