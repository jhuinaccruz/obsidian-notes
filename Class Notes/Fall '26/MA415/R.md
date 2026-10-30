## Installing Packages
```r
library(package_name)
```
## tidyverse/mdsr
```r
library(tidyverse) #includes data science ggplot2, dplyr, tidyr, etc.
library(mdsr) #useful for following through with the mdsr library
```
## Layered Grammar of Graphics
```r
ggplot(data = <DATA>) + 
  <GEOM_FUNCTION>(
     mapping = aes(<MAPPINGS>),
     stat = <STAT>, 
     position = <POSITION>
  ) +
  <COORDINATE_FUNCTION> +
  <FACET_FUNCTION>
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
	
	color = ..., #colors specifically the outline of plotted items (line, dot)
	color = column, #ggplot2 creates a color vector based on the datapoints in said column
	
	size = n, #increases/decreases the scaling of the graph based on the value of n
	size = column, #ggplot2 assigns sizes based on the relative values of the dataframe

	label = column, #maps text instead of a dot

	x = (reorder(columns...)), #sorts the graph based on the ascending order of the relationship between the columns
	
	fill = ..., #fills geometric objects (line, dots) with specified color(s)
	fill = column, #fills a graph based on the values/breakdown of another column
	
	shape = column, #creates shapes on points based on a column calue
	
	alpha = 0.5, #transparency value
	alpha = column, #maps transparency to values of a graph (recommended to be a categorical rather htan discrete variable)

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
#### `geom_jitter()`
```r
ggplot(...) + 
	geom_jitter() # adds jitter (noise) to points to reduce overplotting
```
### Coordinate Systems
#### `coord_flip()`
```r
coord_flip() #flips the graph sideways
```
#### `ggsave()`
```r
g + ggsave(filename = "save_file_name")
```
### `stat_*`
#### `stat_summary()`
```r
ggplot(...) + 
	stat_summary(
		aes(...),
		fun.min = min, # Lower limit function
		fun = median, # Center/main function
		fun.max = max, # Upper limit function
	)
```
## `dplyr`
```r
library("dplyr")
```
### Main Verbs
#### `select()`
```r
select(data_frame,
	column_1, column_2, ..., #returns a dataframe of only the selected columns
	column_n:column_m, #returns a dataframe of only the columns between n and m (inclusive)
	
	!column_n:column_m, #similar to above, except excludes between n and m (inclusive)
	
	where(...), #selects columns that are is.type
	
	new_column_name = existing_column_name #renames columns
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

#automatically drops missing values
```
#### `mutate()`
```r
mutate(data_frame,
	new_column = ..., #creates a new column in the dataframe
	old_column = ..., #changes the values of an existing columns
	.before = n, #sets the previous n mutates to the left instead of the right
	.keep = "used", #keeps only the created/specified variables in the mutate argument
```
#### `relocate()`
```r
relocate(data_frame,
	columns, ... # moves selected columns to the front
	)
```
#### `...if_else(...%in%...)`
```r
mutate(data_frame,
	column = ifelse(conditional, if_not_value, if_yes_value)) #used to check for specific cases where values should not exist through pattern matching and replacing
```
#### `case_when()`
```r
case_when(
	variable_conditional ~ ... #pattern matching a variable to a result
	...
)
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
group_by(data_frame,
	columns, ... #adds metadata to the dataframe, such that further opreations treat the groups as separate entities within a dataframe, each receiving later operations on a group-by-group basis
	.groups = "drop_last" #when grouping by multiple columns, the last column argument is by default "dropped" as a grouping ("drop_last"); can be set to dropping all ("drop") or none ("keep")

summarize(data_frame, #collapses the dataframe into a single value per grouping
	column_1 = ..., #the following determines which variables (columns) appear in the resulting dataframe
	column_2 = ...,
	.by = column_name, # grouping argument within summarize (use c() for multiple columns)
	all_ = all(condition) #takes all values of a column given condition
	any_ = any(condition) #takes all
	
	)

#note: summarize and group_by are almost always used together
data_frame |>
	group_by(column) |> #results in groups of n
	summarize(...) |> #returns a dataframe with n rows, with m columns as specified in the summarize function
```
##### `ungroup()`
```r
data_frame |>
	ungroup() #undoes all grouping
```
#### Slicing (`slice_head()` / `slice_tail()` / `slice_min()` / `slice_max`/`slice_sample()`)
```r
data_frame |>
	slice_head(n = num) |> # takes the first num-th row from each group
	slice_tail(n = num) |> # takes the last num-th row from each group
	slice_max(col, n = num) |> # takes the num-th largest rows based on col's value
	slice_sample(n = num) #takes num-th random rows
```

#### `distinct()`
```r
data_frame |>
	distinct() |> ## removes duplicate rows
	distinct(column_names, .keep_all = FALSE) |> #returns selected columns with distinct row values; if you want to keep all other non-selected columns, set .keep_all to TRUE
```
#### `count()`
```r
data_frame |>
	count(column_names, sort = TRUE) # groups by distinct values and counts occurrences, sorted in descending order (if sort = TRUE)
```
#### `glimpse()`
```r
glimpse(flights) # displays important tibble metadata such as number of rows, columns etc.
```
#### `near()`
```r
near(x, y) #approximation instead of ==, especially for floating numbers
```
#### Joins
```r
data_frame |>
	left_join( #could also be a right_join, inner_join, full_join, anti_join, semi_join
		data_frame_2,
		by = condition, #creates a conditional join
		by = c("left" = "right") #can also use a named vector for a conditional join
	)
	
#cross join (Cartesian Product)
data_frame |>
	cross_join(data_frame)
```
### `pivot_*()`
```r
pivot_longer(
	c(...), # column names that need to be pivoted down and leftwards (strings)
	names_to = col,  # changes column name to a single row named col (string)
	values_to = col_2) #changes the resulting values to another row called col_2
	
pivot_wider(
	... #similar to pivot_longer, but instead needed when observations are spread over two rows
	)

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

#can also be used as an argument in functions (such as groupings) to ignore missing values
```

### `n()/n_distinct()`
```r
summarize(
	column_name = n() #helper function used in aggregator functions to compute aggregated counts
	column_name = n_distinct(column) #similar to n() except it counts only unique values of columns
)
```
## Commenting
```r
# comments can be single lined
```