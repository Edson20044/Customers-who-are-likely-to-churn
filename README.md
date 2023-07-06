The aim of the project is producing a report that identifies customers who are likely churn for a telecommunication provider. The original dataset is available on https://www.kaggle.com/c/customer-churn-prediction-2020/overview. It has been modified with some columns removed, an age column added, and some cleaning performed. The data includes the following columns:

-	two-letter abbreviation of the US state of customer residence
-	customer's age
-	three-digit area code
-	whether or not customer has a voicemail plan
-	number of voicemail messages
-	total minutes of day calls
-	total number of day calls
-	total charge of day calls
-	number of calls to customer service
-	whether the customer has churned or not

1.	**Churn Rate**

First, the churn rate is calculated using the formula below   

The churn rate is 14.07%.  Compared to the whole industry, it is not quite high. However, it is necessary to find and apply relevant methods to prevent customers from churning. Therefore, the types of customers who churned are to be investigated.

2.	**Initial EDA**

For each column, the following metrics are calculated using Excel functions:

•	Number of NULL or blank values
•	The mean of the column
•	The median of the column
•	The standard deviation of the column
•	The minimum value of the column
•	The maximum value of the column

The results presented in a separate table and are as follows:
•	Columns total_day_minutes (54,01), total day calls (19,85), and number_vmail_messages (13,43) have the most variation.
•	The number of vmail_messages differs most in its mean and median. It indicates that the shape of the distribution is skewed to the right.

3.	Exploring Data Grouped by State Churn

A PivotTable grouping the data below is created:

•	State and churn as rows 
•	Average of age, Sum of voice_mail_plan, Sum of number_vmail_messages, Average of total_day_minutes, Count of total_day_calls, Sum of number_customer_service_calls, Churn rate as Values

The PivotTable is sorted by the Churn rate value in descending order.
The findings for the five states with the highest churn rate are as follows:
There seems to be a common pattern when comparing customers who have churned vs. those who haven’t. It is younger customers who tend to churn rather than older ones. Also, the former ones talk more on their phones in a day with fewer day calls. In addition, they turn to customer service less and are charged more on average on a daily basis.

4.	Exploring Data Grouped by Voice_Mail_Plan and Churn

Five states with the highest churn rate were selected and the following characteristics are taken into account:

•	Average of age
•	Sum of voice_mail_plan
•	Sum of number_vmail_messages
•	Average of total_day_minutes
•	Count of total_day_calls
•	Average of total_day_charge	
•	Sum of number_customer_service_calls
•	Churn rate

The analysis of this data helps identify customers who are likely to churn. PivotTable is created grouping the data:

•	Voice_mail_plan and Churn as Rows 
•	Average of age, Sum of number_vmail_messages, Sum of total_day_minutes, Average total_day_charge, Churn rate as Values

Following the results, 86.3% of people who churned didn't have a voicemail plan and had the following characteristics:

•	Younger than those who didn't churn
•	Spend relatively less time on calls
•	Were spending more per day compared to the ones who didn’t churn and didn’t have a voicemail plan

5.	Analyzing Frequency Distributions

These relationships can be explored via appropriate visualizations. For a broader understanding of the dataset, individual distributions of the numerical columns should be observed.

A histogram is created for each column below:

•	age
•	number_vmail_messages
•	total_day_minutes
•	total_day_calls
•	total_day_charge
•	number_service_calls

The histograms reveal the results below:

•	Most customers fall in the age group of 34 to 44 year old
•	Most customers spent from 108 to 252 minutes on calls on a daily basis
•	Significant number of customers pay $28 to $42 per day
•	Over 3,000 customers sent or received fewer than 3 voicemail messages. Most of the remaining customers sent or received 21 to 39 voicemail messages. As the distribution is skewed to the right, the mean is greater than the median
•	Most customers make 80 to 125 calls per day 
•	Considerable number of customers make 1 call. The distribution is right-skewed therefore the mean is greater than the median 

6.	Visualizing Data Grouped by State and Churn

The visualizations are limited to the top three states out of the five that were identified earlier:

•	NJ
•	MN
•	TX

PivotTable is created to group the data:

•	churn as Rows, 
•	state as Columns
•	the average of age as Values

A Bar Chart is created from the above PivotTable that reveals the following findings:

•	In all three states, customers who churned were younger than those who did not. 
•	These two age groups include people of approximately the same age

7.	Exploring and Visualizing Data Grouped by Churn

Finally, differences in other data grouped by churn in states with the highest churn (Minnesota, New Jersey, Texas) are explored. PivotTables are created to look at the following groups:

•	Age
•	Voicemail Plan
•	Daily Charges
•	Voicemail Messages

For each PivotTable, Bar Chart is created depicting that group’s relationship. They confirm the insights discussed above as well as demonstrate the following:

•	In all the three states the customers who churn are about 28 to 31 years old. The older customers, who are 39 to 40, do not tend to churn
•	The customers from New Jersey were charged more compared to the others
•	Churned New Jersey customers sent and received more voicemail messages than those from the other two states

