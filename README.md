# Seven Months HealthCare Analytics Dashboard | Excel

## Overview

This document provides an analysis of key hospital performance data across five departments over a six-month period.

Metrics reviewed include patient visits, readmission risk, treatment cost, length of stay, and recovery outcomes across multiple departments and demographics.

The analysis addresses the following objectives:

- Evaluating monthly patient visit trends by visit type (Emergency vs. Routine)
- Calculating average treatment cost and length of stay by department
- Analyzing readmission risk by gender and age group
- Measuring recovery scores across treatment (visit) types
- Identifying trends, consumer/patient patterns, and changes over time
- Delivering actionable recommendations to hospital stakeholders

The analysis was conducted using Microsoft Excel for data visualization.

The dataset used in this analysis can be downloaded at this [link](https://www.kaggle.com/datasets/abbas829/healthcare-patient-analytics-dataset).

## Table of Contents

- [Dataset](#dataset)
- [Analysis](#analysis)
- [Executive Summary](#executive-summary)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

## Dataset

This dataset covers hospital visit records over a six-month period (January–July), spanning five departments and four regions.

Key metrics include:

- **Total Hospital Visits**: The overall count of patient visits recorded across all departments during the period.
- **Readmission Risk**: A probability score estimating the likelihood of a patient being readmitted, broken down by gender and age group.
- **Treatment Cost**: The average cost incurred per department for patient treatment.
- **Length of Stay**: The average number of days a patient remains admitted.
- **Recovery Score**: A composite score reflecting patient recovery outcomes, tracked by visit/treatment type.
- **Emergency Visits**: The proportion of total visits classified as emergency rather than routine care.

The dataset also categorizes visits by **visit type** (Emergency, Routine), **treatment type** (Medication, Observation, Surgery, Therapy), **gender** (Female, Male), **age group** (18-30, 31-45, 46-60, 60+), **department** (Cardiology, General Medicine, Neurology, Orthopedics, Pediatrics), and **region** (East, North, South, West).

The dataset met a high standard of accuracy, and no further data cleaning was needed.


![](https://github.com/YasirQurashi/six-months-healthcare-analytics-dashboard/blob/main/dashbaord-preview.png)

## Analysis

I began by importing the hospital visit dataset and reviewing its structure and contents.

**Overall performance metrics** for the six-month period were as follows:

- Total Hospital Visits: 5,000
- Average Readmission Risk: 28%
- Average Treatment Cost: $54,915.47
- Average Length of Stay: 4.06 days
- Average Recovery Score: 74.7
- Emergency Visits: 31%

**Monthly visit volume** fluctuated moderately across the period, with May recording the highest total visits (744, combining 214 Emergency and 530 Routine) and January the lowest (744 total, with 237 Emergency and 507 Routine). Routine visits consistently outnumbered Emergency visits in every month, with Emergency visits ranging from roughly 27% to 32% of the monthly total — broadly consistent with the overall 31% Emergency share.

**Visits by department** were fairly evenly distributed, with Orthopedics leading at 1,058 visits, followed by Cardiology (995), General Medicine (991), Pediatrics (989), and Neurology (967). The narrow spread (under 100 visits between highest and lowest) suggests no single department is disproportionately driving hospital volume.

**Average treatment cost per department**, however, showed more separation. Neurology had the highest average cost at $55,761.75, closely followed by Cardiology ($55,632.60) and Orthopedics ($54,912.56). Pediatrics ($54,781.58) and General Medicine ($53,506.40) were the least costly on average. Despite Orthopedics having the highest visit volume, it did not carry the highest average cost — indicating cost is likely driven more by treatment complexity than by patient volume.

**Visit types** (Medication, Observation, Surgery, Therapy) were split evenly at 25% each, indicating a balanced treatment mix with no single treatment approach dominating hospital operations.

**Readmission risk by gender and age group** rose steadily with age. The 18-30 group recorded the lowest risk (0.275 for Female, 0.276 for Male), while the 60+ group recorded the highest (0.279 for Female, 0.294 for Male). Male patients aged 60+ carried the single highest readmission risk of any segment (0.294), suggesting age is the primary driver of readmission risk, with a secondary gender effect that widens in older age groups.

**Recovery scores by visit type** were closely clustered, ranging narrowly from 74.55 (Medication) to 74.81 (Observation and Therapy, tied). Surgery scored 74.70. The tight range (roughly 0.3 points) suggests recovery outcomes are broadly consistent regardless of treatment type.

## Executive Summary

- The hospital handled 5,000 total visits over the six-month period, with Routine visits (69%) consistently outnumbering Emergency visits (31%) month over month.
- Visit volume is well balanced across departments, but treatment cost is not: Neurology and Cardiology are the two most expensive departments on average, despite Orthopedics handling the most patients.
- Readmission risk increases with patient age across both genders, peaking among males aged 60+ (0.294) — nearly 7% higher than the youngest cohort.
- Recovery outcomes are stable across all four treatment types, with less than half a point separating the highest and lowest average recovery scores.
- The average length of stay (4.06 days) and average treatment cost ($54,915.47) provide useful baselines for future cost-control and capacity-planning initiatives.

## Recommendations

The recommendations are organized into three key areas: **Cost Management**, **Patient Risk**, and **Operational Efficiency**.

**Cost Management**

- Investigate the cost drivers behind Neurology and Cardiology treatment, since both carry the highest average costs despite mid-range visit volumes; this may point to higher-complexity cases or resource-intensive procedures.
- Benchmark General Medicine's lower average cost structure against other departments to identify transferable efficiencies.

**Patient Risk**

- Prioritize readmission-prevention programs for patients aged 60+, particularly males, given their elevated readmission risk relative to younger cohorts.
- Introduce closer post-discharge follow-up (e.g., scheduled check-ins or home care coordination) for high-risk age groups to reduce avoidable readmissions.

**Operational Efficiency**

- Since Routine visits make up the majority of volume, consider whether scheduling and staffing can be optimized around predictable Routine demand while keeping flexible capacity reserved for Emergency surges.
- Given the even 25/25/25/25 split across treatment types, ensure staffing and equipment allocation reflect this balance rather than assuming any one treatment type dominates resource needs.

In conclusion, a thorough analysis of the hospital's six-month performance data provided valuable insights into patient volume, cost, risk, and outcomes. Leveraging these insights and implementing the recommendations above can contribute to improved patient outcomes and operational efficiency.

## Limitations

Although the study provides useful insights, it is subject to a couple of limitations:

- The dataset covers only a six-month window, which limits the ability to assess seasonal or year-over-year trends.
- The dataset lacks patient-level clinical detail (e.g., specific diagnoses or comorbidities), which would allow for more precise readmission-risk and recovery-score modeling.
- A more focused root-cause analysis is needed to fully explain the cost disparities observed between departments.
