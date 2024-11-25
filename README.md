**Project Report - Churn Prediction**

*Ujjwal Ravani x Madhav Kamani*

Starting off, we first want to understand and clean the dataset. We read the excel file, and look at the dataframe. It has 5630 customer entries and 20 parameters. There are some typos, some repeated values and other minor errors in the dataset. We clean the dataset, making it ready for analysis. Here are the different columns (parameters) and their unique values :

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.001.jpeg)

For the EDA part, we first decide the questions we want to ask, which would then be answered by analyzing the data. Here are the questions we decided to ask :

1. Is there a relationship between Gender and Churn?
1. Which MartialStatus has the highest Churn rate?
1. Which CityTier has higher Tenure and OrderCount?
1. Do Customers with High SatisfactionScore have high HourSpendOnApp?

   Is there a correlation between SatisfactionScore and HourSpendOnApp?

5. Which CityTier has the most HourSpendOnApp?
5. What is the relation between NumberOfAddress and CityTier?
5. Do people who complain churn more ?
5. What is the relation between Complain and DaySinceLastOrder?
5. Is there a relationship between PreferredLoginDevice and Churn?
5. What is the distance between warehouse and customer house in different city tier?
5. Do different CityTiers have different preferred products?
5. What is the preferred payment mode for different CityTiers?
5. Which CityTier has the highest OrderCount?
5. Does the percentage increase in order amount from last year affect churn rate?
5. What is ordercount for customers with high HourSpendOnApp?
5. Is there a relationship between preferred order category and churn rate?
5. Do customers who use more coupons have lower churn rates?
18. Is there a connection between satisfaction score and number of orders in the past month?
18. Is there a relation between CashbackAmount and order counts within churn?
18. Are customers who complained more, more likely to churn?

1\. a. Some columns are numerical (integers/float) and some columns are categorical

(strings), to understand the data at a high level we first look at the density plot of these features :

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.002.png)

b.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.003.png)

c.

Here’s the correlation matrix of numerical features.![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.004.jpeg)


2\.

1. To find out the relationship b/w gender and churn, we find the % churned users who are male vs female

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.005.png)

2. Next, we looked at the percentage male users who churned vs % female users who churned

   ![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.006.jpeg)

3\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.007.jpeg)

4. Analyzing parameters against City Tier
1. Hours spent on app vs city tier

   ![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.008.jpeg)


2. Tenure vs city tier

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.009.jpeg)



|CityTier|Mean Tenure|
| - | - |
|1|10\.52|
|2|11\.16|
|3|9\.36|

3. Distance of warehouse to home by city tier

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.010.jpeg)

4. Preferred Order Category by City Tier

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.011.png)

5. Preferred Payment Mode by City Tier

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.012.png)

6. Cumulative orders per city tier

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.013.png)

5. Churn Rate vs Preferred order category

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.014.jpeg)

6. Churn Rate by Complain

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.015.jpeg)

7. Days Since Last order vs Complain

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.016.jpeg)

8\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.017.jpeg)

9\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.018.png)

10\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.019.png)

11\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.020.png)

12. Churn % by device type

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.021.jpeg)

13. Churn % by Satisfaction Score

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.022.jpeg)

14\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.023.jpeg)

15\.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.024.png)

EDA Insights

- The males are more likely to churn as we have 63.3 % churned males from the app. This might be due to a lack of products that typically males are interested in.
- If we look at marital status, most customers are married.


- Single customers are most likely to churn from the app.
- City Tier 2 has the highest average tenure, but tenure does not vary strongly with city tier.
- Sum of hours spent on the app and satisfaction seem to have no particular correlation.
- City tier 1 has spent the most hours on the app.
- There is a weak negative relation between complaining and the number of days since last order
- Mobile phone users are likely to churn may be this indicates a problem on the app user experience on the app mobile version.
- The distance of warehouse is fairly constant across different tiers, meaning the company has established its warehouses even in smaller cities.
- Laptop & accessories and mobile phones are the preferred categories across all city tiers
- Preferred payment method for CityTier '1' ==> DebitCard

  Preferred payment method for CityTier '2' ==> UPI

  Preferred payment method for CityTier '3' ==> E wallet

- CityTier '1' has the highest order count with 10298 orders.
- When the Year over Year Order Hike percentage increases, churn decreases. We should think about increasing this, especially for users who have this % value to be 12-15.
- Among the users who have spent a ‘high’ amount of time on the app ( > 3 Hours )
- Customers who have used more coupons tend to churn lower
- SatisfactionScore isn’t correlated to OrderCount
- There is no apparent relation between cash back amount and order count. Customers having cashback amounts in the range 100-200 tend to churn more.
- As expected, customers who’ve complained, tend to churn more.

After applying the algorithms, we rank the features that contribute the most towards churn. Hence, looking at trends of the highest ranked features will give us the most accurate prediction of churn trends in the future.

![](Aspose.Words.78e962b8-d757-41c7-b0b5-fac59d51fe6a.025.jpeg)
