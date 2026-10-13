## Installing Packages
```r
library(package_name)
```
## tidyverse/mdsr
```r
library(tidyverse) #includes data science ggplot2, dplyr, tidyr, etc.
library(mdsr) #useful for following through with the mdsr library
```
## `ggplot2`
```r
#creates a plot object
g <- ggplot(
	data = dataframe_name,
	mapping = ..., #specify dataframe columns to visual plot properties (global)
	)

ggplot(data = ...) + 
	some_geom_function(mapping = aes(...), ...) #general template for ggplot objects
```
### `aes()`
```r
# specifies aesthetics to the ggplot object
ggplot(data, aes(...)

# many aesthetics can be specified, such as

aes(
	x = ..., y = ..., #x and y values (columns of data) (positional syntax)
	x = reorder(x_col, y_col), #reorders the x_col based on the values of y
	
	mapping(...), #local mapping of columns to visuals
	
	color = column, #ggplot2 creates a color vector based on the datapoints in said column
	
	size = n, #increases/decreases the scaling of the graph based on the value of n
	size = column, #ggplot2 assigns sizes based on the relative values of the dataframe

	label = column, #maps text instead of a dot

	x = (reorder(columns...)), #sorts the graph based on the ascending order of the relationship between the columns
	
	fill = column, #fills a graph based on the values/breakdown of another column
	
	shape = column, #fills

)
```
### `coord_trans()`
```r
g + coord_transform(scaling_system) #changes the scaling system (defaults to linear)
```
### `scale_y_continuous()`
```r
g + scale_y_continuous(
	name = column,
	trans = scaling_system,
	labels = scales::format #formats the label based on the scales package
	)
```
### Facets (`facet_wrap()`)
```r
g + facet_swap(
	~columns,
	nrow = ..., #determines the number of subgraphs
	ncol = ... #similar to nrows, subdivisions occur top-down rather than left-right
	)
```
### `geom_*`
#### Univariate Displays
##### `geom_histogram()`
```r
g + geom_histogram(
	binwidth = px_val, #determines bar width
)
```
##### `geom_density()`
```r
g + geom_density(
	adjust = val, #determines the line's smoothness (< 1 being more jagged, > 1 being smoother, defaults to 1)
	linewidth = val,
	alpha = val_decimal, #fills in the curve formed by the line (0 being filled, 1 being transparent, defaults to 1)
	)
```
##### `geom_col()`
```r
g + geom_col(...) #similar to geom_bar, except it does not plot stats
```
##### `geom_bar()`
```r
g + geom_bar(...) #similar to geom_col, with computed stats of count (height)
```
#### Multivariate Displays
##### `geom_point()`
```r
g + geom_point( #
)
```
##### `geom_smooth()`
```r
g + geom_smooth(
	method = regression_model
)
```
##### `geom_boxplot()`
```r
g + geom_boxplot( #creates a boxplot
	...
)
```
##### `geom_mosaic()`
```r
g + geom_mosaic()
```
### Miscellaneous
#### `theme()`
```r
g + theme(
	... #finish
)
```
#### `labs()`
```r
g + labs(
	title = "Title string", #title of the plot
	
	subtitle = "Subtitle string",
	
	x = "x-axis labeling", y = "y-axis labeling",
	
	color = "Color Legend Title", shape = "Shape Legend Title",
	)
```
#### `head()`
```r
head(...) #displays only the first 10 values of a graph
```
#### `coord_flip()`
```r
coord_flip() #flips the graph sideways
```
#### `ggsave()`
```r
g + ggsave(filename = "save_file_name")
```
## `dplyr`
```r
library("dplyr")
```
### Main Verbs
#### `select()`
```r
select(data_frame, column_1, column_2,...) #returns a dataframe of only the selected cols
```
##### Helper Functions (`starts_with()`, `ends_with()`, `contains()`, `num_range()`, `between()`)
```r
select(data_frame,
	starts_with("..."), #matches values starting with ...
	ends_with("..."), #matches values ending with...
	contains(""), #matches values that contain ...
	num_range(column_name, n1:n2) #matches values in column_name's n1 through n2
)
```

#### `filter()`
```r
filter(data_frame, conditional) #retuns a dataframe of only the specified rows based on the conditional
```
#### `mutate()`
```r
mutate(data_frame, new_column = ...) #creates a new column in the dataframe

mutate(data_frame, old_column = ...) #changes the values of an existing columns
```
#### `...if_else(...%in%...)`
```r
mutate(data_frame, column = ifelse(column %in% vector, if_not_value, if_yes_value)) #used to check for specific cases where values should not exist through pattern matching and replacing
```
#### `rename()`
```r
rename(data_frame, column = ...) #renames an existing column
```
#### `arrange()`
```r
arrange(data_frame, desc(column_1), column_2, column_3, ...) #sorts a dataframe based on the values in column_1, using the other columns specified as tiebreaks

#note: can also use asc(...) as a way to arrange in ascending order
```
#### `summarize()`/ `group_by()`
```r
summarize(data_frame, #collapses the dataframe into a single value
	column_1 = ..., #the following determines which variables (columns) appear in the resulting dataframe
	column_2 = ...,
	...
	
	)

group_by(data_frame, column) #adds metadata to the dataframe, such that further opreations treat the groups as separate entities within a dataframe, each receiving later operations on a group-by-group basis

#note: summarize and group_by are almost always used together

data_frame |>
	group_by(column) |> #results in groups of n
	summarize(...) |> #returns a dataframe with n rows, with m columns as specified in the summarize function
```
## `forcats`
```r
install.packages(forcats)
```
## `ggthemes`
```r
library(ggthemes) #offers a colorblind-safe pallete(s)
```
## Nesting and Pipe-Forwarding
```r
select(
	filter(
		mutate(
			... #hard to read, not recommended
		)
	)
)
```

```r
data_frame |>
	select(...) |>
	filter(...) |>
	mutate(...) #better form of chaining long expressions; more readable
```
## Basic Operations
### Arithmetic
```r
1 + 1 #addition
1 - 1 #subtraction
2 * 1 #multiplication
4 / 2 #division

sin(pi / 2) #sin/cos/tan/etc. (output in radians)

5 %/% 3 #integer division (no remainder/decimals)
5 %% 3 #modulo
```
### Descriptive Statistics
```r
mean(...)
mean(vector < n) #filters values within the function

sum(...)

min(...)

max(...)

#cumulators
cummean(...) #returns the values of the mean as they increase

cumsum(...)

cummin(...)

cummax(...)

```
### Object Assignment
```r
object_name <- ... #assigns object to a variable
```
### Vectors
```r
vector_name <- c(...)

#can also perform basic arithmetic on vectors

```
## Miscellanous
### `help()`/`?`
```r
help(mpg)
?mpg #provides documentation for given dataset/function/library
```
### `is.na()`
```r
is.na(...) #evaluates the argument passed as to whether it contains/is an NA value(s)
```
### `na.rm`
```r
function_name(na.rm = TRUE) #default argument for most functions, gives an "impossible" value to column value with NA values
```

### `n()/n_distinct()`
```r
summarize(
	column_name = n() #helper function used in aggregator functions to compute aggregated counts
	column_name = n_distinct(column) #similar to n() except it counts only unique values of columns
)
```