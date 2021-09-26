# TransactionalRetailData-Wrangling-EDA
Data Wrangling, graphical &amp; non-graphical EDA methods to find and fix data problems for transactional retail data from an online electronics store, using Python

In this project, I perform a very thorough and extensive data wrangling and cleansing in 3 datasets, in order to identify any data quality problems, any inconsistency among the attributes, and perform fixes. These 3 datasets contain transactional retail data from an online electronics store located in Melbourne, Australia. The store is exclusively online, and it has 3 warehouses around Melbourne from which goods are delivered to customers. In particular,

For Dirty_data dataset, the data quality problems mainly come in the form of inconsistency of values within the attributes, as well as the interaction among the attributes themselves. I will identify all of these problems and fix them, with the help of business rules.
For Outlier_data dataset, the data quality problems mainly come in the form of outliers. I will detect all of them and remove them.
For Missing_data dataset, the data quality problems mainly come in the form of missing data. I will identify them and impute them with appropriate methods, with the help of business rules.

The business rules associated with these datasets are:

For Dirty_data dataset, any rows can carry no more than 1 anomaly. There can only be 1 anomaly in a single row and all anomalies are fixable. If there are no possible way to fix it, it is not an anomaly.
The retail store focuses on 10 branded items and sells them at competitive prices.
The store has different business rules depending on the season to match the different demands of each season. For example, delivery charges is calculated using a linear model which differs depending on the season. The model depends linearly on:
Distance between customer and nearest warehouse
Whether customer wants an expedited delivery
Whether customer was happy with their last purchase (if no previous purchase, it is assumed that customer is happy)
To check whether a customer is happy with their last purchase, the customer's latest review is classified using a sentiment analysis classifier. A sentiment is considered positive if it has a compound polarity score of at least 0.05
If the customer provided a coupon during purchase, the coupon discount percentage will be applied to the order price before adding the delivery charges. Delivery charges are never discounted.
Coupon discount, delivery charges and ordered quantity values in shopping cart are always correct.
