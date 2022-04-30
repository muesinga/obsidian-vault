//** Functions **//

Also known as a method or procedure, a `function` is a named group of code statements that accomplish something together; similar to a factory machine.

C++ comes with build-in functions as part of the standard library. We gain access to built-in functions through the #include header.

//** Declare & Define **//

A C++ function is comprised of two distinct parts:

• Declaration: this includes the function's name, what the return type is, and any parameters (if the function will accept input values, known as arguments).

• Definition: also known as the body of the function, this contains the instructions for what the function is supposed to do.

This is the overall structure:

return_type function_name( any, paramaters, you, have ) {

	// code block here
	

	return output_if_there_is_any;

}

//** Void **//

A `void` function, also known as a subroutine, has no return value, making it ideally suited for situations where you just want to print stuff to the terminal.

//** Return Types **//

When you do want to return something and pass information back to the rest of your program, C++ has you covered. Just like there are many variable types, there are many different return types for functions.

A function can return most data types, including `double`, `int`, `bool`, `char`, `std::string`, `std::vector`.

The return statement is the last line of code that a function will execute.

//** Return Value **//

When functions have a return type other than `void`, the function has two new requirements:

• There must be a value returned from the function.

• The return value must be the same type as the functions's return type.

The return value gets returned to the place where the function is called.

//** Parametes & Arguments **//

Parameters (sometimes called "formal parameters") are variables used in a function's definition. They act as placeholders for the input values you'll use during your function. 

double get_tip(double price) {

	return price * 0.2;

}

In the function above, price is the function's parameter and it's a double. It is decared between the parentheses and then used in the body of the function. 

Then, when you're ready to call your function, the value you pass to the function is called an "argument" (also known as an "actual parameter"). In this case, 15.75 is the argument that is passed to the function:

double tip = get_tip(15.75);
// tip would be 3.15


//** Multiple Arguments **//

You can add as many arguments as you would like to an argument, but you will have to remember their order when you call the function.

//** How Parameters & Arguments Work **//

A function with parameters has a couple of requirements:

• The function call must include the same number of arguments as there are parameters.

• The corresponding arguments must be pass in the same order.

//** Review **//

• An `if` statement checks a condition and will execute a task if that condition evaluates to true.

• `if` / `else` statements make binary decisions and execute different code blocks based on a provided condition.

• We can add more conditions using `else if` statements.

• Relational operators, including `<`, `>`, `<=`, `>=`, `==`, `!=` can compare two values.

• A `switch` statement can be used to simplify the proess of writing multiple `else if` statements. The `break` keyword stops the remaining cases from being checked and executed in a switch statement.

C++ function syntax:

return_type function_name(parameter1, parameter2) {

	// Code block here
	
	return output_if_there_is_any;

}

bool is_even(int number) {

	if (number % 2 == 0) {
	
		return true;
	
	}
	
	return false;
	
}