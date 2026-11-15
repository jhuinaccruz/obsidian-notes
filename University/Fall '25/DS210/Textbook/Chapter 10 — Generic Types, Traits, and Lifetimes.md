>[!abstract]
>*First we’ll review how to extract a function to reduce code duplication. We’ll then use the same technique to make a generic function from two functions that differ only in the types of their parameters. We’ll also explain how to use generic types in struct and enum definitions.*
>*Then you’ll learn how to use traits to define behavior in a generic way. You can combine traits with generic types to constrain a generic type to accept only those types that have a particular behavior, as opposed to just any type.*
>*Finally, we’ll discuss lifetimes: a variety of generics that give the compiler information about how references relate to each other. Lifetimes allow us to give the compiler enough information about borrowed values so that it can ensure references will be valid in more situations than it could without our help.*

__Generics__: Abstract stand-ins for concrete types or other properties

__Monomorphization__: The process of turning generic code into specific code by filling in the concrete type that are used

__Trait__: The functionality a particular type has and can share with other types, defined by the methods that can be called on that type

__Trait Bounds__: Used to specify that a generic type can be any type that has

__Lifetime__: A kind of generic that ensures references are valid as long as needed to be