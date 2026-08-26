# Workforce Analysis

## Overview

This document records the findings from Phase 3 — Workforce Analysis of the HR Workforce Analytics project.

The analysis uses the prepared employee dataset containing **100,000 employees**.

The analytical grain remains:

> **One row = one employee**

The analysis focuses on:

- Workforce composition
- Compensation
- Performance
- Workload and productivity
- Career development
- Employee experience
- Retention

The analysis follows the general structure:

**Business Question → Metric / Analysis → Result → Interpretation**

The findings describe observed patterns and associations within the dataset. They do not establish causal relationships unless supported by the available data.

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

Department populations remain relatively similar, with each department containing approximately 11,000 employees.

Age groups are:

- 22-29: 20,492
- 30-39: 25,465
- 40-49: 25,710
- 50+: 28,333

The largest age group is **50+**.

Tenure distribution is:

- 0-2 Years: 30,373
- 3-5 Years: 29,930
- 6-10 Years: 39,697
- 11+ Years: 0

The largest tenure group is **6-10 Years**.

## Interpretation

The workforce does not appear to be heavily concentrated within a single department.

The employee population is also distributed across multiple demographic and organisational segments.

The 6-10 Years tenure group and 50+ age group represent the largest segments within their respective dimensions.

---

# 2. Compensation Analysis

## Business Question

What does overall employee compensation look like, and how does compensation vary across performance categories?

## Overall Compensation

| Metric | Result |
|---|---:|
| Minimum Salary | 3,850 |
| Maximum Salary | 9,000 |
| Average Salary | 6,403.21 |
| Median Salary | 6,500 |

The average and median salaries are relatively close, providing a useful overall benchmark.

## Compensation by Performance Category

| Performance Category | Average Monthly Salary |
|---|---:|
| Very Low | 5,422.23 |
| Low | 5,900.28 |
| Moderate | 6,409.52 |
| High | 6,897.63 |
| Very High | 7,397.67 |

## Interpretation

Compensation shows one of the clearest segment-level patterns observed during the workforce analysis.

Average monthly salary increases progressively across the performance categories.

This is an observed association and should not be interpreted as evidence that performance directly causes salary differences.

---

# 3. Performance Analysis

## Business Question

How are employees distributed across performance categories?

## Results

| Performance Category | Employees |
|---|---:|
| Very Low | 20,120 |
| Low | 20,013 |
| Moderate | 19,999 |
| High | 19,940 |
| Very High | 19,928 |
| **Total** | **100,000** |

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

The workload analysis examined:

- Weekly work hours
- Overtime hours
- Projects handled
- Remote work frequency
- Sick days

Additional grouping fields were created:

- `Work_Hours_Group`
- `Overtime_Group`

## Overtime and Resignation

| Overtime Group | Resignation Rate |
|---|---:|
| Low Overtime | 9.99% |
| Moderate Overtime | 9.85% |
| High Overtime | 9.85% |
| Very High Overtime | 10.05% |
| Excessive Overtime | 10.18% |
| **Overall** | **10.01%** |

## Interpretation

Resignation rates across overtime groups remain relatively close to the overall workforce resignation rate.

Although the Excessive Overtime group has the highest observed rate, the differences are relatively small.

The analysis therefore does not provide strong evidence of major variation in resignation rates across overtime categories.

---

# 5. Career Development

## Business Question

How common are promotions within the workforce, and how do promotion rates vary across workforce segments?

## Overall Promotion Rate

Of the 100,000 employees:

- 66,704 employees had `Promotion_Flag = 1`
- Overall promotion rate: **66.70%**

## Promotion Rate by Tenure

| Tenure Group | Promotion Rate |
|---|---:|
| 0-2 Years | 66.63% |
| 3-5 Years | 66.96% |
| 6-10 Years | 66.56% |
| **Overall** | **66.70%** |

## Promotion Rate by Performance

Promotion rates remained close to the overall rate.

Observed rates included:

- High: 66.00%
- Low: 67.22%

## Promotion Rate by Department

Observed departmental rates included:

- HR: 66.24%
- Operations: 67.17%

The remaining departments also remained close to the overall promotion rate.

## Training Analysis

The overall average training hours were:

**49.51 hours**

Average training hours remained highly consistent across the analysed departments and promotion groups.

## Interpretation

Promotion incidence is high across the workforce.

Promotion rates show very limited variation across tenure groups, performance categories and departments.

Similarly, training hours remain relatively consistent across the groups examined.

No major segment-level differences were identified in the career development measures analysed.

---

# 6. Employee Experience

## Business Question

How does employee satisfaction vary across the workforce?

## Analysis

A `Satisfaction_Group` field was created to group employee satisfaction scores into five analytical levels.

## Resignation by Satisfaction Group

| Satisfaction Group | Resignation Rate |
|---|---:|
| 1 | 10.33% |
| 2 | 10.06% |
| 3 | 9.86% |
| 4 | 10.20% |
| 5 | 9.52% |
| **Overall** | **10.01%** |

## Interpretation

Employee satisfaction measures appear broadly consistent across the workforce segments analysed.

The resignation rates across satisfaction groups also show relatively limited variation.

While Satisfaction Group 1 has the highest observed resignation rate and Satisfaction Group 5 has the lowest, the differences remain modest.

The analysis does not support identifying a single satisfaction group as a major retention-risk segment.

---

# 7. Retention Analysis

## Business Question

How common is employee resignation, and do resignation rates vary meaningfully across workforce segments?

## Overall Resignation Rate

Of the 100,000 employees:

- 10,010 employees had resigned.
- 89,990 employees had not resigned.
- Overall resignation rate: **10.01%**

## Resignation by Department

Departmental resignation rates ranged from:

- IT: 9.56%
- Finance: 10.54%

The remaining departments also remained close to the overall rate.

## Resignation by Gender

| Gender | Resignation Rate |
|---|---:|
| Female | 10.03% |
| Male | 10.01% |
| Other | 9.75% |

## Resignation by Age Group

Observed rates ranged from:

- 22-29: 9.84%
- 40-49: 10.11%

The remaining age groups also remained close to 10%.

## Resignation by Tenure

| Tenure Group | Resignation Rate |
|---|---:|
| 0-2 Years | 9.95% |
| 3-5 Years | 10.04% |
| 6-10 Years | 10.04% |

## Resignation by Salary Band

Observed rates ranged from:

- Higher: 9.92%
- Lower: 10.14%

## Resignation by Performance

Observed rates ranged from:

- Very High: 9.70%
- High: 10.19%

## Resignation by Promotion Status

| Promotion Status | Resignation Rate |
|---|---:|
| No Promotion | 10.04% |
| Promotion Recorded | 9.99% |
| **Overall** | **10.01%** |

## Resignation by Satisfaction

Observed rates ranged from:

- Satisfaction Group 5: 9.52%
- Satisfaction Group 1: 10.33%

## Resignation by Overtime

Observed rates ranged from:

- Moderate Overtime: 9.85%
- Excessive Overtime: 10.18%

## Interpretation

The overall resignation rate is **10.01%**.

Across the workforce segments analysed, resignation rates generally remain close to this overall rate.

Some segments show slightly higher or lower observed rates, but the differences are relatively narrow.

The analysis therefore does not identify a single department, demographic group, compensation group, performance category, promotion group, satisfaction group or overtime group as having a substantially different resignation rate.

This should not be interpreted as evidence that these characteristics have no relationship with resignation.

Rather, within the descriptive segment analysis performed in this project, no strong variation was observed.

---

# 8. Key Findings

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

These findings were subsequently translated into the Phase 4 interactive HR reporting dashboard.

The Phase 3 findings now provide the analytical foundation for:

- Phase 5 — Insights & Business Recommendations
- Phase 6 — Finalisation & Portfolio Presentation

The next stage will focus on interpreting the validated findings in business terms and developing evidence-based recommendations.