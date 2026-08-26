# Phase 4 — HR Reporting & Dashboard

## Overview

Phase 4 — HR Reporting & Dashboard translated the validated findings from Phase 3 — Workforce Analysis into an executive-friendly and interactive Excel reporting layer.

The objective of this phase was to communicate the most important workforce measures clearly while allowing users to explore selected workforce segments through interactive filtering.

The dashboard was developed using **Microsoft Excel 2016** and builds upon the PivotTables, analytical groupings and validated workforce metrics developed during the earlier phases.

The reporting workflow followed:

**Workforce Analysis → Dashboard Data Layer → KPI Reporting → Visualisation → Interactive Filtering → Final Dashboard**

---

# 1. Dashboard Objective

The dashboard was designed to provide HR stakeholders with a concise view of the organisation's workforce and selected workforce outcomes.

The dashboard focuses on:

- Workforce size
- Compensation
- Promotion
- Resignation
- Workforce composition
- Performance-related compensation patterns
- Department-level resignation patterns

The dashboard was intentionally designed to prioritise the most relevant workforce indicators rather than reproduce every analysis completed during Phase 3.

The objective was to create a reporting interface that is:

- Clear
- Interactive
- Business-oriented
- Easy to interpret
- Visually consistent
- Suitable for executive-level reporting

---

# 2. Dashboard Data Layer

A dedicated worksheet named:

`Dashboard_Data`

was created to provide supporting data for the dashboard components.

The dashboard data layer contains the supporting summaries required for the KPI cards and visualisations.

These include:

- Total employee count
- Department employee counts
- Age-group employee counts
- Gender employee counts
- Average salary by performance category
- Promotion rates by performance category
- Resignation rates by department

The dashboard data layer separates the reporting calculations from the visual presentation layer.

This structure improves the organisation of the workbook and makes the dashboard easier to maintain.

---

# 3. KPI Cards

The dashboard contains five primary workforce KPIs.

## Total Employees

Measures the total number of employees represented in the analytical population.

**Overall value:**

**100,000 employees**

---

## Average Monthly Salary

Measures the average monthly salary across the selected workforce population.

**Overall value:**

**6,403.21**

---

## Median Monthly Salary

Measures the middle monthly salary value within the workforce population.

**Overall value:**

**6,500**

The median provides a complementary measure to the average salary and helps provide a more representative view of the central salary level.

---

## Promotion Rate

Measures the proportion of employees with a recorded promotion.

**Overall value:**

**66.70%**

---

## Resignation Rate

Measures the proportion of employees with a recorded resignation.

**Overall value:**

**10.01%**

---

# 4. Interactive KPI Reporting

The KPI cards were connected to the dashboard's interactive filtering structure.

The dashboard supports filtering by:

- Department
- Gender

When a user selects a department, gender, or combination of both, the connected KPI indicators update to reflect the selected workforce population.

This allows users to move beyond organisation-wide metrics and examine workforce measures for specific segments.

---

# 5. Dashboard Visualisations

The dashboard includes six primary visualisations.

## 5.1 Workforce by Department

**Chart type:** Column Chart

This visualisation shows the number of employees within each department.

It provides a high-level view of organisational workforce distribution.

---

## 5.2 Workforce by Age Group

**Chart type:** Column Chart

This visualisation shows the distribution of employees across the defined age groups:

- 22-29
- 30-39
- 40-49
- 50+

It provides an overview of the workforce age structure.

---

## 5.3 Workforce by Gender

**Chart type:** Doughnut Chart

This visualisation shows the gender composition of the workforce.

It provides a compact view of the relative representation of the available gender categories.

---

## 5.4 Average Salary by Performance Category

**Chart type:** Column Chart

This visualisation compares average monthly salary across the five performance categories:

- Very Low
- Low
- Moderate
- High
- Very High

The visual communicates one of the clearest segment-level patterns identified during Phase 3: average monthly salary increases progressively across performance categories.

This relationship is presented as an observed association rather than a causal relationship.

---

## 5.5 Promotion Rate by Performance Category

**Chart type:** Column Chart

This visualisation compares promotion rates across performance categories.

The rates remain relatively close to the overall promotion rate of 66.70%.

The chart therefore provides a visual representation of the limited variation identified during the workforce analysis.

---

## 5.6 Resignation Rate by Department

**Chart type:** Column Chart

This visualisation compares resignation rates across departments.

Department-level resignation rates remain relatively close to the overall workforce resignation rate of 10.01%.

The chart provides a concise view of departmental retention patterns without implying that departmental differences are necessarily causal.

---

# 6. Interactive Slicers

Two Excel slicers were incorporated into the dashboard.

## Department Slicer

The Department slicer allows users to filter the dashboard by department.

Available departments include:

- Customer Support
- Engineering
- Finance
- HR
- IT
- Legal
- Marketing
- Operations
- Sales

The slicer supports multi-selection, allowing users to compare or examine multiple departments simultaneously.

---

## Gender Slicer

The Gender slicer allows users to filter the dashboard by gender category.

The available categories are:

- Female
- Male
- Other

The slicer also supports multi-selection.

---

# 7. Dashboard Interactivity

The combination of KPI cards, PivotTable-based reporting and slicers allows the dashboard to function as an interactive workforce exploration tool.

Users can:

- View the overall workforce.
- Filter by department.
- Filter by gender.
- Select multiple departments.
- Select multiple gender categories.
- Examine how KPI values change according to the selected population.

This provides greater analytical flexibility than a static collection of charts.

---

# 8. Median Salary KPI Consideration

The dashboard includes Median Monthly Salary as an important descriptive KPI.

During dashboard development, an attempt was made to determine whether the median salary could be incorporated into the PivotTable-based interactive filtering workflow using Excel Power Pivot.

This approach was investigated because standard Excel 2016 PivotTables do not provide Median as a standard value aggregation in the same way as measures such as Sum, Count and Average.

The Power Pivot approach was ultimately not used for the final dashboard implementation.

The median salary KPI was therefore maintained as a separately calculated metric rather than introducing additional model complexity solely for the purpose of calculating a dynamic median.

The overall workforce median monthly salary is:

**6,500**

This approach allowed the dashboard to retain the median as an important descriptive statistic while keeping the final Excel model relatively simple and maintainable.

---

# 9. Dashboard Visual Design

The dashboard was designed using a consistent visual hierarchy intended to improve readability and reduce visual clutter.

The design focused on:

- Clear KPI hierarchy
- Consistent chart formatting
- Business-friendly labels
- Appropriate chart selection
- Consistent typography
- Restrained colour usage
- Clear spacing between dashboard components
- Compact layout
- Executive readability

The dashboard components were arranged within a single reporting view so that the principal workforce indicators and visualisations could be reviewed without navigating between multiple worksheets.

---

# 10. Dashboard Reporting Principles

The dashboard follows several reporting principles established during the project.

### Business Relevance

Only selected workforce measures were included in the dashboard.

The dashboard was not intended to display every analytical calculation completed during Phase 3.

### Clarity

Charts and KPI cards were designed to communicate the underlying measure without unnecessary complexity.

### Consistency

Formatting, labels and visual hierarchy were kept consistent across dashboard components.

### Interactivity

Slicers were used to allow users to explore selected workforce segments.

### Analytical Accuracy

Dashboard values were based on the validated analytical population and supporting PivotTable or calculation outputs.

### Responsible Interpretation

The dashboard presents observed workforce patterns and associations.

The visualisations should not be interpreted as establishing causal relationships.

---

# 11. Dashboard Output

The completed dashboard provides an interactive summary of the HR workforce dataset.

At the overall workforce level, the dashboard communicates:

- **100,000 employees**
- **6,403.21 average monthly salary**
- **6,500 median monthly salary**
- **66.70% promotion rate**
- **10.01% resignation rate**

The dashboard also allows users to explore workforce composition, compensation, promotion and resignation patterns through interactive filtering.

A static PDF version of the completed dashboard is also included in the project repository for portfolio presentation.

---

# 12. Phase 4 Outcome

Phase 4 successfully transformed the Phase 3 workforce analysis into an executive-friendly and interactive reporting layer.

The completed dashboard provides:

- Workforce KPIs
- Workforce composition visualisations
- Compensation analysis
- Promotion analysis
- Resignation analysis
- Department filtering
- Gender filtering
- Multi-selection capability
- Dynamically filtered KPI reporting
- A presentation-ready dashboard layout

The dashboard represents the reporting layer of the HR Workforce Analytics project and provides the foundation for interpreting the analytical findings in the next phase.

**Status: Complete**

---

# Phase 4 Conclusion

Phase 4 completed the transition from workforce analysis to workforce reporting.

The dashboard provides a concise and interactive representation of the validated findings produced during Phase 3 while maintaining the project's principles of business relevance, analytical accuracy and responsible interpretation.
