__Rust uses a three level hierarchy for organization, consisting of__:
- Package (the project/repository)
- Crate (compilation unit - the program itself)
- Module (a single file)

__Module__: Organize code using namespaces

__Code within a module is by default__: Private

__Package__: The project folder (what `cargo new` creates)

__Crate__: A single program/library that rust compiles
- Binary Crate: The program that runs
- Library Crate: Code created for others to use

__Semantic Versioning__ (for crates): `MAJOR.MINOR.PATCH`