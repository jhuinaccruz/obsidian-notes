## 1.2
__Function__: Defined using `fn...`
- Uses snake_case by convention
- Works at runtime

__Macro__: A function-type piece of code that expands and "writes" code at compilation
- Denoted by the additional use of a  `!` where a function name would be
- Works at compilation

__Rust is an ahead-of-time compiled language, meaning__: Compilation is a separate step to running the program
- After running `rustc`, the program that executes is a separate executable file created by `rustc`

## 1.3
__Cargo__: The all-in-one tool for managing, building, running, testing, and sharing Rust projects
- __Build__: Compiles and creates executable
- __Run__: Compiles and executes
- __Check__: Just compiles

>*Often, cargo check is much faster than cargo build because it skips the step of producing an executable.*

>[!abstract]
>- *We can create a project using `cargo new`.*
>- *We can build a project using `cargo build`.*
>- *We can build and run a project in one step using `cargo run`.*
>- *We can build a project without producing a binary to check for errors using `cargo check`.*
>- *Instead of saving the result of the build in the same directory as our code, Cargo stores it in the _target/debug_ directory.*