__Borrowing__: Temporarily accessing data without taking ownership of it
- Create a reference using the ampersand (`&`)
- Used when data is needed to be read and used temporarily

__`String` vs `&str` vs `&String`__:
- `String`: Owned, growable string on the heap
- `&str`: A string slice, which is a reference directly to string data
- `&String`: A reference to a string, which itself points to the String's stack metadata

__Dereferencing__: Inverse to borrowing (`&`), and extracts data
- Used when operations need the actual data, rather than the pointer, such as;
	- Math Operations
	- Comparisons
	- Match
- Occurs automatically for things like printing and vector functions
- Dereferencing does not transfer ownership. When dereferenced
	- For Copy types: Makes a copy
	- Otherwise, it gives you access without giving ownership