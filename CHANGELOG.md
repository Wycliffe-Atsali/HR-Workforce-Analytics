# Changelog

All significant project milestones and structural changes are documented in this file.

---

## [0.4.0] - Phase 3 Complete

### Added

- Completed the detailed workforce analysis.
- Analysed workforce composition and organisational distribution.
- Analysed demographic and tenure patterns.
- Analysed overall compensation and compensation by performance category.
- Analysed performance category distribution.
- Analysed workload and work arrangement indicators.
- Analysed promotion rates and career development patterns.
- Analysed training patterns.
- Analysed employee satisfaction.
- Analysed employee resignation and retention patterns.
- Added analytical grouping fields for satisfaction, work hours and overtime.
- Added the Phase 3 workforce analysis documentation.

### Key Findings

- Identified a progressive association between performance category and average monthly salary.
- Confirmed an overall promotion rate of 66.70%.
- Confirmed an overall resignation rate of 10.01%.
- Found promotion rates to be broadly consistent across departments, tenure groups and performance categories.
- Found limited variation in training and satisfaction measures across the major segments analysed.
- Found no major segment-level variation in resignation rates across the groups examined.
- Confirmed that the workforce is broadly distributed across key organisational and demographic segments.

### Documentation

- Added `documentation/workforce_analysis.md`.
- Updated the data dictionary with Phase 3 analytical grouping fields.
- Updated the project methodology to record Phase 3 completion.
- Updated the README with the completed Phase 3 status and analysis summary.

### Next Phase

Phase 4 will translate the strongest validated findings into an executive-friendly HR reporting layer and dashboard.

---

## [0.3.0] - Phase 2 Complete

### Data Preparation

Phase 2 — Data Preparation & Excel Data Model was completed.

The following data preparation activities were completed:

- Preserved the original `Raw_Data` worksheet.
- Created the `Clean_Data` working sheet.
- Converted the working dataset into the Excel Table `tblEmployees`.
- Validated Employee IDs.
- Checked for duplicate Employee IDs.
- Checked for missing values.
- Checked categorical consistency.
- Validated numerical fields.
- Validated dates.
- Checked formatting and text consistency.
- Performed final data-quality checks.

### Derived Analytical Fields

Created and validated:

- `Duplicate_ID_Check`
- `Age_Group`
- `Tenure_Group`
- `Salary_Band`
- `Performance_Category`
- `Promotion_Flag`
- `Resignation_Flag`

### Validation

The final analytical population remained:

**100,000 employees**

Three final quality-assurance checks reconciled to 100,000, confirming that:

- The employee population remained unchanged.
- The resignation flag reconciled to the full population.
- The promotion flag reconciled to the full population.

The `11+ Years` tenure category contained zero employees, reflecting the distribution of the dataset rather than a formula error.

### Salary Validation

Validated salary statistics:

- Minimum salary: 3,850
- Maximum salary: 9,000
- Average salary: 6,403.211
- Median salary: 6,500

### Documentation

Updated:

- `README.md`
- `documentation/data_dictionary.md`
- `documentation/methodology.md`
- `CHANGELOG.md`

The completed Phase 2 Excel workbook was also prepared for inclusion in the repository.

### Next Phase

The project is now ready to proceed to:

**Phase 3 — Workforce Analysis**

---

## [0.2.0] - Phase 1 Complete

### Completed

Phase 1 — Project Setup & Analytical Framework was completed.

The project foundation and analytical framework were formally established, including:

- Defined the business scenario.
- Defined the business problem.
- Established the primary project objective.
- Established supporting project objectives.
- Identified key stakeholders.
- Established analytical scope.
- Defined the major workforce analytical perspectives.
- Established the key business questions.
- Defined project success criteria.
- Established the six-phase project methodology.
- Established the analytical principles that will guide the project.

### Analytical Framework

The workforce analysis will be examined through the following perspectives:

- Workforce Composition
- Compensation
- Performance
- Productivity & Workload
- Career Development
- Employee Experience
- Retention

### Stakeholders

The primary stakeholder groups identified are:

- HR Leadership
- HR Business Partners
- Department Managers
- Senior Management

### Documentation

Updated project documentation to reflect completion of Phase 1:

- Business scenario
- Project objectives
- Data dictionary
- Project methodology
- README
- CHANGELOG

### Next Phase

The project is now ready to proceed to:

**Phase 2 — Data Preparation & Excel Data Model**

---

## [0.1.0] - Initial Project Setup

### Added

- Created the HR Workforce Analytics project.
- Added the HR workforce dataset.
- Created the initial Excel analysis workbook.
- Established the initial project documentation.
- Created the project README.
- Created the project CHANGELOG.
- Established the initial GitHub repository structure.
- Defined the six-phase project methodology.

### Documentation

- Added the business scenario.
- Added the project objectives.
- Added the initial data dictionary.
- Added the project methodology.

---

## Upcoming

### Phase 3

Conduct the detailed workforce analysis.

### Phase 4

Develop the HR reporting layer and dashboard.

### Phase 5

Translate analytical findings into HR insights and business recommendations.

### Phase 6

Complete the final project review and portfolio presentation.