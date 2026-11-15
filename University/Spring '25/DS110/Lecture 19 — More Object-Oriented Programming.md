## Inheritance
__Inheritance__: A way of sharing code between similar classes, where a parent class (or base class) share their methods and code with its subclasses

>*Objects also count as their parent class, or any other class they inherited from*

>*...their children get not only their methods, but the methods the parents inherited.*

>*In general, if A inherits from B, A should satisfy an "is-A" relationship with B*

## Overriding
__Override__: Rewrite a method in a class so that it works differently from a parent's implementation

>*When parent and child disagree about how a method works, the child takes precedence and overrides the parent)*

Commonly overriden functions (from the Object class) include:
- \_\_str\_\_(): Returns the string representation of an object (usually the object's address in memory)
- \_\_eq\_\_(): Determines equality with another object, usually never true unless it is literally the same object (necessary for a proper \_\_hash\_\_() function)
- \_\_hash\_\_(): Computes a hash function on the object