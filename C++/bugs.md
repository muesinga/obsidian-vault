In C++, there are many different ways of classifying errors which generally fall into four separate categories:

• Compile-time erros: erros found by the compiler.

• Link-time errors: Errors found by the linker when it is trying to combine object files into an executable program.

• Run-time erros: Errors found by checks in a running program.

• Logic errors: Errors found by the programmer looking for the cause of erroneous results. 

//** Compile-time Erros **//

When we are writing C++ programs, the compiler is the first line of defense against errors.

There are two-types of compile-time errors:

• Syntax errors: Errors that occur when we violate the rules of C++ syntax.

• Type errors: Errors that occur when there are mismatch between the types we declared.

Some common syntax errors are:

• Missing semicolon `;`
• Missing closing parenthesis `)`, square bracket `]`, or curly brace `}`

Some common type errors are:

• Forgetting to declare a variable
• Storing a value into the wrong type

//** Link-time Errors **//

Sometimes the code compiles fine, but there is still a messge because the program needs some function or library that it can't find. This is known as a link-time error.

As our program gets bigger, it is good practice to divide the program into separate files. After compiling them, the linker takes those separate object files and cobines them into a single executalble file. Link-time errors are found by the linker when it is trying to combine object files into an executable file. 

Some common link-time errors:

• Using a function that was never defined

• Writing Main() instead of main()

//** Run-time Errors **//

If our program has no compile-time errors and no link-time errors, it'll run.

Errors which happen during program execution (run-time) after successful compilation are called run-time errors. Run-time errors occur when a program with no compile-time errors and link-time errors asks the computer to do something that the computer is ubable to reliably do.

It happens after we give the `./` execute commmand:

`./a.out`

Some common run-time errors:

• Division by zero also known as division error. These types of errors are hard to find as the compiler doesn't point to the line at which the error occurs.

• Trying to open a ile that doesn't exist

There is no way for the compiler to know about these kinds of errors when the program is compiled.

//** Logic Errors **//

Once we have removed the compile-time errors, link-time errors, and run-time errors, the program runs successfully. But sometimes, the program gives an unexpected output.

These types of errors which provide incorrect output, but appears to be error-free, are called logical erros. These are one of the most common errors that happen to beginners are also usually the most difficult to find and eliminate.

Logical errors solely depend on the logical thinking of the programmer.

Some common logic errors:

• Program logic is flawed

• Some "silly" mistake in as `if` statement or a `for/while` loop

//** Review **//

There are four types of C++ errors:

• Compile-time erros: Errors found by the compiler. 

• Link-time errors: Errors found by the linker when it is trying to combine object files into an executable program.

• Run-time errors: Errors found by checks in a running program.

• Logic errors: Errros found by the programmer looking for the causes of erroneous results