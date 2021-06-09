# Intro to `std::vector`
`std::vector` is a standard C++ container that represents a collection of elements, or as programmers like to call it, an array; i.e. you could have a `std::vector` which contains `int`s like `[0, 2, 4, 5, 8]`.
### The C++ type system
One thing that you might have not caught is that C++ has a strong type system. I.e. you cannot not give a type to a variable (a type being something like `int`, `std::string` or `double` for [floating point arithmetic](https://en.wikipedia.org/wiki/Floating-point_arithmetic) [decimal numbers]). For example this is valid C++:
```cpp
int i = 384;
std::string str = "Some text";
double d = 0.69;
```
but _declaring_ them without types would be illegal. i.e. doing a program like
```cpp
int main() {
    a = 50; // lacking a type (probably int)
}
```
would be wrong.
### Computing the average of notes
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<double> vec;
    double tmp = 0.0;
    while (std::cin >> tmp) { // while the user inputs valid stuff
        vec.push_back(tmp); // append the provided value
    }
    double sum = 0.0;
    for (double d : vec) {
        sum = sum + d;
    }
    double average = sum / vec.size()
}
```
Declaring a vector is sort of simple: `std::vector<TheTypeYouWant>`.
The `for (type thing : otherThing)` basically is equivalent to other langs `for each (thing in otherThing)`; it loops over every element of the `otherThing` and gives you the element as the name you wrote, here `d`. But now you may ask is there ways to make this better? Yes and we will look at them in the nexts chapters, mainly with scopes and `<algorithm>`.
