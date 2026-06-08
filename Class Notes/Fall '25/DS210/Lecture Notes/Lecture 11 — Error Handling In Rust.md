__Compared to most languages, Rust handles "errors" as__: Data that the function can return

__Panicking__: Terminates a function when an error occurs, printing a message to the onsole about where the code panicked

__Result enum__: Passes information about an error to another function

__Error Propagation__: Passing errors "up" through other layers of function calls instead of handling them at the lowest level (compiler)