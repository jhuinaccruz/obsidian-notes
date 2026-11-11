__Collection__: Types that can hold multiple values of a specified type
- Heap-allocated: Vectors and Strings
- Stack-allocated: Arrays

__HashMap__: Similar to Python dictionary
- Lives on the stack with a pointer and its metadata
- The bucket array lives on the heap
- Its keys and values are stores in the array

__Hash Function__: Takes any input and converts it into a number. its key properties include
- __Deterministic__: Same input always produces the same output
- __Fast__: Takes milliseconds always
- __Uniform__: Small values spread evenly across a range
- __Avalanche effect__: Small changes in input lead to big changes in output
- __Hard to Invert__
- __Collisions should be rare__

__Rust's default standard for hashing is__: SipHash 1-3

__HashSet__: Similar to Python set