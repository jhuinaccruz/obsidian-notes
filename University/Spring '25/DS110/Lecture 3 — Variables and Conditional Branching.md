>[!abstract]
>- *Variables store values for later*
>- *Conditional branching allows the program to behave differently under different conditions*
## Variables
```run-python
two_to_the_eighth = 2 ++ 8
print(two_to_the_eighth)
```

__Variable__: stores the value assigned to it

>[!important]
>*The stored value is remembered across code boxes*

To make a new variable, introduce a new word (__identifier__) on the left side of an assignment
```run-python
pay_per_hour = 20

hours = 40

total_pay = pay_per_hour * hours

print(total_pay)
```
>[!important]
>Variable names are case-sensitive (capitalization is important)

>[!important]
>Python uses snake_case for its variable names

```
## Comparisons
```run-python
city = input('What city are we in? ')

print(city == 'Boston')
```
>[!warning]
>*Equality generally cares about type, although the int 4 and the float 4.0 are considered equal*

```run-python
print(1 < 1)

print(1 > 1)

print(1 != 1)

print(1 <= 1)

print(1 >= 1)
```
>[!important]
>*Strings are compared in an order that is alphabetical if the strings are all lowercase letters, their order is complicated with more characters*

```run-python
print('aardvark' < 'zebra')
print('capitalized' == 'Capitalized')
```

## Conditional Branching
```run-python
value = int(input('Enter an integer:'))

if value < 0:
	print('Negative')
else:
	print('Positive')

print('Done')
```

```run-python
password = input('Enter the password: ')

if password == '1234':
	print('Correct!')
	print('Your account has $1000000 in it.')
else:
	print('Incorrect.')
	print('Have a nice day.')
```
>[!important]
>*"Else" and its suite are actually optional. If you just have a lone "if", its suite happens if the condition is true, and regardless, the execution continues after the suite.*

```run-python
language = input('What is your favorite language? ')

if language == 'Python':
	print('Mine too!')
print('But there sure are a lot of languages out there....')
```

>Elif is for cases where one wants to account for multiple conditions

```run-python
value = int(input('Enter an integer between 0 and 100: '))
if value < 0:
    print('No negative numbers!')
elif value > 100:
    print('That value is too large!')
elif value == 42:
    print('That was the number I was thinking of!')
else:
    print('Guess again.')
```

>[!important]
>*An elif only triggers if all the previous if and elif conditions evaluated to False (and its condition evaluates to True).*

## Review Problem

### Original Code
```run-python
num1 = int(input('First number: '))
num2 = int(input('Second number: '))
num3 = int(input('Third number: '))
my_max = max(num1, num2, num3)
my_min = min(num1, num2, num3)
my_mean = (num1+num2+num3)/3  # Note importance of parens!

print('Min: ' + str(my_min))
print('Max: ' + str(my_max))
print('Mean: ' + str(my_mean))

if num1 == num2:
    print(str(num1) + ' was repeated')
elif num2 == num3:
    print(str(num2) + ' was repeated')
elif num1 == num3:
    print(str(num3) + ' was repeated')
else:
    print('The numbers were unique')
# Note:  if all 3 are the same, is that handled correctly?
```
