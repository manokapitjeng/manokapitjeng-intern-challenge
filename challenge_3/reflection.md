# Reflection

## Hardest Part

The hardest part of this challenge was cleaning the data before analysing it. I realised that if the data is not cleaned properly, the analysis can give misleading results even if the code runs without errors. The date column was one of the most challenging parts because the dates were not all in the same format. I had to understand why the `.dt` function was not working at first and why the date column needed to be converted properly before I could create the month column for trend analysis.

The revenue column was also challenging because the values were not clean numbers at first. Some values had currency symbols, commas, spaces, brackets, and negative values. I had to clean the column before using it for calculations such as totals, averages, trends, and the forecast. I also had to think carefully about negative revenue values. Instead of deleting them, I treated them as returns because that made sense in a retail dataset.

Another difficult part was handling missing store values and inconsistent store names. I treated missing store values as Online because online transactions may not have a physical store linked to them. However, I understand that this is still an assumption and could affect the online revenue totals if some missing values were actually data quality issues. I also had to standardise store names, province names, and category names so that the same values were not counted separately.

## What I Would Do Differently

With more time, I would investigate the missing store values more deeply. Instead of only treating them as Online, I would compare the results using Online and Unknown to see how much the assumption changes the analysis. This would help me understand whether the missing store values have a big impact on the final findings.

I would also analyse returns in more detail. For example, I would check which stores, provinces, categories, or months had more returns. This could help the business understand whether returns are linked to specific products or sales periods.

For the prediction section, I used average monthly revenue per store. With more time, I would improve the forecast by adding seasonality, promotions, stock availability, customer demand, and more historical data. I would also improve the charts to make them clearer and more professional.

## What I Learned

I learned that data analysis is not only about coding. It is also about understanding the data, checking assumptions, cleaning carefully, and explaining decisions clearly. I learned how important it is to inspect the dataset first before making changes.

This challenge helped me practise loading a CSV file, checking missing values, cleaning text columns, cleaning numeric values, converting dates, separating returns from sales, using `groupby()`, creating simple visualisations, answering business questions, investigating customers, and building a basic forecast.

I am still learning Python and pandas, but this project helped me understand the full data analysis process better. It also helped me see how small cleaning decisions can affect the final business insights.
