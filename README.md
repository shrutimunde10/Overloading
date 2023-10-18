# Overloading
# Theory
Function overloading is a feature that allows you to define multiple functions with the same name but different parameters. These functions can have the same name, but they must have different parameter lists, which may include a different number of parameters or parameters of different types. The C++ compiler determines which function to call based on the number and types of arguments provided when the function is invoked.

Some key points and principles related to function overloading in C++:

1)Function Name Overloading: In C++, you can have multiple functions with the same name, but they must have different parameter lists. The return type of the function is not considered when overloading; only the parameter list matters.

2)Parameter Lists: The parameter lists of overloaded functions must differ in one of the following ways:

-The number of parameters
-The data types of parameters
-The order of parameters
3)Return Type: The return type of overloaded functions can be the same or different. However, the return type alone cannot be used to distinguish overloaded functions. If two functions have the same parameter list but different return types, it will result in a compilation error.

4)Function Overload Resolution: When you call an overloaded function, the C++ compiler determines which function to execute based on the arguments you pass. It selects the function that best matches the argument types. If there is no exact match, the compiler will try to perform type conversions to find a suitable match. If there is still no clear choice, it results in a compilation error.

5)Default Arguments: Default arguments can be used in function overloading. For example, you can have multiple overloads of a function with different sets of default arguments, and the compiler will choose the appropriate version based on the number of arguments provided.

6)Member Function Overloading: You can overload member functions of a class just like global functions. Overloaded member functions are distinguished by the parameter list of the member functions.
# Example(syntax)
#include <iostream>

int add(int a, int b) {
    return a + b;
}

double add(double a, double b) {
    return a + b;
}

int main() {
    int result1 = add(3, 5);
    double result2 = add(3.5, 2.7);

    std::cout << "Result 1: " << result1 << std::endl;
    std::cout << "Result 2: " << result2 << std::endl;

    return 0;
}
