## Lecture Note Questions
### Lecture 7 Review Quiz
Take 2 minutes with a partner to discuss these questions and I'll call on you

1. Can you change `x` to a different type using `mut`? Using shadowing?
2. What's the largest value a `u8` can hold?
3. What are three different changes you could make so that this compiles?
```rust
let x: i32 = 10;
let y: i16 = 5;
let sum = x + y;
```
4. What's wrong with this? 
```rust
const PI = 3.14
```
### Lecture 8 Review Quiz
Take 2 minutes with a partner to review functions from last lecture:

5. **What's wrong with this function signature?**
```rust
    fn calculate_area(width, height) -> f64 {
```
    
6. **What's wrong with this function?**
    
```rust
fn mystery(x: i32) -> i32 {
	let result = x * 2;
	result + 1;
	}
```
    
7. **How can you fix this so it compiles?**
```rust
let x = 4;
let y = 4.5;
let z = x + y;
println!("{}",z);
```
### Quick Review: Lectures 7-9
**1. Variables & Types (Lecture 7)**
```rust
#![allow(unused)]
fn main() {
let x = 5;
x = 10;  // What happens here?
}
```

1. Works fine
2. Compiler error
3. Runtime error

**2. Functions (Lecture 8)**
``
```rust
fn calculate(a: i32, b: i32) -> i32 {
	a + b;
}
```

What does this function return?

1. The sum of a and b
2. The unit type ()
3. A compiler error

**3. Loops & Arrays (Lecture 9)**

`let arr = [1, 2, 3, 4, 5]; for (index, value) in arr.iter().enumerate() {     if value % 2 == 0 {         ________      }     println!("Index: {}, Value: {}", index, value); }`

What goes in the blank to skip to next iteration without printing?

### Quick Quiz (Lecture 11)

**1. Which `#[derive()]` trait lets you print an enum with `{:?}`?**

**2. Why won't this compile?**

```rust
enum Status {
    Loading,
    Complete,
    Error,
}

let status = Status::Complete;
match status {
    Status::Complete => println!("Finished!"),
    Status::Error => println!("An error has occurred!"),
}
```

**3. What do you think this will print?**

```rust
let result = Some(42);
match result {
    Some(x) if x > 40 => println!("Large: {}", x),
    Some(x) => println!("Small: {}", x),
    None => println!("Nothing"),
}
```

