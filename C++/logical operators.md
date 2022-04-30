Often, when we are trying to create a contrl flow for our program, we'll encounter situations where the logic cannot be satisfied with a single condition.

Logical operators are used to combine two or more conditions. They allow programs to make more flexible decisions. The result of the operation of a logical operator is a `bool` value of either `true` or `false`.

There are three logical operators we will cover:

• && : the `and` logical operator
•||: the `or` logical operator
•!: the `not` logical operator

![[Screen Shot 2021-10-23 at 11.03.37 AM 1.png]]

//** Logical Operator: && **//

The `and` logical operator is denoted by `&&`.

It returns `true` if the condition on the left and the condition on the right are both `true`. Otherwise, it returns `false`.

//** Logical Operator: II **//

The `or` logical operator is denoted by `||`.

It returns `true` when the condition on the left is `true` of the condition on the right is `true`. Only one of them needs to be `true`.

//** Logical Operator: ! **//

The `not` logical operator is denoted by `!`.

It reverses the `bool` outcome of the expression that immediately follows.

//** Review **//

`&&`: the `and` logical operator
`||`: the `or` logical operator
`!`: the `not` logical operator

int main() {

	int y = 0;
	// declare integer variable 'y' and assign it to 0
	
	std::cout << "Enter year: ";
	std::cin >> y;
	
	// assign input from terminal to variable 'y'
	
	if (y < 1000 || y > 9999) {
	
		std::cout << "Invalid entry. \n";
	
	}
	
	// if 'y' is a number with less than, or more than 4 digits, then 'y' is an invalid entry
	
	else if (y % 4 == 0 && y % 100 != 0 || y % 400 == 0) {
	
		std::cout << y;
		std::cout << " falls on a leap year.\n";
	}
	
	else {
	
		std::cout << y;
		std::cout << " is not a leap year.\n";
		}

}
