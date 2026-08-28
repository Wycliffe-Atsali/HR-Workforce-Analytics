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
* Work hours per week
* Projects
* Overtime
* Sick days
* Remote work
* Team size
* Training
* Promotions
* Employee satisfaction
* Resignation status

During the data preparation stage, the dataset was validated and enhanced with analytical fields supporting the workforce analysis.

A detailed description of the dataset fields is maintained in:

`documentation/data_dictionary.md`

---

## Tools

| Tool                 | Purpose                                                          |
| -------------------- | ---------------------------------------------------------------- |
| Microsoft Excel 2016 | Data preparation, analysis, PivotTables, dashboard and reporting |
| Excel PivotTables    | Workforce analysis and aggregation                               |
| Excel Slicers        | Interactive dashboard filtering                                  |
| Excel Charts         | Visual reporting                                                 |
| Git                  | Version control                                                  |
| GitHub               | Portfolio repository and project versioning                      |
| Markdown             | Project documentation                                            |

---

# Project Methodology

The project follows a six-phase analytical framework.

## Phase 1 — Project Setup & Analytical Framework

Established the business scenario, business problem, objectives, stakeholders, analytical scope, business questions and overall methodology.

**Status: Complete**

## Phase 2 — Data Preparation & Excel Data Model

Validated, cleaned and standardised the dataset, created the analysis-ready Excel data model and validated the derived analytical fields.

**Status: Complete**

## Phase 3 — Workforce Analysis

Analysed workforce composition, demographics, compensation, performance, workload, career development, employee experience and retention.

**Status: Complete**

## Phase 4 — HR Reporting & Dashboard

Translated the strongest validated findings into an executive-friendly Excel reporting layer and interactive dashboard.

The dashboard includes:

* Workforce KPI cards
* Workforce composition charts
* Compensation and performance analysis
* Promotion analysis
* Resignation analysis
* Interactive slicers
* Dynamic KPI filtering
* Dashboard-level visual formatting and presentation

**Status: Complete**

## Phase 5 — Insights & Business Recommendations

Interpreted the validated analytical findings and translated them into evidence-based HR insights and practical recommendations.

The recommendations focus on:

* Maintaining and monitoring the positive relationship between performance and compensation.
* Investigating the high overall promotion rate and monitoring promotion quality.
* Maintaining broad workforce and retention monitoring rather than focusing on a single high-risk segment.
* Investigating employee resignation using additional explanatory data.
* Using the dashboard as an ongoing workforce monitoring and management tool.
* Applying targeted interventions only where future evidence identifies meaningful variation.

**Status: Complete**

## Phase 6 — Finalisation & Portfolio Presentation

Completed the final quality assurance, documentation review, repository review and portfolio presentation preparation.

The finalisation stage included:

* Reviewing the completed Excel workbook and analytical outputs.
* Confirming the completed interactive dashboard.
* Including a PDF dashboard snapshot as a portfolio deliverable.
* Reviewing repository structure and file consistency.
* Reviewing project documentation for alignment with the completed workflow.
* Confirming that all six phases of the project are documented.
* Finalising the project for GitHub and portfolio presentation.

**Status: Complete**

---

# Current Project Status

| Phase | Description                           | Status   |
| ----- | ------------------------------------- | -------- |
| 1     | Project Setup & Analytical Framework  | Complete |
| 2     | Data Preparation & Excel Data Model   | Complete |
| 3     | Workforce Analysis                    | Complete |
| 4     | HR Reporting & Dashboard              | Complete |
| 5     | Insights & Recommendations            | Complete |
| 6     | Finalisation & Portfolio Presentation | Complete |

---

# Phase 2 — Data Preparation Summary

The original raw dataset was preserved and a working copy was prepared for analysis.

The working dataset was converted into the Excel Table:

`tblEmployees`

The data preparation process included:

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

## Derived Analytical Fields

The following fields were created and validated:

* `Duplicate_ID_Check`
* `Age_Group`
* `Tenure_Group`
* `Salary_Band`
* `Performance_Category`
* `Promotion_Flag`
* `Resignation_Flag`

During the workforce analysis, additional grouping fields were created:

* `Satisfaction_Group`
* `Work_Hours_Group`
* `Overtime_Group`

These fields provide standardised categories and indicators for analysing workforce patterns and relationships.

---

## Salary Validation

| Metric                 |    Result |
| ---------------------- | --------: |
| Minimum Monthly Salary |     3,850 |
| Maximum Monthly Salary |     9,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary  |     6,500 |

---

# Phase 3 — Workforce Analysis Summary

Phase 3 converted the prepared employee-level dataset into a structured workforce analysis.

The analysis examined:

* Workforce composition
* Demographics
* Compensation
* Performance
* Workload
* Career development
* Employee satisfaction
* Resignation and retention

The analysis was conducted using Excel PivotTables and supporting analytical groupings.

The focus was on identifying meaningful distributions, comparisons and relationships across workforce segments rather than simply producing charts or descriptive summaries.

## Key Workforce Metrics

| Metric                 |    Result |
| ---------------------- | --------: |
| Total Employees        |   100,000 |
| Average Monthly Salary | 6,403.211 |
| Median Monthly Salary  |     6,500 |
| Promotion Rate         |    66.70% |
| Resignation Rate       |    10.01% |
| Average Training Hours |     49.51 |

---

## Selected Analytical Findings

### Workforce Composition

The workforce consists of **100,000 employees** distributed relatively evenly across nine departments.

The largest age group is **50+**, while the largest tenure group is **6-10 Years**.

Overall, the workforce does not show major concentration within a single department or demographic segment.

### Compensation and Performance

Average monthly salary increases progressively across performance categories:

| Performance Category | Average Monthly Salary |
| -------------------- | ---------------------: |
| Very Low             |               5,422.23 |
| Low                  |               5,900.28 |
| Moderate             |               6,409.52 |
| High                 |               6,897.63 |
| Very High            |               7,397.67 |

This represents one of the clearest segment-level patterns identified in the analysis.

The relationship is an observed association and should not be interpreted as proof that performance directly causes salary differences.

### Career Development

The overall promotion rate is:

**66.70%**

Promotion rates remained highly consistent across tenure groups, departments and performance categories.

Average training hours were also relatively consistent across the major workforce segments examined.

### Employee Satisfaction

Satisfaction was grouped into five analytical levels using `Satisfaction_Group`.

Resignation rates across satisfaction groups ranged from approximately **9.52% to 10.33%**.

The observed differences were relatively narrow and did not identify a major satisfaction-based retention-risk segment.

### Workload

Workload was analysed using weekly work hours and overtime groupings.

Resignation rates across overtime groups remained close to the overall resignation rate of **10.01%**.

The analysis therefore did not identify substantial variation in resignation across overtime categories.

### Resignation and Retention

The overall resignation rate is:

**10.01%**

A total of **10,010 employees** had a resignation flag of `1`.

Resignation rates were examined across department, gender, age group, tenure, salary band, performance, promotion status, satisfaction and overtime.

Across these segments, resignation rates generally remained close to the overall workforce rate.

The descriptive analysis therefore did not identify a single major workforce segment as a substantially different resignation-risk group.

---

# Phase 4 — HR Reporting & Dashboard

Phase 4 translated the strongest validated findings from the workforce analysis into an executive-friendly Excel dashboard.

The dashboard was designed to provide a concise overview of the workforce while allowing users to interactively explore selected workforce segments.

## Dashboard Components

The dashboard includes five core KPI indicators:

* Total Employees
* Average Monthly Salary
* Median Monthly Salary
* Promotion Rate
* Resignation Rate

The dashboard also contains six analytical charts covering areas such as:

* Workforce distribution by department
* Workforce distribution by age group
* Workforce distribution by gender
* Compensation by performance category
* Promotion patterns by performance category
* Resignation patterns by department

The dashboard uses:

* PivotTables
* PivotCharts
* Slicers
* Linked KPI calculations
* Consistent visual formatting
* Executive-style layout

## Dashboard Interactivity

Two slicers were incorporated into the dashboard to allow users to filter the workforce analysis interactively.

The dashboard supports combined filtering, allowing users to examine selected workforce segments such as a particular department and gender combination.

The KPI cards linked to the underlying PivotTable calculations respond dynamically to the selected filters.

The median salary KPI is retained as an overall workforce benchmark rather than being presented as a dynamically filtered median.

## Dashboard Design

The dashboard was designed with emphasis on:

* Clear hierarchy
* Consistent colours
* Readable labels
* Appropriate chart sizing
* Minimal visual clutter
* Consistent KPI presentation
* Executive-friendly communication

The objective was to create a reporting layer that communicates the workforce story clearly without attempting to display every analytical result produced during Phase 3.

A detailed dashboard description is available in:

`documentation/phase_4_dashboard.md`

A PDF snapshot of the completed dashboard is included in the repository as:

`HR_Workforce_Analytics_Dashboard.pdf`

**Status: Complete**

---

# Phase 5 — Insights & Business Recommendations

Phase 5 translated the validated findings from the workforce analysis into practical business insights and recommendations.

The recommendations were developed using the following reasoning framework:

**Finding → Evidence → Business Meaning → Recommendation**

## Key Insights

### Compensation and Performance

The strongest observed segment-level pattern was the progressive increase in average monthly salary across performance categories.

**Business Insight:** The organisation shows a clear association between higher performance categories and higher average compensation.

**Recommendation:** HR should maintain regular monitoring of compensation across performance levels and periodically review whether the observed progression remains consistent, fair and aligned with the organisation's reward philosophy.

### Career Development

The overall promotion rate was **66.70%**, with limited variation across departments, tenure groups and performance categories.

**Business Insight:** Promotion incidence is high and broadly consistent across the workforce, but the consistency also means the available analysis does not identify a specific group requiring immediate intervention.

**Recommendation:** HR should supplement promotion monitoring with additional measures such as promotion timing, role progression, promotion quality and post-promotion outcomes to better understand the effectiveness of career development.

### Retention

The overall resignation rate was **10.01%**, and no single segment showed substantially different resignation levels.

**Business Insight:** The descriptive analysis does not support concentrating retention interventions on one specific demographic or workforce segment.

**Recommendation:** Maintain organisation-wide retention monitoring and collect or analyse additional explanatory variables to investigate the underlying reasons for employee resignation.

### Employee Experience and Workload

Resignation rates showed limited variation across satisfaction and overtime groups.

**Business Insight:** Satisfaction and overtime differences alone did not identify a major retention-risk segment within the descriptive analysis.

**Recommendation:** Avoid assuming that a single satisfaction or workload category is driving resignation. Future analysis should investigate combinations of factors and additional employee experience information.

### Workforce Monitoring

Several major workforce measures showed limited variation across the analysed segments.

**Business Insight:** The absence of large differences is itself a meaningful finding and suggests that management should avoid creating targeted interventions without sufficient evidence.

**Recommendation:** Use the completed dashboard for ongoing monitoring and investigate new patterns only when meaningful deviations emerge.

A detailed record of the insights and recommendations is available in:

`documentation/insights_recommendations.md`

**Status: Complete**

---

# Phase 6 — Finalisation & Portfolio Presentation

Phase 6 completed the final review and preparation of the project as a portfolio-ready analytical deliverable.

The final review confirmed that:

* The six-phase analytical workflow was completed.
* The analytical population remained documented as **100,000 employees**.
* The final Excel workbook is included in the repository.
* The interactive HR dashboard is included in the workbook.
* A PDF dashboard snapshot is included for portfolio viewing.
* The repository structure contains the required project deliverables.
* The documentation reflects the completed analytical workflow from project setup through business recommendations.
* The project is ready for portfolio presentation and repository publication.

## Final Project Outcome

The completed project demonstrates an end-to-end HR workforce analytics workflow using Microsoft Excel 2016.

The workflow progressed from:

**Business Problem → Data Preparation → Workforce Analysis → Reporting → Recommendations → Finalisation**

The project demonstrates:

* Business problem definition.
* Analytical framework development.
* Data validation and quality assurance.
* Excel data modelling.
* Derived analytical field creation.
* Workforce analysis using PivotTables.
* KPI development.
* Interactive dashboard reporting.
* Evidence-based business interpretation.
* Practical HR recommendations.
* Documentation and version control.
* Final portfolio preparation.

**Status: Complete**

---

# Project Completion

All six phases of the HR Workforce Analytics project have been completed.

The final project combines a validated employee-level dataset, structured workforce analysis, an interactive Excel dashboard, evidence-based business recommendations and supporting documentation.

The project is now complete and prepared as a portfolio-ready example of an end-to-end Excel-based workforce analytics workflow.

---

# Project Structure

```text
HR-Workforce-Analytics/
│
├── documentation/
│   ├── business_scenario.md
│   ├── project_objectives.md
│   ├── data_dictionary.md
│   ├── methodology.md
│   ├── workforce_analysis.md
│   ├── phase_4_dashboard.md
│   └── insights_recommendations.md
│
├── HR_Workforce_Analytics.xlsx
├── HR_Workforce_Analytics_Dashboard.pdf
├── README.md
├── CHANGELOG.md
└── .gitignore
```

---

# Analytical Principles

The project follows several core analytical principles:

1. **Business First** — Analysis begins with business questions.

2. **Data Quality Before Analysis** — Data is validated before interpretation.

3. **Preserve the Raw Data** — The original dataset remains unchanged.

4. **Purposeful Transformation** — Derived fields are created only when analytically useful.

5. **Association Does Not Equal Causation** — Observed relationships are not automatically interpreted as causal.

6. **Business Relevance** — Findings are prioritised according to their potential business value.

7. **Meaningful Differences Matter** — Small differences are not overstated.

8. **Reproducibility** — Important analytical decisions are documented.

9. **Progressive Documentation** — Documentation is updated as each phase is completed.
