>*Python documentation strings (or docstrings) provide a convenient way of associating documentation with Python modules, functions, classes, and methods. It's used in source code that is used, like a comment, to document a specific segment of code.*[^1]

## Declaration
Docstrings are declared with triple single or double quotes below the class, method, or function declaration

>[!important]
>*All functions should have a docstring*[^1]

## Conventions
A docstring should:
- Begin with a capital letter
- End with a period
- Contain a short description within its first line
	- If there are more lines in the docstring, the second line should be blank to separate the summary from the rest of the description
- The following lines should be one or more paragraphs describing the objects:
	- calling conventions
	- side effects, etc.

```python
def my_function():
    '''Demonstrates triple double quotes
    docstrings and does nothing really.'''
 
    return None

print("Using __doc__:")
print(my_function.__doc__)

print("Using help:")
help(my_function)

#code from fn1
```
### Google-Style
>*Google style docstrings follow a specfiic format and are inspired by Google's documentation style guide. They provide a structured way to document Python code, including parameters, return values, and descriptions*

```python
def function_name(a, b, ...):
	"""
	Docstring summary...

	Args:
		a (type): (describe the meaning of argument A)
		...

	Returns:
		(type): (describe what the function)
```



[^1]: https://www.geeksforgeeks.org/python-docstrings/
