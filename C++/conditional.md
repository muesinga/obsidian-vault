//** If Statement **//

An `if` statement is used to test an expression for truth and execute some code base on it. 

If the condition is `true`, then the statements within are executed. Otherwise, the statements are skipped and the program continues on.

The `if` keyword is followed by a set of parentheses (). Inside the parentheses (), a condition is provided that evaluates to `true` or `false`:
• If the condition evaluates to `true`, the code is inside the curly braces {} executes.

• If the condition evaluates to `false`, the code won't execute.

So in the code above, if `flip` is equal to 1, the program outputs "Heads"; if it does not, then nothing happens and the program continues.

//** Relational Operators**//

When writing conditional statements, sometimes we need to use different types of operators to compare values. These operators are called relational operators.

To have a condition, we need relational operators:

• `==` equal to
• `!=` not equal to
• `>` greater than
• `<` less than
• `>=` greater than or equal to
• `<=` less than or equal to

Relation operators compare the value on the left with the value on the right.

//** Else Clause **//

We can also add an `else` clause to an `if` statement to provide code that will only be execute if the condition is `false`. Here's a form of an `if` statement that includes and `else` clause:

if (condition) {

	do something
	
} else {

	do something else
	
}

• If condition is `true`, statement1 is executed. Then the program skips statement2 and executes any code statements following the `if/else` clause.

• If condition is `false`, statement1 is skipped and statement2 is executed. After statement2 completes, the program executes any code statements following the `if/else` clause.

//** Else If **//

if (condition) {

	some code
	
} else if (condition) {

	some code

} else {

	some code 

}

The `else if ` statement always comes after the `if` statement and before the `else` statement. The `else if` statement also takes a condition. You can have more that one `else if` conditional statement.

//** Switch Statement **//

Programs with multiple outcomes are so common that C++ provides a special statement for it; the `switch` statement.

A `switch` statement provides an alternatie syntax that is easier to read and write. However, you are going to find these less frequently than `if`, `else if`, `else` in the wild.

example of a switch statement:

switch (grade) {  
  
 	case 9:  
 		std::cout << "Freshman\n";  
		break;  
	case 10:  
		std::cout << "Sophomore\n";  
		break;  
	case 11:  
		std::cout << "Junior\n";  
		break;  
	case 12:  
		std::cout << "Senior\n";  
		break;  
	default:  
		std::cout << "Invalid\n";  
 		break;
}

• The `switch` keyword initiates the statement and is followed by (), which contains the value that each case will compare. In the example, the value or expression of the switch statement is `grade`. One restriction on this expression is that it must evaluate to an integral type (`int`, `char`, `short`, `long`, `long long`, `enum`).

• Inside the block, `{}`, there are multiple cases

• The `case` keyword checks if the expression matches the specified value that comes after it. The value following the first case is `9`. If the value of `grade` is equal to `9`, then the code that follows the `:` would run.

•The `break` keyword tells the computer to exit the block and not execute any more code or check any other cases inside the code block.

• At the end of each switch statement, there is a `default` statement. If none of the cases are `true`, then the code in the `default` statement will run. It's essentially the `else` part.
 In the code above, suppose `grade` is equal to `10`, the output would be "Sophomore".
 
 Note: Without the `break` keyword at the end of each case, the program would execute the code for the first matching case and all subsequent cases, including the `default` code. This behavior is different from `if` /  `else` conditional statements which execute only one block of code. 
 
 //** Review **//
 
 • An `if` statement checks a condition and will execute a task if that condition evaluates to true.
 
 • `if` / `else` statements make binary decisions and execute different code blocks based on a provided condition.
 
 • We can add more conditions using `else if` statements.
 
 • Relational operators, including `<`, `>`, `<=`, `>=`, `==`, and `!=` can compare two values.
 
 • A `switch` statement can be used to simplify the process of writing multiple `else if` statements. The `break` keyword stops the remaining cases from being checked and executed in a switch statement.
 
 //** Example **//
 
 #include <iostream>
 
int main() {
 
  double weight;
  int x;
 
  std::cout << "Please enter your current earth weight: ";
  std::cin >> weight;
 
  std::cout << "\nI have information for the following planets:\n\n";
  std::cout << "   1. Venus   2. Mars    3. Jupiter\n";
  std::cout << "   4. Saturn  5. Uranus  6. Neptune\n\n";
 
  std::cout << "Which planet are you visiting? ";
  std::cin >> x;
 
  if (x == 1) {
 
    weight = weight * 0.78;
 
  } else if (x == 2) {
 
    weight = weight * 0.39;
 
  } else if (x == 3) {
 
    weight = weight * 2.65;
 
  } else if (x == 4) {
 
    weight = weight * 1.17;
 
  } else if (x == 5) {
 
    weight = weight * 1.05;
 
  } else if (x == 6) {
 
    weight = weight * 1.23;
 
  }
 
  std::cout << "\nYour weight: " << weight << "\n";
 
}