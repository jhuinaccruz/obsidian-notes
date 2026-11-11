## Hand-coding

Create a struct Person with a name (String), employer (String), and year_hired (u32)
__Requirements__:
- Implement .greet() and .get_age() on the `Person`
	- .greet() should print "Hello _____!" with the person's name
-  Create an `Employee` trait that promised two methods:
	- .get_years_worked() should be a promised implementation
	- .is_tenured() should return true if the person has worked for more than 10 years (default implementation)
	- Implement the `Employee` trait on the `Person` struct

Write a function that takes two generic types that implement the Employee Trait (empl1, and empl2) AND another common trait that allows for printing debugging-related information
- Print empl1 and **returns 1** if empl1 worked longer than empl2
- Print empl2 and **returns 2** if empl2 worked longer than empl1
- Returns -1 if both employees worked for the same amount of years
