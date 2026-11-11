__File I/O__: File reading
- In Rust, files are subject to scope and ownership same as variables, preventing null pointers and parsing issues

__Buffer__: Temporary storage in memory for data being transferred, like a "waiting area" for data
- In computer systems, useful for loading data such as in video streaming or copy/pasting so that systems can be smoother

__NDArray__: "NumPy" for Rust, useful for multidimensional arrays and mathematics like linear algebra, statistics and scientific computing

__Core__: A physical processing unit in the CPU that execute instructions

__Thread__: A sequence of instructions that run independently of user input

__Concurrent programming__: Allows for multiple cores working in parallel

__Amdahl's Law__: Parallelism has limits because the sequential portion of the process limits

__Challenges of parallel code__:
- Race conditions
- Deadlocks between threads
- Difficult debugging
- Overhead of physical capabilities

__Concurrency Patterns in Rust__:
- Message Passing: Used when concurrently running tasks in the background
- Shared state with locks (Mutex): When multiple threads need to update the same shared resource, there is a buffer between each thread accessing data at one time
- Data parallelism: Separating large of amounts of data into chunks and giving a thread one of those parts to work on