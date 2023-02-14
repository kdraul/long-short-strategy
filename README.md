# Developing a Long-Short Equity Strategy out of the Relationships between the Stock Returns and the Financial Ratios and Growths
This project is a result of the combination of the assignments from the "Data-Driven Investing with Python | Financial Data Science" course from 'Fervent' on Udemy. The platform used for this project is the 'Jupyter Notebook' which is an integrated development environment (IDE) and a presentation tool for the Python programming language.

Several important libraries of Python like NumPy, pandas, Matplotlib, seaborn and statsmodels, that are in extensive use today in the field of Data Science, were used for the analysis.

The project delves into the analysis of relationships between the *annual average of the stock price returns* and their *annual volatility in a year* and the several financial benchmarks like the *Cash Flow from Operations (CFO) to EBITDA ratio, Debt-to-Equity ratio, EBITDA growth, Cash Flow from Operations (CFO) growth*. The strength of each relationship is tested using t-test for correlation, and out of these, the statistically significant relationship is chosen for the *Long-Short strategy*. And in the final leg of the analysis, the strategy is tested for significance.
-----
The project is divided into four parts which follows the general pattern of data analysis:

### Part 1 - Collection of Data:  
This includes choosing approximately **90 companies** for the analysis using *Stratified Random Sampling* and then **downloading of stock price data** of these companies using 'yfinance' api (Yahoo! Finance). The process of extracting the **financial ratios and financial growth** values can't be seen in the Jupyter Notebook since they were **manually obtained by reading 500+ Annual Reports** of the companies and those values were inserted in a comma-seperated values (.csv) file for each company.

### Part 2 - Cleaning the Data and EDA:  
This includes **removing errors and outliers** from the data, while also **removing any irrelevent data points** from the data. It is while conducting an exploratory data analysis using the **line charts, histograms and boxplots** that we detect the outliers (the extreme values) in the data. Then seperate '.csv' files were created for stock returns, volatility, financial ratios and financial growths to be used in the Part 3 Jupyter Notebook.

### Part 3 - Regression Analysis:  
Each financial ratios and financial growths, stock returns and stock volatility are then analysed for relationships. The **dependent variable** for the regression is either the **stock returns or the volatility (risk)** of stock, and the **independent variable** being **EBITDA growth, Cash Flow from Operations (CFO) growth, CFO to EBITDA ratio or Debt-to-Equity ratio**.
The variables which have significant relationship are then chosen for the next part which is the long-short equity strategy.

### Part 4 - Testing the Long-Short Equity Strategy:  
Finally, the significant relationship from the Part 3 is used in the long-short strategy. The **daily returns are segregated into 5 Quintiles** based on the relationship. Then, the **difference of returns** of the top and the bottom quintiles is used as the basis **calculating the Alpha $\alpha$** of the strategy i.e. the excess returns over and above the market returns. The alpha tells us the significance of the long-short strategy.

The outcomes of the regression analyses, the observations and the Alpha generated from the Long-Short strategy are all in the Jupyter Notebooks. You're welcomed to have a look at them. Thank you! :)
