# Data Dictionary

## Dataset Overview

The HR Workforce Analytics project uses a synthetic employee-level workforce dataset containing **100,000 employee records**.

The intended analytical grain of the dataset is:

> **One row = one employee**

The dataset contains information covering employee demographics, employment characteristics, compensation, performance, workload, development, employee experience and resignation.

This document provides a high-level definition of the original dataset fields.

Derived analytical fields and data-quality results will be documented after the data preparation phase has been completed.

---

## Original Fields

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

## Field Groupings

The dataset can be broadly organised into the following analytical areas.

### Employee Identification

- `Employee_ID`

### Demographics

- `Gender`
- `Age`
- `Education_Level`

### Employment & Organisation

- `Department`
- `Job_Title`
- `Hire_Date`
- `Years_At_Company`
- `Team_Size`

### Compensation

- `Monthly_Salary`

### Performance & Productivity

- `Performance_Score`
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

### Employee Experience

- `Employee_Satisfaction_Score`

### Retention

- `Resigned`

---

## Analytical Use

The dataset will be prepared and validated before being used for detailed analysis.

During the data preparation phase, additional analytical fields may be created where they provide clear analytical value.

Any derived fields will be added to this document once they have been created and validated.

---

## Data Dictionary Status

**Current status: Initial dataset documentation**

The dictionary currently describes the original dataset only.

Data-quality findings and derived analytical fields will be documented as the project progresses.