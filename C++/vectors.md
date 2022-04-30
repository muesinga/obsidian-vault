//** Introduction to Vectors **//

To do anything of interest in programming, we will need a group of data to work with. 

The need for storing a collection of data is endless.

We are familiar with data types like `int` and `double`, but how do we store a group of `int`s or a group of `double`s?

A vector is one of the simplest and most useful ways to store data in C++.

A vector is a sequence of elements that you can access by index.

//** Creating a Vector **//

The `std::vector` lives in the `<vector>` header. It is nessecary to us the "preprocessor directive" that tells the compiler to #include whatever library that follows. To use vectors in C++, we will need to #include <vector>.
	
The syntax to create a vector looks like:
	
`std::vector<type> name;`
	
Inside the angle brackets is the data type of the vector. After the angle brackets is the name of the vector.
	
Note: The type of the vector (i.e., what data type is stored inside) cannot be changed after the declaration.

//** Initializing a Vector **//
	
Now we know how to create a vector, we can also initialize a vector with values.
	
For example, we can initialize a `double` vector named `location`:
	
std::vector<double> location = {42.651443, -73.749302};
	
//** Index **//
	
After initializing a `vector` we are able to access an individual element from the `vector` through the use of an index value assigned to the element.
	
An `index` refers to an element's position within an ordered list. Vectors are 0-indexed, meaning the first element has index 0, the second index 1, and so on.
	
//** Adding and Removing Elements **//

Often, we start with a vector that's either empty or a certain length. As we read or compute data we want, we can grow the vector as needed.
	
.push_back()
	
To add a new element to the "back", or end of the vector, we can use the `.push_back()` function.

.pop_back()

You can also remove elements from the "back" of the vector using .pop_back().
	
.size()
	
<std::vector> not only stores the elements; it also stores the size of the vector:
	
The .size() function returns the number of elements in the vector.
	
//** Operations **//
	
In order to change each of the values within a vector you are able to use a `for` loop. 
	
You can change all the values held within a vector by iterating from index 0 to `vector.size()`. You can use the counter of the `for` loop as the index.
	
//** Review **//
	
• Vectors are a sequence of elements that you can access be an index.
	
`std::vector<int> even = { 2, 4, 6, 8 , 10};`
	
• The first index in a vector is `0`.
	
• Some of the functions that come with vectors:
		• .push_back()
		• .pop_back()
		• .size()
	
• We can use a `for` loop to iterate through a vector. 
	

	


