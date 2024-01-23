---
title: "Homework 1"
author: "Sandra Nwankwo"
date: "`r Sys.Date()`"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
### Question 1

Categorical Variables = 9, Quantitative Variables = 18.

### Question 2

```{r}
SleepStudy <- read.csv("~/PUBH 6450/SleepStudy.csv")
str(SleepStudy)
```

### Question 3

Gender, Class Year, Early Class, All Nighter


### Question 4

```{r}
summary(SleepStudy$DepressionScore)
range(SleepStudy$DepressionScore)[2]
IQR(SleepStudy$DepressionScore)
(SD = sqrt(var(SleepStudy$DepressionScore)))

summary(SleepStudy$AverageSleep)
range(SleepStudy$AverageSleep)[2]
IQR(SleepStudy$AverageSleep)
(SD = sqrt(var(SleepStudy$AverageSleep)))

```

### Question 5

For AverageSleep:
Mean = 7.97 hours.
College students in this dataset, on average, sleep around 7.97hours per night.
Median = 8 hours
The middle value of the sleep time is 8 hours. This suggests that the data distribution is possibly symmetrical.
First Quartile, Q1 = 7.43
25% of the data are below this value.
Third Quartile, Q3 = 8.59
75% of the data are below this value.
Interquartile range, Q3 - Q1 = 1.16
This shows there is variability in sleep duration within the central portion of the dataset.
Standard Deviation = 0.9648396
This measures the average deviation of each data point from the mean.

### Question 6

```{r}
hist(SleepStudy$DepressionScore)
hist(SleepStudy$AverageSleep)
```

### Question 7

```{r}
boxplot(SleepStudy$DepressionScore)
boxplot(SleepStudy$AverageSleep)
```
### Question 8

The histogram shows a symmetrical distribution (mean = 7.97, median =8). The measure of the spread here is IQR and Standard deviation. The IQR (1.16 hours) and standard deviation (0.96) show there is moderate variability in the sleep duration among these students. The measure of center, median, shows sleep duration is centered around 8 hours.

### Question 9

I think MEAN is the best because looking at the histogram, the mean provides a good central measure for the data. The shape of the histogram also looks relatively symmetrical which favors the mean.

### Question 10

For DepressionScore, the median offers a better representation because of the presence of (many) outliers

### Question 11

For measure of center, median is less affected by extreme values. The median doesnt require computing the entire values in the data set

For measure of spread, IQR is less influenced. Since IQR is based on values that come from the middle half of the distribution, it's unlikely to be influenced by outliers.

### Question 12

The Middle Line represents the MEDIAN
Whiskers represent the DATA RANGE

### Question 13

Average Sleep: 5 outliers
Depression: 10 outliers

### Question 14

A student who averages 5.7 hours of sleep is an outlier 

### Question 15

7 bins

### Question 16

```{r}
hist(SleepStudy$DepressionScore, main="Histogram of DepressionScore (Small Bins)", xlab="DepressionScore", col="skyblue", border="black", breaks=30)

hist(SleepStudy$DepressionScore, main="Histogram of DepressionScore (Large Bins)", xlab="DepressionScore", col="lightcoral", border="black", breaks=10)

```


### Question 17

The smaller the number of bins, the more overly smooth the histogram appears. This could result in poor resolution. The larger the number of bins, the more granular the histogram appear

### Question 18

```{r}
hist(SleepStudy$DepressionScore, main="Histogram of DepressionScore (Optimal Bins)", xlab="DepressionScore", col="lightgreen", border="black", breaks=20)

```
breaks = 20 gave me a view of the dataset i find preferable

### Question 19

I think it is the histogram because it shgows the shape of the distribution. For example, in Depression Score, we can see more students have lower depression score because the data is more concentrated around zero

### Question 20

```{r}
table_ClassYear <- table(SleepStudy$ClassYear)
print(table_ClassYear)

table_AlcoholUse <- table(SleepStudy$AlcoholUse)
print(table_AlcoholUse)

```
### Question 21

```{r}
barplot(table_ClassYear, main="Barplot of ClassYear", xlab="Class Year", ylab="Frequency", col="skyblue")

barplot(table_AlcoholUse, main="Barplot of AlcoholUse", xlab="Alcohol Use", ylab="Frequency", col="lightcoral")

```

### Question 22

```{r}
# Number of sophomores
num_sophomores <- table_ClassYear["2"]

# Total number of participants
total_participants <- length(SleepStudy$ClassYear)

# Proportion of sophomores
proportion_sophomores <- num_sophomores / total_participants

cat("Number of sophomores:", num_sophomores, "\n")
cat("Proportion of sophomores:", proportion_sophomores, "\n")

```

### Question 23

Heavy=16, Abstain = 34, Moderate = 120, Light = 83
From the information above, we can see that the college students use alcohol significantly

### Question 24

College students at Northeastern University, United States.

### Question 25
The results of this study cannot be generalized to the entire population of college students at Northeastern University. This is because the survey sampled students from just one college in the university.  Northeastern University has 9 colleges.
```{r}

```

```{r}

```

```{r}

```

```{r}

```

```{r}

```
