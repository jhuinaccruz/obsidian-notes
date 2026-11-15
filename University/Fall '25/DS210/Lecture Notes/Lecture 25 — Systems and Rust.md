__Systems Programming__: Writing software that controls the machine. Its main characteristics are that it
- Has direct control over memory
- Is performance critical
- Runs for long periods of time
- Runs under application programming

__Use-after-free__: Using memory that has been previously "freed"

__Double-Free__: Freeing the same memory twice

__Dangling Pointer__: A reference that outlives the data it points to (data is freed but the reference is still referencing the now-freed data)

__Buffer Overflow__: Writing past the end of an array

__Data Race__: Two threads access the same memory without synchronization