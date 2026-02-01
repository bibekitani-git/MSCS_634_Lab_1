This lab was designed to walk through the essential early stages of the data science lifecycle. My primary goal was to take a raw sales dataset and transform it into a clean, analyzed format ready for machine learning or business reporting. By focusing on data collection, visualization, and rigorous preprocessing, I aimed to understand how individual variables influence overall sales performance and how to handle common data quality issues like missing values and outliers.

Key Insights and Discoveries
While exploring the data through visualizations, I noticed that the distribution of sales across different product categories was relatively uneven, with certain sectors driving the majority of the revenue. The box plots were particularly revealing because they highlighted several extreme transactions that sat far outside the typical range, suggesting either high-value bulk orders or potential entry errors.

From a statistical standpoint, the correlation analysis showed that the relationship between discount levels and total sales was not as strong as initially expected. This suggests that while discounts might move inventory, they aren't the sole factor driving high-value revenue in this specific dataset. Additionally, the central tendency measures confirmed that our average sale price was being heavily skewed upward by outliers before the cleaning process took place.

Challenges and Decision Making
One of the main hurdles I encountered was deciding how to treat the missing values in the sales amount column. I ultimately chose to use mean replacement because the data was missing at random and the dataset was small enough that dropping those rows would have cost me valuable information.

Another significant decision involved the outlier removal process. I opted for the Interquartile Range (IQR) method because it is more robust than standard deviation when dealing with skewed sales data. While it resulted in a smaller final dataset, the remaining data is far more representative of daily business operations. Finally, I applied Min-Max scaling to the numerical values to ensure that when this data is used in future models, features with larger scales don't unfairly dominate the results.

Data Files
For the purpose of this lab, I generated a synthetic sales dataset containing 200 records to simulate real-world business scenarios. This allowed me to intentionally inject missing values and outliers to demonstrate preprocessing techniques. The raw data is saved in this repository as sales_dataset.csv and the final processed version is available as cleaned_sales_data.csv.
