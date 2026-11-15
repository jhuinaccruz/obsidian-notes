__Dangling Reference__: A reference pointer to something that no longer exists

__Lifetime__: How long a piece of data is valid in your program

__Lifetime Annotations__: Tell the compiler how references relate to each other across function boundaries
- The compiler needs help when there are multiple possible sources for a returned reference
- *For some lifetime `'a`, inputs with said lifetime live at least that long, and the output lives no longer than that.*
- Lifetime annotations do not change how long data lives, but allow compilation when it is possible
- If a struct holds references, it needs lifetime annotations
- If there are multiple input references with a reference returned, it needs lifetime annotations

__`'static` Lifetime__: Means the data lives for the entire program, such as
- String Literals
- Static constants
- Leaked allocations