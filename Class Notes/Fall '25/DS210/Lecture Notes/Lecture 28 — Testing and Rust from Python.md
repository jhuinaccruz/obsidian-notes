__Why keep things private in Rust__:
- Encapsulation: Prevents modifications by external code
- Flexibility: Internal changes don't create bugs in outside implementations
- External clarity
- Prevents misuse of functions

__Test-Driven Development__:
1. Write code
2. Write tests
	1. Write tests that capture desired behavior
	2. Write code until it passes the tests
	3. Improve and "refactor" the code
3. Run tests per run automatically
4. Fix bugs

__Good Tests...__:
- Test one thing at a time
- Use `#[should_panic]` for expected errors
- Test edge cases
- Test behavior, not implementation
- Test logic rather than import's behaviors
- Keep tests independent

__Unit Test__: Individual function tests

__Integration Tests__: Test how multiple components work together
- Within Rust, they typically go in a separate directory and file within the repo
- Useful for larger projects and such

__Python's Main Uses__:
- Data exploration
- Quick prototyping
- Large ecosystem
- Easy to write

__Rust's Main Uses__:
- Efficient performance
- Memory safety
- Parallel processing

__Rust + Python Uses__:
- Processing large datasets
- Heavy numerical computations
- Performance-critical parts of the pipeline

__PyO3__: A Rust library that allows Python integration, where Python can call Rust and vice versa as well as creating Python modules within Rust

__maturin__: A tool for building Python packages in Rust, so that it compiles Rust code and installs it as a Python module into another Python environment on the local disk