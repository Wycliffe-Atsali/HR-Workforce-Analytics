# Workforce Analysis

## Overview

This document records the findings from Phase 3 — Workforce Analysis of the HR Workforce Analytics project.

The analysis uses the prepared employee dataset containing **100,000 employees**.

The analytical grain remains:

> **One row = one employee**

The analysis focuses on the following areas:

- Workforce composition
- Compensation
- Performance
- Workload and productivity
- Career development
- Employee experience
- Retention

The analysis follows the general structure:

**Business Question → Metric / Analysis → Result → Interpretation**

The findings presented in this document describe observed patterns and associations within the dataset. They do not establish causal relationships unless supported by the available data.

---

# 1. Workforce Composition

## Business Question

What does the overall workforce look like, and how is it distributed across key demographic and organisational segments?

## Analysis

The workforce was examined by:

- Department
- Gender
- Age group
- Tenure group

## Results

The dataset contains **100,000 employees**.

The workforce is broadly distributed across the organisation's departments, with department populations remaining relatively similar and generally close to 11,000 employees.

Age groups are also broadly distributed across the workforce:

- 22-29: 20,492 employees
- 30-39: 25,465 employees
- 40-49: 25,710 employees
- 50+: 28,333 employees

The largest age group is employees aged **50+**.

Tenure distribution is:

- 0-2 Years: 30,373 employees
- 3-5 Years: 29,930 employees
- 6-10 Years: 39,697 employees

No employees were recorded in the 11+ Years category.

## Interpretation

The workforce does not appear to be heavily concentrated within a single department. The employee population is distributed across multiple demographic and organisational segments.

The 6-10 Years tenure group represents the largest tenure segment, while employees aged 50+ represent the largest age group.

These findings provide important context for interpreting the remaining workforce analysis.

---

# 2. Compensation Analysis

## Business Question

What does overall employee compensation look like, and how does compensation vary across performance categories?

## Overall Compensation

The monthly salary analysis produced the following results:

- Minimum Salary: 3,850
- Maximum Salary: 9,000
- Average Salary: 6,403.21
- Median Salary: 6,500

The average and median salaries are relatively close, providing a useful overall benchmark for the workforce.

## Compensation by Performance Category

Average monthly salary increases progressively across the performance categories:

- Very Low: approximately 5,422
- Low: approximately 5,900
- Moderate: approximately 6,410
- High: approximately 6,898
- Very High: approximately 7,398

## Interpretation

Compensation shows one of the clearest segment-level patterns observed during the workforce analysis.

Higher performance categories are associated with progressively higher average monthly salaries in the dataset.

This is an observed association and should not be interpreted as evidence that performance directly causes salary differences.

---

# 3. Performance Analysis

## Business Question

How are employees distributed across performance categories?

## Results

The workforce is distributed relatively evenly across the five performance categories:

- Very Low: 20,120 employees
- Low: 20,013 employees
- Moderate: 19,999 employees
- High: 19,940 employees
- Very High: 19,928 employees

Each category represents approximately one-fifth of the total workforce.

## Interpretation

The performance distribution is highly balanced across the five categories.

No individual performance category dominates the employee population.

The clearest additional pattern involving performance is the progressive increase in average salary across performance categories.

---

# 4. Workload and Productivity

## Business Question

How do workload and work arrangement indicators vary across the workforce?

## Analysis

The workload analysis examined indicators including:

- Weekly work hours
- Overtime hours
- Projects handled
- Remote work frequency
- Sick days

Additional grouping fields were created to support more meaningful analysis of workload measures:

- `Work_Hours_Group`
- `Overtime_Group`

## Results

The analysis did not identify a strong concentration of workforce outcomes around a single workload segment.

Overtime groups were also examined in relation to resignation.

The resignation rates across overtime categories were:

- Low Overtime: 9.99%
- Moderate Overtime: 9.85%
- High Overtime: 9.85%
- Very High Overtime: 10.05%
- Excessive Overtime: 10.18%

The overall resignation rate was 10.01%.

## Interpretation

The observed resignation rates across overtime groups remain relatively close to the overall workforce resignation rate.

Although the Excessive Overtime group has the highest observed rate, the differences between the overtime categories are relatively small.

The analysis therefore does not provide strong evidence of major variation in resignation rates across the overtime groups examined.

---

# 5. Career Development

## Business Question

How common are promotions within the workforce, and how do promotion rates vary across workforce segments?

## Overall Promotion Rate

Of the 100,000 employees:

- 66,704 employees had `Promotion_Flag = 1`
- Overall promotion rate: **66.70%**

## Promotion Rate by Tenure Group

Promotion rates were:

- 0-2 Years: 66.63%
- 3-5 Years: 66.96%
- 6-10 Years: 66.56%

## Promotion Rate by Performance Category

Promotion rates ranged from:

- High: 66.00%
- Low: 67.22%

The remaining performance categories also remained close to the overall promotion rate.

## Promotion Rate by Department

Promotion rates ranged from:

- HR: 66.24%
- Operations: 67.17%

The remaining departments also showed rates close to the overall promotion rate.

## Training Analysis

The overall average training hours were:

**49.51 hours**

Average training hours were also examined by department and promotion status.

The observed values remained highly consistent across the analysed groups.

## Interpretation

Promotion incidence is high across the workforce, with **66.70%** of employees having at least one recorded promotion.

Promotion rates show very limited variation across tenure groups, performance categories and departments.

Similarly, average training hours remain highly consistent across the groups examined.

No major segment-level differences were identified in the career development measures analysed.

---

# 6. Employee Experience

## Business Question

How does employee satisfaction vary across the workforce?

## Analysis

A `Satisfaction_Group` field was created to group employee satisfaction scores into five analytical levels.

The analysis examined satisfaction across relevant workforce segments.

## Results

The average satisfaction measures examined were generally clustered around approximately 3.0.

The analysis did not identify substantial variation in satisfaction across the major workforce segments reviewed.

Resignation rates by satisfaction group were:

- Satisfaction Group 1: 10.33%
- Satisfaction Group 2: 10.06%
- Satisfaction Group 3: 9.86%
- Satisfaction Group 4: 10.20%
- Satisfaction Group 5: 9.52%

The overall resignation rate was 10.01%.

## Interpretation

Employee satisfaction appears broadly consistent across the workforce segments analysed.

The resignation rates across satisfaction groups also show relatively limited variation.

While Satisfaction Group 1 has the highest observed resignation rate and Satisfaction Group 5 has the lowest, the overall differences remain modest.

The analysis does not support identifying a single satisfaction group as a major retention-risk segment based on the available data.

---

# 7. Retention Analysis

## Business Question

How common is employee resignation, and do resignation rates vary meaningfully across workforce segments?

## Overall Resignation Rate

Of the 100,000 employees:

- 10,010 employees had resigned
- 89,990 employees had not resigned
- Overall resignation rate: **10.01%**

## Resignation by Department

Departmental resignation rates ranged from:

- IT: 9.56%
- Finance: 10.54%

The remaining departments also remained close to the overall resignation rate.

## Resignation by Gender

Resignation rates were:

- Female: 10.03%
- Male: 10.01%
- Other: 9.75%

## Resignation by Age Group

Resignation rates ranged from:

- 22-29: 9.84%
- 40-49: 10.11%

The 50+ group also had a rate close to 10%.

## Resignation by Tenure Group

Resignation rates were:

- 0-2 Years: 9.95%
- 3-5 Years: 10.04%
- 6-10 Years: 10.04%

## Resignation by Salary Band

Resignation rates ranged from:

- Higher: 9.92%
- Lower: 10.14%

## Resignation by Performance Category

Resignation rates ranged from:

- Very High: 9.70%
- High: 10.19%

## Resignation by Promotion Status

Resignation rates were:

- No Promotion: 10.04%
- Promotion Recorded: 9.99%

## Resignation by Satisfaction Group

Resignation rates ranged from:

- Satisfaction Group 5: 9.52%
- Satisfaction Group 1: 10.33%

## Resignation by Overtime Group

Resignation rates ranged from:

- Moderate Overtime: 9.85%
- Excessive Overtime: 10.18%

## Interpretation

The overall resignation rate is **10.01%**.

Across the workforce segments analysed, resignation rates generally remain close to this overall rate.

Some segments show slightly higher or lower observed resignation rates, but the differences are relatively narrow.

The analysis therefore does not identify a single department, demographic group, compensation group, performance category, promotion group, satisfaction group or overtime group as having a substantially different resignation rate.

This finding should not be interpreted as evidence that these characteristics have no relationship with resignation. Rather, within the descriptive segment analysis performed in this project, no strong variation was observed.

---

# 8. Key Findings

The strongest findings from the Phase 3 workforce analysis are:

## 1. Compensation shows the clearest segment-level pattern

Average monthly salary increases progressively from lower to higher performance categories.

This represents the strongest observed differentiation across the major workforce segments analysed.

## 2. Promotion incidence is high and broadly consistent

The overall promotion rate is **66.70%**.

Promotion rates remain highly consistent across tenure groups, performance categories and departments.

## 3. The overall resignation rate is 10.01%

Employee resignation represents approximately one in ten employees in the workforce.

However, the descriptive analysis did not identify major differences in resignation rates across the segments examined.

## 4. The workforce is broadly distributed

The workforce is distributed across multiple departments, age groups and tenure groups without a single segment dominating the organisation.

## 5. Training and satisfaction measures show limited variation

Average training hours and satisfaction measures remain relatively consistent across the major segments analysed.

## 6. Many workforce outcomes are relatively uniform across segments

A major outcome of the analysis is that several workforce measures show limited variation across the groups examined.

This is a valid analytical finding and should not be overstated as a hidden problem where the data does not support one.

---

# 9. Phase 3 Conclusion

The Phase 3 analysis examined workforce composition, compensation, performance, workload, career development, employee experience and retention across a population of **100,000 employees**.

The strongest observed segment-level pattern is the progressive relationship between performance category and average monthly salary.

Promotion incidence is high across the workforce, while promotion rates, training measures, satisfaction measures and resignation rates generally show limited variation across the workforce segments analysed.

The overall resignation rate is **10.01%**, but no single segment examined showed a substantially different resignation rate within the descriptive analysis.

These findings provide the validated analytical foundation for:

- Phase 4 — HR Reporting & Dashboard
- Phase 5 — Insights & Business Recommendations

The next phases will focus on selecting the most important findings for communication and translating the validated results into clear business meaning and evidence-based recommendations.