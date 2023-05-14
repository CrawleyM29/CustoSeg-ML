# Customer Segmentation using Machine Learning in R
Using R-language, this project is to display Customer Segmentation Machine Learning to find our best customer. I will be using unsupervised learning and using clustering techniques to help a Mall to identify several segments of customers that will allow them to target the potential user base. To do this, we first need to explore the data and then create visuals to get to know the customers.

## Data Exploration
To gain insights, we need to know our dataset.  Displaying the first six rows of the dataset using the function head() and summary() function can help us take a look at what we will be working with. Lets take a look.

![Screenshot of using the str function and names function to see column names, list of objects and their structure.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration1.JPG)

![Head and Summary function.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration2.JPG)

![Getting to know data for each column.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration3.JPG)

We now understand that the minimum age of Mall customers is 18 with an average of around 38. The minimum income for Mall customers is 15 while average is around 60.

## Customer Gender Visualization

Creating visuals helps us understand what the data is trying to tell us a lot quicker.  Lets take a look at customer gender to see who our main customer is for the Mall.

![Gender Comparison](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Gender%20Comparison%20BarPlot.JPG)

By the barplot, we can see that tne number of females is higher than male customers.  Using a pie chart can help us see by how much percentage wise.

![Gender Ratio](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Male_Female%20Ratio%20Pie%20Chart.JPG)

Mall customers are 56% females and 44% males.  This is a 12% difference to our Mall customers. Now that we have an idea of what gender tends to shop the most at the Mall, lets look at the ages of our customers.

![Age Summary](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AgeSummary.JPG)

![Age Count Histogram](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Age%20Count%20Histogram.JPG)

![Descriptive Analysis of Age](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Age%20DescriptiveAnalysis%20Boxplot.JPG)

Baste on the Histogram and Boxplot, we can see that the maximum customer ages are between 30 and 35, while our minium customer age is 18, maxium customer age is 70.

## Annual Income of Customers Analysis

We now want to see what the annual income of our customers at the Mall is through visualizations.  We can do this using histogram and a density plot.

![Annual Income Histogram Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AnnualIncome%20Histogram.JPG)

![Annual Income Density Plot](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Annual%20Income%20Density%20Plot.JPG)



