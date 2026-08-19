# Project Methodology

## Overview

The HR Workforce Analytics project follows a structured six-phase analytical workflow designed to move from a defined business problem to evidence-based HR recommendations.

The methodology is intended to ensure that:

- Business questions are defined before analysis.
- Data quality is assessed before interpretation.
- Analytical decisions are documented.
- Findings are supported by evidence.
- Insights are translated into practical business recommendations.

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

The project will distinguish between observed associations and causal relationships throughout the analysis.

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

The validation results were:

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

The dataset is now considered analysis-ready.

The final analytical population is:

**100,000 employees**

The final analytical grain is:

> **One row = one employee**

The final analytical table is:

`tblEmployees`

**Status: Complete**

---

## Phase 3 — Workforce Analysis

The third phase will convert the prepared employee dataset into structured workforce analysis.

The analysis will examine areas such as:

- Workforce composition
- Demographics
- Department structure
- Compensation
- Performance
- Workload and productivity
- Training and development
- Promotions
- Employee satisfaction
- Resignation and retention

The analysis will focus on:

- Distributions
- Comparisons
- Relationships between variables
- Workforce segments
- Potential areas requiring management attention

The analysis will follow the general workflow:

**Business Question → Metric Definition → Excel Analysis → Result → Interpretation → Business Implication**

**Status: Upcoming**

---

## Phase 4 — HR Reporting & Dashboard

The fourth phase will translate the most important analytical findings into an executive-friendly reporting layer.

The reporting stage is expected to focus on:

- Workforce KPIs
- Workforce composition
- Compensation indicators
- Performance indicators
- Employee experience indicators
- Retention indicators
- Important workforce comparisons

The objective will be to create concise reporting that supports HR decision-making rather than simply presenting a large number of charts.

**Status: Upcoming**

---

## Phase 5 — Insights & Business Recommendations

The fifth phase will interpret the findings produced during the workforce analysis.

The analytical reasoning framework will be:

**Finding → Evidence → Business Meaning → Potential Implication → Recommendation**

Recommendations will be based on observed evidence and will avoid unsupported causal claims.

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

---

## 5. Association Does Not Equal Causation

Observed relationships between employee characteristics should not automatically be interpreted as causal relationships.

---

## 6. Business Relevance

The analysis should prioritise findings that could reasonably influence HR decision-making.

---

## 7. Reproducibility

Important analytical decisions and transformations should be documented so that the workflow can be understood and reproduced.

---

## 8. Progressive Documentation

Project documentation will be developed alongside the analysis.

Information will be added or updated as each phase is completed rather than documenting the entire project in advance.

This ensures that the repository accurately reflects the actual development of the project at each stage.

---

# Phase 2 Completion

Phase 2 established the analysis-ready Excel data model.

The original dataset was preserved, validated and transformed into the working table `tblEmployees` while maintaining the original population of **100,000 employees**.

The completed preparation process provides a validated foundation for the workforce analysis that will be conducted in Phase 3.