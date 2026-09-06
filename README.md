# What Drives Household Food Spending? A Regression Analysis

An individual applied regression project using real household expenditure
data.

## The business problem

Understanding what drives a household's weekly food spending is useful for
anyone trying to model or predict household budgets. This analysis looks
at household characteristics and spending patterns, and specifically asks
whether the relationship between alcohol spending and food spending
changes depending on how much debt a household carries. If it does, debt
level would be an important segmentation factor; if it doesn't, one model
can be used across debt levels without splitting the population up.

## What this project does

- Checks the data for missing values, duplicates, and unrealistic values
  before analysis
- Visualises the distribution of food, alcohol, and debt spending, and
  the relationships between them
- Fits a multivariate linear regression on food spending against household
  characteristics and other spending
- Adds an alcohol-by-debt interaction term to test directly whether debt
  changes the alcohol-food relationship
- Uses an ANOVA model comparison and estimated marginal means (emmeans) to
  interpret whether that interaction is meaningful

## Files

| File | Purpose |
|---|---|
| `household_food_spending.Rmd` | The full analysis |
| `household_food_spending.html` | The knitted report |
| `HouseholdExpenditure_csv.csv` | Weekly household expenditure data |

## How to run it

```r
install.packages(c("tidyverse", "emmeans", "gridExtra", "readr"))
```

Put all three files in the same folder, open
`household_food_spending.Rmd` in RStudio, and click Knit.

## Key result

Housing and alcohol spending are the strongest predictors of food
spending; higher spending in either is associated with higher food
spending, while higher debt is linked to slightly lower food spending. The
alcohol-by-debt interaction is not statistically significant, meaning the
alcohol-food relationship holds consistently across debt levels rather
than becoming stronger for higher-debt households. Household size, number
of children, sex, and income category show no significant effect once
spending patterns are accounted for.
