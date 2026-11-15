## Formatted Strings
F-strings (formatted strings): A string where f precedes the string, and an expression precedes the variable name

__Delimiter__: A sequence of one or more characters for specifying the boundary between separate, independent regions in plain text
### Escape Characters

__\n__: newline

__\t__: tab

\\\\: \

__\s__: whitespace

__\w__: any alphanumeric character

__\d__: any digit

## DataFrames and String Operations
>*DataFrames have great integration with the Python string methods. You can call a string function and have it automatically applied to every item in the same column. You just need to access the .str attribute*

>*DataFrames are also well-integrated with regular expression matching*
## Regular Expressions
>*Regular expressions search for patterns in your data.*

__Escape Sequences__: Represent whole categories of symbol:
- \\d: any digit
- \\s: whitespace
- \\w: any alphanumeric character
- \*: Matches zero or more characters
- +: Matches one or more characters
- ?: an unknown character that may be there or not
- |: Allows the regular expression to accept this or that