__Struct__: A custom data type that stores its data on the stack and heap

__Methods__: Add behavior (functions) that belong to the struct

__Enums vs Structs__:
- Enums use
	- Data that can be one of several alternatives that exist independently
	- The variants are fundamentally different
- Structs use
	- Multiple pieces of data that exist together
	- The attributes work in tangent as a unit
>*Use structs to group related data, and enums inside structs to represent choices.*