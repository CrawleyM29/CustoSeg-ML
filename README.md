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

![k2 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k2%200.29.JPG)

![k3 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k3%200.38.JPG)

![k4 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k4%200.41.JPG)

![k5 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k5%200.44.JPG)

![k6 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k6%200.45.JPG)

![k7 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k7%200.44.JPG)

![k8 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k8%200.43.JPG)

![k9 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k9%200.41.JPG)

![k10 Silhouette Results](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/AverageSilhouette%20k10%200.38.JPG)

Now we can push a visual to showcase the optimal number of clusters by using fviz_nbclust() function

![Optimal Number of Clusters](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/OptimalNum%20of%20Clusters.JPG)

Perfect! We now can see that the optimal cluster is 6. We can use this information and move forward to the gap statistics method.

### Gap Statistic Method

We can use the gap statistic method to any clustering method like hierarchical clustering, K-means etc. Using this method can help compare the total intracluster variation for different values of k along with the expected values under the null reference distribution of data.

![Gap Statistic (k)](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/stat_gap%20visual.JPG)

Based on our gap statistic results, k = 6 as our optimal cluster.

![k6 clustering](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/k6%20cluster%20results.JPG)

As we observe our results, we can see a lit with several key information:

**cluster*: A vector of several integers that denote the cluster which has an allocation for each point.

**totss*: Represents the total sum of squares

**centers*: A matrix comprising of numerous cluster centers

**withinss*: A vector that presents the intra-cluster sum of squares having one component per cluster

**betweenss*: The sum of between-cluster squares

**size*: The total number of points that each cluster holds

## Visualizing the Clustering Results using the First Two Principle Components

Lets take a look at the principal component analysis.

![Components and Rotation](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/visual%20for%201st%20two%20principle%20components%202.JPG)

Standard Deviation is drastic between PC1/PC2 and PC3.  PC1 and PC2 both have around 26.0 while PC3 has 12.93. Looking at juct the rotation of PC1 and PC2 since they are closer in points, Age, Annual Income, and Spending Score is similar as well when it comes to range.

### Segments of Mall Customers K-means Clustering

![Mall Customers K-means](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/Segment%20Mall%20Customers%20kmeans%20clustering.JPG)

Our virst Mall Customer K-mean visuals shows that there is a distribution of 6 clusters:

   **Cluster 6 and 4*: Representing the customer_data with the medium income salary as well as the medium annual spend of salary.

   **Cluster 1*: Represents the customer_data having a high annual income with high yearly spending.

   **Cluster 3*: Denoting the customer_data with low annual income with a low yearly spending of income

   **Cluster 2*: Denotes a high annual income and low yearly spending.

   **Cluster 5*: Represening a low annual income with a high yearlt spending.

### PCA1 and PCA2 k-means Results

![k-means clusters for PCA1 and PCA2](https://github.com/CrawleyM29/CustoSeg-ML/blob/data-engineering/Customer%20Segmentation/Visuals/k-means%20cluster.JPG)

   **Cluster 4 and 1*: These two clusters shows the customers with medium PCA1 and medium PCA2 scores

   **Cluster 6*: Representing customers with a high PCA2 and a low PCA1 score

   **Cluster 5*: Customers with a medium PCA1 and a low PCA2 score

   **Cluster 3*: Customers with a high PCA1 income and a high PCA2

   **Cluster 2*: Customers with a high PCA2 and a medium annual spend of income.
    
Clustering can help stakeholders understand the variables a lot better, promoting better business decisions. With identifying customers, organizations can create and release products and services that aim more towards customers based on several parameters like spending patterns, age, and income. Based on our clustering, customers with a medium income spends more regularly based on their medium annual spending of their salary. 

# Summary

Going through the customer segmentation model, we developed this model by using an unsupervised machine learning. Clustering algorithms called K-means clustering, we analyzed and pushed visualization to show the data and then proceeded to implement the algorithm to better understand the type of customer the Mall needs to focus on for higher sales.
