# Customer Segmentation using Machine Learning in R
Using R-language, this project is to display Customer Segmentation Machine Learning to find our best customer. I will be using unsupervised learning and using clustering techniques to help a Mall to identify several segments of customers that will allow them to target the potential user base. To do this, we first need to explore the data and then create visuals to get to know the customers.

## Data Exploration
To gain insights, we need to know our dataset.  Displaying the first six rows of the dataset using the function head() and summary() function can help us take a look at what we will be working with. Lets take a look.

![Screenshot of using the str function and names function to see column names, list of objects and their structure.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration1.JPG)

![Head and Summary function.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration2.JPG)

![Getting to know data for each column.](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/DataExploration3.JPG)

We now understand that the minimum age of Mall customers is 18 with an average of around 38. The minimum income for Mall customers is 15 while average is around 60.

### Customer Gender Visualization

Creating visuals helps us understand what the data is trying to tell us a lot quicker.  Lets take a look at customer gender to see who our main customer is for the Mall.

![Gender Comparison](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Gender%20Comparison%20BarPlot.JPG)

By the barplot, we can see that tne number of females is higher than male customers.  Using a pie chart can help us see by how much percentage wise.

![Gender Ratio](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Male_Female%20Ratio%20Pie%20Chart.JPG)

Mall customers are 56% females and 44% males.  This is a 12% difference to our Mall customers. Now that we have an idea of what gender tends to shop the most at the Mall, lets look at the ages of our customers.

![Age Summary](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AgeSummary.JPG)

![Age Count Histogram](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Age%20Count%20Histogram.JPG)

![Descriptive Analysis of Age](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Age%20DescriptiveAnalysis%20Boxplot.JPG)

Baste on the Histogram and Boxplot, we can see that the maximum customer ages are between 30 and 35, while our minium customer age is 18, maxium customer age is 70.

### Annual Income of Customers Analysis

We now want to see what the annual income of our customers at the Mall is through visualizations.  We can do this using histogram and a density plot.

![Annual Income Histogram Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AnnualIncome%20Histogram.JPG)

![Annual Income Density Plot](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Annual%20Income%20Density%20Plot.JPG)

The results from our descriptive analysis, we can see that the minimum income of our Mall customers is 15 and the maximum income is 137. Customers earning  an average of 10 also have the highest frequency count which means they are spending more.  Average salary of our customers is 60.56 as well, a good think to note to our stakeholders. The results from the Kernal Density Plot  shows that the annual income has a normal distribution.  Lets take a look at customer spending.

### Customer Spending Analysis

It's important to most stakeholders to know how much customers are spending on average.

![Spending Analysis Boxplot](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/SpendingScore%20Boxplot.JPG)

![Spending Analysis HistoGram](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/SpendingScore%20HistoGram.JPG)

Looking at our two visuals, the minimum spending is 1, a max sore of 99 in spending, with an average of our customers spending 50.20 via our boxplot. Our Descriptive Analysis of Spending is that minimum is 1, maximum is 99, and having an average spending score of 50.20.  The histogram shows that the customers between 40 and 50 of age is our highest spenders among all of the other age groups with a score of 40.

## K-means Algorithm

In this section, we will be using k-means clustering algorithm.  First we need to find the optimal clusters to get our final output. To get the results we need to see, we need to use the updated cluster mean which goes through several iterations until the cluster assignments stop altering. 

### Determining Optimal Clusters - Elbow Method

Using the Elbow method, Silhouette Method, and Gap statistics, we will find our optimal clusters. By using the Elbow Method, we will be able to see the oppropriate number of clusters based on where the bend in the elbow is.

![Elbow Method for Clustering](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Number%20of%20clusters%20K.JPG)

Based on the elbow, we can conclude that 4 is the appropriate number of clusters.

### Average Silhouette Method

Using the average silhouette method can help us measure the quality of our clustering operation.  We can determine how well within our cluster is the data object.  Obtaining a high average silhouette width means that we have good clustering.  Silhouette methods' average is calculated by the mean of silhouette observations for different k clusters which we can maximize the average silhouette over significant values for k clusters.

![k2 to k10 Silhouettes](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/k%20means%20codes.JPG)



