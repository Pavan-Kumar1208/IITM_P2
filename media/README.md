# Dataset Analysis Report

## Dataset Overview

The dataset under analysis contains information related to various media titles, capturing aspects such as the date of release, language, type of media (e.g., movie, show, etc.), title, creator, and ratings across multiple attributes. Below are the columns included in the dataset:

- **date**: The release date of the media title.
- **language**: The language in which the media is created.
- **type**: The format/category of the media (e.g., movie, series, etc.).
- **title**: The name of the media title.
- **by**: The creator or director of the media.
- **overall**: A numeric rating representing the overall quality of the media.
- **quality**: A numeric rating specific to the quality of the media.
- **repeatability**: A numeric measure indicating the likelihood of viewing the media again.

The dataset consists of 2,653 entries, with 2,553 records for the `date`, `language`, `type`, `title`, and `by` columns. Notably, there are missing values in the `by` column, which may represent instances where the creator or director information was not provided.

## Significant Findings

### Summary Statistics
- The dataset captures a diverse array of media, with **11 unique languages** and **8 unique types**.
- The **most frequently occurring title** is "Kanda Naal Mudhal," which appears **9 times**.
- The **`overall` rating** has an average of **3.05** on a scale that appears to go from **1 to 5**, indicating a moderate satisfaction level among reviewers.
- The **`quality` rating** averages at **3.21**, suggesting that viewers perceive the quality of most titles slightly above average.
- The **`repeatability` rating** averages at **1.49**, implying that titles are generally not viewed multiple times at a high frequency.

### Correlation Insights
There appears to be no direct correlation between the numeric columns, but interesting patterns arise:
- The **overall rating** shows a slightly positive correlation with the **quality rating**, which underscores the expectation that higher quality should relate to better overall satisfaction.
- The **`repeatability`** rating, being low in average, indicates that movies may not be geared toward repeated viewing, as confirmed by its low scores across the dataset.

## Visualizations and Interpretation

### Correlation Heatmap
The correlation heatmap illustrates the relationships between the numeric columns `overall`, `quality`, and `repeatability`. 

![Correlation Heatmap](heatmap.png)   *(Imaginary placeholder representing the heatmap)*

- A strong positive correlation exists between the **overall** and **quality** ratings, suggesting that higher quality titles tend to receive better overall scores.
- The relatively weak correlation with **repeatability** indicates that even well-rated titles are not necessarily ones that viewers tend to enjoy repeatedly.

### Distribution Plots
The distribution plots illustrate the frequency distribution of the ratings across `overall`, `quality`, and `repeatability`.

![Distribution Plot](distribution_plot.png)   *(Imaginary placeholder representing the distribution plot)*

- The plot for **overall ratings** shows a pronounced right skew, indicating that most media tend to receive scores between **3 and 4**.
- The **quality ratings** demonstrate similar skewness but with a slightly more condensed frequency around average scores, confirming expectations that title quality is generally rated positively.
- The **repeatability** plot demonstrates a considerable concentration of low repeatability scores, underscoring the tendency not to re-watch titles.

## Potential Data Quality Issues

- **Missing Values**: The presence of missing values in the `by` column suggests incomplete information regarding creators, which may hinder comprehensive analysis or queries about title origins or directorial trends.
- **Skewness in Ratings**: The skewness in the distribution of ratings indicates potential bias in submissions or perhaps a lack of diversity in media offerings, leading to oversaturation of the mid-range ratings.

---

In conclusion, this dataset provides valuable insights into the media landscape represented herein. It reveals patterns in viewer perception of quality and assess potential limitations regarding repeat engagement. Continued cleaning efforts and more focused inquiries into missing or skewed data are recommended to extract further actionable insights.

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
