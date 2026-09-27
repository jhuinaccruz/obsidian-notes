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
g <- ggplot(data = dataframe_name, ...)
```
### `aes()`
```r
# specifies aesthetics to the ggplot object
ggplot(data, aes(...)

# many aesthetics can be specified, such as

aes(x = ..., y = ...) #x and y values (columns of the data)

aes(x = reorder(x_col, y_col) ...) #reorders the x_col based on the values of y

aes(color = column) #ggplot2 creates a color vector based on the datapoints in said column

aes(size = n) #increases/decreases the scaling of the graph based on the value of n
aes(size = column) #ggplot2 assigns sizes based on the relative values of the dataframe

aes(label = column) #maps text instead of a dot

aes(x = (reorder(columns...))) #sorts the graph based on the ascending order of the relationship between the columns
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
### Canonical Data Graphics
#### Univariate Displays
##### `geom_histogram()`
```r
g + geom_histogram(
	binwidth = px_val,
)
```
##### `geom_density()`
```r
g + geom_density(
	adjust = val, #determines the line's smoothness (< 1 being more jagged, > 1 being smoother, defaults to 1)
	)
```

##### `geom_col()`
```

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
```
#### `head()`
```r
head(...) #displays only the first 10 values of a graph
```
