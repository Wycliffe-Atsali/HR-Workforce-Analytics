# CHANGELOG

All significant project milestones and structural changes are documented in this file.

---

## [1.0.0] - Final Project Complete

### Finalisation

* Completed Phase 6 — Finalisation & Portfolio Presentation.
* Completed the final review of the Excel workbook and project deliverables.
* Confirmed completion of all six phases of the analytical workflow.
* Completed the final repository structure review.
* Completed the final portfolio presentation review.
* Completed the final documentation alignment and quality review.
* Confirmed that the project is ready for portfolio presentation.

### Deliverables

The final project includes:

* The completed Excel workforce analytics workbook.
* The interactive HR reporting dashboard.
* A PDF snapshot of the completed dashboard.
* Business scenario documentation.
* Project objectives and business questions.
* Data dictionary and analytical field documentation.
* Project methodology documentation.
* Workforce analysis documentation.
* Dashboard documentation.
* Insights and business recommendations.
* Final project documentation and changelog.

### Documentation

Updated:

* `README.md`
* `documentation/methodology.md`
* `documentation/data_dictionary.md`
* `CHANGELOG.md`

The final documentation now records the completion of all six project phases.

### Final Project Outcome

The HR Workforce Analytics project is now complete.

The project demonstrates an end-to-end Excel-based analytical workflow:

**Business Problem → Data Preparation → Workforce Analysis → Reporting → Recommendations → Finalisation**

The completed project includes data validation, analytical transformations, workforce analysis, interactive dashboard reporting, evidence-based recommendations and portfolio-ready documentation.

---

## [0.6.0] - Phase 5 Complete

### Added

* Completed the Insights & Business Recommendations phase.
* Interpreted the validated findings from the workforce analysis in business terms.
* Developed evidence-based HR recommendations.
* Added recommendations based on compensation and performance findings.
* Added recommendations relating to career development and promotion monitoring.
* Added recommendations for organisation-wide retention monitoring.
* Added recommendations for further investigation of employee resignation drivers.
* Added recommendations relating to employee experience and workload analysis.
* Added recommendations for ongoing dashboard-based workforce monitoring.
* Documented the importance of not targeting workforce segments without sufficient evidence of meaningful variation.
* Added `documentation/insights_recommendations.md`.

### Key Business Insights

* The clearest observed segment-level pattern remains the progressive increase in average monthly salary across performance categories.
* Promotion incidence is high at 66.70% and remains broadly consistent across the workforce segments examined.
* The overall resignation rate is 10.01%, with no single segment showing substantially different resignation levels within the descriptive analysis.
* Satisfaction and overtime groups did not identify a major retention-risk segment.
* Several workforce outcomes showed limited variation across the groups examined.
* The absence of material differences was treated as a valid analytical finding.

### Recommendations

The Phase 5 recommendations focus on:

* Monitoring compensation progression across performance levels.
* Expanding promotion analysis beyond promotion incidence alone.
* Maintaining broad organisation-wide retention monitoring.
* Collecting or analysing additional variables to investigate resignation drivers.
* Avoiding unsupported assumptions about satisfaction or workload as single causes of resignation.
* Using the completed dashboard for ongoing workforce monitoring.
* Applying targeted interventions only when future evidence identifies meaningful differences.

### Documentation

Updated:

* `README.md`
* `documentation/methodology.md`
* `documentation/data_dictionary.md`

Added:

* `documentation/insights_recommendations.md`

### Phase 5 Outcome

The project now contains a complete evidence-based interpretation layer connecting the workforce analysis and dashboard findings to practical HR recommendations.

The recommendations are based on observed patterns within the available synthetic dataset and do not present associations as causal relationships.

### Next Phase

The project was ready to proceed to:

**Phase 6 — Finalisation & Portfolio Presentation**

---

## [0.5.0] - Phase 4 Complete

### Added

* Completed the HR Reporting & Dashboard phase.
* Created the final Excel workforce dashboard.
* Added executive-level KPI cards.
* Added interactive dashboard filtering using Excel slicers.
* Connected KPI indicators to the underlying PivotTable analysis.
* Added workforce composition visualisations.
* Added compensation and performance visualisation.
* Added promotion analysis visualisation.
* Added resignation analysis visualisation.
* Applied consistent dashboard formatting and visual design.
* Organised dashboard charts into a structured two-row layout.
* Added dashboard-level visual hierarchy and presentation formatting.

### Dashboard KPIs

The completed dashboard includes:

* Total Employees
* Average Monthly Salary
* Median Monthly Salary
* Promotion Rate
* Resignation Rate

The interactive KPI indicators respond to selected dashboard filters where supported by the underlying PivotTable calculations.

The median monthly salary is retained as an overall workforce benchmark rather than being dynamically recalculated through the dashboard filters.

### Dashboard Interactivity

Two slicers were implemented to provide interactive filtering across the dashboard.

The slicers allow users to analyse combinations of workforce segments, including department and gender.

The dashboard therefore provides a more interactive management view than a static reporting page.

### Dashboard Visualisation

The dashboard includes six primary analytical charts covering:

* Department workforce distribution
* Age group distribution
* Gender distribution
* Average salary by performance category
* Promotion rate by performance category
* Resignation rate by department

### Documentation

Updated:

* `README.md`
* `documentation/methodology.md`
* `documentation/workforce_analysis.md`
* `documentation/data_dictionary.md`

The project documentation now records the completion of Phase 4 and the transition to Phase 5.

### Phase 4 Outcome

The project now contains a completed analytical dashboard that translates the detailed Phase 3 workforce analysis into an interactive executive reporting layer.

### Next Phase

The project was ready to proceed to:

**Phase 5 — Insights & Business Recommendations**

---

## [0.4.0] - Phase 3 Complete

### Added

* Completed the detailed workforce analysis.
* Analysed workforce composition and organisational distribution.
* Analysed demographic and tenure patterns.
* Analysed overall compensation and compensation by performance category.
* Analysed performance category distribution.
* Analysed workload and work arrangement indicators.
* Analysed promotion rates and career development patterns.
* Analysed training patterns.
* Analysed employee satisfaction.
* Analysed employee resignation and retention patterns.
* Added analytical grouping fields for satisfaction, work hours and overtime.
* Added the Phase 3 workforce analysis documentation.

### Key Findings

* Identified a progressive association between performance category and average monthly salary.
* Confirmed an overall promotion rate of 66.70%.
* Confirmed an overall resignation rate of 10.01%.
* Found promotion rates to be broadly consistent across departments, tenure groups and performance categories.
* Found limited variation in training and satisfaction measures across the major segments analysed.
* Found no major segment-level variation in resignation rates across the groups examined.
* Confirmed that the workforce is broadly distributed across key organisational and demographic segments.

### Documentation

* Added `documentation/workforce_analysis.md`.
* Updated the data dictionary with Phase 3 analytical grouping fields.
* Updated the project methodology to record Phase 3 completion.
* Updated the README with the completed Phase 3 status and analysis summary.

### Next Phase

Phase 4 would translate the strongest validated findings into an executive-friendly HR reporting layer and dashboard.

---

## [0.3.0] - Phase 2 Complete

### Data Preparation

Phase 2 — Data Preparation & Excel Data Model was completed.

The following data preparation activities were completed:

* Preserved the original `Raw_Data` worksheet.
* Created the `Clean_Data` working sheet.
* Converted the working dataset into the Excel Table `tblEmployees`.
* Validated Employee IDs.
* Checked for duplicate Employee IDs.
* Checked for missing values.
* Checked categorical consistency.
* Validated numerical fields.
* Validated dates.
* Checked formatting and text consistency.
* Performed final data-quality checks.

### Derived Analytical Fields

Created and validated:

* `Duplicate_ID_Check`
* `Age_Group`
* `Tenure_Group`
* `Salary_Band`
* `Performance_Category`
* `Promotion_Flag`
* `Resignation_Flag`

### Validation

The final analytical population remained:

**100,000 employees**

Three final quality-assurance checks reconciled to 100,000, confirming that:

* The employee population remained unchanged.
* The resignation flag reconciled to the full population.
* The promotion flag reconciled to the full population.

The `11+ Years` tenure category contained zero employees, reflecting the distribution of the dataset rather than a formula error.

### Salary Validation

Validated salary statistics:

* Minimum salary: 3,850
* Maximum salary: 9,000
* Average salary: 6,403.211
* Median salary: 6,500

### Documentation

Updated:

* `README.md`
* `documentation/data_dictionary.md`
* `documentation/methodology.md`
* `CHANGELOG.md`

The completed Phase 2 Excel workbook was also prepared for inclusion in the repository.

### Next Phase

The project was ready to proceed to:

**Phase 3 — Workforce Analysis**

---

## [0.2.0] - Phase 1 Complete

### Completed

Phase 1 — Project Setup & Analytical Framework was completed.

The project foundation and analytical framework were formally established, including:

* Defined the business scenario.
* Defined the business problem.
* Established the primary project objective.
* Established supporting project objectives.
* Identified key stakeholders.
* Established analytical scope.
* Defined the major workforce analytical perspectives.
* Established the key business questions.
* Defined project success criteria.
* Established the six-phase project methodology.
* Established the analytical principles that will guide the project.

### Analytical Framework

The workforce analysis will be examined through the following perspectives:

* Workforce Composition
* Compensation
* Performance
* Productivity & Workload
* Career Development
* Employee Experience
* Retention

### Stakeholders

The primary stakeholder groups identified are:

* HR Leadership
* HR Business Partners
* Department Managers
* Senior Management

### Documentation

Updated project documentation to reflect completion of Phase 1:

* Business scenario
* Project objectives
* Data dictionary
* Project methodology
* README
* CHANGELOG

### Next Phase

The project was ready to proceed to:

**Phase 2 — Data Preparation & Excel Data Model**

---

## [0.1.0] - Initial Project Setup

### Added

* Created the HR Workforce Analytics project.
* Added the HR workforce dataset.
* Created the initial Excel analysis workbook.
* Established the initial project documentation.
* Created the project README.
* Created the project CHANGELOG.
* Established the initial GitHub repository structure.
* Defined the six-phase project methodology.

### Documentation

* Added the business scenario.
* Added the project objectives.
* Added the initial data dictionary.
* Added the project methodology.
