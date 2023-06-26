# TELUS-Call-Center-Analysis
This is an analysis to check how well TELUS Call Center discharge their services to their customers

---

# Introduction

The dataset contains 10 columns and 5,000 rows. The columns are;
"Call Id", "Agent", "Date", "Time", "Topic", "Answered(Y/N)", "Resolved", "Speed of answer in seconds", "AvgTalkDuration", "Satisfaction rating".

---

# Data Cleaning and Transformation

The transformation and cleaning of the data was done using power query in Power BI desktop. The cleaning were performed starting from the first column which was the "Call Id" to the last column which was the " Satisfaction rating".

![ai](https://github.com/Meenah001/TELUS-Call-Center-Analysis/assets/97677904/254963d0-f841-4940-ae3b-95e1129e51ca)

The above image depict the dataset in it raw form before cleaning 

---

Having checked each column for missing values, inconsistencies, data type error, Outliers, Ivalid data and structural errors, I got to know that "Call Id", "Agent", "Date", "Topic", "Answered(Y/N)" and "Resolved" columns had no problem, they are perfectly okay. But the "Time", Speed of answere in seconds", "AvgTalkDuration", and "Satisfaction rating" columns have some cleaning to be done on them.

Starting with the "Time" column, It's seen that it contains both date and time. In order to extract only the time I usded the split column function. splitting using the space delimeter (Left-most delimeter). By doing this I got my "Time" column with the date being mixed with it.

It was seen in the "Speed of answer in seconds" column that there were some missing values (null). After checking that if the null values were removed it won't affect the whole dataset I decided to remove them from the column, This makes the column cleaned.

The "AvgTalkDuration" column was removed entirely from the dataset because it contains contaminated entries. Time and Year were found in this column which doesn't represent what the column header is.
























