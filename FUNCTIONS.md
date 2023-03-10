# SWIFT FUNCTIONS

Swift functions are blocks of code that perform specific tasks or actions. They allow you to organize code into reusable components, making your code easier to read, maintain, and modify. In Swift, functions are first-class citizens, which means they can be used just like any other type, such as strings or integers.

Functions in Swift can take parameters (inputs) and return values (outputs), or they can have no parameters and no return value. Here's an example of a function in Swift that takes two parameters, adds them together, and returns the result:

    func addNumbers(_ a: Int, _ b: Int) -> Int {
            return a + b
        }

In this example, addNumbers is the name of the function, and it takes two integer parameters, a and b. The -> Int specifies that the function returns an integer value. The return keyword is used to return the sum of a and b.

## How to write a Swift Function

To write a Swift function, you need to follow these basic steps:

1. Start with the func keyword, which tells Swift that you're declaring a new function.
2. Add the name of the function, which should be descriptive of what the function does. Use camel case convention to name your function (e.g. calculateSum).
3. Add parentheses after the function name. If the function takes input parameters, list them inside the parentheses separated by commas. If the function doesn't take any parameters, leave the parentheses empty.
4. If the function returns a value, use the -> symbol followed by the return type. If the function doesn't return anything, omit the -> and the return type.
5. Write the body of the function inside curly braces { }, and add the code that performs the task you want the function to accomplish.

Swift functions also follow the principles of functional programming, which emphasizes immutability and the absence of side effects. This means that a function should not modify any of its input parameters or any other external state, and should always produce the same output for a given set of input parameters.

## Swift functions advance features

Default parameter values: You can provide default values for function parameters, so that they can be omitted when the function is called. For example, the following function has a default value of 0 for the parameter b:


    func calculateSum(a: Int, b: Int = 0) -> Int {
        return a + b
    }

If you call this function with only one argument (a), the default value for b will be used:

    let result1 = calculateSum(a: 5) // Result: 5

Variadic parameters: Functions can take a variable number of input parameters by using the ... notation before the parameter type. For example, the following function takes any number of integers and returns their sum:

    func calculateSum(numbers: Int...) -> Int {
        var sum = 0
        for number in numbers {
            sum += number
        }
        return sum
    }

You can call this function with any number of arguments:

    let result1 = calculateSum(numbers: 1, 2, 3, 4) 

In-out parameters: Functions can modify the values of their input parameters by using the inout keyword before the parameter type. For example, the following function swaps the values of two integers:

    func swapValues(_ a: inout Int, _ b: inout Int) {
        let temp = a
        a = b
        b = temp
    }

You can call this function with variables and use the & operator before the variables to pass them as in-out parameters:

    var x = 10
    var y = 20
    swapValues(&x, &y)
    print("x = \(x), y = \(y)") /


# Practice

1. Write a function that takes in an array of integers and returns the sum of all the even numbers in the array.
2. Write a function that takes in a string and returns true if the string is a palindrome (i.e., reads the same backward as forward) and false otherwise.
3. Write a function that takes in a date and returns the day of the week (e.g., Monday, Tuesday, etc.) as a string.
4. Write a function that takes in a sentence and returns the number of words in the sentence.
5. Write a function that takes in an array of integers and returns the largest and smallest integers in the array as a tuple.
6. Write a function that takes in a string and returns the number of vowels in the string.
7. Write a function that takes in two integers and returns their greatest common divisor (GCD).
8. Write a function that takes in an array of strings and returns the longest string in the array.
9. Write a function that takes in an array of integers and returns the second largest integer in the array.
10. Write a function that takes in a string and capitalizes the first letter of each word in the string.