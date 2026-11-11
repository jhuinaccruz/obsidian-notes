---
title: "Midterm Write-Up"
output: word_document
date: "2024-10-30"
---

# R Index

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE, root.dir = "~/Documents/ps211/my code")

library("psych")
library("dplyr")
library("ggplot2")
```

## Data and Table Manipulation

```{r}
#import data from transpop file
data <- read.csv("~/Documents/ps211/my code/midterm/transpop1s.csv", header = TRUE, encoding = "UTF-8")

#filter out data so that there is only X (the count of data points),
# SEXMINID (the categorical variable) and ACE()
two_var_table <- data %>%
  select(X, SEXMINID, ACE_I)

#create variables for easier recall and access, as well as readability

varA <- data$SEXMINID #variable A
varB <- data$ACE_I #variable B


n <- length(data$X) #total number of participants
varAn <- length(data$SEXMINID[data$SEXMINID == 0]) #total number of heterosexual participants
carBn <- length(data$SEXMINID[data$SEXMINID == 1])
```

## SEXMINID (categorical variable):

### Frequency:

```{r}
#calculates frequencies
f_het <- length(varA[data$SEXMINID == 0]) #heterosexual frequency
f_min <- length(varA[data$SEXMINID == 1]) #sexual minority frequency

#calculates relative frequency
rf_het <- f_het / n * 100 #heterosexual relative frequency percentage
rf_min <- f_min / n * 100 #sexual minority relative frequency percentage
```

### Visualization (Figure I)

```{r}
#pie chart for frequencies
barplot(
  height = c(f_het, f_min),
  names.arg = c("Identify as 'heterosexual' (0)", "Identify as a 'sexual minority' (1)"),
  main = "Frequency of SEXMINID",
  xlab = "SEXMINID (0 or 1)",
  ylab = "Frequency",
  beside = TRUE,
  ylim = c(0, 1300),
  col = c("blue", "purple")
)

#pie chart for relative frequencies
pie(
  c(rf_het, rf_min),
  labels <- c("Identify as 'heterosexual' (0)", "Identify as a 'sexual minority' (1)"),
  col = c("blue", "purple"),
  main = "Relative Frequency of SEXMINID"
)

```

## ACE_I (continuous variable):

### Central Tendency

#### Mean

```{r}
#calculated mean
mean(varB)

```

#### Median

```{r}
#calculated median
median(varB)
```

### Dispersion

#### Standard Deviation

```{r}
#calculate standard deviation
sd(varB)
```

#### Range

```{r}
#calculate range
max(varB) - min(varB)
```

#### Interquartile Range

```{r}
#calculates IQR
IQR(varB)
```

### Shape

#### Skewness

```{r}
#calculates skewedness
skew(varB)
```

#### Kurtosis

```{r}
kurtosi(varB)
```

### Visualization (Figure II)

```{r}
#histogram
hist(varB,
     main = "Distribution of Adverse Childhood Experiences",
     xlab = "Reported Severity of Adverse Childhood Experience",
     ylab = "Frequency",
     breaks = 10,
     ylim = c(0,600)
)

#boxplot
boxplot(varB,
        main = "Adverse Childhood Experiences: Box-Plot"
        
)
```

## Bivariable Analysis

### Mean/Variance

```{r}
#for the SEXMINID == 0

data_A <- data$ACE_I[data$SEXMINID == 0] #isolates ACE_I when SEXMINID is 0

mean(data_A) #calculates mean
var(data_A) #calculates variance

data_B <- data$ACE_I[data$SEXMINID == 1]

mean(data_B)
var(data_B)

```

### Visualization

```{r}
#modify the data so that the points reflect percentages (relative frequency) rather than total participants



x <- c()



for (i in 1:8) {
  b <- varB[varB == i]
  x <- c(x, sum(b)/sum(varB))
}

barplot_data <- table(
  varA,
  varB)



barplot(
  x,
  col = c("blue", "purple"),
  main = "How Sexual Minority Identity affects Adverse Childhood Experiences",
  xlab = "Severity of Adverse Childhood Experience",
  ylab = "Frequency (Participants)",
  ylim = c(0,1),
  beside = FALSE,
)
```

```{r}
# Sample data
data <- matrix(c(20, 30, 50, 40, 30, 30), nrow = 2, byrow = TRUE,
               dimnames = list(c("Group A", "Group B"), c("Category X", "Category Y", "Category Z")))

# Create the grouped bar chart
barplot(data, beside = TRUE, col = c("lightblue", "lightgreen"),
        xlab = "Group", ylab = "Percentage",
        legend.text = rownames(data))
```
