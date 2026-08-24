# HR Workforce Analytics

## Project Overview

The **HR Workforce Analytics** project is an Excel-based workforce analysis designed to transform employee-level HR data into meaningful business insights.

The project examines workforce composition, employee performance, compensation, career progression, employee experience and retention to help HR leadership better understand the characteristics and behaviour of the workforce.

The analysis follows a structured business-oriented workflow:

**Business Problem → Data Preparation → Workforce Analysis → Reporting → Recommendations → Finalisation**

The project uses **Microsoft Excel 2016** as the primary analytical tool, with Git and GitHub used for version control and portfolio documentation.

---

## Business Scenario

An organisation has accumulated a large employee dataset containing demographic, employment, compensation, performance, workload, development, satisfaction and resignation information.

Although the organisation has access to this information, HR leadership needs a clearer understanding of the workforce and the factors associated with employee outcomes.

The purpose of this project is to analyse the employee data and translate the findings into practical HR insights that can support workforce planning and management decisions.

A detailed description of the business scenario is available in:

`documentation/business_scenario.md`

---

## Project Objectives

The project aims to:

- Understand the composition of the workforce.
- Examine employee demographics and organisational structure.
- Analyse compensation across workforce segments.
- Evaluate employee performance.
- Examine workload and productivity indicators.
- Analyse employee development and career progression.
- Evaluate employee satisfaction.
- Investigate employee resignation patterns.
- Identify meaningful workforce patterns and potential areas of concern.
- Translate analytical findings into practical HR recommendations.

The detailed project objectives and business questions are documented in:

`documentation/project_objectives.md`

---

## Dataset

The project uses a synthetic HR workforce dataset containing **100,000 employee records**.

The final analytical population remains:

> **100,000 employees**

The analytical grain is:

> **One row = one employee**

The analysis-ready Excel table is:

`tblEmployees`

The dataset contains information covering areas such as:

- Employee identification
- Department
- Gender
- Age
- Job title
- Hire date
- Tenure
- Education
- Performance
- Salary
- Work hours per week
- Projects
- Overtime
- Sick days
- Remote work
- Team size
- Training
- Promotions
- Employee satisfaction
- Resignation status

During the data preparation stage, the dataset was validated and enhanced with analytical fields supporting the workforce analysis.

A detailed description of the dataset fields is maintained in:

`documentation/data_dictionary.md`

---

## Tools

| Tool | Purpose |
|---|---|
| Microsoft Excel 2016 | Data preparation, analysis and reporting |
| Git | Version control |
| GitHub | Portfolio repository and project versioning |
| Markdown | Project documentation |

---

## Project Methodology

The project follows a six-phase analytical framework.

### Phase 1 — Project Setup & Analytical Framework

Establish the business scenario, business problem, objectives, stakeholders, analytical scope, business questions and overall methodology.

**Status: Complete**

### Phase 2 — Data Preparation & Excel Data Model

Validate, clean and standardise the dataset, create the analysis-ready Excel data model and validate the derived analytical fields.

**Status: Complete**

### Phase 3 — Workforce Analysis

Analyse workforce composition, demographics, compensation, performance, workload, career development, employee experience and retention.

**Status: Complete**

### Phase 4 — HR Reporting & Dashboard

Translate the most important analytical findings into an executive-friendly Excel reporting layer and dashboard.

**Status: Upcoming**

### Phase 5 — Insights & Business Recommendations

Interpret the analytical findings and develop evidence-based HR recommendations.

**Status: Upcoming**

### Phase 6 — Finalisation & Portfolio Presentation

Complete quality assurance, documentation, repository review and final portfolio presentation.

**Status: Upcoming**

---

## Current Project Status

| Phase | Description | Status |
|---|---|---|
| 1 | Project Setup & Analytical Framework | Complete |
| 2 | Data Preparation & Excel Data Model | Complete |
| 3 | Workforce Analysis | Complete |
| 4 | HR Reporting & Dashboard | Upcoming |
| 5 | Insights & Recommendations | Upcoming |
| 6 | Finalisation & Portfolio Presentation | Upcoming |

---

# Phase 2 — Data Preparation Summary

The original raw dataset was preserved and a working copy was prepared for analysis.

The working dataset was converted into the Excel Table:

`tblEmployees`

The data preparation process included:

- Employee ID validation.
- Duplicate checking.
- Missing-value checks.
- Categorical consistency checks.
- Numerical validation.
- Date validation.
- Formatting and text consistency checks.
- Creation of analytical derived fields.
- Final population reconciliation.

The completed analytical population is:

**100,000 employees**

The final quality-assurance checks reconciled to the full employee population, confirming that the analytical population remained unchanged during preparation.

## Derived Analytical Fields

The following fields were created and validated:

- `Duplicate_ID_Check`
- `Age_Group`
- `Tenure_Group`
- `Salary_Band`
- `Performance_Category`
- `Promotion_Flag`
- `Resignation_Flag`

During the workforce analysis, additional grouping fields were created to support meaningful analysis of employee experience and workload:

- `Satisfaction_Group`
- `Work_Hours_Group`
- `Overtime_Group`

These fields provide standardised categories and indicators for analysing workforce patterns and relationships.

---

## Salary Validation

During the data preparation stage, the salary field was validated.

| Metric | Result |
|---|---:|
| Minimum Monthly Salary | 3,850 |
| Maximum Monthly Salary | 9,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary | 6,500 |

---

## Derived Field Validation

The primary derived fields were reconciled against the full employee population.

### Age Group

| Age Group | Employees |
|---|---:|
| 22-29 | 20,492 |
| 30-39 | 25,465 |
| 40-49 | 25,710 |
| 50+ | 28,333 |
| **Total** | **100,000** |

### Tenure Group

| Tenure Group | Employees |
|---|---:|
| 0-2 Years | 30,373 |
| 3-5 Years | 29,930 |
| 6-10 Years | 39,697 |
| 11+ Years | 0 |
| **Total** | **100,000** |

The absence of employees in the `11+ Years` category reflects the distribution of the dataset rather than a formula error.

### Performance Category

| Performance Category | Employees |
|---|---:|
| Very Low | 20,120 |
| Low | 20,013 |
| Moderate | 19,999 |
| High | 19,940 |
| Very High | 19,928 |
| **Total** | **100,000** |

### Promotion Flag

| Promotion Flag | Employees |
|---|---:|
| 0 | 33,296 |
| 1 | 66,704 |
| **Total** | **100,000** |

### Resignation Flag

| Resignation Flag | Employees |
|---|---:|
| 0 | 89,990 |
| 1 | 10,010 |
| **Total** | **100,000** |

### Salary Band

| Salary Band | Employees |
|---|---:|
| Lower | 20,129 |
| Lower-Middle | 17,151 |
| Middle | 25,783 |
| Upper-Middle | 22,648 |
| Higher | 14,289 |
| **Total** | **100,000** |

---

# Phase 3 — Workforce Analysis Summary

Phase 3 converted the prepared employee-level dataset into a structured workforce analysis.

The analysis examined:

- Workforce composition
- Demographics
- Compensation
- Performance
- Workload
- Career development
- Employee satisfaction
- Resignation and retention

The analysis was conducted using Excel PivotTables and supporting analytical groupings.

The focus was on identifying meaningful distributions, comparisons and relationships across workforce segments rather than simply producing charts or descriptive summaries.

---

## Key Workforce Metrics

| Metric | Result |
|---|---:|
| Total Employees | 100,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary | 6,500 |
| Promotion Rate | 66.70% |
| Resignation Rate | 10.01% |
| Average Training Hours | 49.51 |

---

## Selected Analytical Findings

### 1. Workforce Composition

The workforce consists of **100,000 employees** distributed relatively evenly across the nine departments.

Gender distribution was also broadly balanced between female and male employees, while the `Other` category represented a smaller proportion of the workforce.

The largest age group was **50+**, followed by the **40-49** and **30-39** age groups.

Tenure was concentrated across the three defined categories, with the largest employee population in the **6-10 Years** group.

Overall, the workforce structure does not show major concentration within a single department or demographic segment.

---

### 2. Compensation and Performance

Compensation was analysed across performance categories and other workforce segments.

Average salary differences between performance categories were limited, indicating that higher performance categories did not show a strong material separation in compensation within the dataset.

This finding suggests that compensation differences should not be interpreted as being strongly driven by performance alone based on the observed data.

The salary benchmark for the overall workforce was:

- **Average Monthly Salary:** 6,403.211
- **Median Monthly Salary:** 6,500
- **Minimum Monthly Salary:** 3,850
- **Maximum Monthly Salary:** 9,000

The close relationship between the average and median salary provides a useful benchmark for understanding overall compensation levels.

---

### 3. Career Development

The overall promotion rate was:

> **66.70%**

Promotion rates remained highly consistent across tenure groups:

| Tenure Group | Promotion Rate |
|---|---:|
| 0-2 Years | 66.63% |
| 3-5 Years | 66.96% |
| 6-10 Years | 66.56% |
| **Overall** | **66.70%** |

Promotion rates were also highly consistent across departments and performance categories, with only small differences between groups.

Training hours showed similarly limited variation across departments.

The analysis therefore found **no material differences in promotion or training patterns across the major workforce segments examined**.

---

### 4. Employee Satisfaction

Employee satisfaction was grouped into five analytical levels using:

`Satisfaction_Group`

The grouping converted the original satisfaction score into standardised categories from **1 to 5**.

The analysis found relatively limited variation in resignation rates across satisfaction groups.

The observed resignation rates ranged from **9.52% to 10.33%**, indicating no major separation between satisfaction categories within the dataset.

This result should be interpreted as an observed association rather than evidence that satisfaction has no relationship with employee retention in a broader organisational context.

---

### 5. Workload

Workload was analysed using:

- `Work_Hours_Per_Week`
- `Work_Hours_Group`
- `Overtime_Hours`
- `Overtime_Group`

The work hours grouping created six business-friendly ranges:

- 30-34 Hours
- 35-39 Hours
- 40-44 Hours
- 45-49 Hours
- 50-54 Hours
- 55-60 Hours

The overtime grouping created five workload categories:

- Low Overtime
- Moderate Overtime
- High Overtime
- Very High Overtime
- Excessive Overtime

Resignation rates across overtime groups remained close to the overall workforce resignation rate of **10.01%**, with no substantial variation between the categories.

---

### 6. Resignation and Retention

The overall resignation rate was:

> **10.01%**

A total of **10,010 employees** had a resignation flag of `1`.

Resignation rates were analysed across:

- Department
- Gender
- Age Group
- Tenure Group
- Remote Work Frequency
- Salary Band
- Performance Category
- Promotion Status
- Satisfaction Group
- Overtime Group

Across the analysed segments, resignation rates generally remained close to the overall rate.

Selected examples include:

- **Department:** approximately 9.56% to 10.54%
- **Age Group:** approximately 9.84% to 10.11%
- **Tenure Group:** approximately 9.95% to 10.04%
- **Salary Band:** approximately 9.92% to 10.14%
- **Performance Category:** approximately 9.70% to 10.19%
- **Satisfaction Group:** approximately 9.52% to 10.33%
- **Overtime Group:** approximately 9.85% to 10.18%

Promotion status also showed virtually no meaningful difference:

| Promotion Status | Resignation Rate |
|---|---:|
| No Promotion | 10.04% |
| Promotion | 9.99% |
| **Overall** | **10.01%** |

Overall, the retention analysis identified **no material differences in resignation rates across the major workforce segments examined**.

This is an important analytical finding in itself and indicates that no single examined characteristic stood out as a strong differentiator of resignation within this synthetic dataset.

---

## Phase 3 Analytical Conclusion

The Phase 3 analysis produced several key conclusions:

1. **The workforce is broadly distributed across departments and major demographic segments.**
2. **The overall compensation benchmark is centred around an average monthly salary of 6,403.211 and a median of 6,500.**
3. **Compensation differences across performance categories were not materially large.**
4. **The overall promotion rate is high at 66.70% and remains highly consistent across tenure, departments and performance categories.**
5. **Training levels also showed limited variation across departments.**
6. **The overall resignation rate is 10.01%.**
7. **Resignation rates remained relatively consistent across the workforce segments examined.**
8. **No major workforce segment emerged as a strong resignation-risk differentiator based on the available data.**
9. **The absence of material differences is itself a meaningful analytical result and should not be replaced with unsupported explanations.**

The analysis identifies observed patterns and associations only. It does not establish causal relationships between employee characteristics and workforce outcomes.

---

## Project Structure

```text
HR-Workforce-Analytics/
│
├── documentation/
│   ├── business_scenario.md
│   ├── project_objectives.md
│   ├── data_dictionary.md
│   ├── methodology.md
│   └── phase_3_workforce_analysis.md
│
├── HR_Workforce_Analytics.xlsx
├── README.md
├── CHANGELOG.md
└── .gitignore