# Age-Based Memory Retention Analysis

## Project Overview

This project uses nonparametric statistical methods in R to investigate whether word recall among 18-year-old males exceeds a reference median reported for 65-year-old males.

**Research question:** Is the population median number of recalled words for 18-year-old males greater than the reference median of 4 words for 65-year-old males?

## Technologies and Methods

- **Language:** R
- **Package:** BSDA
- **Methods:** One-sample sign test, descriptive statistics, 95% confidence intervals
- **Visualizations:** Histograms and boxplots (base R)

## Data

The analysis uses 10 word-recall observations for 18-year-old males:

```r
words <- c(15, 7, 12, 14, 11, 10, 4, 13, 9, 2)
```

The reference median for 65-year-old males is **4 words**. The original analysis provides this benchmark, not individual observations from the older group.

| Statistic | Value |
|---|---:|
| Sample size | 10 |
| Mean | 9.70 |
| Median | 10.50 |
| Standard deviation | 4.27 |
| Minimum | 2 |
| Maximum | 15 |
| Older-group reference median | 4 |

## Analysis

### Exploratory Data Analysis

Calculated the mean, median, standard deviation, and summary statistics for word recall. Created a histogram and boxplot with reference lines at 4 words to compare the observed scores with the older-group benchmark.

### Hypothesis Test

A **one-sample sign test** was used to test whether the median recall score exceeded 4 words without assuming normally distributed data.

- **Null hypothesis (H₀):** Population median word recall is 4 words.
- **Alternative hypothesis (H₁):** Population median word recall is greater than 4 words.
- **Significance level:** α = 0.05
- **One-sided p-value:** **0.01953**

Because the p-value is below 0.05, the test rejects the null hypothesis in favor of higher median recall for the younger group relative to the reference value.

### Confidence Interval

The sign-test output also reports a **95% two-sided interpolated confidence interval for the median of approximately [4.97, 13.68] words**. This interval comes from the two-sided test; the one-sided test produces a different, one-sided interval.

## Key Findings

1. **Higher median recall:** The younger group recalled a median of **10.5 words**, compared with the older-group benchmark of **4 words**.
2. **Statistical significance:** The one-sided sign test returned **p = 0.0195**, indicating evidence that the younger group's population median exceeds the benchmark.
3. **Observed distribution:** Eight of the 10 observations exceeded 4 words, one equaled 4, and one was below 4.

## Practical Takeaway

This analysis demonstrates how a nonparametric hypothesis test can evaluate a difference in typical performance even when normality is not assumed. The results provide evidence of higher word recall in the sampled younger group relative to the older-group reference median.




