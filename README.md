# Robust Statistics -- Automated Anomaly Detection

## Objective
I tested how different summary statistics and outlier detection methods behave on housing price data, including when part of the data is corrupted.

## Methodology
- I loaded the California Housing dataset (20,640 observations).
- I computed summary statistics that are sensitive to outliers (mean, standard deviation) and statistics that resist them (median, trimmed mean, IQR, MAD), then compared them.
- I implemented Tukey Fences by hand to flag price outliers.
- I applied Isolation Forest to detect anomalies across multiple features at once.
- I compared the observations flagged by Tukey Fences with those flagged by Isolation Forest.
- I corrupted 5% of the data and recomputed each statistic to measure how much it shifted.

## Key Findings
- Tukey Fences and Isolation Forest flagged different observations. Tukey looks at one variable at a time, while Isolation Forest looks at combinations of features.
- After 5% contamination, the mean shifted by [YOUR VALUE]%, while the median shifted by only [YOUR VALUE]%.
- The median, trimmed mean, IQR, and MAD stayed close to their original values under contamination. The mean and standard deviation did not.
