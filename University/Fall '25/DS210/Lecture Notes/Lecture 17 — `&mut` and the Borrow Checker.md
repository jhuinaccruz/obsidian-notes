__Borrow Checker Rules__:
- You can only have either one mutable reference or immutable references
- References cannot outlive the original

__Data races__: Two threads modifying a piece of data at the same time

__Use-after-free__: Trying to access memory that has been freed

__Iterator invalidation__: Modifying a collection while iterating

