# Project Methodology

## Overview

The HR Workforce Analytics project follows a structured six-phase analytical workflow designed to move from a defined business problem to evidence-based HR insights and recommendations.

The methodology is intended to ensure that:

- Business questions are defined before analysis.
- Data quality is assessed before interpretation.
- Analytical decisions are documented.
- Findings are supported by evidence.
- Insights are translated into practical business recommendations.
- Observed patterns are not incorrectly presented as causal relationships.

The overall workflow is:

**Business Problem → Data Preparation → Workforce Analysis → Reporting → Recommendations → Finalisation**

---

# Six-Phase Framework

## Phase 1 — Project Setup & Analytical Framework

The first phase established the foundation of the project.

Activities completed included:

- Defining the business scenario.
- Identifying the business problem.
- Establishing the primary and supporting project objectives.
- Identifying key stakeholders.
- Defining analytical scope.
- Establishing business questions.
- Identifying relevant workforce analytical perspectives.
- Establishing analytical principles.
- Defining the overall project methodology.
- Establishing project success criteria.

The analytical perspectives established during this phase are:

- Workforce Composition
- Compensation
- Performance
- Productivity & Workload
- Career Development
- Employee Experience
- Retention

The primary stakeholders identified are:

- HR Leadership
- HR Business Partners
- Department Managers
- Senior Management

The project distinguishes between observed associations and causal relationships throughout the analysis.

**Status: Complete**

---

## Phase 2 — Data Preparation & Excel Data Model

Phase 2 prepared the employee dataset for workforce analysis while preserving the original data.

### Data Preparation Workflow

The original `Raw_Data` worksheet was preserved.

A working copy was created as:

`Clean_Data`

The working dataset was converted into an Excel Table named:

`tblEmployees`

The analytical grain remained:

> **One row = one employee**

### Data Validation

The dataset was checked for:

- Employee ID validity.
- Duplicate Employee IDs.
- Missing values.
- Categorical consistency.
- Numerical validity.
- Date validity.
- Formatting and text consistency.
- General data-quality issues.

No meaningful duplicate, missing-value or categorical/numerical consistency issues were identified during the validation process.

The helper field:

`Duplicate_ID_Check`

was retained because it supports the Data Quality worksheet and validation process.

### Derived Analytical Fields

The following analytical fields were created:

- `Duplicate_ID_Check`
- `Age_Group`
- `Tenure_Group`
- `Salary_Band`
- `Performance_Category`
- `Promotion_Flag`
- `Resignation_Flag`

These fields provide standardised categories and indicators for subsequent workforce analysis.

### Derived Field Validation

The derived fields were validated against the full employee population.

| Derived Field | Validation Result |
|---|---:|
| Age Group | 100,000 |
| Tenure Group | 100,000 |
| Performance Category | 100,000 |
| Promotion Flag | 100,000 |
| Resignation Flag | 100,000 |
| Salary Band | 100,000 |

The `11+ Years` tenure category contained zero employees. This reflects the distribution of the source dataset and does not indicate a formula error.

### Final Quality Assurance

Three final population checks were performed.

Each reconciled to:

**100,000 employees**

This confirmed that:

- The employee population remained unchanged.
- The resignation flag reconciled to the full population.
- The promotion flag reconciled to the full population.

### Phase 2 Outcome

The dataset was confirmed as analysis-ready.

The final analytical population is:

**100,000 employees**

The final analytical grain is:

> **One row = one employee**

The final analytical table is:

`tblEmployees`

**Status: Complete**

---

## Phase 3 — Workforce Analysis

The third phase converted the prepared employee dataset into structured workforce analysis.

The analysis examined:

- Workforce composition.
- Demographics.
- Department structure.
- Compensation.
- Performance.
- Workload.
- Career development.
- Employee experience.
- Resignation and retention.

The analysis focused on:

- Distributions.
- Comparisons.
- Relationships between variables.
- Workforce segments.
- Potential areas requiring management attention.

The general analytical structure followed was:

**Business Question → Metric Definition → Excel Calculation / PivotTable → Result → Interpretation → Business Implication**

### Analytical Grouping Fields

Additional analytical grouping fields were created where they improved the interpretation of numerical workforce measures:

- `Satisfaction_Group`
- `Work_Hours_Group`
- `Overtime_Group`

These fields were used to convert detailed numerical values into more meaningful business categories for comparison and interpretation.

### Satisfaction Grouping

`Satisfaction_Group` was created from:

`Employee_Satisfaction_Score`

The field grouped employee satisfaction into five standardised levels:

- 1
- 2
- 3
- 4
- 5

This supported comparisons between satisfaction levels and workforce outcomes such as resignation.

### Work Hours Grouping

`Work_Hours_Group` was created from:

`Work_Hours_Per_Week`

The field grouped weekly working hours into:

- 30-34 Hours
- 35-39 Hours
- 40-44 Hours
- 45-49 Hours
- 50-54 Hours
- 55-60 Hours

### Overtime Grouping

`Overtime_Group` was created from:

`Overtime_Hours`

The field grouped overtime into:

- Low Overtime
- Moderate Overtime
- High Overtime
- Very High Overtime
- Excessive Overtime

### Analytical Findings

The Phase 3 analysis identified the clearest segment-level pattern in the relationship between performance category and average monthly salary.

Other analysed measures generally showed limited variation across the workforce segments examined.

These included:

- Promotion rates across tenure groups, departments and performance categories.
- Average training hours across departments.
- Resignation rates across demographic, compensation, performance, promotion, satisfaction and workload segments.

The overall promotion rate was:

**66.70%**

The overall resignation rate was:

**10.01%**

The analysis found no major segment-level differences in resignation rates across the workforce characteristics examined.

The absence of material differences was treated as a valid analytical finding rather than being replaced with unsupported explanations.

### Analytical Interpretation

Phase 3 followed a descriptive and association-based analytical approach.

Observed patterns were interpreted as evidence of relationships or differences within the available dataset, but were not interpreted as proof of causation.

Where differences between workforce segments were small or not materially meaningful, this was documented as part of the analytical conclusion.

### Phase 3 Outcome

Phase 3 produced a structured workforce analysis and identified the most relevant findings for reporting.

The selected findings focused on:

- Workforce composition.
- Compensation by performance.
- Overall compensation benchmarks.
- Promotion rates.
- Resignation rates.
- The absence of material differences across several major workforce segments.

These findings provided the foundation for the executive reporting and dashboard stage.

**Status: Complete**

---

## Phase 4 — HR Reporting & Dashboard

Phase 4 translated the most important validated findings from Phase 3 into an executive-friendly Excel reporting layer and interactive dashboard.

### Reporting Objectives

The reporting stage focused on:

- Presenting headline workforce KPIs.
- Communicating workforce composition.
- Presenting compensation benchmarks.
- Showing compensation differences across performance categories.
- Presenting promotion indicators.
- Presenting resignation indicators.
- Allowing selected workforce segments to be explored interactively.

### Dashboard KPIs

The dashboard includes five primary KPI indicators:

- Total Employees
- Average Monthly Salary
- Median Monthly Salary
- Promotion Rate
- Resignation Rate

The KPI cards were connected to the underlying PivotTable calculations where dynamic filtering was supported.

The median monthly salary was retained as an overall workforce benchmark rather than being dynamically recalculated through the dashboard filtering mechanism.

### Dashboard Visualisation

The dashboard contains six primary charts covering:

- Workforce distribution by department.
- Workforce distribution by age group.
- Workforce distribution by gender.
- Average salary by performance category.
- Promotion rate by performance category.
- Resignation rate by department.

The charts were arranged into a two-row dashboard layout to provide a balanced presentation while maintaining readability.

### Dashboard Interactivity

Two slicers were incorporated into the dashboard.

The slicers allow users to filter the dashboard by selected workforce dimensions, including:

- Department
- Gender

The dashboard supports combined filtering, allowing users to examine specific workforce combinations.

The KPI indicators linked to the underlying PivotTable calculations respond dynamically to the selected filters.

### Dashboard Design

The dashboard design prioritised:

- Clear visual hierarchy.
- Consistent colour usage.
- Readable chart labels.
- Appropriate chart sizing.
- Minimal visual clutter.
- Consistent KPI formatting.
- Executive-friendly presentation.

The dashboard intentionally avoids displaying every analysis produced during Phase 3 and instead focuses on the most useful workforce indicators.

### Phase 4 Outcome

Phase 4 produced a completed interactive Excel dashboard that provides an executive-level reporting layer over the validated workforce analysis.

The dashboard allows users to:

- Review headline workforce KPIs.
- Explore workforce composition.
- Compare compensation across performance categories.
- Review promotion patterns.
- Examine resignation patterns.
- Filter workforce results by selected dimensions.

**Status: Complete**

---

## Phase 5 — Insights & Business Recommendations

The fifth phase will interpret the findings produced during the workforce analysis and reporting stages.

The analytical reasoning framework will be:

**Finding → Evidence → Business Meaning → Potential Implication → Recommendation**

Recommendations will:

- Be based on observed evidence.
- Reflect the limitations of the available dataset.
- Avoid unsupported causal claims.
- Distinguish between strong findings and areas requiring further investigation.
- Focus on practical HR relevance.

Where the analysis identifies no material differences between workforce segments, this conclusion will also be incorporated into the overall business interpretation where relevant.

**Status: Upcoming**

---

## Phase 6 — Finalisation & Portfolio Presentation

The final phase will prepare the project for completion and portfolio presentation.

Planned activities include:

- Final quality assurance.
- Documentation review.
- README refinement.
- Repository structure review.
- Changelog update.
- Final workbook review.
- Final project summary.
- Portfolio presentation.
- Project retrospective.

The final review will confirm that the workbook, documentation and repository accurately represent the completed analytical workflow.

**Status: Upcoming**

---

# Analytical Principles

## 1. Business First

Analysis should begin with a business question rather than a desire to create a particular chart or calculation.

---

## 2. Data Quality Before Analysis

The dataset should be validated and prepared before analytical conclusions are drawn.

---

## 3. Preserve the Raw Data

The original dataset should remain unchanged.

Cleaning and transformation should be performed in a separate working or analysis layer.

---

## 4. Purposeful Transformation

Derived fields should only be created when they provide clear analytical value.

Analytical grouping fields should simplify interpretation without unnecessarily distorting the underlying data.

---

## 5. Association Does Not Equal Causation

Observed relationships between employee characteristics should not automatically be interpreted as causal relationships.

The project analyses patterns and associations within the available synthetic dataset.

---

## 6. Business Relevance

The analysis should prioritise findings that could reasonably influence HR decision-making.

Not every numerical difference should automatically be treated as a meaningful business finding.

---

## 7. Meaningful Differences Matter

Analytical conclusions should consider whether observed differences are materially meaningful.

Where workforce segments show only small differences, the project should avoid overstating those differences.

The absence of a material difference is also a valid analytical finding when supported by the data.

---

## 8. Reproducibility

Important analytical decisions, transformations, metrics and derived fields should be documented so that the workflow can be understood and reproduced.

---

## 9. Progressive Documentation

Project documentation will be developed alongside the analysis.

Information will be added or updated as each phase is completed rather than documenting the entire project in advance.

This ensures that the repository accurately reflects the actual development of the project at each stage.

---

# Current Methodology Status

The project has completed:

- **Phase 1 — Project Setup & Analytical Framework**
- **Phase 2 — Data Preparation & Excel Data Model**
- **Phase 3 — Workforce Analysis**
- **Phase 4 — HR Reporting & Dashboard**

The dataset has been validated, transformed into an analysis-ready Excel data model, analysed across the major workforce perspectives and translated into an interactive Excel dashboard.

The project is now ready to proceed to:

**Phase 5 — Insights & Business Recommendations**