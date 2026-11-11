>[!abstract]
>- We dissect a very small program that prints *Hello, world!*
>- We discuss expressions and statements, the building blocks for programs

## Analyzing a First Program
```run-python
print('Hello, world!')
```

__Interpreter__: The program that interprets and executes code.

__Statement__: A single line of a program

>[!note]
>*Given multiple statements, the interpreter executes them one at a time from top to bottom*

```run-python
print('Hello 1')

print('Hello 2')

print('Hello 3')
```

__String__: Text that appears in quotations marks ("" or '')

```run-python
print('Hello, world!')
```

>[!important]
>To comment, use a hashtag (#) before the text and/or statement(s)

__Expression__: A piece of code that evaluates something

*When expressions are acted on by operators, they're called operands*

```run-python
print(1) # Technically an expression

print(1+2) # Two operands and an operator make an expression

print(10*(10+1)) # The expression (10+1) acting as an operand
```

## Types
```run-python
1.00000000000000001 - 1
```

There are four main types of data in Python:
- __int__
- __float__
- __str__
- __bool__
```python
type() # returns the type of a value as "<class 'type'>"
```

>[!important]
>*The imprecision we saw earlier is caused by the fact that computers represent numbers in **binary**, bits that indicate which powers of two to sum.  Powers of 2 can sum to any integer, but some fractions, like 1/10, can only be represented as infinite sums of fractional powers of two (1/2, 1/4, ...), so their representation is an approximation.  (Exact computations can use the Decimal type to avoid this, but Decimal is slower and not used as often.)*

```run-python
0.1 + 0.1 + 0.1
```

To __concatenate__, you must input two of the same kind
```run-python
'Hello' + 'World' + '1' + '0.1'
```

You can also type cast using type() to force a value to a different type
```python
int()
str()
float()
bool()
```
