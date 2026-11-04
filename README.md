# Wellspring Member Engagement Analysis

Statistical analysis of member registration and attendance data for Wellspring, a cancer support organization, to assess the impact of a new registration system and examine how age and cancer type relate to attendance. Built in R with Quarto.

## Questions
1. Did first-month attendance differ before versus after the new registration system (March 4, 2024)?
2. Does age predict attendance rate?
3. Do the most and least prevalent cancer types have different attendance rates?

## Methods
- Two-sample proportion test (RQ1)
- Member-level linear regression (RQ2)
- Wilcoxon rank-sum test on pooled groups (RQ3, exploratory)

## Key findings
- **Registration system:** First-month attendance was 78% before and 57% after (difference about 20.5 points, 95% CI 17 to 24, p < 0.001). Records with no data rose from 13% to 39%, so the drop cannot be attributed to the system alone.
- **Age:** +0.13 percentage points per year (p = 0.002), but R² = 0.0037, so age explains very little.
- **Cancer type:** No statistically significant difference in the pooled comparison (Wilcoxon p = 0.303); the least prevalent groups have only 11 observations combined.

## Recommendation
Audit and improve the completeness of registration and attendance records before drawing causal conclusions or targeting outreach by age or diagnosis.

## Limitations
Month-level dates, missing and unequal follow-up, incomplete age records, small cancer subgroups, and an observational design.

## Data
The data is confidential and is not included in this repository. Running the code requires `Member_Background.csv` and `Service_Deliveries.csv`.

## Files
- `wellspring_analysis.qmd`: analysis and slide source
- `wellspring_presentation.pdf`: final presentation
