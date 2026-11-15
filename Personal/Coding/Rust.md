```rust
fn function_name(Parameter_1: Type, Parameter_2, Type_2...) -> Return_Type {
	//body
}
//if no return type is specified and there is no return value specified, the unit type will instead be returned (an empty tuple that takes no memory)
```

```bash
rustc filename.rs

./main
```
## Libraries/Crates
```rust
use library::sublibrary
```
### std
```rust
use std
```
#### io
```rust
use std::io
use std::io::{BufRead, Bufreader}; //for iteratively reading files
```
#### Filesystem
```rust
use std::fs //for reading files
use std::fs::File;
```
#### rand
```
```
#### VecDeque
```rust
use std::collections::VecDeque;
```
#### BinaryHeap
```rust
use std::collection::BinaryHeap;
```
### PyO3
```shell
cargo add pyo3 --features extension-module
```

```rust
use pyo3::prelude::*; //for integration of Python and Rust
```
### maturin
### Rayon
```toml
[dependencies]
rayon = "1.7"
```

```rust
use rayon::prelude::*

let parallel_iterator = data.par_iter(); 
//functionally similar to .iter(), but with rust parallelism
```
## Variables
```rust
let variable_name = value //creates an immutable variable

let mut variable_name = value //creates a mutable character
```
## Constants
```rust
const variable_name: type_name = value //creates a constant with annotation
```
## Input/Output
```rust
println!(string) //prints the string

println!("Words {variable_name}") //where the brackets are a placeholder for a variable
println!("Word(s) {}... {}", variable_1, variable_2) // similar to the above, except it replaces the placeholder brackets with the listed variables separated by commas, in the order by which they appear
```

```rust
io::stdin()
	.read_line(&mut guess)
```
## Types
### Scalar
```rust
//Integers
let a: u64 = 1
let b: i64 = -1

//Floating Integers
let c: f32 = 1.0

//Booleans
let d: bool = true

//Characters
let e: char = 'P'
```

### Compound
```rust
//Tuples
let a: (type_1, type_2...) = (_,_,...)
let (var_1, var_2,...) = a //Pattern matching

let a.index_value = value_at_index


//Array
let b: [type: num_of_values] = [val_1, val_2, ...] //creates an array of values of type of length num_of_values
let c: [val, num_of_values] = [val, val, ...] //creates an array of val of size num_of_values

let x = b[index] //indexing starts at 0
```
### Unit
```rust
let a = () //Unit Type
```
### String
```rust
let s = String::from("word");
```
###
### enum (Enumeration)
###
## Comments
```rust
// creates a single comment

/*
creates multiple-line comments
*/

///Creates a docstring
```
## If-else
```rust
if condition {
	...
}
else if {
	...
}
else {

}

let value = if condition {value_1} else {value_2} //Assign value from if-else
```
## Loops
```rust
loop {
	...
	break //breaks the loop at this point
}

'loop_label: loop {
	...
	break `loop_label
	continue `loop_label
	}

let a = loop {
	...
	break expression; // returns a value defined by the expression
}
```
### While
```rust
while conditional {
	...
}
```
### For
```rust
for element in elements {
	...	
}

for element in (start..end) //non-inclusive

for element in (start..=end) //inclusive

for element in (start..end).rev() //reverses the order

for element in (start..end)/step_by(step)

for (index, &value) in fruits.iter().enumerate() //enumerates when the index and value is both needed 
```
## Arrays
```rust
let arr: [type, length] = [...]
let arr2 = [value: length] //creates an array of length "length", where each element is "value"

arr.len() //returns the length of the array

arr.sort() //returns the original array sorted

arr.contains(&val) //returns a boolean based on whether the value can be found in the array
```
## Vectors
```rust
let mut vector = Vec::new(); //Empty vector
let mut vector = Vec![...]; //Vector with data
let mut vector = Vec<String> = Vec::new(); //Empty with type annotation

numbers.push(value) //adds element
numbers.pop() //removes last element

numbers.len() //returns the length of the vector

numbers[index] //access elements at number, returns a copy to said value

let mut vector = Vec::with_capacity(n) // reserves space for n elements
```
## Box
```rust
let box = Box::new([0; 10_000_000]);
```
## Enums
```rust
//#[derive(Debug)] //used to display a non-pre-existing nenum type
//#[derive(PartialEq)] // used to compare enum values for equality
enum enum_name {
	variant_1(type),
	variant_2...
	}
	
use enum_name::* //can onny be used when the enum is in a different file

let val_1 = enum_name::variant_1(...)
let val_2 = variant_2(...)
```
### Option\<T>
```rust
//Defined in the standard library as:
enum Option<T> {
	None,
	Some(T),
	}
	
fn ...(var: Option<T>) -> ...{
	let ... = var? //unwraps the Option variable, immediately returns none if var is None
	
match var {
	Some(value) => ...,
	None => ...,
	}
	
var.unwrap() //unwraps an Option, panics if var is None
var.is_some() //Returns True if is Some(T)
var.is_none() //Returns True if is None

var.expect(message) //Similar to unwrap, except it returns a message if it is None after panicking
var.unwrap_or(default_value:T) //returns default value if None
```
### Result\<T, E>
```rust
enum Result<T, E> {
	Ok(T),
	Err(E),
	}
```
#### panic!
```rust
panic!("Panic message")
```
###
## Pattern Matching
```rust
match expression_or_variable {
	pattern_1 => statement,
	...
	_ => statement, //must go last
}
```

## Strings
```rust
let mut s = String::from("word"); //creates a mutable string

s.push_str("..."); //appends a literal to a String
s = s + "..." //would change ownership if the first s was something else
let s = format!("{}...", s);


let dot1 = &s[0..1] //creates a slice from index a to index b, such that it creates a fat pointer on the stack to a part of a String in the heap

let dot2 = ".." // string literals are also string slices
```
## Characters
```rust
let c: char = 'e';

let s: String = c.to_string();

let char: Vec<char> = vec!['a', 'c'];

let s: String = char.iter().collect(); //turns a collection of characters into a String
```
## HashMap
```rust
use std::collections::HashMap;

let mut dictionary = HashMap::new();
dictionary.insert(key, value);

match dictionary.get(key) { //.get() returns an Option
	Some(x) => ...,
	None => ...,
};

dictionary.contains_key(key) //returns a boolean

dictionary.entry(key).or_insert(value)
```
## HashSet
```rust
let set = vector_of_type_T.iter().cloned().collect(); //keeps original vector
let set = numbers.into_iter().collect(); //consumes the vector
```
## Structs
```rust
struct Object {
	attribute1; type,
	attribute2: ...
	...
}
struct Tuple_Struct(T, T, T); //Has field safety without needing named fields

let object1 = Object {
	attribute1 = value,
	attribute2 = ...
	...
};

let object2 = Object {
	..object1 // words as long as the copied fields are Copy types, otherwise use object1.clone()
}

object1.attribute1 = new_value;

match object1 {
	Object {attribute1, ..} => *attribute,
	}
```
## Methods
```rust
impl Struct_Name {
	fn ...(&self) {
	} // using method syntax
}
```
## Generics
```rust
fn function_name<T, ...>(...) -> T {
	... // T is used as a generic type
}

struct struct_name<T, ...> {

}

impl<T, ...> struct_name<T, ...> {...}
impl Struct_name<Specific Type> {...}
```
## Traits
```rust
pub trait Trait_Name {
	fn trait_behavior(&self) -> T;
	fn default_trait_behavior(&self) -> T {
		...
	}
}

impl Trait_Name for Struct_Name {
	fn trait_behavior(&self) -> T {
		...
	}
	fn trait_as_parameter(item: &impl trait_behavior + ...) {
		...
	}
}

fn some_function<T: Trait + ...>(t: &T) -> T {
	...
}
fn some_function<T> (t: &T) -> T 
where
	T: Trait + ...,
{
	...
}

pub fn some_function<T: Trait_Name>(...) {
	...
}

pub fn some_function(item1: &impl Trait_Name,...) {
	...
}

trait Supertrait: Trait_Name {
	//can use Trait_Name methods as well
}
```
### \#Derive()
```rust
#[derive(...)] //A macro that auto-generates trait implementation
```
## Lifetimes
```rust
'a type // a reference with explicit lifetime 'a
&'a mut type //a mutable reference with explicit lifetime 'a
```
## Namespaces
```rust
mod namespace_name {
	code...
	}
	
mod module_hierarchy {
	mod nested_submodule{
		fn method1() ...
		...
	}
}
	
fn main(){
	namespace__name::process(); //runs the code in the namespace block
	module_hierarchy::nested_submodule::method1();
}

```
## Paths
```rust
crate::namespace_name::nested_submodule::method(); //absolute path

super::namespace_name::method() //relative path

use namespace_name::nested_submodule //bring something into scope

```
## Importing Files as Modules
```rust
mod file_name_minus_.rs //within the same package as the current
```
## Crates
```shell
cargo new program_name #creating a package as a binary crate

cargo new --lib library_name #creating a package as a library crate
```
### External Crates
Edit `Cargo.toml` file to add the crate and crate version under `[dependencies]`:
```toml
[dependencies]
crate_name = "crate_version"
```
...or use a shell command:
```shell
cargo add crate_name
```
## Testing
```rust
#[test] //typically live in a tests module at the bottom of the file
#[cfg(tests)] //only compiles test when running cargo test
#[should_panic(expected = "panic_message")]
fn test_function() {
	...
	//testing macros that panic if the assertion fails
	assert!(boolean_condition); //checks if something is true
	assert_eq!(left, right); //checks for equality
	assert_eq!(left, right); //checks for non-equality
	
	//adding an additinoal argument for each of these macros that
	//give an additional custom error message
}
```

```shell
cargo test #runs the test_function because it has the test attribute
```

## Closures
```rust
let closure = |parameters| expression //can have no parameters, and can have multiple statements/expressions
let closure_1 = || expression;
let closure_2 = |parameter_1, parameter_2| {
	statement_1;
	statement_2;
	}
```
## Iterators
```rust
let iterator = iterative_structure.iter(); //makes a "list" of references
//structure must have implemented the Iterator trait

//Turbofish syntax for telling the compiler what type you want the chain of methods to return
iterator.methods...(arguments...)::<Type>();
```
### Methods
#### `.map()`
```rust
iterator.map(closure); //maps a closure onto every value of the iterative structure
```
#### `.filter()`
```rust
iterator.filter(boolean_closure); //filters elements out based on the resulting boolean
//said closure works with references rather than booleans
```
#### `.collect()`
```rust
iterator.collect(); //turns iterator back into its original form
```
#### `.copied()`
```rust
iterator.copied(); //converts into an iterator without the references
//only works for iterator Copy types
```
#### `.cloned()`
```rust
iterator.cloned(); //similar to copied, but for iterator Clone types
```
#### `.sum()`
```rust
iterator.sum(); //iterates through the iterator and returns the types as a single sum of whatever it is
```
#### `.product()`
```rust
iterator.product(); //iterates through the iterator and returns the the product of whatever the type is
```
#### `.max()`
```rust
iterator.max(); //returns an Option of a maximum value within the iterator collection
```
#### `.min()`
```rust
iterator.min(); //returns an option of the minimum value within the iterator collection
```
#### `.count()`
```rust
iterator.count(); //returns the number of items in the iterator collection
```
#### `.find()`
```rust
iterator.find(boolean_closure);
//returns an Option of the first appearing match based on the closure's parameters
```
#### `.fold()`
```rust
iterator.fold(closure);
//returns the cumulative result based on the operations defined by the closure, similar to a summation method of sorts
```
#### `.any()`
```rust
iterator.any(boolean_closure); //returns if any items in the iterative collection matches the boolean closure
```
#### `.all()`
```rust
iterator.all(boolean_closure); //similar to any, but only returns if all the items match the closure
```
#### `.take()`
```rust
iterator.take(n); //takes the first n values in the collection in ascending index order
```
#### `.skip()`
```rust
iterator.skip(n); //skips the first n values in the collection in ascending index order
```
## File I/O
#### Reading
```rust
use std::fs

let file_content = fs::read_to_string(relative_path_filename)
	.expect("Error message"); //returns an option, None if file doesn't exist
	

```
#### Writing
```rust
fs::write(target_filename, data)
	.expect("Error message");
```
### Iteratively Reading (BufReader)
```rust
use std::io::{BufRead, BufReader};

let file = File::open(relative_path_filename).expect("Error message");

let reader = BufReader::new(file); //reads chunks from disk into RAM, ready for deployment into the program

for line in reader.lines() { //essentially creates an iterator
	let line' = line.expect("Error message");
}
```
## NDArrray
```toml
[dependencies]
ndarray = "0.15"
```

```rust
use ndarray::prelude::*

let array = array![...];
```
## Stack
```rust
let mut stack = Vec::new(); //Vectors already work as a stack
```
## Queue
```rust
let mut queue = Vec::new(); //Functionally works like a Queue, except removing an item takes O(n) time

use std::collections::VecDeque;

let queue: VecDecDeque<i32> = VecDeque::new(); //Double ended queue, fixes the issue of removing items from the front as an array with front and back pointers
```
## BinaryHeap
```rust
use std::collections::BinaryHeap;

let mut heap = BinaryHeap::new();
let mut heap = BinaryHeap::from(collection); //creates a heap
```
### Methods
#### `.push()`
```rust
heap.push(value); //adds value to the push in O(n)
```
#### `.peek()`
```rust
heap.peek(); // returns an Option array representation of the heap
```
## B-Tree
```rust
use std::collections::BTreeSet;
use std::collections::BTreeMap;

let mut btree = BTreeSet::new(); //A set but with B-Tree organization
let mut btree = BTreeMap::new(); //A dictionary but with B-Tree organization
```
### Methods
#### 
##
## Misc Functions
### main()
```rust
fn main() {
	//the first code that runs in every program
	//every function requires curly brackets around it
}
```

### println!()
```rust
println!(); //prints a string
```

### cargo
```bash
cargo new dir_name #creates a new directory and project under dir_name

cd dir_name
```

#### .toml (Tom's Obvious Minimal Language)
```toml
[package] #indicates the following statements are confuguring a package
name = "hello_cargo"
version = "0.1.0"
edition = "2024"
[dependencies] #lists any of the project dependencies
```

#### init
```bash
cargo init #creates a cargo toml file if it doesnt exist already
```

#### build
```bash
cargo build #creates an exeutable file

./target/debug/hello_cargo #runs the created executable (a debug build by default)
```
#### run
```bash
cargo run #runs the compiler (build) and executes the code in one
```
#### check
```bash
cargo check #compiles the code but doesn't create an executable
```
#### update
```bash
cargo update #updates the crates in your file to the latest versions 
```
### as
```rust
value as new_data_type
```
### drop
```rust
{
	...
} // Rust runs drop at the end of the scope
```
### clone
```rust
let heap_data_type = String::from("...");
let idk = heap_data_type.clone(); //makes a copy of the heap data from the first variable and creates another variable
```
### copy (for stack data only)
```rust
let stack_data_type = 1;
let idk = stack_data_type; // creates a copy of the stack data from the first variable to create another variable
```
### Iteration
```rust
.iter() //Gives immutable references
.iter_mut() //Gives mutable references

.iter().sum(); //Returns an Option<&i32>
.iter().collect(); //collects into a single string
```

### .chars()
```rust
"pop".chars(); //returns the length of a string, as opposed to .len(), which returns the number of bytes
```

