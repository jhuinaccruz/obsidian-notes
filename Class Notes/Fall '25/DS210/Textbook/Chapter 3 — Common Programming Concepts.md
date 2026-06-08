## 3.1

__By default, variables are__: Immutable

__Immutable__: Unchangeable once bounded to a name

__Constants__: Similar to immutable variables, they are unchangeable
- Unlike immutable variables:
	- Type must be annotated
	- Has no fixed address
	- Evaluated at compiling
	- is more adjacent to a literal than a variable

__Shadowing__: Allows for the declaration of a new variable with the same name as a previous one, where the new declaration replaces ("shadows") the old one
## 3.2

__Statically Typed Language__: Must know the types of all variables at compilation

### Scalar Types
__Scalar Type__: Representing a single value. Rust's primary scalar types include
- Integers (default to i32)
- Floating-point numbers (defaults to f64)
- Booleans
- Characters

__Integers__: A number without a fractional component, can be denoted as either `U..`(unsigned) or `i..`(signed), indicating whether it can be negative or not

$$
{-(2^{n-1})}≤isize≤2^{n-1}
$$

$$
{0≤usize≤2^{n}-1}
$$
where:
- n = bit size
- isize/usize = size of signed/unsigned numbers of n bits

__Float__: A number with a fractional component, denoted as either `f32` or `f64`

__Boolean__: True or false

__Character__: Rust's most primitive alphabetic type, denoted as `char`, defined by singular quotes, with a size of four bytes

### Compound Types
__Compound Type__: Used to group multiple values into a single type. Rust's most basic compound types:
- Tuples
- Array

__Tuple__: A way of grouping together a variety of types into one, having a fixed length once declared, denoted by parenthesis around

__Unit__: A place holder, returned when no value is present

__Array__: A collection of multiple values of the same type, fixed in length once declared, denoted by brackets around the values

__Vector__: A collection of multiple values that can change in length once declared

## 3.3
__Function__: Denoted by the `fn` keyword, uses snake_case as the convention for function names

__In function signatures, you *must*__: Declare the type of each parameter

__In functions__:
- You can declare return with `return`, or simply omit the usual semicolon
## 3.4
>*All programmers strive to make their code easy to understand, but sometimes extra explanation is warranted. In these cases, programmers leave comments in their source code that the compiler will ignore but people reading the source code may find useful.*
### 3.5
__Control Flow__: Most commonly through `if` and loops

__If Expression__: Allows for control through conditionals (booleans)

__Loop__: Repeats a block of code more than once. Rust's loops include
- `loop`
- `while`
- `for`

__Loop Labels__: Used to differentiate nested loops, denoted by a single unclosed quote `'`

__While Loop__: Used to loop until a certain conditional evaluates to false

__For Loop__: Used to loop over a collection of items