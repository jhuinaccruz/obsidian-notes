__Ownership__: Tracks what variable is responsible for data that is on the heap, making memory efficient and prevents "undefined behavior"

__Rust's Ownership Rules__:
- Each value has an owner
- There can only be one owner at a time
- When the owner goes out of scope, the value gets dropped

__Stack data gets \_, heap data gets \___: Copied, moved

__Vector__: Contains a single type, but with mutable size and lives on the heap

__Box__: Used for large datasets, big matrices, or deep structures, lives on the heap