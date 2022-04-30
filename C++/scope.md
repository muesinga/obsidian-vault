//** Headers **//

As the program grows, you will have to scroll through many declarations before you see `main()`.  That is why we use a header file-- usually with the same name as the file all of the function definitions - with the extension .hpp or .h. For example, if your function definitions are in my_functions.cpp, the corresponding header file would be my_functions.hpp or my_functions.h.

With headers in particular, you can just add `#include "my_functions.hpp"` to the very top of main.cpp

//** Default Arguments **//

If you add a parameter to a function in C++, then an argument will be required when you call the function. 

But what if 9 times out of 10 you know you'll use the same input value?

To make your code more flexible for situations like this, you can add default arguments to your function declarations. Default arguments are values assigned to paramenters when the function is declared and defined.

Then, if you leace the argument blank in your function call, instead of an error, your function will run with default value. Meanwhile, if you DO have an argument to add when you call the function, that argument will replace the default argument when your code executes.

IMPORTANT: Your computer determines which argument corresponds with which parameter based on order.

Parameters without default arguments come first. 

//** Function Templates **//

When two functions have different types but the same body there is a solution that allows for a C++ function to have a parameters that contain multiple data types. 

Note: Using templates will slow down the program's compile time, but speed up the execution time. 

Templates look like this:

template <typename T>
return_type some_function_name(T item1, T item2) {
		// do stuff with item1 and item2
	}
	
//** Review **//
	
Scope is the region of code that has access to an element:
	
	• Globally scoped variables are accessible everywhere
	
	• A variable created inside a function has local scope and can't be accessed outside the function.
	
C++ functions are usually split to make code more modular:
	
	• The declaration is a header file.
	
	• The definition in another .cpp file.
	
Programs with multiple .cpp files need to be linked at compile time:
	
	`g++ main.cpp fns.cpp`
	
Header files must be `include`d in the file `main()`:
	
	`#include "fns.hpp"`
	
You can define a function inline using the `inline` keyword, which may or may not improve execution speed.
	
Default arguments can be added to function declarations so that you can call the function without including those arguments.
	
You can overload C++ functions so that they handle different types of input and return different types.
	
A function template enables a function to behave the same with different types of parameters.