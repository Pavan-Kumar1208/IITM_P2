# Dataset Analysis Report

## Dataset Overview

The dataset under analysis includes the following columns: 
- **date**: The date when the entry was recorded.
- **language**: The language of the content.
- **type**: The type of media (e.g., movie, series).
- **title**: The title of the content.
- **by**: The individual or organization associated with the entry.
- **overall**: A numeric rating representing the overall quality.
- **quality**: A numeric indicator of content quality.
- **repeatability**: A measure indicating how often the content can be revisited or rewatched.

The dataset consists of **2553 rows** and **8 columns**. It's noteworthy that there are missing values present in two columns, which indicates potential data quality issues and should be addressed during analysis.

## Summary Statistics

From the summary statistics, we can observe:
- The **date** column is unique with **2055 distinct dates** extracted from the data, indicating a wide span of content across various times.
- The **language** column shows a predominance of **English**, with **1306 occurrences**, significantly more than other languages.
- The **type** of media presents eight unique categories, with a strong inclination towards the **movie** type (count of **2211**).
- The overall ratings, with a mean of approximately **3.05** (on a scale from 1 to 5), suggest an acceptable level of quality among the entries.

## Significant Findings

### Skewness in Numeric Columns
The analysis indicates some skewness in the numeric columns, particularly in the **overall** ratings and the **quality** assessments. 

- The **mean** rating of **3.05** compared with a **standard deviation** of **0.76** suggests that while the average is around the midpoint, there may be ratings that are heavily clustered toward higher ratings, given the maximum score is **5**.

### Outliers
Outliers were detected in the **overall** and **quality** columns while examining data distribution. These outliers could be influential and may require further investigation to determine their cause and relevance.

### Correlation Insights
The correlation heatmap reveals the interrelationships among the numeric columns. 

1. **Correlation Heatmap**: 
   The heatmap illustrates the relationships between the numeric features, confirming that certain features exhibit multicollinearity. Notably:
   - The **overall rating** shows a positive correlation with **quality**, which is expected as content rated higher in quality typically receives better overall ratings.
   - The **repeatability** metric shows a weaker correlation with both ratings, indicating this measure may not relate strongly with how content is perceived overall or in terms of quality.

   ![Correlation Heatmap](.\media\correlation_heatmap.png)

2. **Distribution Plot**: 
   The distribution plots for the **overall** and **quality** ratings further depict the spread of data, highlighting that both columns exhibit a left-skewed distribution. Most ratings tend to cluster around the higher end of the scoring range.

   ![Overall Distribution Plot](.\media\overall_distribution.png)

## Implications of Visualizations

These visualizations provide a robust framework for understanding the underlying patterns and relationships within the data:
- The left-skewness observed suggests that many entries received relatively high ratings.
- Understanding the correlations allows for the identification of potentially redundant metrics that could simplify the dataset and the modeling process.

## Potential Data Quality Issues

The presence of missing values in two columns could impact the integrity of the dataset and lead to biases in the analysis. It is pivotal to:
- Investigate the nature of these missing values—whether they are missing at random or if a pattern exists.
- Consider strategies such as imputation, removal, or analysis based on the non-missing subset of data to minimize potential biases in the results.

### Conclusion
In summary, this dataset provides valuable insights into the media's perceived quality and user ratings. It is essential to address missing values and outliers for robust and reliable analysis. Moving forward, focusing on the inherent relationships identified through the visualizations will play a crucial role in enhancing further inquiries into this content.

## Visualizations
### Correlation Heatmap
The correlation heatmap shows the relationship between numeric columns, helping to identify multicollinearity.
![Correlation Heatmap](.\media\correlation_heatmap.png)

### Distribution Plots
The distribution plots highlight the spread, central tendency, and skewness of numeric data. For example:
- **date**: Distribution shows negative skewness.
![Distribution of date](.\media\date_distribution.png)
- **language**: Distribution shows negative skewness.
![Distribution of language](.\media\language_distribution.png)
- **type**: Distribution shows negative skewness.
![Distribution of type](.\media\type_distribution.png)
- **title**: Distribution shows negative skewness.
![Distribution of title](.\media\title_distribution.png)
- **by**: Distribution shows negative skewness.
![Distribution of by](.\media\by_distribution.png)
- **overall**: Distribution shows positive skewness.
![Distribution of overall](.\media\overall_distribution.png)
- **quality**: Distribution shows positive skewness.
![Distribution of quality](.\media\quality_distribution.png)
- **repeatability**: Distribution shows positive skewness.
![Distribution of repeatability](.\media\repeatability_distribution.png)
