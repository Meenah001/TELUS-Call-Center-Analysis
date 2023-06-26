# TELUS-Call-Center-Analysis
This is an analysis to check how well TELUS Call Center discharge their services to their customers

---

# Introduction

The dataset contains 10 columns and 5,000 rows. The columns are;
"Call Id", "Agent", "Date", "Time", "Topic", "Answered(Y/N)", "Resolved", "Speed of answer in seconds", "AvgTalkDuration", "Satisfaction rating". The Agent are 8 in number, there were 5,000 customers (4,054 after cleaning was perfomed on the dataset)

---

# Data Cleaning and Transformation

The transformation and cleaning of the data was done using power query in Power BI desktop. The cleaning were performed starting from the first column which was the "Call Id" to the last column which was the " Satisfaction rating".

![ai](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/254963d0-f841-4940-ae3b-95e1129e51ca)

The above image depict the dataset in it raw form before cleaning 

---

Having checked each column for missing values, inconsistencies, data type error, Outliers, Ivalid data and structural errors, I got to know that "Call Id", "Agent", "Date", "Topic", "Answered(Y/N)" and "Resolved" columns had no problem, they are perfectly okay. But the "Time", Speed of answere in seconds", "AvgTalkDuration", and "Satisfaction rating" columns have some cleaning to be done on them.

* Starting with the "Time" column, It's seen that it contains both date and time. In order to extract only the time I usded the split column function. splitting using the space delimeter (Left-most delimeter). By doing this I got my "Time" column with the date being mixed with it.

* It was seen in the "Speed of answer in seconds" column that there were some missing values (null). After checking that if the null values were removed it won't affect the whole dataset I decided to remove them from the column, This makes the column cleaned.

* The "AvgTalkDuration" column was removed entirely from the dataset because it contains contaminated entries. Time and Year were found in this column which doesn't represent what the column header is.

* "Satisfaction rating" column also contains some missing values (null). I removed all these null entries from the column in order for the column to be cleaned.

I went ahead to do some little changes to the "Date", "Answered (Y/N)" and "Resolved" columns. For "Answered (Y/N)" and "Resolved" columns, I replacd the value "Y" and "N" TO "Yes" and "No" respectively. I extracted the "Month Name" and "Day Name" from the "Date" column. 

Below is the image of the data after it has been thoroughly cleaned

![aii](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/f3c4dcc7-5c87-47f5-bfd2-c687b5c17527)

---

# Data Analysis and Visualization

![Satisfaction by day](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/017bd2ab-d40d-4091-9d4b-475eb93247e4)

The highest satisfaction rating was recorded on Monday

![satisfaction by month](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/454f1f3d-684e-436b-9868-e21271d9801e)

5,026 was the highest rating and this was gotten in the month of January

![Satisfaction by agent](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/c5645397-3c6f-44e4-a92d-af9f09732a7e)

Jim had the highest satisfaction rating. This means the customers enjoyed his service 

![Ribbon ](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/206492e3-cdae-4bdd-951d-dd6cef1c3b27)

The above image shows the trend between "Speed of answered in seconds", "Month" and "Topic". In January, 'Streaming' which is one of the many topic discussed by customers had the highest speed of answer in seconds while 'Admin Support' had the lowest. In March, 'Payment method' which is also one of the topics had the highest speed of answer in seconds while 'Contract related' had the lowest. The final Month, which is February, 'Technical Support' had the highest speed of answered in seconds while 'Payment method' had the lowest

---

# Dashboard Image

![Dash](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/58772c5f-7107-4ba4-8edb-45d16f829e44)










