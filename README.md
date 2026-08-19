# HR Workforce Analytics

## Project Overview

The **HR Workforce Analytics** project is an Excel-based workforce analysis designed to transform employee-level HR data into meaningful business insights.

The project examines workforce composition, employee performance, compensation, career progression, employee experience and retention to help HR leadership better understand the characteristics and behaviour of the workforce.

The analysis follows a structured business-oriented workflow:

**Business Problem → Data Preparation → Workforce Analysis → Reporting → Recommendations**

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

* Understand the composition of the workforce.
* Examine employee demographics and organisational structure.
* Analyse compensation across workforce segments.
* Evaluate employee performance.
* Examine workload and productivity indicators.
* Analyse employee development and career progression.
* Evaluate employee satisfaction.
* Investigate employee resignation patterns.
* Identify meaningful workforce patterns and potential areas of concern.
* Translate analytical findings into practical HR recommendations.

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

* Employee identification
* Department
* Gender
* Age
* Job title
* Hire date
* Tenure
* Education
* Performance
* Salary
* Working hours
* Projects
* Overtime
* Sick days
* Remote work
* Team size
* Training
* Promotions
* Employee satisfaction
* Resignation status

During Phase 2, the dataset was validated and enhanced with analytical fields supporting later workforce analysis.

A detailed description of the dataset fields is maintained in:

`documentation/data_dictionary.md`

---

## Tools

| Tool                 | Purpose                                     |
| -------------------- | ------------------------------------------- |
| Microsoft Excel 2016 | Data preparation, analysis and reporting    |
| Git                  | Version control                             |
| GitHub               | Portfolio repository and project versioning |
| Markdown             | Project documentation                       |

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

Analyse workforce composition, demographics, compensation, performance, productivity, development, employee experience and retention.

**Status: Upcoming**

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

| Phase | Description                           | Status          |
| ----- | ------------------------------------- | --------------- |
| 1     | Project Setup & Analytical Framework  | ✅ Complete      |
| 2     | Data Preparation & Excel Data Model   | ✅ Complete      |
| 3     | Workforce Analysis                    | ⏳ Upcoming      |
| 4     | HR Reporting & Dashboard              | ⏳ Upcoming      |
| 5     | Insights & Recommendations            | ⏳ Upcoming      |
| 6     | Finalisation & Portfolio Presentation | ⏳ Upcoming      |

---

## Phase 2 — Data Preparation Summary

The original raw dataset was preserved and a working copy was prepared for analysis.

The working dataset was converted into the Excel Table:

`tblEmployees`

The Phase 2 process included:

* Employee ID validation.
* Duplicate checking.
* Missing-value checks.
* Categorical consistency checks.
* Numerical validation.
* Date validation.
* Formatting and text consistency checks.
* Creation of analytical derived fields.
* Final population reconciliation.

The completed analytical population is:

**100,000 employees**

The final quality-assurance checks reconciled to the full employee population, confirming that the analytical population remained unchanged during preparation.

### Derived Analytical Fields

The following fields were created and validated:

* `Duplicate_ID_Check`
* `Age_Group`
* `Tenure_Group`
* `Salary_Band`
* `Performance_Category`
* `Promotion_Flag`
* `Resignation_Flag`

These fields provide standardised categories and indicators for the workforce analysis in Phase 3.

---

## Salary Validation

During Phase 2, the salary field was validated.

| Metric | Result |
|---|---:|
| Minimum Monthly Salary | 3,850 |
| Maximum Monthly Salary | 9,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary | 6,500 |

---

## Derived Field Validation

The derived fields were reconciled against the full employee population.

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
| Very Low | 19,940 |
| Low | 20,013 |
| Moderate | 19,999 |
| High | 19,928 |
| Very High | 20,120 |
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
| Lower | 14,289 |
| Lower-Middle | 20,129 |
| Middle | 17,151 |
| Upper-Middle | 25,783 |
| Higher | 22,648 |
| **Total** | **100,000** |

---

## Project Structure

```text
HR-Workforce-Analytics/
│
├── documentation/
│   ├── business_scenario.md
│   ├── project_objectives.md
│   ├── data_dictionary.md
│   └── methodology.md
│
├── HR_Workforce_Analytics.xlsx
├── README.md
├── CHANGELOG.md
└── .gitignore
```

---

## Analytical Approach

The project will follow several principles throughout the analysis:

* Begin with business questions rather than charts.
* Validate data before drawing conclusions.
* Preserve the original dataset.
* Use derived fields only when they provide analytical value.
* Distinguish association from causation.
* Prioritise findings with business relevance.
* Document important analytical decisions.
* Maintain a reproducible workflow.

---

## Phase 2 Completion

Phase 2 established the analysis-ready Excel data model.

The original employee population was preserved at **100,000 records**, with one row representing one employee.

The dataset was validated for duplicates, missing values, categorical consistency, numerical validity, dates and general formatting. Analytical fields were then created and validated to support the next stage of the project.

The project is now ready to proceed to:

**Phase 3 — Workforce Analysis**