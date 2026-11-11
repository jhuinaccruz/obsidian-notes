## Variable Assignment
```run-r
#variable names can be uppercase, lowercase, and cannot include hashes, spaces, and/or start with anything other than a letter/period

my_variable <- "blah blah blah"
print(my_variable)
```

## Printing Variables
```r
print(my_variable)
```
## Data Types

- Numeric
- Character
- Logical
- Factoral

## Vectors

### Making a Vector
```r
#takes x arguments, puts it into the function
my_vector <- c(argument_1, argument_2, ...)
```

#### Making Sequences
```r
#takes two numbers, x and y, and makes a vector sequence from x to y in increments of 1
my_sequence <- 1:10
# 1,2,3,4,5,6,7,8,9,10

#takes at most three arguments, x y and z, and creates a vector sequence from x to y, in increments of z
my_sequence <- seq(1, 10, by = 1)
# 1,2,3,4,5,6,7,8,9,10
```

### Replication
```r
#takes at most four arguments, a, b, c, d and replicates a, b number of times, outputting a vector of c length, repeating each element in (a) d times
my_vector <- rep(1:3, times = 3, length.out = 18, each = 2)
#1,1,2,2,3,3,1,1,2,2,3,3,1,1,2,2,3,3
```

### Subsetting

```run-r
#you can take specific elements from a vector using brackets
my_vector <- 1:10
my_vector[c(1,5,10)]
##1, 5, 10

#you can also take specific elements from a vector using logical operators
my_vector <- 1:10
my_vector[my_vector > 5]
# 6, 7, 8, 9, 10
```

### Named Vectors

```r
my_vector <- c(a = 1, b = 2, c = 3)

#to retrieve vector from 
```
## Character Functions

### Concatenation

```r
#takes in at most three arguments, x y and z, and returns a string separated by z
my_string <- paste("i", "love", sep = " ")
#"i love"

# takes in at most two arguments, x and y, and returns a string without a separator
my_string <- paste0("i", "love")
#"ilove"
```

## Logical Operators

__&__: and
__|__: or
__!__: not

## Type Coercion

```r
#takes in vector x, returns its type
typeof("paper")
#character

#takes in vector x, forces it to be a specific type, returns vector of said new type

as.{type}(x)

as.integer("paper")
```

## Importing Packages

>[!info]
>Packages are collections of function, data, and compiled code that extend R's functionality for specific tasks such as data manipulation and visualization.

### Installing and Loading Packages
```r
#takes in the name of the package and installs it
install.packages(dplyr)

#takes in the name of a package and loads it
library(dplyr)

```

## Data Frames

### Making a Data Frame
```r
#using vectors x y z
my_data <- data.frame(x,y,z,...)

#using .csv files

my_data <- read.csv("filename.csv")
```

### Inspecting a Data Frame

```r
#display the first 6 rows of data
head(my_data)

#display the last 6 rows of data
tail(my_data)

#return the names of the columns of the data set
names(my_data)

#returns a summarized view of the data
glimpse(my_data)

#returns the dimensions of the data
dim(my_data)

#returns the dunmber of rows/columns in a data respectively
nrow(my_data), ncol(my_data)

#returns a summary of each variable based on the type of the variable
summary(my_data)
```

### Selecting and Subsetting a Data Frame

```r
#use the $ operator if the variables have names
my_data$names

#use brackets to subset using brackets (data[row, column])
my_data[1,2]
#alternately, you can use to brackets as (data[row/column, row/column name])
my_data[1, names]
```

### Working with package(dplyr)

```r
#takes a subset of columns
select(names)

#takes a subset of rows 
filter()

mutate()

arrange()
```

## Bar Chart

```r
#makes a bar chart
barplot()
```

### Transposing a Chart (switching axes)
```r
#takes in data frame, switches the x- and y-axes
t(my_data)
```

### Customizing a Bar Chart
```r
#makes a bar chart and takes in the following
barplot(
	#a vector representing the value of each bar
	heights = c(1,2,3,4,5)

	#a vector of labels for the x-axis
	names.arg = c("A", "B", "C", "D", "E")

	#the name of the bar chart
	main = "name"

	#labels for the x- and y- axis respectively
	xlab =  "letters"
	ylab = "numbers"

	#colors for the bars
	col = c("red", "blue", "green", "yellow", "orange")

	#boolean that ensures the bars are either stacked (false) or grouped (true)
	beside = false #stacked
	beside = true #grouped
	

	#the following are additional and not always necessary

	#a vector of length two that adjusts the limits of the y-axis
	ylim <- c(0, 10)
)
```

## Pie Chart

```r
#makes a pie chart
pie()
```

### Customizing a Pie Chart
```r
pie(
	#takes in a vector of values
	my_vector
	
	#vector of names (labels) for the chart
	labels <- c("A", "B")
	
	#colors for the bars
	col <- c("red", "blue")

	#string for the main title/naming of the chart
	main <- "name"
	)
```

## Descriptive Statistics

### Central Tendency
```r
#takes in a vector and outputs the average of the numeric values
mean(my_vector)

#takes in a vector and outputs the median value of the numeric values
median(my_vector)

#method for finding the numeric value of the mode
as.numeric(names(table(my_data$specific_variable)[which.max(my_data$specific_variable)])
```

### Variability
```r
#takes in a vector, outputs the variance of said vector
var(my_vector)

#or calculate using the formula
bfi_f = bfi_n[bfi_n$gender=="F"]  # Create a subset of the dataset
sum((bfi_f$age - mean(bfi_f$age))^2) / (nrow(bfi_f) - 1)


#takes in a vector, outputs the standard deviation
sd(my_vector)
sqrt(sum((my_vector - mean(my_vector))^2) / (nrow(my_data) - 1))

#

#takes in a vector, outputs the interquartile range
IQR(my_vector)

#or, manually calculate it
quantile(my_vector, .75) - quantile(my_vector, .25)
```

### Shape
```r
#takes in a vector, outputs the skewness
skew(my_vector)

#takes in a vector, outputs the kurtosis
kurtosi(my_vector)

```