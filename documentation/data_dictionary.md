# Data Dictionary

## Dataset Overview

The HR Workforce Analytics project uses a synthetic employee-level workforce dataset containing **100,000 employee records**.

The analytical grain of the dataset is:

> **One row = one employee**

The dataset contains information covering employee demographics, employment characteristics, compensation, performance, workload, development, employee experience and resignation.

This document defines the original dataset fields and the additional analytical fields created during the project.

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

The following fields were created during Phase 2 — Data Preparation & Excel Data Model.

| Field                  | Purpose                                                                 |
| ---------------------- | ----------------------------------------------------------------------- |
| `Duplicate_ID_Check`   | Identifies potential duplicate Employee IDs for data-quality validation |
| `Age_Group`            | Groups employees into analytical age ranges                             |
| `Tenure_Group`         | Groups employees by length of service                                   |
| `Salary_Band`          | Groups monthly salaries into analytical compensation bands              |
| `Performance_Category` | Converts numerical performance scores into descriptive categories       |
| `Promotion_Flag`       | Indicates whether an employee has recorded at least one promotion       |
| `Resignation_Flag`     | Converts resignation status into a binary analytical flag               |

---

# Phase 3 Analytical Grouping Fields

The following fields were created during Phase 3 — Workforce Analysis.

These fields were created to support descriptive analysis and business-friendly grouping of workforce measures.

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

| Satisfaction ScoreGroup |   |
| ----------------------- | - |
| 1.00-1.49               | 1 |
| 1.50-2.49               | 2 |
| 2.50-3.49               | 3 |
| 3.50-4.49               | 4 |
| 4.50-5.00               | 5 |

---

## Work_Hours_Group

**Purpose:** Group weekly work hours into meaningful workload ranges.

**Formula:**

```excel
=IF([@[Work_Hours_Per_Week]]<=34,"30-34 Hours",IF([@[Work_Hours_Per_Week]]<=39,"35-39 Hours",IF([@[Work_Hours_Per_Week]]<=44,"40-44 Hours",IF([@[Work_Hours_Per_Week]]<=49,"45-49 Hours",IF([@[Work_Hours_Per_Week]]<=54,"50-54 Hours","55-60 Hours")))))
```

**Groups produced:**

| Work HoursGroup |             |
| --------------- | ----------- |
| 30-34           | 30-34 Hours |
| 35-39           | 35-39 Hours |
| 40-44           | 40-44 Hours |
| 45-49           | 45-49 Hours |
| 50-54           | 50-54 Hours |
| 55-60           | 55-60 Hours |

---

## Overtime_Group

**Purpose:** Group overtime hours into meaningful workload categories.

**Formula:**

```excel
=IF([@[Overtime_Hours]]<=5,"Low Overtime",IF([@[Overtime_Hours]]<=10,"Moderate Overtime",IF([@[Overtime_Hours]]<=15,"High Overtime",IF([@[Overtime_Hours]]<=20,"Very High Overtime","Excessive Overtime"))))
```

**Groups produced:**

| Overtime HoursGroup |                    |
| ------------------- | ------------------ |
| 0-5                 | Low Overtime       |
| 6-10                | Moderate Overtime  |
| 11-15               | High Overtime      |
| 16-20               | Very High Overtime |
| 21-29               | Excessive Overtime |

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

# Data Dictionary Status

**Current status: Updated through Phase 3 — Workforce Analysis**

The dictionary documents:

* The original dataset fields
* Phase 2 derived fields
* Phase 3 analytical grouping fields

The analytical population remains **100,000 employees**, with the analytical grain remaining **one row = one employee**.
