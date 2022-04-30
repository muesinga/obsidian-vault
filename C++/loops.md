//** Loops **//

A loop is a programming tool that repeats some code or a set of instructions until a specified condition is reached. To iterate simply means "to repeat".

The `while` loop is similar in syntax to an `if` statement. Just like an `if` statement, it executes the code inside of it if the condition is `true`.

The `while` loop will continue to execute the code, over and over again as long as the condition is true.


while (condition) {

	statements

}

//** while loop example **//

#include <iostream>

int main() {

	int guess;
	int tries = 0;
	std::cout << "I have a number 1-10.\n";
	std::cout << "Please guess it: ";
	std::cin >> guess;

// Write a while loop here:

while (guess != 8 && tries < 50) {
	std::cout << "Wrong guess, try again: ";
	std::cin >> guess;
	tries++;
	}

	if (guess == 8) {
		std::cout << "You got it!\n";
	}
}

//** For Loops **//
	
When we know exactly how many times we want to iterate we can use a `for` loop instead of a `while` loop.

The condition of a `for` loop is established by logic that resides within a parenthesis immediately following the declaration of the `for` loop.

An example of the `for` loop syntax:
	
	for (int i = 0; i < 20; i++)
						   
There are three seperate parts to this separated by ;:

• The initialization of a counter: int i = 0
• The continue condition: i < 20
• The change in the counter (in this case an increment): i++
	
//** Incrementing `for` loop **//
	
for (int i = 0; i < 20; i++)
{
}
					   
//** Decrementing `for` loop **//
					   
for (int i = 20; i > 0; i--)
{
}